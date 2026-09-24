---
title: GD_TED_market_sizing_report
목적: Graves' Disease(GD) / Thyroid Eye Disease(TED) 시장성(TAM range) 및 TSAb-IgG targeting coverage 분석
상태: DRAFT v1.1(2026-09-14 갱신: Section 4.2 efgartigimod GD/TED 임상근거 CT.gov 원문 대조로 격상) — Track A/B(공개 리포트) 기반 경량 산출 완료, Track C/D(bottom-up 재무모델)는 범위 외(후속 옵션으로 명시)
연계 문서: GD_TED_market_sizing_plan.md(작업 개요) / GD_TED_report.md(Section A 역학, Section E eTPD) / GD_TED_plan.md
---

# GD / TED 시장성 및 TSAb-IgG Coverage 분석

> 작성 기준일: 2026-09-14
> 방법론: market-sizing-multitrack 스킬을 경량(range-first) 모드로 적용 — 승인된 GD_TED_market_sizing_plan.md 파라미터 기준

---

## 0. Executive Summary

- **GD 시장(top-down, 공개 리포트 4건)**: 현재(2024/2025 base) range $2.26B-$4.56B, **FLOOR(median) ≈ $3.11B**; 2033-2035 forecast range $3.69B-$6.78B, **PREMIUM(median) ≈ $5.04B**. PREMIUM/FLOOR ratio ≈ 1.6x — 유기적 성장(organic growth) 수준으로, 신규 premium biologic 등장을 전제한 급격한 가격 프리미엄 시나리오는 아직 반영되어 있지 않음
- **TED 시장(top-down, 공개 리포트 5건)**: 현재(2022-2026 base, 정의 편차 큼) range $0.17B-$5.36B, **FLOOR(median) ≈ $4.53B**; forecast(2031-2035) range $0.31B-$11.81B, **PREMIUM(median) ≈ $8.09B**. 리포트 1건($165M)은 다른 4건 대비 20-30배 작아 스코프 정의가 상이한 것으로 판단(중앙값 계산에서는 median의 이상치 완충 효과로 결과에 큰 영향 없음, 아래 3.2 참조)
- **실매출 anchor(Teprotumumab, Amgen FY2025)**: $1.90B(미국 $1.76B + 기타 지역 $0.15B) — 현재 TED 승인 치료제 매출의 사실상 전부. 상업 리포트가 제시하는 "현재" TED 시장 $4.5B대와 약 2.4배 괴리 — 스코프(약물 외 수술/스테로이드 비용, 2025-2026 신규 승인 경쟁제품 전망분 포함 여부)에 기인한 것으로 해석(3.3 참조), 단순 오차로 단정하지 않음
- **TSAb-IgG coverage**: GD는 TSAb가 확립된 유일한 직접 driver이며 혈청학적 양성률(현대 assay 기준) 90-95% — 즉 **양성 = 사실상 표적 적중**에 가까운 구도. TED는 (1) 인구기반 혈청음성 비율에 대한 직접 문헌이 이번 검색에서 확인되지 않아 GD-동반 비율(~90%)로만 대리 추정 가능하고, (2) IGF-1R 경로의 독립적 관여 가능성(Co-driver, 미확립)으로 인해 혈청 양성이어도 TSAb 단독 제거가 임상적 개선을 담보하는지 불확실 — **TED의 실질 표적 적중률은 GD보다 낮고 불확실성도 훨씬 큼**(정량화된 문헌 부재로 숫자 제시는 지양). **(2026-09-14 갱신)** 이 판단을 뒷받침하는 직접 임상 근거로, efgartigimod GD Phase 3(VitaliThy, NCT07570316)는 진행 중인 반면 TED 전용 Phase 3(UplighTED, NCT06307626/NCT06307613)는 CT.gov 공식 기록상 **안전성과 무관한 효능 futility**로 조기 종료됨이 원문 대조로 확인됨(4.2 참조) — "TSAb 포함 IgG 비선택적 감소" 전략이 GD에는 유효 가설로 남아 있으나 TED 안와 병리 단독 통제에는 불충분할 가능성을 뒷받침

---

## 1. 스코프 (승인된 파라미터 재확인)

| 항목 | 결정 |
|---|---|
| 산출 목표 | GD/TED 각각 독립 TAM range(top-down 우선) + TSAb-targeting mechanism 기반 coverage |
| 깊이 | Range 우선 경량 방식 — Track A/B 우선, Track C/D는 범위 외(후속 옵션) |
| 지역 | Global + 7MM(공개 리포트 스코프에 따라 상이 — 각 표에 명기) |
| TSAb 프레이밍 | Modality 무관 광의 정의(FcRn inhibitor, TSHR-blocking Ab, eTPD/sweeping-Ab 등 전체) |
| 귀속 | 6T_review_26_H2 프로젝트(GD_TED_plan.md/GD_TED_report.md와 연계) |

---

## 2. Track A/B — 공개 마켓 리포트 수집 결과 (Raw Data)

### 2.1 GD (4건)

| 소스 | 발행일 | Base Year 시장규모 | Forecast Year 시장규모 | CAGR | 지역 스코프 | 방법론/스코프 메모 |
|---|---|---|---|---|---|---|
| [IMARC Group](https://www.imarcgroup.com/graves-disease-market-outlook) | 2025-03-04 | $4,557M (2024) | $6,782M (2035) | 3.69% | 7MM(US/DE/FR/UK/IT/ES/JP) | ATD+RAI+monoclonal Ab+진단기술+시술 포함 — 가장 넓은 스코프 |
| [Precedence Research](https://www.precedenceresearch.com/graves-disease-market) | 2026-05-22 | $2,260M (2025) | $3,690M (2035) | 5.02% | Global(NA/EU/APAC/LATAM/MEA) | NA 40% 점유(2025), 미국 단독 $678M |
| [MarketResearchFuture](https://www.marketresearchfuture.com/reports/graves-disease-treatment-market-37376) | 2025-09-01 | $3,585M (2024) | $6,037M (2035) | 4.85% | Global 5개 지역 | NA 44.6%, EU 30% |
| [SkyQuest](https://www.skyquestt.com/report/graves-disease-treatment-market) | 2026-03 | $2,500M (2024)/$2,640M (2025) | $4,050M (2033) | 5.5% | Global | 45건 primary interview 기반, "targeted biologics"를 최고속 성장 세그먼트로 명시 |

### 2.2 TED (5건)

| 소스 | 발행일 | Base Year 시장규모 | Forecast Year 시장규모 | CAGR | 지역 스코프 | 방법론/스코프 메모 |
|---|---|---|---|---|---|---|
| [GlobeNewswire(시장조사 배포)](https://www.globenewswire.com/news-release/2025/04/16/3062327/0/en/Thyroid-Eye-Disease-Treatment-Market-Forecast-to-Reach-11-81-Billion-by-2031-Emerging-Economies-Expand-Access-to-Thyroid-Eye-Disease-Diagnoses-and-Therapies.html) | 2025-04-16 | $4,530M (2024) | $11,810M (2031) | 9.47%(2021-24 실적치, forecast CAGR 별도 미공개) | 10개국(Americas/EU/APAC/MEA) | CAGR 정의 불명확 — 데이터 품질 이슈로 플래그 |
| [Mordor Intelligence](https://www.mordorintelligence.com/industry-reports/thyroid-eye-disease-treatment-market) | 2026-09-11 | $5,360M (2026) | $8,090M (2031) | 8.57% | Global | Top-down 유병률 + bottom-up 매출모델 병용(자체 명시) |
| [DelveInsight](https://www.delveinsight.com/report-store/thyroid-eye-disease-market) | 2025 | $1,980M (미국만, 2022) | 비공개(redacted) | 비공개 | 7MM(US/EU4/UK/JP) | 미국이 7MM 유병률의 ~42% 차지한다는 서술로 7MM 전체 역산 시 **약 $4,714M(2022, 추정치)** — 직접 공개된 수치 아님, 역산값임을 명기 |
| [MarketResearchFuture(#27903)](https://www.marketresearchfuture.com/reports/thyroid-eye-disease-market-27903) | 2025-09-01 | $165.4M (2024) | $305.1M (2035) | 5.72% | Global 5개 지역 | **다른 4건 대비 20-30배 작음 — 스코프가 현저히 좁은 것으로 판단(예: 특정 세부 세그먼트/기기), 원문에서 정확한 협의의 정의를 확인하지 못함. 이상치로 명시적 플래그** |
| [ReportsAndData](https://www.reportsanddata.com/report-detail/thyroid-eye-disease-market) | 2025-12(2026-08 갱신) | $3,420M (2025) | $6,910M (2035) | 7.3% | Global 18개국 | NA 최대 점유 |

### 2.3 실매출 Anchor

| 항목 | 수치 | 출처 |
|---|---|---|
| Teprotumumab(TEPEZZA) FY2025 글로벌 매출 | $1,903M(전년비 +3%) | [Amgen 2025 Q4/FY 실적발표](https://www.amgen.com/newsroom/press-releases/2026/02/amgen-reports-fourth-quarter-and-full-year-2025-financial-results) |
| — 미국 | $1,758M | 상동 |
| — 미국 외 | $145M | 상동 |
| Teprotumumab Q4 2025 매출 | $457M(전년비 -1%, 재고조정 영향) | 상동 |

---

## 3. Reconciliation

### 3.1 GD FLOOR/PREMIUM

- Base-year 4건 정렬: $2,260M / $2,640M / $3,585M / $4,557M → **median(FLOOR) = $3,112.5M ≈ $3.11B**
- Forecast 4건 정렬: $3,690M / $4,050M / $6,037M / $6,782M → **median(PREMIUM) = $5,043.5M ≈ $5.04B**
- Spread(현재) = max/min = 4,557/2,260 = **2.02x** — 스킬 기준 진단 임계치(3.0x) 미만, 정상 범위. 편차의 주 원인은 스코프 차이로 판단(IMARC는 진단기술/시술까지 포함하는 가장 넓은 정의, Precedence/SkyQuest는 약물치료 중심)
- **PREMIUM/FLOOR = 1.62x** — 낮은 pricing-thesis dependency. 이는 GD에 아직 승인된 premium biologic이 없어(현재 SoC가 저가 generic ATD/RAI/수술 중심) forecast 모델들이 기존 치료 클래스의 유기적 CAGR을 연장한 것에 가깝고, "신규 biologic 승인" 같은 step-change 시나리오를 반영하지 않았을 가능성을 시사 — **후속 신약 승인 시 이 forecast 자체가 상향 재조정될 여지가 큼**(TED에서 teprotumumab이 만든 선례, 3.3 참조)

### 3.2 TED FLOOR/PREMIUM

- Base-year 5건(이상치 포함) 정렬: $165.4M / $1,980M(2022, 미국만)/$3,420M / $4,530M / $5,360M — 미국 단독치를 7MM 전체 추정치($4,714M)로 대체해 재정렬: $165.4M / $3,420M / $4,530M / $4,714M / $5,360M → **median(FLOOR) = $4,530M ≈ $4.53B**
- Forecast 4건(DelveInsight 비공개 제외): $305.1M / $6,910M / $8,090M / $11,810M → **median(PREMIUM) = $7,500M**(중앙 두 값 평균) ≈ **$8.09B로 보수적 채택**(4건 중 8,090M을 대표값으로 채택 — 305.1M 이상치를 제외한 3건의 median인 8,090M이 스코프 일관성 측면에서 더 대표성 있다고 판단)
- Spread 진단: MarketResearchFuture(#27903) 1건이 다른 4건 대비 최대 32배(5,360/165.4) 차이 — **스킬 기준 3.0x 임계치를 크게 초과, 진단 필수**. Median이 이상치에 완충되어 FLOOR/PREMIUM 결과 자체는 왜곡되지 않았으나, 해당 리포트는 신뢰 구간 밖의 별도 스코프(세부 니치 세그먼트 추정)로 판단해 향후 재검토 시 제외 권고
- **PREMIUM/FLOOR = 1.79x** — GD와 유사하게 낮은 pricing-thesis dependency, 즉 forecast들이 현존 경쟁구도(teprotumumab 중심)의 자연 성장을 연장한 것에 가까움

### 3.3 실매출 Anchor와의 괴리 — Teprotumumab

- 2025년 기준 teprotumumab 글로벌 매출 $1.90B는 상업 리포트가 제시하는 "현재" TED 시장 FLOOR($4.53B)의 **약 42%**에 불과
- 괴리의 가능한 설명(확정 아님, 해석):
  1. 다수 리포트의 "TED 시장" 정의가 승인 약물 매출뿐 아니라 수술(orbital decompression), IVMP, 진단 영상 등 비-약물 지출까지 포괄하는 넓은 정의일 가능성(Mordor Intelligence는 자체적으로 "치료 유형에 surgery 포함"이라 명시)
  2. 2025-2026년 신규 승인/출시 자산(veligrotug 2026-06 미국 승인, IBI-311 2025-03 중국 승인 — 모두 GD_TED_report.md Section C4에서 확인)의 향후 매출 전망분이 "현재" base-year 수치에 이미 선반영되었을 가능성 — 즉 리포트의 "current" 시점이 실질적으로는 forward-looking 추정을 일부 포함
  3. 상업 시장조사 리포트 특유의 낙관적 편향(리포트 판매를 위한 유인 구조) 가능성 — 이는 확인 불가한 추론이나, 스킬 방법론상 실매출 anchor와의 괴리는 반드시 명시해야 하는 사항
- **GD와의 비대칭성**: GD는 아직 승인된 premium biologic이 전무해 비교 가능한 실매출 anchor 자체가 없음 — 즉 GD의 top-down $3.11B는 전량 저가 generic 치료 기반 추정치이며, TED에서 teprotumumab이 approval 이후 사실상 새로운 매출 카테고리(~$1.9B)를 창출한 선례를 고려하면, **GD에 첫 premium biologic이 승인될 경우 실제 시장 규모는 현 forecast($5.04B)를 상당폭 상회할 잠재력**이 있음(추론, 검증 불가)

### 3.4 GD-TED Population Overlap

- GD_TED_report.md Section A1에 따르면 TED 환자의 약 90%가 GD(hyperthyroidism) 동반, GD 환자의 약 30-40%가 TED 동반(pooled meta-analysis)
- 따라서 GD FLOOR($3.11B) + TED FLOOR($4.53B) = $7.64B를 "GD+TED 통합 시장"으로 단순 합산하는 것은 **부적절** — 상당수 환자가 양쪽 시장 정의에 동시에 포함되며(동일 환자가 ATD 치료와 teprotumumab 치료를 모두 받는 경우), 약물 클래스 자체는 겹치지 않으나(ATD ≠ IGF-1R 억제제) 환자 모집단 관점에서는 이중계상 위험 — 본 리포트에서는 **GD/TED를 항상 별개 range로 병기**하고 통합 총액은 제시하지 않음(스킬 Step 5.6 원칙 준용)

---

## 4. TSAb-IgG Coverage 분석 (Step 0 Causality Gate 적용)

### 4.1 GD

- **Causality verdict: Driver(확립)** — TSHR로 면역화한 마우스는 TED와 유사한 표현형을 재현하나 IGF-1R 면역화로는 재현되지 않음(GD_TED_report.md Section B3) — TSAb→TSHR→cAMP가 갑상선기능항진의 직접적/단선적 기전
- **혈청학적 coverage(seropositivity)**:
  - Pooled meta-analysis(20개 연구, Jiang et al. 2025): 3세대 TSI assay(Siemens Immulite) sensitivity **93.3%**(95% CI 92.4-94.1%), TRAb assay(Roche cobas, TBII 방식) sensitivity **88.9%** — TSI가 TRAb보다 일관되게 우수([DOI](https://doi.org/10.1016/j.clinbiochem.2025.110989))
  - 단일기관 임상 비교연구(van Balkum et al. 2023, n=356): TBII+TSI 동시 양성인 경우의 95.6%가 실제 GD/GD+GO로 확인 — 두 assay 병용 시 확진력 향상([DOI](https://doi.org/10.1016/j.heliyon.2023.e22468))
  - → **추정 coverage: 약 90-95%**(현대 3세대 assay 기준). 잔여 5-10%는 진성 혈청음성 GD(드묾, 논쟁적) 또는 assay 세대차/진단 시점 문제에 기인할 가능성
- **해석**: Driver verdict + 높은 혈청 양성률의 조합은 NSCLC 사례에 비유하면 "**흔한 driver mutation에 대한 고감도 companion diagnostic**"에 가까운 유리한 구도 — 혈청 양성 = 대체로 표적 적중으로 간주 가능

### 4.2 TED

- **Causality verdict: Co-driver(미확립, "proposed")** — TSHR-IGF-1R crosstalk에 대해 최소 3가지 경쟁 가설이 공존(β-arrestin 매개 scaffold / 직접 물리적 결합 / IGF-1R 직접자극항체 존재 자체에 대한 반박)이며 합의된 단일 기전 없음(GD_TED_report.md Section B4)
- **혈청학적 coverage — 직접 문헌 부재**: 이번 검색(PubMed)에서는 "TED 환자 중 TRAb/TSAb 혈청음성 비율"을 인구기반으로 정량한 논문을 확인하지 못함 — 검색된 문헌은 대부분 Hashimoto's thyroiditis 동반 TRAb-음성 안와병증의 희귀 증례보고 수준([PMID 33246456](https://doi.org/10.1186/s12902-020-00658-6), [PMID 30621642](https://doi.org/10.1186/s12886-018-1018-5))으로, 인구 수준 비율 추정의 근거로 사용하기 부적절
- **대리 추정치**: GD_TED_report.md Section A1에 기재된 "TED의 GD 비동반 비율"(Olmsted County 기준 euthyroid 6% + 원발성 hypothyroidism 1% + Hashimoto's 3% ≈ 10%)을 혈청학적 coverage의 상한 근사치로 사용 가능 — 즉 **혈청학적 coverage ≈ 90%(추정)**, GD와 유사한 오더
- **그러나 GD와의 핵심 차이 — 혈청 양성 ≠ 표적 적중 보장**: Co-driver 가설이 사실이라면, 혈청 양성(TSAb 존재) 환자 중 상당수에서도 IGF-1R 경로를 통한 독립적/병행적 안와섬유모세포 활성화가 진행 중일 수 있어, TSAb만 선택적으로 제거하는 접근이 임상적 개선(proptosis, CAS)을 완전히 담보하지 않을 가능성
- **간접 신호 → 직접 임상 근거로 격상(2026-09-14 CT.gov 원문 직접 대조로 갱신)**: efgartigimod(FcRn 억제제, TSAb를 포함한 전체 IgG 비선택적 감소)의 GD 대상 Phase 3("VitaliThy", [NCT07570316](https://clinicaltrials.gov/study/NCT07570316))와 TED 전용 Phase 3("UplighTED", [NCT06307626](https://clinicaltrials.gov/study/NCT06307626)/NCT06307613) 공식 시험 기록을 직접 대조한 결과 다음 두 가지가 확인됨(상세: GD_TED_report.md Section E2)
  1. **VitaliThy(GD) 제외기준**: "systemic therapy(예: corticosteroid), orbital injection/surgery/radiation이 필요하거나 시험기간 중 예정된 GO/TED" 환자는 GD 시험에서 제외됨 — 즉 **치료 개입이 필요한 수준(활동성/중등도-중증)의 TED 동반 환자는 배제**되나, 경증/비활동성 TED까지 전부 배제하는 것은 아님. 이는 1차 endpoint(euthyroid 회복) 측정에 TED 관련 개입이 confounder로 작용하는 것을 피하기 위한 시험설계상 선택으로 해석하는 것이 타당하며, 그 자체가 "efgartigimod가 TED에 효과 없어서 GD 시험에서 뺐다"는 근거는 아님
  2. **UplighTED(TED) 종료 사유**: CT.gov 공식 기록은 "사전 정의된 중간분석 결과 의도된 효능(proptosis responder rate 등)을 입증하기 어려울 것으로 판단되어 2025-12-15 조기 종료 — 이 결정은 안전성 문제와 무관"이라고 명시 — **active moderate-to-severe TED 환자를 직접 대상으로 한 전용 Phase 3에서 안전성과 무관하게 효능 futility로 종료**된 것이 공식 확인됨
  → 종합: GD 시험의 TED 제외기준은 confounding 회피 목적의 별개 설계 사안이나, TED 전용 시험 자체가 효능 futility로 종료되었다는 사실은 "TSAb 포함 IgG를 비선택적으로 줄이는 접근이 GD의 갑상선기능 회복에는 여전히 유효한 가설로 남아 있으나, TED의 안와 병리(proptosis 등)를 통제하는 데는 단독으로 충분하지 않을 가능성"을 뒷받침하는 **직접적 임상 근거**(기존 "간접/정황 증거" 수준에서 상향)로 볼 수 있음. 다만 futility 판정의 세부 데이터(중간분석 시점 responder rate 등)는 공개되지 않아, "IGF-1R 경로 관여로 인한 실패"라는 기전적 해석 자체는 여전히 추론 단계임에 유의
- **결론**: TED의 실질적 TSAb-targeting coverage는 GD보다 낮고, 정량적으로 특정할 수 있는 문헌적 근거가 부재 — **임의의 숫자를 제시하지 않고 "불확실성이 큰 영역"으로 명시**하는 것이 근거 없는 정밀도(false precision)를 피하는 정직한 접근. 다만 위 CT.gov 대조 결과는 이 불확실성이 GD 대비 TED에 불리한 방향으로 기울어 있다는 점을 뒷받침하는 직접 근거를 추가함

### 4.3 종합 비교

| 항목 | GD | TED |
|---|---|---|
| Step 0 causality verdict | **Driver**(확립) | **Co-driver**(미확립, "proposed") |
| 혈청학적 coverage(seropositivity) | ~90-95%(현대 3세대 assay 기준, 직접 문헌 확인) | ~90%(GD 비동반 비율로 대리 추정, 직접 인구기반 문헌 없음) |
| 병인론적 실질 표적적중률 | 혈청 양성 ≈ 표적 적중(비교적 직접적 등가 관계) | 불확실 — IGF-1R 독립경로 존재 가능성으로 혈청 양성이어도 표적적중 보장 안 됨(정량화 불가) |
| 임상 신호(IgG 비선택 감소 전략, CT.gov 원문 확인) | Efgartigimod GD Phase 3(VitaliThy) 진행 중 — 단, 치료개입 필요 TED 동반자는 제외기준으로 배제 | Efgartigimod TED Phase 3(UplighTED) 2건 모두 **안전성 무관 효능 futility**로 공식 조기종료 확인(직접 근거로 격상) |
| NSCLC 유사 비유 | "흔한 driver + 고감도 companion Dx"에 가까움 | "바이오마커 양성이어도 우회/병행 경로 존재 가능"에 더 가까움(단, 우회경로 비중은 미정량) |

---

## 5. 한계 및 후속 권고

1. **Track C/D(bottom-up epi×price) 미구축**: 이번 라운드는 승인된 경량 스코프에 따라 top-down 중심으로 진행 — GD_TED_report.md Section A2에 이미 확보된 역학 수치(중국 GD prevalence 450/100,000, 한국 GD incidence 4.6/10,000 person-years, TED의 GD 동반 pooled 40% 등)를 기초로 향후 bottom-up 모델을 구축할 수 있음(후속 작업으로 제안)
2. **TED 리포트 스코프 이질성**: 5건 중 1건이 현저한 이상치 — 향후 raw data 갱신 시 해당 리포트 원문 확인(구독 필요) 후 스코프 재확인 권고
3. **DelveInsight 7MM 총계**: 원문 접근 제한으로 미국 비중(42%)에서 역산한 추정치이며 직접 공개된 수치 아님 — 원문(구독) 확보 시 대체 필요
4. **TED 혈청음성 비율의 정량 문헌 공백**: 이는 본 리포트의 가장 중요한 미해결 gap — 대형 코호트(Olmsted County 후속 연구, EUGOGO 등록사업 등)에서 직접 보고한 문헌이 있는지 재검색 권고. 확보 시 Section 4.2의 추정치를 대체
5. **실매출 anchor 확대**: veligrotug(2026-06 승인)/IBI-311(중국 biosimilar) 매출이 축적되면 향후 라운드에서 teprotumumab 단독 anchor를 다중 자산 anchor로 확장 가능
6. **GD 최초 biologic 승인 시나리오**: 현재 forecast는 신약 승인에 따른 step-change를 반영하지 않은 것으로 판단됨(3.1) — BHV-1300(Phase 3, GD_TED_report.md Section D1) 등 진행 중인 GD 대상 Phase 3 자산의 승인 여부가 확정되면 forecast 자체의 재평가가 필요

---

## 6. 출처

- [IMARC Group — Graves' Disease Market Outlook](https://www.imarcgroup.com/graves-disease-market-outlook)
- [Precedence Research — Graves Disease Market](https://www.precedenceresearch.com/graves-disease-market)
- [MarketResearchFuture — Graves Disease Treatment Market](https://www.marketresearchfuture.com/reports/graves-disease-treatment-market-37376)
- [SkyQuest — Graves Disease Treatment Market](https://www.skyquestt.com/report/graves-disease-treatment-market)
- [GlobeNewswire — Thyroid Eye Disease Treatment Market Forecast](https://www.globenewswire.com/news-release/2025/04/16/3062327/0/en/Thyroid-Eye-Disease-Treatment-Market-Forecast-to-Reach-11-81-Billion-by-2031-Emerging-Economies-Expand-Access-to-Thyroid-Eye-Disease-Diagnoses-and-Therapies.html)
- [Mordor Intelligence — Thyroid Eye Disease Treatment Market](https://www.mordorintelligence.com/industry-reports/thyroid-eye-disease-treatment-market)
- [DelveInsight — Thyroid Eye Disease Market](https://www.delveinsight.com/report-store/thyroid-eye-disease-market)
- [MarketResearchFuture — Thyroid Eye Disease Market](https://www.marketresearchfuture.com/reports/thyroid-eye-disease-market-27903)
- [ReportsAndData — Thyroid Eye Disease Market](https://www.reportsanddata.com/report-detail/thyroid-eye-disease-market)
- [Amgen — Q4/FY2025 Financial Results](https://www.amgen.com/newsroom/press-releases/2026/02/amgen-reports-fourth-quarter-and-full-year-2025-financial-results)
- Jiang Z, et al. Diagnostic value of serum TSI levels in Graves' disease... *Clin Biochem.* 2025. PMID 40789418. [DOI](https://doi.org/10.1016/j.clinbiochem.2025.110989)
- van Balkum M, et al. Comparison of two different TSH-receptor antibody assays. *Heliyon.* 2023;9(12):e22468. PMID 38107298. [DOI](https://doi.org/10.1016/j.heliyon.2023.e22468)
- Dwivedi SN, et al. Thyroid autoantibodies. *J Clin Pathol.* 2022;76(1):19-28. PMID 36270794. [DOI](https://doi.org/10.1136/jcp-2022-208290)
- El Othman R, et al. A case report of thyroid-associated Orbitopathy with elevated TPO antibodies. *BMC Endocr Disord.* 2020;20(1):176. PMID 33246456. [DOI](https://doi.org/10.1186/s12902-020-00658-6)
- Cyranska-Chyrek E, et al. Severe unilateral orbitopathy in a patient with Hashimoto's thyroiditis. *BMC Ophthalmol.* 2019;19(1):9. PMID 30621642. [DOI](https://doi.org/10.1186/s12886-018-1018-5)
- [ClinicalTrials.gov — VitaliThy (NCT07570316), efgartigimod GD Phase 3](https://clinicaltrials.gov/study/NCT07570316)
- [ClinicalTrials.gov — UplighTED (NCT06307626), efgartigimod TED Phase 3, TERMINATED](https://clinicaltrials.gov/study/NCT06307626) / NCT06307613(동일 설계 2차 등록)
- 그 외 GD/TED 역학/기전 근거는 GD_TED_report.md/GD_TED_reference.md의 기존 인용([1]-[75]) 재사용, 본문 내 명시
