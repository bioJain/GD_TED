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

## 문서 서식

- 한국어 본문, 유전자/단백질/약물/임상시험/규제/통계 용어는 영어 유지.
- 가운뎃점(·) 사용 금지. `/`, `,`, `;`로 대체.

## 커밋 메시지

Linear 이슈 번호를 포함한다(예: `JHA-70: GD line-of-therapy table draft`).
