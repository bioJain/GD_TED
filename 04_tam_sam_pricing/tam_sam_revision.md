---
linear_issue: JHA-82
created: 2026-09-28
source: manual
milestone: cluster-4-tam-sam-pricing
status: in-review
inputs:
  - 00_legacy_unsorted/GD_TED_market_sizing_report.md
  - 00_legacy_unsorted/GD_TED_market_sizing_plan.md
  - 00_baseline_biomni/epi_soc_run_260914/report_graves_ted_landscape.md
  - 01_competitive_landscape/gd_line_of_therapy.md
  - 01_competitive_landscape/ted_line_of_therapy.md
  - 04_tam_sam_pricing/teprotumumab_veligrotug_pricing.md
  - 04_tam_sam_pricing/sources/README.md
  - 04_tam_sam_pricing/tam_sam_revision_qa.md
---

# GD/TED TAM/SAM range 및 TSAb-IgG coverage 재검토

> **기준일: 2026-09-28.** 본 문서는 동결된 legacy 초안을 의사결정용으로 재구성한 요약본임. 아래 시장금액, 환자 수, coverage 환산은 모두 **추정치(E), Evidence grade D**임. 상업 market report의 정의와 기준연도가 서로 달라 회계상 market size나 valuation으로 사용하기 전에 원문 scope 확인 및 bottom-up 검증이 필요함.

## 0. 한 장 브리핑

| 적응증 | FLOOR, 현재 top-down TAM (E, D) | PREMIUM, forecast top-down TAM (E, D) | TSAb 기준 mechanism SAM 해석 (E, D) | 의사결정 요약 |
|---|---:|---:|---|---|
| GD | **$3.11B**, 원자료 범위 $2.26B-$4.56B | **$5.04B**, 원자료 범위 $3.69B-$6.78B | TAM의 **약 90-95%가 serology-positive**일 가능성. 단순 금액 환산 시 FLOOR 약 **$2.80B-$2.96B**, PREMIUM 약 **$4.54B-$4.79B** | TSAb는 확립된 driver여서 혈청 양성과 표적 적중의 연결이 비교적 직접적. 다만 금액 환산은 환자별 지출이 동일하다는 검증되지 않은 가정임 |
| TED | **$4.53B**, 원자료 범위 $0.17B-$5.36B | **$8.09B**, 원자료 범위 $0.31B-$11.81B | serology proxy는 약 **90%**이나 병인론적 실질 coverage는 **정량 불가**. 따라서 금액 SAM 제시 보류 | TSAb는 proposed co-driver이고 IGF-1R 병행/독립 경로 가능성이 있어 혈청 양성만으로 임상 표적 적중을 보장하지 못함 |

**결론:** GD는 TSAb-IgG 접근의 우선순위가 높고 90-95%는 환자 선별의 출발점으로 사용할 수 있음. TED는 약 90% serology proxy를 SAM으로 곧바로 곱하지 말고, 별도의 clinical response haircut이 확보될 때까지 `NR`로 유지하는 것이 타당함. GD와 TED는 환자 overlap이 크므로 두 시장금액을 합산하지 않음.

**추가 결론:** mechanism SAM과 별도로 **therapy-line SAM 산출은 가능**함. 다만 현재 입력으로는 환자 수 기반의 exploratory range만 산출하며, top-down 시장금액에 치료선 비율을 곱한 dollar SAM은 제시하지 않음. 최종 상업 SAM은 `TAM 환자 pool x therapy-line eligibility x mechanism eligibility x access`의 교집합으로 산출해야 하며 mechanism SAM과 therapy-line SAM을 더하지 않음.

## 1. 산정 정의와 재검토 판정

### 1.1 이번 문서에서 사용하는 정의

- **TAM:** 공개 market report가 포괄하는 전체 GD 또는 TED 시장. `FLOOR`는 base-year 중앙 대표값, `PREMIUM`은 forecast-year 대표값임.
- **Mechanism SAM:** TAM 중 TSAb-IgG targeting이 병인론적으로 도달할 수 있는 부분. 환자 seropositivity와 causality를 함께 봄.
- **중요한 명명 한계:** FLOOR/PREMIUM은 현재/미래의 top-down TAM scenario이지, 그 자체가 TAM/SAM 구분은 아님. 특히 PREMIUM은 premium drug 가격을 적용한 bottom-up 결과가 아니라 상업 report forecast의 대표값임.
- **범위 밖:** 진단률, 치료율, eligible severity, 접근성, 점유율을 차감한 serviceable obtainable market은 산출하지 않음. Track C/D `epidemiology x price` 모델도 미구축 상태임.

### 1.2 원자료 재계산

| 항목 | 정렬된 원자료 | 산식 및 채택값 | 재검토 판정 |
|---|---|---|---|
| GD FLOOR | $2.260B, $2.640B, $3.585B, $4.557B | 중앙 2개 평균 = **$3.1125B**, 보고값 **$3.11B (E, D)** | 산술 일치 |
| GD PREMIUM | $3.690B, $4.050B, $6.037B, $6.782B | 중앙 2개 평균 = **$5.0435B**, 보고값 **$5.04B (E, D)** | 산술 일치 |
| TED FLOOR | $0.1654B, $3.420B, $4.530B, $4.714B, $5.360B | median = **$4.530B (E, D)** | 산술 일치. $4.714B는 미국 $1.980B/미국 비중 42%의 역산값임 |
| TED PREMIUM | $0.3051B, $6.910B, $8.090B, $11.810B | 기계적 median은 **$7.500B**. 협의 scope 이상치 $0.3051B를 제외한 3건 median **$8.090B (E, D)**를 채택 | 기존 문서의 `$8.09B로 보수적 채택` 표현은 부정확함. **scope-adjusted 대표값**으로 명시해야 함 |

- GD의 PREMIUM/FLOOR는 **1.62x**, TED의 scope-adjusted 값은 **1.79x**임. 이는 report forecast의 성장배수일 뿐 신약 launch uplift나 risk-adjusted peak sales 배수가 아님.
- TED base 범위는 약 **32.4x**로 scope 이질성이 매우 큼. $165.4M/$305.1M series는 원문 세부 정의를 확인하기 전 별도 sensitivity로 격리함.
- Tepezza FY2025 글로벌 매출 **$1.903B**는 TED FLOOR $4.53B의 약 **42%**임. 승인 약물 외 수술/IVMP/진단 포함 여부, 기준시점, 상업 report의 전망성 차이가 가능한 설명이며 어느 하나로 확정하지 않음.

## 2. 환자 pool 교차검증

Legacy top-down 금액은 환자 수에서 계산된 값이 아니므로 baseline의 환자 pool과 **직접 일치해야 하는 구조가 아님**. 대신 규모와 정의가 서로 모순되는지 아래처럼 대조함.

| 범위 | GD prevalence pool (E, D) | TED population-based prevalence pool (E, D) | TED의 GD 연동 pool, 경증 포함 (E, D) |
|---|---:|---:|---:|
| 7MM, 미국/EU5/일본 | **약 396만 명** | **약 19.6만-51.6만 명** | **약 135만 명** |
| 참고, 한국 | 약 10만 명 | 약 1.3만-3.4만 명 | 약 4.5만 명 |
| 참고, 중국 | 약 746만 명 | 약 34.7만-91.5만 명 | 약 328만 명 |

### 차이와 사유

1. **TED에서 두 환자 pool이 7MM 기준 약 2.6-6.9배 차이:** population-based 진단 prevalence와 `GD prevalence x 지역별 TED 동반율`이 같은 개념이 아님. 후자는 경증/일과성 안검 변화까지 포함하고, 전자는 의료기록에서 진단된 case에 가까워 더 작을 수 있음.
2. **지역 scope 불일치:** GD/TED market report에는 Global, 7MM, 10/18개국 및 미국 단독 수치가 혼재함. 따라서 7MM 환자 pool로 global market report의 implied annual spend를 계산하지 않음.
3. **질환 정의/비용 scope 불일치:** market report는 약물 외 수술, steroid, 진단을 포함할 수 있으나 epidemiology pool은 질환 보유자 수임. market value를 환자 수로 나눈 결과는 약가나 addressable 환자당 매출이 아님.
4. **검증 판정:** order-of-magnitude상 명백한 모순을 확정할 수는 없지만, 두 데이터셋은 독립 산출물이므로 서로를 검증했다고 볼 수도 없음. 다음 모델에서는 지역, severity/activity, 진단/치료율 및 치료비 scope를 통일해야 함.

## 3. TSAb-IgG coverage

### 3.1 GD: 높은 coverage, 비교적 직접적인 causality

- **Causality:** TSAb-TSHR-cAMP 축은 갑상선기능항진의 확립된 driver로 평가.
- **Serology:** 3세대 TSI assay meta-analysis sensitivity 93.3%, TRAb assay 88.9%를 바탕으로 **약 90-95% coverage (E, D)**를 유지.
- **Mechanism SAM:** 단순 환산은 FLOOR $3.11B x 90-95% = **$2.80B-$2.96B**, PREMIUM $5.04B x 90-95% = **$4.54B-$4.79B (모두 E, D)**.
- **제한:** assay sensitivity는 치료반응률이 아니며, market dollar가 biomarker status에 균등 분포한다는 보장도 없음. 위 금액은 screening ceiling에 가까운 방향성 scenario임.

### 3.2 TED: serology proxy와 실질 coverage를 분리

- **Causality:** TSHR-IGF-1R crosstalk에는 경쟁 가설이 존재하므로 TSAb를 **proposed co-driver**로 유지.
- **Serology proxy:** TED의 GD 비동반 비율 약 10%를 역으로 사용한 **약 90% (E, D)**임. TED 환자의 TSAb 양성률을 직접 측정한 population-based estimate가 아니므로 상한 근사치로만 사용.
- **실질 coverage:** IGF-1R 병행/독립 경로 가능성 때문에 `serology positive = TSAb 제거에 임상 반응`으로 등치할 수 없어 **정량 불가**.
- **임상 방향성 신호:** legacy 검토에서는 efgartigimod의 GD Phase 3 VitaliThy는 진행 중인 반면 TED Phase 3 UplighTED 2건은 안전성 문제가 아닌 efficacy futility로 조기 종료된 것으로 정리함. 이는 TED에서 비선택적 IgG 감소만으로 충분하지 않을 가능성과 일관되지만, 실패 원인을 IGF-1R로 확정하는 근거는 아님.
- **판정:** TED FLOOR/PREMIUM에 90%를 곱한 $4.08B/$7.28B는 계산 가능하나 **의사결정용 SAM으로 채택하지 않음**. 임상 response-based factor 없이 제시하면 false precision임.

### 3.3 GD/TED overlap

TED의 다수가 GD 맥락에서 발생하고 동일 환자가 GD 치료와 TED 치료를 모두 받을 수 있음. 치료비 category가 다르더라도 환자 기반 opportunity를 합산하면 이중계상 위험이 있으므로 **GD $3.11B + TED $4.53B = $7.64B를 통합 TAM으로 제시하지 않음**.

## 4. 별도 트랙: therapy-line SAM

### 4.1 산출 원칙

Therapy-line SAM은 biomarker가 아니라 실제 치료경로상의 위치를 기준으로 함. 따라서 mechanism SAM과 서로 다른 축이며 아래처럼 단계적으로 교차해야 함.

`질환 환자 pool -> 진단/치료 환자 -> 목표 severity/activity -> 목표 치료선 -> mechanism eligible -> 지역별 access`

- **GD:** 공식 severity stage가 없으므로 `newly diagnosed/ATD 1차`, `ATD 후 비관해 또는 재발`, `RAI/수술 후 persistent disease`를 구분함. RAI와 thyroidectomy는 환자 선호나 임상상황에 따라 처음부터 선택될 수 있어 무조건 2차로 간주하지 않음.
- **TED:** 단일 직선형 line이 아니므로 severity, activity, phenotype 및 시력 위협을 먼저 분기함. `mild supportive`, `active moderate-to-severe systemic 1차`, `approved targeted therapy`, `재발/무반응 후속`, `inactive rehabilitative surgery`를 별도 state로 둠.
- 한 환자가 시간에 따라 여러 state를 거칠 수 있으므로 prevalence state를 더해 unique patient TAM으로 만들지 않음.

### 4.2 `SCLC_Graves_population_model.xlsx` 검토 및 채택 판정

2026-09-28 공유된 [Google Sheets 원본](https://docs.google.com/spreadsheets/d/1urdrkYPYPKDpIBIhP0GsPKjK62GlxgtKkq8T2hIr_gk/edit?usp=sharing)의 `01_Assumptions`, `03_Graves`, `04_Sensitivity`, `05_Sources` 시트와 수식을 직접 확인함. PR에 binary XLSX를 포함하지 않고 [Google Drive XLSX direct export](https://docs.google.com/spreadsheets/d/1urdrkYPYPKDpIBIhP0GsPKjK62GlxgtKkq8T2hIr_gk/export?format=xlsx)로 연결했으며, 출처/검토일/검토 당시 export SHA-256은 [`sources/README.md`](sources/README.md)에 기록함. 이 모델은 미국 성인 신규 환자를 1차 ATD/RAI/수술, 1차 ATD 관해/비관해 또는 재발, 2차 ATD/definitive therapy 및 장기 저용량 ATD로 분기하므로 **therapy-line 구조에는 relevant**함. 그러나 아래 이유로 모델 출력은 모두 **E, D의 exploratory US scenario**로만 채택함.

| 검토 항목 | 판정 | 반영 방식 |
|---|---|---|
| Stock/flow 분리 | 적절 | 전체 유병 104.8만/131.0만/157.2만 명과 연간 신규 5.24만/7.86만/10.48만 명을 구분 |
| 1차 modality 분기 | 방향성 relevant | ATD 75%/82%/88%, RAI 11.1%를 사용하되 ATD share는 간접 역산 C, 수술은 잔차이므로 최종 base case로 고정하지 않음 |
| 1차 ATD 관해 | relevant | 37%/45%/56%를 사용해 post-ATD 비관해/재발 flow 산출. 문헌별 관해 정의/시점 차이를 유지 |
| 비관해/재발 후 2차 ATD/장기 유지 | 구조는 relevant, 비율은 취약 | 2차 ATD 선택 50%/60%/70%와 장기 유지 20%/30%/40%는 analyst assumption D이므로 sensitivity로만 표시 |
| ATD uncontrolled | 상업 target proxy로 relevant | 25%/27.5%/30%는 Immunovant 단일 기업 공시 B에 의존. 독립 검증 전 core SAM으로 채택하지 않음 |
| 출처 추적성 | 부분 미흡 | 일부 source row가 선행 세션/2차 경유 링크이고 원문 식별자가 없음. 특히 R08은 JAMA review를 명시하지만 URL은 Wikipedia 경유, R10/R12/R13은 원문 URL 미기재 |
| Scenario 결합 | 한계 있음 | Low/Base/High가 상관관계를 반영한 확률구간이 아니며 high에서 수술 share가 0.9%까지 축소됨. 범위 끝값을 신뢰구간으로 해석하지 않음 |
| 7MM 외삽 | 부적절 | 미국 치료선 분배를 EU5/일본에 적용하지 않고 미국 scenario만 교체. 기존 7MM 값은 coarse ceiling으로 격하 |

Workbook의 성별 유병률 입력은 전체 유병률 계산에 사용되지 않으며, 남성 0.5%/여성 3.0%와 전체 0.5%가 같은 표 안에서 산술적으로 양립하지 않음. 이번 SAM에는 해당 성별 입력을 사용하지 않음.

### 4.3 현재 입력으로 가능한 환자 수 proxy

#### GD: 미국 therapy-line flow

| 치료 state | Low/Base/High 환자 수 (E, D) | 산식 | 해석 |
|---|---:|---|---|
| 연간 신규 진단 | **5.24만/7.86만/10.48만 명** | 미국 성인 2.62억 x incidence 20/30/40 per 100,000 | 치료 전 flow. incidence는 역사적 단일 county 자료 기반 |
| 1차 ATD 시작 | **3.93만/6.45만/9.22만 명** | 신규 진단 x ATD share 75%/82%/88% | RAI/수술 initial choice를 제외하므로 기존 `전체 신규 x failure`보다 치료선 정의가 개선됨 |
| 1차 ATD 후 비관해/재발 | **2.48만/3.54만/4.06만 명** | 1차 ATD x (1 - remission 37%/45%/56%) | post-ATD therapy-line SAM의 우선 proxy. 각 scenario 내 연동값이며 단순 최솟값/최댓값 조합이 아님 |
| 2차 ATD 진입 | **1.24만/2.13만/2.84만 명** | 1차 비관해/재발 x 2차 ATD 선택 50%/60%/70% | 선택률이 D assumption이므로 sensitivity only |
| 1차 비관해/재발 후 즉시 RAI/수술 | **1.24만/1.42만/1.22만 명** | 1차 비관해/재발 - 2차 ATD | scenario가 단조롭지 않음. base가 low/high보다 큰 것은 결합 가정의 결과이며 오류가 아님 |
| 2차 ATD 후 재발/불응 | **0.77만/0.96만/0.69만 명** | 2차 ATD x (1 - 2차 remission 38%/55%/75.8%) | 2차 remission 범위가 넓고 source trace가 약해 exploratory only |
| ATD uncontrolled state-entry sensitivity | **1.33만/2.44만/3.70만 건** | workbook의 `1차+2차+장기유지` state-entry 합 x 25%/27.5%/30% | **환자 수 또는 연간 SAM으로 사용 금지.** 동일 신규 cohort의 순차 state를 합산하여 환자 중복이 있고, state별 treatment duration을 반영하지 않음 |

기존 문서의 `7MM 신규 21.2만 x 비관해/재발 50-70% = 10.6만-14.8만 명`은 1차 ATD 이외 modality를 차감하지 않아 therapy-line SAM을 과대평가할 수 있음. 따라서 **core therapy-line proxy에서 제외**하고, 지역별 치료분배 자료가 없는 7MM coarse ceiling으로만 보존함.

#### TED: 기존 7MM sensitivity 유지

| 치료 state | 환자 수 proxy (E, D) | 사용 가능성 및 제한 |
|---|---:|---|
| Systemic/targeted therapy 후보 | **약 2.9만-7.7만 명** | 7MM population-based prevalence 19.6만-51.6만 명 x 일본 청구 DB의 `치료 대상 중등도 이상 약 15%`. active 여부, phenotype, 진단/접근성 미차감 |
| 재발/무반응 후속치료 후보 | **약 0.65만-2.32만 명** | 위 후보 x 일본 draft 추가치료 필요 22-30%. 서로 다른 1차 치료, endpoint 및 지역을 혼합하므로 base case로 사용 금지 |

별도 broad severity check로 pooled review의 moderate-to-severe 22%와 sight-threatening 1%를 합치면 7MM prevalent pool의 약 **4.5만-11.9만 명**이나 active disease 및 실제 systemic treatment 대상과 같지 않아 base case로 채택하지 않음.

### 4.4 mechanism SAM과의 교집합

| 적응증 | Therapy-line pool (E, D) | Mechanism factor | 교집합 proxy (E, D) | 판정 |
|---|---:|---:|---:|---|
| 미국 GD, 1차 ATD 후 비관해/재발 | 연간 2.48만/3.54만/4.06만 명 | TSAb serology 90-95% | **Low 약 2.23만-2.35만, Base 약 3.19만-3.37만, High 약 3.65만-3.85만 명/년** | post-ATD mechanism-fit의 우선 방향성 proxy. 실제 label, contraindication 및 access 차감 필요 |
| 미국 GD, ATD uncontrolled | **교집합 산출 보류** | TSAb serology 90-95% | **NR** | 입력이 unique annual patients가 아니므로 serology를 곱해도 SAM이 되지 않음. 환자 단위 deduplication, state 점유기간, 관찰 기간을 통일한 후에만 재산출 |
| TED systemic/targeted therapy 후보 | 2.9만-7.7만 명 prevalent | 약 90% serology proxy | 산술상 약 2.6만-7.0만 명이나 **채택 보류** | TED는 serology가 clinical mechanism response를 보장하지 않으므로 별도 response/causality factor 없이는 SAM이 아님 |

위 결과는 **환자 수 SAM**이며 dollar SAM이 아님. 특히 top-down TAM은 generic ATD, RAI, surgery, steroid, 진단 및 biologic 지출을 서로 다른 비중으로 포함할 수 있어, 환자 비율을 시장금액에 바로 곱하면 치료선별 지출 구조를 왜곡함.

### 4.5 Dollar therapy-line SAM 산출에 추가로 필요한 입력

1. 지역별 diagnosed/treated rate와 치료선별 annual flow.
2. GD의 first ATD course 종료, non-remission/relapse 및 장기 low-dose MMI 선택 비율; RAI/thyroidectomy 이동 비율.
3. TED의 severity x activity x phenotype joint distribution과 각 1차 치료 mix.
4. 치료선별 product uptake, contraindication, payer authorization 및 reimbursement.
5. 제품별 regimen/vial rounding, gross-to-net 및 재치료 비용.

이 입력이 확보되면 `eligible patients x annual net cost per line` 방식으로 therapy-line dollar SAM을 산출하고, 현재의 top-down TAM 안에서 중복 여부를 검산함.

## 5. JHA-81 약가 비교 반영

JHA-81 repo 산출물은 작성되어 있으나 제공된 Linear context에서는 **In Review** 상태임. 따라서 아래 결론은 이번 문서에 **참조만** 하고 FLOOR/PREMIUM 산식에는 아직 편입하지 않음. JHA-81 review가 확정되면 그 결과를 최종 모델에 반영할 예정임.

1. Tepezza FY2025 매출 **$1.903B**는 현재 관측된 real-world revenue anchor로 유지.
2. Lumvoa의 공개 signal은 75 kg 환자 기준 **약 $450,000/course WAC**이며, Tepezza와의 `course-of-therapy parity` 설명임. vial/mg unit price가 동일하다는 뜻이 아니므로 두 제품에 동일 unit price를 적용하지 않음.
3. Lumvoa $450,000은 경영진 인용 2차 보도에 기반한 **Evidence grade C**이고 gross WAC임. 공식 unit WAC, net price, 제품별 CMS payment limit 및 누적 매출이 확인되지 않아 TAM/SAM의 실매출 anchor에는 합산하지 않음.
4. 따라서 본 문서의 FLOOR/PREMIUM은 가격 비교 결과로 재산정하지 않음. **JHA-81 결과 확정 후 반영 예정**이며, 향후 bottom-up model에서는 제품별 regimen, 체중, vial rounding, gross-to-net 및 payer access를 분리해야 함.

## 6. 발표용 메시지

> **GD는 현재 약 $3.11B에서 forecast 약 $5.04B 규모의 top-down TAM으로 보이며, TSAb가 확립된 driver이고 serology coverage가 약 90-95%여서 mechanism-fit이 높다. 미국 population workbook을 반영한 별도 therapy-line 관점에서는 1차 ATD 후 비관해/재발이 Low/Base/High 연간 약 2.48만/3.54만/4.06만 명이고, TSAb 교집합은 각각 약 2.23만-2.35만/3.19만-3.37만/3.65만-3.85만 명이다. 다만 치료분배와 비관해/재발 후 선택 가정이 취약해 E, D의 방향성 scenario다. TED는 현재 약 $4.53B, scope-adjusted forecast 약 $8.09B이고 systemic/targeted therapy 후보는 약 2.9만-7.7만 명으로 추정되나, 약 90% serology proxy를 임상 SAM으로 직접 환산하지 않는다. Tepezza 실매출 $1.903B는 관측 anchor로 유지하고, Lumvoa의 약 $450,000/course WAC signal은 제품별 가격 scenario로만 참조한다.**

## 7. 한계, next step 및 QA 상태

- **필수 next step:** 동일 지역/연도 기준 `prevalence/incidence -> diagnosed -> severity/activity -> therapy line -> TSAb-positive -> response-eligible -> access` cascade와 제품별 net course price를 적용한 bottom-up model 구축.
- **데이터 gap:** TED 직접 TSAb-positive population estimate, severity/activity별 환자 수, 진단/치료율, 2026 Tepezza unit WAC/net price, Lumvoa 공식 unit WAC/HCPCS/CMS payment limit.
- **업데이트 trigger:** Lumvoa 공식 가격/수가 또는 누적 매출, TED TSAb cohort, GD biologic 승인, 상업 report 원문 scope 확보 시 재산정.
- **QA 상태:** PR #19 follow-up에서 A1-H3 전 항목 QA, 산술 재계산, workbook 수식 대조, 일부 1차 출처 대조를 수행함. 다만 Tier-상 cross-model 검증이 남아 full QA는 미완료임. 상세 결과와 미해결 gap은 [`tam_sam_revision_qa.md`](tam_sam_revision_qa.md)에 기록함. 상업 report 원문 scope, workbook의 R08/R10-R13 원출처, TED direct TSAb cohort는 미확인이므로 본 문서는 `in-review`를 유지함.

## 8. 근거 추적

| claim | tier | 검증 방법 | 결과 | 일자 |
|---|---|---|---|---|
| GD/TED FLOOR/PREMIUM | 상 | legacy raw table에서 median 재계산 | GD 일치, TED $8.09B를 scope-adjusted 값으로 재명명 | 2026-09-28 |
| 2024 환자 pool | 상 | baseline 1.2/2.2 지역 합계 재계산 | 본문 합계와 일치 | 2026-09-28 |
| TSAb coverage | 상 | legacy 4.1/4.2의 근거/한계 재검토 | GD 90-95% 유지, TED 약 90%는 proxy로 강등 유지 | 2026-09-28 |
| Therapy-line 환자 pool | 상 | baseline 1.2/2.2, line-of-therapy 및 공유 workbook 수식/출력 대조 | 미국 post-ATD flow로 교체, 기존 7MM 단순값은 coarse ceiling으로 격하, dollar SAM은 보류 | 2026-09-28 |
| Tepezza/Lumvoa 가격 해석 | 상 | JHA-81 결론과 적용 제한 대조 | unit parity 금지, Lumvoa는 scenario만 반영 | 2026-09-28 |

### 사용한 repo 근거

- `00_legacy_unsorted/GD_TED_market_sizing_report.md`: raw market report, reconciliation, 실매출 anchor, TSAb-IgG coverage.
- `00_legacy_unsorted/GD_TED_market_sizing_plan.md`: TAM/SAM 목적, causality gate 및 경량 Track A/B 설계.
- `00_baseline_biomni/epi_soc_run_260914/report_graves_ted_landscape.md` 1.2/2.2: 2024 지역별 GD/TED 환자 pool.
- `01_competitive_landscape/gd_line_of_therapy.md`: GD 치료선 정의, ATD 기간/재발 및 definitive therapy 분기.
- `01_competitive_landscape/ted_line_of_therapy.md`: TED severity/activity 선분기, systemic/targeted/refractory 치료경로.
- `04_tam_sam_pricing/teprotumumab_veligrotug_pricing.md`: JHA-81 course price, coding 및 anchor 처리 결론.
- [`Google Drive XLSX direct export`](https://docs.google.com/spreadsheets/d/1urdrkYPYPKDpIBIhP0GsPKjK62GlxgtKkq8T2hIr_gk/export?format=xlsx): Google Sheets ID `1urdrkYPYPKDpIBIhP0GsPKjK62GlxgtKkq8T2hIr_gk`의 외부 workbook. 미국 GD state-transition 구조와 Low/Base/High formula 검토용. 가변 원본이므로 검토 시점 hash는 `sources/README.md`에서 대조.
