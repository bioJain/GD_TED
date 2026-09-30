---
linear_issue: JHA-82
created: 2026-09-30
source: manual
milestone: cluster-4-tam-sam-pricing
status: in-review
inputs:
  - 04_tam_sam_pricing/tam_sam_revision.md
  - 04_tam_sam_pricing/sources/README.md
  - _shared/GD_TED_qa_checklist.md
---

# PR #19 follow-up fact-check 및 QA

> **검토 기준일: 2026-09-30.** PR #19 작성 세션과 분리된 follow-up 검토임. 문서의 산술, 내부 일관성, source traceability, 핵심 공개 근거를 재검토하고 A1-H3 전 항목을 판정함. 상업 market report의 유료 원문과 workbook에서 식별자가 빠진 출처는 확인할 수 없었으므로 `PASS`로 승격하지 않음.

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

## 4. A1-H3 전체 QA checklist

> 판정 기준: 대상 문서 `tam_sam_revision.md`에 실제로 기재된 내용만 평가함. Checklist가 종합 disease report를 전제로 하므로 TAM/SAM 문서 범위 밖 항목도 생략하지 않고 `PARTIAL`로 표시하고, "해당 서술 없음"과 후속 조치를 명시함. 따라서 아래 표는 **전 항목 실행 기록**이지 전체 QA 통과 선언이 아님.

### A. 질환 구분/개념 정확성

| 항목 | 판정 | 문제 문구/근거 및 correction |
|---|---|---|
| A1 | PASS | GD/TED 시장을 별도 행으로 제시하고 “두 시장금액을 합산하지 않음”으로 구분함 |
| A2 | PASS | “TED의 GD 비동반 비율 약 10%”를 명시하되 serology 직접 측정값이 아님을 제한함 |
| A3 | PARTIAL | 문제 문구: “TED의 GD 연동 pool, 경증 포함”. GD 환자 중 mild orbital change와 clinically significant TED 비율을 구분하지 않음. Correction: 다음 epidemiology revision에서 두 정의/비율을 별도 행으로 추가 |

### B. 역학 수치 정확성

| 항목 | 판정 | 문제 문구/근거 및 correction |
|---|---|---|
| B1 | PARTIAL | 문제 문구: “incidence는 역사적 단일 county 자료 기반”. Cohort 수준임은 표시했으나 원 PMID/DOI가 workbook R09에 없음. Correction: Olmsted County 원 논문 식별자 추가 전 D-grade 유지 |
| B2 | PASS | TED population-based prevalence pool과 `GD prevalence x TED 동반율` pool을 별도 열로 표시하고 정의 차이를 설명함 |
| B3 | PASS | 7MM 값이 baseline 입력 기반임을 명시하고, 단일 일본 자료의 15%를 타 지역에 적용한 한계를 명시함 |
| B4 | PASS | prevalence `stock`, 신규 진단 `flow`, state-entry를 구분하며 ATD 합계의 annual-patient 사용을 금지함 |

### C. Staging/Severity 정확성

| 항목 | 판정 | 문제 문구/근거 및 correction |
|---|---|---|
| C1 | PARTIAL | 해당 서술 없음: CAS 7점/10점 체계를 다루지 않음. Correction: 본 TAM/SAM 문서 범위 밖으로 유지하고 staging 근거는 `ted_line_of_therapy.md`에 위임 |
| C2 | PARTIAL | 해당 서술 없음: EUGOGO 3-tier 수치 기준을 재기재하지 않음. Correction: severity별 bottom-up model 구축 시 정의표를 인용 |
| C3 | PARTIAL | 해당 서술 없음: NOSPECS를 사용하지 않음. Correction: 본 문서에서 NOSPECS 기반 산출을 도입할 때만 정의/근거 추가 |
| C4 | PASS | “GD: 공식 severity stage가 없음”을 명시하고 therapy line을 별도 정의함 |

### D. 병리기전 정확성

| 항목 | 판정 | 문제 문구/근거 및 correction |
|---|---|---|
| D1 | PARTIAL | 문제 문구: “TSAb-IgG”만 사용하며 TBAb/neutral TRAb 구분은 해당 서술 없음. Correction: mechanism deep-dive가 아닌 시장 문서이므로 현 범위를 유지하되 TRAb 전체와 TSAb를 동의어로 쓰지 않음 |
| D2 | PASS | TED에서 TSAb를 “proposed co-driver”로 한정하고 IGF-1R 병행/독립 경로 가능성을 명시함 |
| D3 | PARTIAL | 해당 서술 없음: Thy-1 양성/음성 fibroblast fate를 다루지 않음. Correction: mechanism SAM에 해당 분화축을 적용할 경우에만 1차 근거와 함께 추가 |
| D4 | PARTIAL | 해당 서술 없음: RAI 후 TED 악화/흡연 상호작용을 다루지 않음. Correction: therapy eligibility 모델에 RAI/TED risk exclusion을 도입할 때 추가 |
| D5 | PARTIAL | 해당 서술 없음: active/inactive cytokine milieu를 다루지 않음. Correction: TED activity별 pool 구축 시 `ted_line_of_therapy.md`의 정의를 인용 |
| D6 | PARTIAL | 해당 서술 없음: 흡연 risk factor를 다루지 않음. Correction: incidence/risk-adjusted epidemiology 모델 범위에 포함할 때 추가 |

### E. 치료제 정보 정확성

| 항목 | 판정 | 문제 문구/근거 및 correction |
|---|---|---|
| E1 | PARTIAL | 해당 서술 없음: Tepezza 승인일/승인 당시 적응증을 재기재하지 않음. Correction: 매출 anchor만 사용하는 현 범위 유지; label eligibility 산출 시 FDA 원문 추가 |
| E2 | PARTIAL | 해당 서술 없음: Tepezza 청각 AE를 다루지 않음. Correction: safety-adjusted SAM 구축 전 label/primary trial 근거 추가 |
| E3 | PARTIAL | 문제 문구: TED state에 “systemic 1차”만 기재하고 IVMP/EUGOGO 근거를 본문에서 재확인하지 않음. Correction: 치료별 dollar SAM 도입 시 regimen과 guideline source 추가 |
| E4 | PARTIAL | 문제 문구: “remission 37%/45%/56%”. Workbook R11이 2차 웹페이지이며 원 meta-analysis 식별자가 없음. Correction: 원 DOI/PMID 확보 전 sensitivity only 유지 |
| E5 | PARTIAL | 해당 서술 없음: RAI 후 prednisolone 예방을 다루지 않음. Correction: RAI pathway cost/eligibility 모델에 포함할 때 guideline 근거 추가 |
| E6 | PASS | 언급한 indication-specific trial은 VitaliThy GD와 UplighTED TED로 분리하고 ClinicalTrials.gov 상태를 직접 대조함 |
| E7 | PASS | 중단된 UplighTED는 경쟁 pipeline 후보가 아니라 negative clinical evidence로만 명시하며 현재 asset 목록에 포함하지 않음 |

### F. 인용/참고문헌 정확성

| 항목 | 판정 | 문제 문구/근거 및 correction |
|---|---|---|
| F1 | PARTIAL | 문제 문구: “3세대 TSI assay meta-analysis sensitivity 93.3%, TRAb assay 88.9%”에 같은 문단의 직접 링크/번호가 없음. 새 산출물 규약에 따라 말미 repo 근거는 있으나 claim-level anchor가 부족함. Correction: DOI/PMID inline link 추가 |
| F2 | PARTIAL | `[x]` 체계를 사용하지 않아 reference 번호 불일치는 없지만 전수 대응도 불가함. Correction: 신규 문서 규약대로 각 외부 claim에 inline link 또는 자체 참고문헌 key 부여 |
| F3 | PASS | 자체 참고문헌 번호 목록이 없어 중복 번호가 없고, 말미 repo 근거 파일도 중복되지 않음 |
| F4 | PASS | PMID 40789418, 38107298, 33246456, 30621642, 34297684의 PubMed record 실존을 2026-09-30 API로 확인함 |
| F5 | PASS | “revolutionary”, “breakthrough”, “game-changing” 등 마케팅 표현 없음 |
| F6 | PASS | TED mechanism은 `proposed`, serology는 `proxy`, 수치 결과는 E/D와 `exploratory`로 제한함 |

### G. eTPD 섹션 분리 원칙

| 항목 | 판정 | 문제 문구/근거 및 correction |
|---|---|---|
| G1 | PARTIAL | 문제 문구: 본 문서는 checklist의 Section A-E 구조가 아니므로 “Section E에만” 조건을 직접 적용할 수 없음. Correction: eTPD 상세는 포함하지 않고 TSAb-IgG market fit만 유지 |
| G2 | PASS | eTPD/TSAb-selective 접근의 TED 적용은 clinical response factor 부재와 `정량 불가`를 명시함 |
| G3 | PASS | FcRn의 전체 IgG 감소와 TSAb-selective 제거를 구분하고, UplighTED futility를 TED 한계 신호로 제한적으로 해석함 |

### H. 언어/형식

| 항목 | 판정 | 문제 문구/근거 및 correction |
|---|---|---|
| H1 | PASS | TSHR, IGF-1R, TSAb, TRAb, FcRn, TAM/SAM 등 기술 용어를 영문으로 유지함 |
| H2 | PASS | U+00B7 가운뎃점 검색 결과 0건 |
| H3 | PARTIAL | 문제 문구: 일부 문장이 “확인함/필요함/유지함” 서술형으로 끝남. Correction: 다음 편집 라운드에서 표/개조식 중심으로 통일하되 의미 변경은 하지 않음 |

## 5. Tier-상 claim 별도 검증 로그

| Claim | Cross-model | 원문/direct record 대조 | 판정 |
|---|---|---|---|
| GD/TED top-down TAM 원 수치 | 미완료 | 공개 landing page만 확인, 유료 원문 scope 미확인 | PARTIAL, valuation 사용 금지 |
| 미국 GD incidence/prevalence workbook 입력 | 미완료 | workbook R08/R09가 원 PMID/DOI 대신 경유 출처 사용 | PARTIAL, E/D 유지 |
| TSI/TRAb sensitivity 93.3%/88.9% | 미완료 | PMID 40789418의 논문 존재/설계 확인, paywalled full table direct quote 미완료 | PARTIAL |
| UplighTED status/종료 사유 | 미완료 | CT.gov 두 record에서 `TERMINATED`, intended efficacy 미입증 가능성, safety 무관 문구 확인 | PASS for registry status; cross-model pending |
| VitaliThy status | 미완료 | CT.gov NCT07570316에서 `RECRUITING` 확인 | PASS for registry status; cross-model pending |
| Tepezza FY2025 매출 | 미완료 | Amgen FY2025 table에서 total 1,903, US 1,758, ROW 145 확인 | PASS for company-reported sales; cross-model pending |

Cross-model 열이 미완료인 claim은 repo 규약상 최종 QA 통과가 아님. 따라서 이 문서의 `status`는 `in-review`로 유지함.

## 6. PMID 실존 확인 로그

| PMID | 확인된 문헌 |
|---|---|
| [40789418](https://pubmed.ncbi.nlm.nih.gov/40789418/) | TSI/TRAb diagnostic performance systematic review/meta-analysis |
| [38107298](https://pubmed.ncbi.nlm.nih.gov/38107298/) | Two TSH-receptor antibody assays clinical practice study |
| [33246456](https://pubmed.ncbi.nlm.nih.gov/33246456/) | Thyroid-associated orbitopathy case report |
| [30621642](https://pubmed.ncbi.nlm.nih.gov/30621642/) | Hashimoto thyroiditis unilateral orbitopathy case report |
| [34297684](https://pubmed.ncbi.nlm.nih.gov/34297684/) | 2021 EUGOGO clinical practice guideline |

## 7. 잔여 blocker 및 권고

1. **ATD uncontrolled:** 환자 단위 longitudinal data로 중복 제거 후, 각 state의 체류기간과 동일 관찰창을 적용하기 전에는 annual patient SAM 산출 금지.
2. **Workbook source repair:** R08은 JAMA DOI/PMID로 교체하고 R10/R12/R13은 원문 식별자와 직접 URL을 채운 뒤 evidence grade 재평가.
3. **Top-down TAM:** 동일 지역, 기준연도, 포함 비용항목으로 scope를 통일하고 유료 원문 표를 확인하기 전에는 `$3.11B/$5.04B/$4.53B/$8.09B`를 valuation input으로 사용 금지.
4. **TED mechanism SAM:** 직접 TSAb-positive TED cohort와 response-based factor가 확보되기 전 `$4.08B/$7.28B` 채택 금지.
5. **Full QA completion:** Tier-상 claim의 cross-model 검증과 미확인 원문 direct-quote 대조 완료 후에만 `status: done`으로 변경.
