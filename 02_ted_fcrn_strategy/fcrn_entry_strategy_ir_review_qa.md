---
linear_issue: JHA-74
created: 2026-09-30
source: manual
milestone: cluster-2-ted-fcrn-strategy
status: done
inputs:
  - 02_ted_fcrn_strategy/fcrn_entry_strategy_ir_review.md
  - _shared/GD_TED_qa_checklist.md
  - docs/repo_conventions.md
---

# fcrn_entry_strategy_ir_review.md 독립 follow-up QA

**QA 실행일:** 2026-09-30

**QA 대상:** `02_ted_fcrn_strategy/fcrn_entry_strategy_ir_review.md`

**연계 PR:** [#15](https://github.com/bioJain/GD_TED/pull/15)

**적용 규칙:** `_shared/GD_TED_qa_checklist.md`, `docs/repo_conventions.md`

## 1. 독립성 및 범위

- 이 QA는 PR #15의 작성 세션과 분리된 follow-up 세션에서 수행했다. 입력은 merge된 문서, 공용 checklist, repo conventions, 공개 1차 출처로 제한했다.
- PR #15의 수정 코멘트에는 선행 검토 대응이 Claude Code로 수행됐다고 명시돼 있다. 본 QA는 GPT-5.6 Sol로 수행해 다른 provider/model의 재확인 요건을 충족했다.
- `상` tier로 분류된 임상 phase, 실패/중단, endpoint 수치, 시험설계 claim은 ClinicalTrials.gov API v2와 SEC 원문을 새로 조회하고 direct quote를 대조했다.
- live source 기준일은 2026-09-30이다. 원문 문서의 2026-09-28 조사 기준일 및 repo v2의 2026-09-10 frozen cut과 구분했다.

## 2. PR #15 코멘트 재검증

| 기존 코멘트 | 판정 | 독립 확인 |
|---|---|---|
| 68.8%/31.3%를 순수 정상화율로 쓰면 안 됨 | PASS | NCT05907668 outcome title은 두 수치를 각각 정상화 **또는** FT3/FT4가 LLN 미만인 composite로 정의한다. posted value는 68.8%, 31.3%다. 53.1% outcome만 FT3/FT4 정상화로 정의된다. 본문 3.1절은 세 지표를 정확히 구분한다. |
| Imeroprubart의 TED 시험 부재 claim에 전용 검색 필요 | PASS | [S15] 검색 결과의 condition을 전수 확인했다. 반환된 3건은 모두 GD 시험이고 TED는 exclusion 문구에만 등장한다. 본문은 이를 회사의 개발 의사결정이 아니라 공개 등록시험 부재로 제한한다. |
| 상 tier claim은 별도 QA/cross-model/direct quote 필요 | PASS | 아래 3절에 별도 QA, 다른 provider/model, 1차 출처 direct quote 대조 결과를 claim별 기록했다. |

## 3. Tier-상 claim 검증

### 3.1 Batoclimab TED Phase 3 실패 및 전체 개발 중단

- **SEC 10-K direct quote:** “neither of which met the primary endpoint” 및 “discontinue further development of batoclimab across all indications”.
- **Registry 대조:** NCT05517421과 NCT05524571은 모두 `PHASE3`, `COMPLETED`, condition `Thyroid Eye Disease`, primary outcome `Percentage of proptosis responders` at Week 24로 확인됐다.
- **판정:** PASS. 실패 결과는 sponsor 10-K가, 시험의 phase/적응증/endpoint는 두 registry record가 독립적으로 지지한다. Registry의 `COMPLETED`는 시험 수행 상태이며 primary endpoint 성공을 뜻하지 않으므로 sponsor 결과와 충돌하지 않는다.

### 3.2 Efgartigimod UplighTED futility 종료

- **Registry direct quote:** 두 record의 `whyStopped`는 “continuing the trials is unlikely to demonstrate the intended efficacy”라고 명시한다.
- **Registry 대조:** NCT06307613과 NCT06307626은 모두 `PHASE3`, `TERMINATED`, randomized/quadruple-masked/placebo-controlled이며 Week 24 proptosis responder가 primary outcome이다.
- **SEC 대조:** argenx FY2025 20-F는 UplighTED를 `Clinical trial discontinued in 2025`로 기록한다.
- **판정:** PASS. 본문의 “사전 interim futility 분석 후 종료”는 registry의 중단 사유와 일치한다. 안전성 문제로 인한 중단이 아니라는 registry 설명도 확인했다.

### 3.3 Batoclimab GD endpoint 수치

NCT05907668 posted results를 outcome title과 value 단위로 대조했다.

| Week 24 outcome 원문 요지 | value | 본문 표기 | 판정 |
|---|---:|---|---|
| FT3/FT4 정상화 또는 하나 이상이 LLN 미만, baseline 대비 ATD 증량 없음 | 68.8% | composite | PASS |
| FT3/FT4 정상화, ATD 용량 baseline의 50% 이하 | 53.1% | 순수 정상화 | PASS |
| off-ATD이며 FT3/FT4 정상화 또는 하나 이상이 LLN 미만 | 31.3% | composite | PASS |

Study design도 `PHASE2`, actual enrollment 32, single-group/open-label, 680 mg SC QW 12주 후 340 mg SC QW 12주로 본문과 일치한다.

### 3.4 IMVT-1402 및 efgartigimod GD 설계

| 시험 | registry direct field 확인 | 판정 |
|---|---|---|
| NCT06727604 | `PHASE2`, randomized/double-masked, 240명 예정; Week 26 euthyroid/off-ATD primary; Week 52 및 치료 중단 후 6/12개월 지속성 secondary | PASS |
| NCT07018323 | `PHASE2`, randomized/double-masked, 210명 예정; 두 IMVT-1402 dose와 placebo; Week 26 euthyroid/off-ATD primary, seronegativity secondary | PASS |
| NCT07570316 | `PHASE3`, randomized/quadruple-masked, 230명 예정; Week 24 euthyroid/off-ATD primary; low-dose ATD 및 TRAb seronegativity secondary | PASS |
| NCT07596849 | `PHASE3`, randomized/quadruple-masked, 230명 예정; NCT07570316과 같은 primary/주요 secondary 구조 | PASS |

본문은 NCT07018323의 TRAb seronegativity를 “핵심 endpoint”로 요약하나 primary라고 부르지 않는다. 실제 registry에서는 secondary outcome이므로 현 문구는 허용 가능한 범위이며, 후속 인용 시에는 primary/secondary를 구분해야 한다.

## 4. 출처 및 인용 무결성

- [S1], [S2], [S4] SEC filing은 접근 가능하며 본문의 회사 전략, TED 가설, 개발 중단 서술을 지지한다.
- [S3]는 accession은 맞지만 기존 파일명 `argenxex991q42025earnings.htm`이 SEC directory에 없어 HTTP 404를 반환했다. 같은 6-K accession의 실제 exhibit 파일 `a09earningspressreleaseq4.htm`로 교정했다. 교정된 원문에는 “Registrational study in Graves’ disease ... expanding development into thyroid-driven autoimmunity”가 존재한다.
- [S5]-[S12] NCT record의 phase, status, design, outcome을 API v2로 재조회했다. 본문의 주요 사실 claim과 일치한다.
- [S13]-[S15]는 검색 부재를 회사 의사결정으로 확대하지 않고 `no public trial identified`로 제한해 기술했다. 이 한계 표기는 적절하다.

## 5. 적용 가능한 checklist 판정

원 checklist는 종합 report용이므로 이 전략 review에 포함되지 않은 질환 역학/staging/eTPD 항목은 N/A로 처리했다.

| 항목 | 판정 | 코멘트 |
|---|---|---|
| A1 GD/TED 구분 | PASS | GD biochemical/remission endpoint와 TED orbital endpoint를 명시적으로 분리한다. |
| B1-B4 역학 | N/A | 독립 역학 분석이 아니라 회사 market-sizing 수치를 회사 추정치로 인용한 문서다. 해당 수치를 외부 역학치로 취급하지 않는다는 제한을 명시한다. |
| D2 불확실한 mechanism 표현 | PASS | GD의 상대적 mechanistic fit을 임상 입증 전 가설로 제한한다. |
| E6 indication-specific phase | PASS | efgartigimod, batoclimab, imeroprubart를 적응증별 registry record로 확인했다. |
| E7 discontinued 자산 처리 | PASS | 문서 목적상 실패 사례를 분석 범위에 포함하되, 중단 상태를 명확히 표시한다. |
| F1 source traceability | PASS | 사실 claim은 [S1]-[S15]로 연결되며 잘못된 [S3] URL을 이번 QA에서 교정했다. |
| F5 marketing language | PASS | 회사의 `first-in-class`/`best-in-class`는 공시상 전략 문구임을 표시하고 분석자의 입증된 효능 표현으로 사용하지 않는다. |
| F6 불확실성 한정 | PASS | 추론, 근거 수준, registry 부재의 한계를 일관되게 표시한다. |
| H1 영문 기술 용어 | PASS | TSHR, TRAb, FcRn, ATD 등 주요 기술 용어를 영문으로 유지한다. |
| H2 가운뎃점 금지 | PASS | 대상 문서와 본 QA 문서에서 가운뎃점 미검출. |
| H3 개조식 문체 | PARTIAL | 표는 개조식이나 분석 본문은 평서형이다. 정확성 영향이 없고 기존 문서 형식을 유지한다. |

## 6. 최종 결론

**PASS, 필수 교정 1건 완료.** PR #15의 세 코멘트 대응은 실제 1차 출처와 일치했다. 상 tier 임상 claim은 별도/cross-model/direct-quote 검증을 통과했다. 추가로 발견한 유일한 필수 결함은 [S3]의 존재하지 않는 SEC exhibit 파일명이며 실제 exhibit URL로 교정했다. 그 외 결론을 바꿀 사실 오류는 확인되지 않았다.

본 QA는 2026-09-30 시점 공개자료 검증이며, 향후 registry 상태 또는 회사 개발전략 변경을 보증하지 않는다.
