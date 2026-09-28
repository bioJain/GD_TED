---
title: repo_conventions
created: 2026-09-24
---

# 작성 규칙

## 산출물 frontmatter (cluster 폴더의 모든 신규 md)

```yaml
---
linear_issue: JHA-70
created: 2026-09-24
source: claude-code        # claude-code | claude-ai | manual
milestone: cluster-1-competitive-landscape
status: draft              # draft | in-review | done (Linear status와 동기화)
inputs:                    # 이 산출물이 읽은 repo 내 파일(상대경로)
  - 00_baseline_biomni/landscape_v2/soc_outcomes_v2.csv
---
```

## 인용과 근거

- 인용 번호 체계가 둘이다. 혼용 금지.
  - legacy `[n]`: `_shared/GD_TED_reference.md` (claude.ai report 계열)
  - Biomni v2 `[N]`: `00_baseline_biomni/landscape_v2/reference_v2.md`
  - 신규 산출물은 본문에서 출처 파일명을 명시하고, 새 문헌은 문서 말미에 자체 참고문헌 목록을 둔다. 번호 통합은 별도 작업으로 다룬다.
- 수치를 v2 CSV에서 가져올 때 `claim_id` 또는 `trial_id`/`soc_id`/`asset` 키를 함께 적는다.
- Biomni v2 수치는 data cut 2026-09-10 기준이다. 이후 live 조회 결과와 섞지 말고 as-of 날짜를 병기한다.
- 상업 DB(Cortellis 등) 파생 수치는 본문에 전재하지 않고 요약/집계 수준으로만 쓴다(public repo).

## 바이너리 정책

- `*.pptx`는 git에 커밋하지 않는다(`.gitignore`). 저장소는 Google Drive, 링크와 SHA-256만 `docs/EXTERNAL_ASSETS.md`에 기록한다.
- deck 개요(md)와 figure(SVG/PNG, 수 MB 이하)는 git에 둔다.

## Figure 소싱

- 외부 원본(논문, 학회 포스터, IR 자료 등)에서 뽑아온 raw figure는 `<cluster 폴더>/sources/figures_raw/`에 두고, 각 파일과 같은 이름의 `.meta.yaml`에 출처를 기록한다.

  ```yaml
  source_doc: <저널/포스터/IR 자료명 또는 URL>
  source_page: 3
  extracted: 2026-09-28
  extraction_method: pymupdf   # pymupdf | pdf2image+crop | camelot | manual
  linear_issue: JHA-86
  ```

- Deck에 최종적으로 들어가는 figure는 raw 그대로 삽입하지 않고, `06_deck/figures/`(또는 해당 cluster의 `figures_v2/`와 동일한 패턴)에 재작업한 SVG/PNG로 둔다. raw는 참고/근거 보존용이고, 재작업본만 최종 산출물에 들어간다.
- 재작업본의 frontmatter/메타에 `derived_from: <raw figure 경로>`를 적어 원본과의 연결을 남긴다.
- PDF에서 embedded figure를 그대로 뽑을 때는 `PyMuPDF`(fitz), 페이지 레이아웃 일부를 크롭할 때는 `pdf2image` + bbox crop, 표는 `camelot`/`pdfplumber`를 기본으로 쓴다. 도구가 다르면 `.meta.yaml`의 `extraction_method`를 갱신한다.

### Deck 배치 워크플로우 (draft → 확정 → 재작업 → 배치)

Figure 재작업을 매 슬라이드마다 먼저 끝내고 배치/수정하는 방식은 무겁다. 대신 레이아웃을 먼저 확정한 뒤에만 재작업을 진행한다.

1. **초안 deck (draft)**: 슬라이드별로 figure가 들어갈 자리를 box outline으로만 표시한다. box 안에는 최종 그림 대신 `[FIGURE: <raw figure 경로 또는 source_doc#page>]` 식으로 어떤 raw로부터 어떤 재작업본이 들어갈지 텍스트로 명시한다. 이 단계에서는 재작업을 하지 않는다.
2. **레이아웃 검토**: 유저가 초안 deck 전체를 보고 figure 배치/구성(어떤 그림을 쓸지, 슬라이드당 몇 개, 위치)을 수정한다. 필요하면 box 자체를 옮기거나 빼거나 다른 raw로 바꾼다.
3. **레이아웃 확정 후 재작업**: 확정된 box 목록만큼만 개별 figure를 재작업한다(SVG/PNG, `derived_from` 메타 포함). 확정 전 box에 대해서는 재작업하지 않는다.
4. **최종 배치**: 재작업본을 확정된 box 자리에 넣어 deck을 완성한다.

- Draft 단계의 box outline은 `06_deck/`의 슬라이드 개요 md에 슬라이드별 목록으로 남긴다(placeholder 텍스트 그대로 보존해 어떤 raw를 참조했는지 나중에도 추적 가능하게 한다).

## 문서 서식

- 한국어 본문, 유전자/단백질/약물/임상시험/규제/통계 용어는 영어 유지.
- 가운뎃점(·) 사용 금지. `/`, `,`, `;`로 대체.

## QA 독립성과 검증 강도 차등

- QA 세션은 작성 세션과 분리한다(별도 session/conversation). QA 세션에는 report.md와 checklist만 넘기고, 작성 과정의 프롬프트/추론/중간 draft는 넘기지 않는다 — 작성자의 편향을 이어받지 않게 하기 위함.
- 아래 상 claim은 cross-model 검증을 거친다(작성에 쓴 모델과 다른 provider/모델로 같은 claim을 재확인). 상 claim이 아닌 항목은 동일 QA 세션의 checklist 통과로 충분하다.
  - **상**: 규제 승인일/적응증, AE 발생률, 임상 phase, 역학 수치(incidence/prevalence), 가격/TAM 추정에 쓰인 원 수치
  - **중**: 병리기전 서술 중 정량적 근거가 딸린 것(예: 특정 cytokine 우세 비율)
  - **하**: 정성적 서술, 메커니즘 가설의 존재 유무 자체(수치 없음)
- 상 claim은 QA 통과 후에도 원문(PMID/1차 출처) direct quote 대조를 최소 1회 거친다. `evidence_claims_v2.csv`처럼 claim 단위 anchor가 있는 산출물은 거기에 검증 결과를 기록하고, 없는 신규 산출물은 문서 말미에 검증 로그 표(claim, tier, 검증 방법, 결과, 일자)를 둔다.
- `_shared/GD_TED_qa_checklist.md`의 QA 시스템 프롬프트는 이 규칙(분리된 세션, tier 구분)을 전제로 실행한다.

## 커밋 메시지

Linear 이슈 번호를 포함한다(예: `JHA-70: GD line-of-therapy table draft`).
