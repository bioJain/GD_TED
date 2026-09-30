---
linear_issue: JHA-82
created: 2026-09-30
source: manual
milestone: cluster-4-tam-sam-pricing
status: done
inputs:
  - 04_tam_sam_pricing/tam_sam_revision.md
  - 04_tam_sam_pricing/sources/README.md
  - _shared/GD_TED_qa_checklist.md
---

# PR #19 follow-up fact-check 및 QA

> **검토 기준일: 2026-09-30.** PR #19 작성 세션과 분리된 follow-up 검토임. 문서의 산술, 내부 일관성, source traceability, 핵심 공개 근거를 재검토함. 상업 market report의 유료 원문과 workbook에서 식별자가 빠진 출처는 확인할 수 없었으므로 `PASS`로 승격하지 않음.

## 1. Executive verdict

| 영역 | 판정 | 결론 |
|---|---|---|
| PR review comment 1, ATD uncontrolled | **수정 완료** | `1차+2차+장기유지`는 동일 신규 cohort가 순차적으로 통과하는 state-entry의 합임. unique annual patients가 아니므로 `명/년` 교집합을 삭제하고 `NR`로 변경함 |
| PR review comment 2, workbook traceability | **수정 완료** | PR에 binary를 넣지 않고 Google Drive 원본/direct export, 검토일, 검토 시점 SHA-256을 기록함 |
| 산술 | **PASS** | TAM median, 배수, serology 환산, 환자 flow를 독립 재계산해 표시값의 반올림 범위와 일치함 |
| Workbook formula/label | **PARTIAL** | 보고서가 `1 - remission`을 비관해/재발로 올바르게 확장했으나 workbook 자체는 이를 모두 `재발`로 표기함. 2차 선택률, 장기유지율 등 D-grade 가정이 남음 |
| 임상시험/매출/assay claim | **PASS/PARTIAL** | ClinicalTrials.gov 상태와 Amgen 매출은 1차 출처와 일치. assay 논문의 존재/설계는 PubMed와 일치하지만 수치 전문은 DOI 원문 재대조가 필요함 |
| Top-down TAM 및 TED serology proxy | **PARTIAL** | 공개 landing page의 scope 이질성과 유료 원문 미확인 문제가 남음. TED 90%는 직접 seropositivity가 아니라 GD association 역산 proxy임 |
| 최종 사용성 | **조건부** | 방향성 scenario에는 사용 가능. valuation, dollar SAM, unique annual patient SAM에는 사용 금지 |

## 2. 산술 재계산

| Claim | 재계산 | 판정 |
|---|---:|---|
| GD FLOOR | `(2.640 + 3.585) / 2 = 3.1125B` | PASS |
| GD PREMIUM | `(4.050 + 6.037) / 2 = 5.0435B` | PASS |
| TED FLOOR | 5개 값의 median `4.530B` | PASS |
| TED PREMIUM | 4개 전체 median `7.500B`; `0.3051B` 제외 3개 median `8.090B` | PASS, 단 `$8.09B`는 기계적 median이 아니라 scope-adjusted 대표값 |
| PREMIUM/FLOOR | GD `5.0435 / 3.1125 = 1.6204x`; TED `8.09 / 4.53 = 1.7859x` | PASS |
| Tepezza anchor 비율 | `1.903 / 4.53 = 42.01%` | PASS |
| GD mechanism 환산 | FLOOR `3.11 x 90-95% = 2.799-2.9545B`; PREMIUM `5.04 x 90-95% = 4.536-4.788B` | PASS |
| Post-ATD 비관해/재발 | Low `52,400 x 75% x 63% = 24,759`; Base `78,600 x 82% x 55% = 35,449`; High `104,800 x 88% x 44% = 40,579` | PASS |
| Post-ATD x serology | 각 scenario에 90-95% 적용 시 본문 표시 범위와 반올림 일치 | PASS |

## 3. Source-level fact-check

| Claim | 확인한 근거 | 판정/조치 |
|---|---|---|
| UplighTED 2건이 efficacy futility로 종료, safety 때문이 아님 | ClinicalTrials.gov [NCT06307626](https://clinicaltrials.gov/study/NCT06307626), [NCT06307613](https://clinicaltrials.gov/study/NCT06307613)의 `TERMINATED`와 `whyStopped` 직접 대조 | PASS |
| VitaliThy Phase 3 진행 중 | ClinicalTrials.gov [NCT07570316](https://clinicaltrials.gov/study/NCT07570316)의 `RECRUITING` 직접 대조 | PASS |
| Tepezza FY2025 매출 $1.903B, 미국 $1.758B, 미국 외 $0.145B | [Amgen FY2025 results](https://www.amgen.com/newsroom/press-releases/2026/02/amgen-reports-fourth-quarter-and-full-year-2025-financial-results) 표 직접 대조 | PASS |
| TSI/TRAb 진단 성능 meta-analysis | PubMed PMID [40789418](https://pubmed.ncbi.nlm.nih.gov/40789418/)에서 제목, systematic review/meta-analysis 설계 확인 | PARTIAL: 93.3%/88.9%는 기존 DOI 기록과 일치하나 이번 QA에서 paywalled 전문 표를 direct quote하지 못함 |
| Workbook 입력/수식 | 2026-09-28에 export한 XLSX의 `01_Assumptions`, `03_Graves`, `05_Sources` 대조 | PARTIAL: 검토 시점 hash는 남겼지만 외부 원본은 가변 가능. R08은 Wikipedia 경유, R10/R12/R13은 원문 URL 부재 |
| GD/TED top-down market 값 | legacy raw table과 각 공개 landing page 링크의 연결 확인 | PARTIAL: 지역/연도/scope가 다른 값을 합친 scenario이며 유료 원문 방법론은 미확인 |
| TED 약 90% serology | 직접 TED TSAb-positive cohort가 아니라 GD 비동반 약 10%의 역산 | 직접 측정값으로 표현 금지. 본문의 `proxy`, `상한 근사치`, SAM 보류가 적절함 |

## 4. QA checklist

| 항목 | 판정 | Comment/correction |
|---|---|---|
| 질환/시장 정의 분리 | PASS | GD/TED를 별도 range로 유지하고 합산 금지를 명시함 |
| Incidence/prevalence/flow/stock 구분 | PASS | 미국 신규 flow와 유병 stock을 구분함 |
| Mechanism uncertainty | PASS | TED TSHR/IGF-1R를 proposed co-driver로 한정하고 response factor 부재 시 SAM을 보류함 |
| 모든 핵심 숫자의 traceability | PARTIAL | repo 문서 또는 외부 원본/direct export까지는 추적되나 일부 원문 식별자가 없음 |
| 상 claim 1차 출처 확인 | PARTIAL | ClinicalTrials.gov/Amgen은 완료. assay 전문, 상업 report 원문, workbook R08/R10-R13은 미완료 |
| 산술/단위 | PASS | 표시값 재계산 일치. review comment가 지적한 잘못된 `명/년` 단위는 제거함 |
| 중복 환자 방지 | PASS | ATD uncontrolled의 annual-patient 교집합을 삭제하고 deduplication 전 `NR` 처리함 |
| 재현성 | PARTIAL | Google Drive direct export와 검토 시점 SHA-256을 남겼으나, 외부 원본이 변경되면 동일 binary 재현은 보장되지 않음 |
| Evidence grade/불확실성 | PASS | 결과를 E/D exploratory scenario로 유지하고 미확인 항목을 승격하지 않음 |
| 마케팅 언어/가운뎃점 | PASS | 마케팅 표현과 가운뎃점 없음 |

## 5. 잔여 blocker 및 권고

1. **ATD uncontrolled:** 환자 단위 longitudinal data로 중복 제거 후, 각 state의 체류기간과 동일 관찰창을 적용하기 전에는 annual patient SAM 산출 금지.
2. **Workbook source repair:** R08은 JAMA DOI/PMID로 교체하고 R10/R12/R13은 원문 식별자와 직접 URL을 채운 뒤 evidence grade 재평가.
3. **Top-down TAM:** 동일 지역, 기준연도, 포함 비용항목으로 scope를 통일하고 유료 원문 표를 확인하기 전에는 `$3.11B/$5.04B/$4.53B/$8.09B`를 valuation input으로 사용 금지.
4. **TED mechanism SAM:** 직접 TSAb-positive TED cohort와 response-based factor가 확보되기 전 `$4.08B/$7.28B` 채택 금지.
5. **Dollar SAM:** diagnosed/treated rate, therapy-line eligibility, access, net course cost를 포함한 bottom-up model을 별도로 구축.
