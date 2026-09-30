---
linear_issue: JHA-87
created: 2026-09-30
source: claude-code
milestone: cluster-1-competitive-landscape
status: draft
inputs:
  - 01_competitive_landscape/gd_line_of_therapy.md
  - 01_competitive_landscape/ted_line_of_therapy.md
  - 01_competitive_landscape/class_limitation_matrix.md
  - 01_competitive_landscape/moa_phase_matrix_extended.md
  - 00_legacy_unsorted/GD_TED_report.md
  - 00_baseline_biomni/epi_soc_run_260914/report_graves_ted_landscape.md
  - 00_baseline_biomni/landscape_v2/soc_outcomes_v2.csv
  - 00_baseline_biomni/landscape_v2/direct_source_documents_v2.jsonl
  - 00_baseline_biomni/landscape_v2/reference_v2.md
  - 03_mechanism_deepdive/r1b_asset_identification.md
---

# GD/TED address 가능 환자군 교차분석

> **분석 기준일:** pipeline/SoC frozen data cut 2026-09-10. JHA-73의 별도 live cross-confirm은 2026-09-29 기준이다. 이 문서는 JHA-70/71/72/73 결과와 legacy Section C6를 교차한 환자군 gap map이며, 치료 권고나 시장 규모 산출물이 아니다.

## 1. 결론

여기서 **현재 class 조합**은 JHA-72의 8개 행을 단순히 모두 병용한다는 뜻이 아니다. **SoC 4개 class(ATD, RAI, thyroidectomy, IVMP)와 JHA-73에서 확인한 active/approved pipeline class를 환자 여정에서 순차 또는 대안으로 사용할 수 있는 전체 선택지 집합**을 뜻한다. JHA-72의 `TSAb-IgG sweeping(eTPD)`은 임상 자산이 없는 concept이므로 현재 coverage에는 포함하지 않았고, JHA-73의 P1/preclinical 자산도 실제 환자 coverage로 계수하지 않았다.[12,13,14,15]

이 선택지 집합이 가장 잘 address하는 영역은 GD의 **thyroid hormone source control**과 TED의 **active inflammation/proptosis**다. 반대로 아래 환자군은 하나의 승인 또는 후기개발 class가 질환 상태, phenotype, 내약성, durability를 동시에 해결하지 못한다.

1. **ATD 장기불응/불내성 또는 중단 후 재발 GD 중 RAI/수술을 원치 않거나 부적합한 환자**
2. **Chronic/inactive TED 중 승인 IGF-1R 치료에 접근할 수 없거나 부적합/무반응이고, 고정 diplopia/proptosis/eyelid deficit에 수술도 원치 않거나 부적합한 환자**
3. **TRAb 음성 또는 assay-discordant TED**: 진단과 target engagement 선별에서 누락될 수 있고, TSHR/TSAb 표적 접근의 생물학적 적용 가능성도 불확실
4. **Steroid-resistant/intolerant active TED 및 IGF-1R inhibitor nonresponder/relapser**
5. **청각질환, diabetes, IBD, 감염 고위험, pregnancy/lactation, pediatric 등 독성 또는 근거 공백으로 주요 class 선택이 제한되는 환자**
6. **DON/각막 위협 환자**: routine drug sequence가 아니라 emergency IVMP/decompression access가 핵심이므로 일반 class 경쟁표로 포착되지 않음
7. **GD와 치료가 필요한 TED가 함께 있는 환자**: GD biochemical endpoint와 TED structural/inflammatory endpoint를 한 class가 모두 충족한다는 근거가 없음

따라서 여기서 `잔여 환자군`은 **치료가 전혀 없는 환자**가 아니라, 현재 SoC와 active pipeline을 합쳐도 핵심 임상 목표가 불완전하거나 선택지가 독성, 침습성, 접근성, 근거 부족으로 제한되는 환자를 뜻한다.

## 2. 교차분석 방법과 판정 기준

### 2.1 네 입력의 역할

| 입력 | 본 분석에서 답한 질문 |
|---|---|
| JHA-70 GD line-of-therapy | ATD, RAI, thyroidectomy가 어느 failure state를 처리하며 무엇을 남기는가 |
| JHA-71 TED line-of-therapy | Activity, severity, phenotype별 현재 경로가 어디서 끊기는가 |
| JHA-72 class 한계 | 각 class가 해결하지 못하는 endpoint와 contraindication은 무엇인가 |
| JHA-73 MoA x Phase | 해당 gap을 메울 active asset이 어느 indication/phase까지 존재하는가 |

### 2.2 `미포괄` 판정

- **완전 미포괄:** 현재 승인 systemic option이나 통상 SoC가 핵심 질환 상태를 직접 치료하지 않음
- **조건부 미포괄:** option은 있으나 contraindication, 불내성, 수술 부적합, 지역 access 또는 phenotype 불일치로 사용할 수 없음
- **durability 미포괄:** 초기 response option은 있으나 relapse/re-treatment의 장기 근거와 표준 경로가 확립되지 않음
- **진단/biomarker 미포괄:** assay 음성 또는 상태 전환 예측 불가로 올바른 class 배정 자체가 불안정함

`Approved`, `Phase 3` 또는 class 존재만으로 환자군을 포괄했다고 판정하지 않았다. 적응증, activity, endpoint, contraindication 및 실패 후 경로가 함께 맞아야 한다.

## 3. 질환/환자 상태 x class coverage map

| 환자 상태 | 현재 사용 가능 class/경로 | active pipeline의 가장 가까운 축 | 남는 gap | 판정 |
|---|---|---|---|---|
| Newly diagnosed GD, ATD 반응 | ATD로 biochemical control | GD P3 pan-IgG 제거/FcRn, P2 TSHR 길항 등 | Off-treatment durable autoimmune remission은 별도 endpoint | 부분 포괄 |
| ATD 중단 후 재발 또는 장기불응/불내성 GD | 장기 low-dose ATD, RAI, thyroidectomy | BHV-1300 P3, efgartigimod P3; GenSci098 P2; imeroprubart/felzartamab/rilzabrutinib P2 | 비침습적이고 pathogen-selective하며 치료 중단 후 지속되는 대안은 미확립. Active/severe TED, 임신, 큰 goiter, 수술 위험에 따라 선택지 축소 | **우선 잔여군** |
| 임신/수유 또는 pediatric GD | 임신 시기별 PTU/MMI, 전문 수술; RAI 제한/금기 | 해당 special population을 직접 포괄하는 후기 자산 확인 안 됨 | fetal/infant/growth safety와 장기 disease modification 자료 부족 | **조건부 잔여군** |
| Mild active TED | Local/supportive care, selected selenium | 다수 TED pipeline은 moderate-to-severe 중심 | 진행 예측과 조기 disease modification 기준 부족 | 부분 포괄 |
| Active moderate-to-severe, inflammation 중심 TED | IVMP 기반, 지역에 따라 IGF-1R therapy | IGF-1R P3/P2/P1, IL-6 계열, 기타 면역조절 | steroid/IGF-1R 부적합 또는 nonresponse, phenotype별 직접 비교 부족 | **조건부 잔여군** |
| IGF-1R 치료 후 nonresponse/relapse | 재평가 후 alternate immunomodulation, RT, surgery | 다른 IGF-1R 및 IL-6/CD40L/plasma-cell 축 | class 내 교체 효과, relapse 정의, retreatment와 장기 durability 불확실 | **durability 잔여군** |
| Chronic/inactive TED, 고정 구조 이상 | Staged surgery; 미국에서는 teprotumumab과 veligrotug가 activity/duration 무관 승인, EU/UK에서는 teprotumumab이 성인 moderate-to-severe TED에 승인; 중국은 IBI311 승인 | IBI311/MHB018A 등 inactive/chronic 연구 | 지역별 authorization/access 차이, IGF-1R 부적합/무반응, durability/retreatment와 실제 surgery-avoidance 근거, 이미 고정된 deficit의 잔존 | **조건부/durability 잔여군** [13,15,16,26] |
| TRAb 음성/assay-discordant TED | 임상상, imaging, 복수 assay를 포함한 진단 | TSHR/TSAb 표적 및 broad immune class가 존재하나 seronegative subgroup 근거 미확인 | 진단 지연, trial enrichment 누락, target biology와 response 예측 불확실 | **biomarker 잔여군** |
| DON/각막 위협 | Emergency IVMP, urgent decompression | 일반 pipeline sequence로 대체 불가 | referral/decompression 접근성과 vision-specific evidence가 핵심 | **경로 잔여군** |
| GD + 치료 필요 TED 동반 | GD modality와 TED therapy를 병행/순차 선택 | GD 자산과 TED 자산은 indication-specific으로 분리 개발 | Thyroid control, orbital disease, autoimmunity를 동시에 해결하는 검증된 class 없음. RAI는 TED 위험 때문에 제한 가능 | **교차 적응증 잔여군** |

## 4. 우선 잔여 환자군 상세

### 4.1 ATD 장기불응/불내성 또는 재발 GD

**진입 조건:** ATD 복용 중 poor control/중대한 toxicity, 통상 치료 후 relapse, 또는 장기 low-dose 유지에도 durable off-treatment remission을 기대하기 어려운 상태.

- JHA-70에 따르면 재발 후 RAI/thyroidectomy 또는 환자 선호 시 장기 low-dose MMI가 가능하다. 즉 임상 경로 자체는 존재한다.
- 그러나 RAI와 thyroidectomy는 thyroid-source control이며 pathogenic autoimmunity의 소실과 동의어가 아니다. 각각 영구 hypothyroidism/replacement, TED 악화 위험 또는 수술 합병증/접근성 부담이 남는다.
- Conventional-duration MMI RCT의 84개월 relapse는 56%였으나 특정 protocol의 단일 RCT 결과다. 이를 전체 5개국 GD pool에 곱해 `불응 환자 수`로 환산하지 않는다.
- JHA-73에서는 GD P3 pan-IgG 제거/FcRn 축과 P2 TSHR/면역 축이 확인되지만 승인된 disease-modifying GD class로 간주할 수 없다. Broad IgG lowering은 protective IgG 감소와 반복투여/rebound 부담을, TSHR 직접 차단은 정상 TSH signaling 차단과 초기 임상 근거 한계를 가진다.

**잔여 정의:** RAI/수술을 원치 않거나 부적합하면서, 반복/장기 ATD의 toxicity와 monitoring을 피하고 off-treatment durability를 원하는 환자.

### 4.2 Chronic/inactive TED

**진입 조건:** inflammatory activity가 안정화됐으나 proptosis, strabismus/diplopia, eyelid abnormality, exposure 등 기능/외형 후유증이 남은 상태.

- 고정된 기능/외형 후유증의 표준 재활 경로는 안정된 inactive/euthyroid 상태에서 decompression, strabismus surgery, eyelid correction 순의 staged surgery다.[13]
- 그러나 systemic option이 전혀 없는 것은 아니다. 미국에서는 teprotumumab과 veligrotug가 TED activity/duration과 무관하게 승인돼 chronic/inactive 환자도 label상 포함하며, teprotumumab에는 chronic/low-activity trial 근거도 있다. EU/UK teprotumumab label은 성인 moderate-to-severe TED를 포함하고, 중국에서는 IBI311이 승인돼 있다. 반면 일본 teprotumumab 승인은 active TED이고, 한국의 IGF-1R authorization/access는 curated input에서 unresolved다.[13,15,16,26]
- IVMP는 inactive fibrotic deficit을 일관되게 해결하지 못한다. 승인 IGF-1R therapy도 모든 고정 diplopia/eyelid deficit의 가역성, 장기 durability, retreatment 및 실제 surgery avoidance를 보장하지 않으며 hearing/metabolic/IBD risk나 access로 사용이 제한될 수 있다.[13,14]
- JHA-73은 IBI311의 active/inactive 시험과 MHB018A의 chronic/inactive P3을 추가로 포착한다. IBI311은 승인 자산이므로 `pipeline-only`로 분류하지 않고, ongoing inactive 연구는 승인 후 evidence expansion으로 구분한다.[15]

**잔여 정의:** 승인 IGF-1R option의 지역 access가 없거나, safety/contraindication/nonresponse 때문에 사용할 수 없거나, 치료 후에도 고정 deficit이 남으면서 수술도 원치 않거나 부적합한 환자. 따라서 chronic/inactive TED 전체를 `현재 systemic option 부재`로 계수하지 않는다.

### 4.3 TRAb 음성 또는 assay-discordant TED

- Legacy C6은 TSHRAb assay 병용에서도 9.4% 불일치를 기록했지만, 계획서의 `TRAb-seronegative TED 5-10%`는 원저로 직접 확인하지 못했다고 명시한다.
- 따라서 `TED pool x 5-10%` 계산은 수행하지 않는다. TRAb 음성은 진성 병태, assay sensitivity/cutoff, 질환 시점 효과가 섞인 operational subgroup일 수 있다.
- 이 환자군은 TSHR/TSAb 표적 class에서 특히 중요하다. Seronegativity가 실제 target 부재를 뜻하는지, 측정 한계인지에 따라 eligibility와 response 가설이 달라지기 때문이다.

**잔여 정의:** 임상/imaging상 TED가 의심되나 표준 serology가 음성이거나 assay 간 불일치하여 진단, trial inclusion 또는 target engagement 판단이 불명확한 환자.

### 4.4 Active TED 치료 실패/부적합

- Steroid-resistant/intolerant 환자는 IVMP의 hepatic/cardiovascular/metabolic/infection risk 때문에 반복 치료가 제한된다.
- IGF-1R inhibitor nonresponder/relapser는 다른 승인/개발 자산이 존재해도 class switch, retreatment, durable response를 연결하는 표준화된 근거가 부족하다.
- Hearing impairment, diabetes, IBD, pregnancy/pediatric 환자는 IGF-1R class의 safety 또는 근거 공백과 steroid toxicity가 겹칠 수 있다.
- FcRn은 GD에서 개발 중이지만 TED efgartigimod Phase 3 두 건이 futility로 종료돼 GD 결과를 TED rescue 효과로 외삽하지 않는다.

**잔여 정의:** Active disease가 남아 있으나 steroid와 IGF-1R 중 하나 이상이 ineffective, contraindicated, intolerable 또는 inaccessible하고, 대체기전의 확립된 순서가 없는 환자.

## 5. 환자 pool과 정량화 경계

### 5.1 5개국/지역 전체 disease pool

아래 합계는 baseline report 1.2/2.2장의 2024 인구 기반 값을 단순 합산한 **질환 전체 pool**이다. 환자 중복, 진단률, 치료 적격성 또는 잔여군 비율을 반영하지 않는다.[1,4,5]

| 질환 | 미국 + EU5 + 한국 + 일본 + 중국 합계 | 계산 | 사용 가능 범위 |
|---|---:|---|---|
| GD 유병 | 약 **1,152만 명** | 170 + 164 + 10 + 62 + 746만 | 상단 disease pool context만 가능 |
| GD 연간 신규 | 약 **60.6만 명/년** | 9.1 + 8.8 + 1.7 + 3.3 + 37.7만 | incidence context만 가능 |
| TED 유병, 인구기반 저/고 시나리오 | 약 **55.6만-146.5만 명** | 국가별 24.65/10만 및 65/10만 시나리오 합계 | TED 전체 시나리오, 잔여군 규모 아님 |
| TED 연간 신규, 저/고 시나리오 | 약 **11.2만-25.1만 명/년** | baseline 표의 반올림 수치 합계 | TED 전체 시나리오, 잔여군 규모 아님 |
| TED, GD 동반률 연동 추정 | 약 **467.5만 명** | 지역별 GD pool x 메타분석 동반률의 baseline 합계 | 경증/일과성 포함, 인구기반 pool과 합산 금지 |

> **근거등급 주의:** 위 환자 pool은 문헌 rate x 2024 인구의 추정치로, 본 이슈에서 **D 성격의 planning estimate**로 취급한다. 특히 TED의 인구기반 시나리오와 GD 연동 추정은 case definition과 포착 방식이 달라 서로 더하거나 평균내지 않는다.

### 5.2 잔여군 규모의 scenario estimate

아래 값은 환자 단위 관찰자료가 아니라 **전체 pool x 문헌 비율**의 planning scenario다. 환자군 간 중복이 크므로 합산할 수 없으며, `addressable`은 임상적으로 검토할 수 있는 상단 population이지 진단률, 접근성, 점유율을 반영한 시장 규모가 아니다.[1]

| 잔여군 | 계산 논리 | 5개국/지역 대략 규모 | Confidence | 해석 |
|---|---|---:|---|---|
| GD, 첫 ATD course 후 비관해/재발 | 연간 신규 GD 60.6만 x ATD-first 90% x 비관해/재발 50-70% | **연 27.3만-38.2만 명의 incident cohort** | **낮음-중간** | 12-18개월 뒤 발생하는 failure이므로 같은 calendar year의 환자 수가 아님. 90%는 국제 clinician survey, 50-70%는 remission 30-50%의 역산이며 국가별 practice와 장기 ATD로 크게 변동[2,3] |
| TED, 추가치료가 필요한 refractory/relapse | TED 연간 신규 저/고 11.2만-25.1만 x 22-30% | **연 2.5만-7.5만 명** | **낮음** | 22-30%는 일본 guidance context이며 전 지역 efficacy rate가 아님. Active/inactive와 약물별 failure가 혼재[13] |
| Chronic/inactive TED | TED 연간 신규 저/고 x 일본 inactive 74% | **연 8.3만-18.6만 명** | **매우 낮음** | 질환 자연사상 언젠가 inactive가 되는 사람의 scenario로, residual deficit이나 치료 필요 환자 수가 아님. 일본 한 국가의 단면 분포를 타 지역에 외삽[5] |
| TRAb 음성/assay-discordant TED | 검증된 공통 rate 없음 | **산출 불가** | **매우 낮음** | Legacy의 assay 불일치 9.4%를 진성 seronegative prevalence로 치환할 수 없음 |
| DON/각막 위협, special population, 수술 부적합 | 중복 없는 5개국 분모/rate 없음 | **산출 불가** | **매우 낮음** | 각각 임상 상태, contraindication, 선호, access가 겹치며 repo 입력에 joint distribution 부재 |

**핵심 범위:** 수치화 가능한 가장 큰 잔여 flow는 첫 ATD course 후 비관해/재발 GD의 연 27만-38만 명 scenario다. 그러나 이는 곧 특정 신약의 eligible population이 아니다. RAI/수술 선호, spontaneous/late remission, 장기 ATD, 연령, 임신, goiter, prior definitive therapy와 biomarker 기준을 적용하면 실제 trial/commercial eligibility는 감소한다.[2,3,6]

### 5.3 산출 가능한 제한적 예시와 산출 금지 항목

- 일본 자료는 TED 유병 2.5만-3.9만 명, 비활성 약 74%를 함께 보고한다. 같은 연구 맥락의 단순 곱은 약 **1.85만-2.89만 명**의 inactive TED를 시사하지만, severity, residual deficit, 치료 의향, 수술 적합성을 반영하지 않은 탐색적 상한 context다. 이를 일본의 addressable market으로 사용하지 않는다.[5]
- ATD conventional-duration RCT relapse 56%를 전체 GD pool에 직접 적용하지 않는다. 치료기간, 중단 eligibility, 추적, 지역 practice가 다르다.[3]
- TRAb-seronegative TED의 검증된 분모/rate가 없으므로 환자 수를 제시하지 않는다.
- Steroid/IGF-1R nonresponder, 수술 부적합, special population은 서로 중복 가능하므로 합산하지 않는다.

## 6. Anti-TSHR autoantibody 제거 class의 가상 target population

### 6.1 분석 대상과 근거 경계

본 절의 class는 circulating anti-TSHR autoantibody를 선택적으로 결합해 neutralization/clearance하는 접근을 뜻한다. LCA-0321은 sponsor가 anti-TSHR AAb LYTAC degrader로 설명하며 GD/TED 잠재 적응증을 제시했고, CTIS에는 GD Phase 1 SAD/MAD로 등록돼 있다.[7,8] MER511은 TSHR ectodomain-Fc fusion으로 anti-TSHR AAb neutralization/clearance와 antigen-specific B-cell 기능 억제를 의도하며, 현재 NEXUS는 성인 GD Phase 1 safety/PK/PD 시험이다.[9,10,11]

두 자산 모두 human efficacy, durable off-treatment remission, TED 구조적 개선을 아직 입증하지 않았다. 따라서 아래 coverage는 **target biology와 임상경로에 기반한 가설**이며 class effect가 아니다.[7,8,9,10,11]

**Evidence tier 규칙:** repo v2와 동일하게 A1은 official registry/regulator, A2는 society guideline, B1은 peer-reviewed primary/review, B2는 conference abstract, C1은 sponsor primary를 뜻한다. Tier는 source authority이지 추론의 확실성이 아니다. 아래 가설 행은 source tier와 별도로 `human efficacy 미확립`을 명시한다.

### 6.2 Address 가능성이 높은 환자군

| 우선순위/therapy line | 환자군 | 적합 논리 | 주요 필요조건 | 근거 tier |
|---|---|---|---|---|
| **1순위, GD 2차 또는 add-on** | ATD로 조절 중이나 TRAb/TSAb가 지속적으로 높고 중단 시 비관해 위험이 큰 환자 | Thyroid를 파괴하지 않고 pathogenic driver를 낮춰 ATD 감량/off-ATD normalization을 시험하기 가장 직접적 | 기능성 TSAb 양성, intact thyroid, reversible hyperfunction, ATD 병용 하에서 안전성/PD 확인 | **A1 registry/C1 sponsor/B2 abstract, human efficacy 미확립** [8,9,10,11] |
| **1순위, 재발 GD** | 첫 ATD course 후 biochemical relapse, RAI/수술 전 환자 | 현재 definitive therapy 전에 pathogen-directed option을 배치할 수 있음 | 재발 시점 TSAb 양성, 충분히 빠른 onset, rebound 억제 및 off-treatment durability | **A2 guideline/B1 primary, 배치전략은 추론** [3,6,12] |
| **2순위, newly diagnosed GD** | ATD와 병용해 빠른 antibody reduction 또는 remission 확률 개선을 노리는 환자 | 가장 큰 incident pool이나 자연 관해와 ATD 효과 때문에 incremental benefit 입증이 더 어려움 | ATD-alone 대조, remission enrichment biomarker, 장기 treatment-free endpoint | **A2 guideline/B1 primary, 배치전략은 추론** [2,3,6] |
| **탐색, early active TED** | 기능성 TSAb 양성이고 active inflammatory disease가 있으며 고정 fibrosis 전인 환자 | TSHR autoantibody가 orbital fibroblast signaling에 기여한다는 biology를 겨냥 | GD control과 별도로 CAS, proptosis, diplopia, QoL 개선 입증; steroid/IGF-1R 대비 또는 병용 자료 | **C1 sponsor/B2 abstract, preclinical/기전 외삽** [9,11,13] |

### 6.3 Address하기 어렵거나 불가능한 환자군

아래 한계는 GD/TED SoC와 공개된 construct 설명을 교차한 **mechanism-based hypothesis**이며 human outcome으로 확인된 class effect가 아니다.[7,9,11,12,13]

| 환자군 | 제한 원인 | Class-내재적 여부 |
|---|---|---|
| TRAb/TSAb 진성 음성 TED | 제거할 circulating target이 없거나 현재 assay가 포착하지 못함 | **내재적일 가능성 높음**, 단 assay false-negative이면 companion diagnostic으로 일부 회복 가능 |
| Chronic/inactive fixed fibrosis, stable strabismus/eyelid deficit | Autoantibody를 낮춰도 이미 형성된 구조 변화가 역전된다는 근거 없음 | **내재적 가능성 높음**, 재활 수술/anti-fibrotic 병용 없이는 coverage 제한 |
| DON/각막 위협 | 약효 onset을 기다릴 수 없고 urgent IVMP/decompression 필요 | **경로상 내재적 한계**, rescue를 대체하지 말고 adjunct/재발예방만 검토 |
| Thyroidectomy/ablative RAI 후 GD hyperthyroidism endpoint | Thyroid hormone source가 제거돼 GD biochemical benefit을 측정할 대상이 없음 | **적응증 구조상 내재적**, 동반 active TED는 별도 가능성 평가 |
| 큰 goiter/압박 또는 malignancy 의심 | 구조적/종양학적 문제는 autoantibody clearance로 해결 불가 | **내재적**, surgery 대체 불가 |
| TBAb/neutral TRAb가 섞인 환자 | 모든 anti-TSHR AAb 제거가 thyroid function에 미치는 순효과를 TSAb 감소만으로 예측하기 어려움 | **class risk**, 기능성 bioassay와 epitope/phenotype stratification으로 완화 가능 |
| Antibody-independent downstream inflammation이 우세한 TED | Cytokine, IGF-1R crosstalk, fibrosis 등 downstream disease가 지속 가능 | **class risk**, 병용 또는 phenotype selection 필요 |

### 6.4 Class pros/cons와 asset-level 차별화

Pros는 sponsor/preclinical design intent, cons와 전략은 그 intent가 충족되기 위한 검증 조건이다. MER511 또는 LCA-0321에서 아직 확인된 임상효과로 읽지 않는다.[7,8,9,10,11]

| 축 | Class-level pros | Class-내재적 cons | Asset-level 개발 전략 |
|---|---|---|---|
| 선택성 | FcRn/pan-IgG와 달리 protective total IgG를 보존할 잠재력 | 다양한 polyclonal epitope/affinity를 충분히 포획하지 못하면 escape | Patient sample panel에서 epitope breadth, TSAb/TBAb/neutral TRAb별 결합과 functional neutralization 검증 |
| 정상 생리 | Receptor 직접 길항보다 native TSH signaling을 보존할 잠재력 | TSHR ectodomain construct가 TSH 또는 정상 signaling에 간접 영향을 줄 가능성은 human에서 미확정 | TSH binding 없음, cAMP bioassay, euthyroid volunteer 불가 시 환자 내 TSH/FT4/FT3 exposure-response 입증 |
| 면역 범위 | 병원성 antibody와 antigen-specific B-cell source를 함께 줄이면 durability 가능 | Long-lived plasma cell이 계속 항체를 만들면 rebound, 반복투여 필요 | B-cell source suppression 여부, TRAb nadir/rebound, dosing-free remission을 장기 추적; 필요 시 plasma-cell therapy 병용 |
| Safety | General immunosuppression을 피할 잠재력 | Immune complex, Fc-mediated clearance, immunogenicity, soluble/tissue TSHR sink는 construct별 위험 | Fc effector silencing/endocytic bias, ADA/immune-complex/complement monitoring, SC formulation과 dose-exposure 최적화 |
| TED coverage | GD와 TED의 공통 upstream driver를 겨냥할 잠재력 | Circulating antibody 제거가 orbital tissue-bound signal과 established fibrosis를 되돌린다는 보장 없음 | Early active/TSAb-high enrichment, orbital biomarker, IGF-1R/anti-inflammatory 병용 cohort, inactive cohort는 별도 proof-of-concept |
| 실사용성 | Thyroid-preserving alternative가 될 잠재력 | Biologic 비용, 주사, 반복투여와 companion assay가 접근성을 제한 | SC/self-administration, 긴 half-life, functional TSAb assay, stopping rule과 retreatment algorithm 개발 |

### 6.5 연간 addressable population scenario

| Scenario | 산식 | 5개국/지역 patient flow | Confidence |
|---|---|---:|---|
| **Broad GD ceiling, 1차/2차 포함** | 신규 GD 60.6만 x ATD-first 90% | **연 약 54.5만 명** | **낮음-중간** |
| **Priority GD line, 첫 ATD course failure** | 60.6만 x 90% x 50-70% | **연 약 27.3만-38.2만 명** | **낮음-중간** |
| **TED biological ceiling** | 신규 TED 저/고 scenario 전체 | **연 약 11.2만-25.1만 명** | **낮음** |
| **Early/active TED proxy** | 신규 TED x active 26%, 일본 inactive 74%의 역산 | **연 약 2.9만-6.5만 명** | **매우 낮음** |

이 수치는 **technical addressability ceiling**이다. 실제 eligible population을 계산하려면 최소한 국가별 진단/치료율, functional TSAb 양성률, prior RAI/surgery, age/comorbidity, pregnancy, goiter, active TED, payer access의 joint distribution이 필요하지만 현재 repo에 없다. 특히 `TRAb 양성률`을 추가로 곱하지 않은 이유는 assay 종류와 disease stage에 따라 sensitivity가 달라지고, 이 class에는 단순 binding TRAb보다 functional TSAb 및 epitope coverage가 더 중요한 enrollment variable이기 때문이다. 따라서 priority GD의 27.3만-38.2만 명은 **asset별 label-eligible 수가 아니라 임상개발이 겨냥할 수 있는 line-level 후보군**으로만 사용한다.[7,8,9,10,11,12]

### 6.6 Coverage를 넓히는 임상개발 순서

1. **GD 2차/add-on에서 de-risk:** Stable ATD 환자 중 functional TSAb-high를 선별하고 antibody depletion, FT4/FT3 normalization, ATD reduction을 연결
2. **Durability를 차별화:** 치료 종료 후 6-12개월 이상 euthyroidism, TRAb/TSAb rebound 및 rescue therapy를 사전 정의
3. **Polyclonal breadth 입증:** 지역/인종과 disease duration을 넓힌 patient-derived antibody panel로 escape subgroup 규명
4. **TED는 별도 PoC:** Early active/TSAb-high cohort에서 GD biochemical endpoint와 독립된 proptosis/diplopia/CAS/QoL endpoint 사용
5. **Combination 전략:** Downstream inflammation에는 IGF-1R/anti-inflammatory, persistent antibody production에는 plasma-cell/B-cell 축과 순차 또는 병용을 검토
6. **제형/진단 동시개발:** SC dosing, functional TSAb companion assay, response-based stopping/retreatment rule로 접근성과 benefit-risk 개선

## 7. 주요 개발 class별 10년 positioning scenario

### 7.1 공통 산정 archetype과 지역별 patient flow

향후 class 간 비교에는 동일한 분모가 필요하므로 아래 다섯 archetype을 사용한다. 이는 forecast가 아니라 **어떤 therapy line을 겨냥할 수 있는지 보여주는 technical patient-flow scenario**다. 모든 비율은 지역별 직접 관찰값이 아니며, 특히 TED의 15%, 22-30%, 26%는 일본 자료/경로를 5개국에 외삽하므로 confidence가 낮거나 매우 낮다.[1,2,3,5,13]

- `G0`: 신규 GD x ATD-first 90%, broad medical-treatment ceiling
- `G1`: 신규 GD x ATD-first 90% x 첫 course 비관해/재발 50-70%, priority post-ATD line
- `T0`: 전체 신규 TED 저/고 scenario, broad biological/label ceiling
- `T1`: 신규 TED x non-mild 15%, systemic clinically significant proxy
- `T2`: 신규 TED x 추가치료 22-30%, refractory/relapse proxy

| 지역 | G0, broad GD | G1, post-ATD failure | T0, 전체 신규 TED | T1, systemic proxy | T2, refractory/relapse proxy |
|---|---:|---:|---:|---:|---:|
| 미국 | 8.2만 | 4.1만-5.7만 | 1.7만-3.8만 | 0.26만-0.57만 | 0.37만-1.14만 |
| EU5 | 7.9만 | 4.0만-5.5만 | 1.6만-3.7만 | 0.24만-0.56만 | 0.35만-1.11만 |
| 한국 | 1.5만 | 0.77만-1.07만 | 0.26만-0.57만 | 0.04만-0.09만 | 0.06만-0.17만 |
| 일본 | 3.0만 | 1.5만-2.1만 | 0.6만-1.4만 | 0.09만-0.21만 | 0.13만-0.42만 |
| 중국 | 33.9만 | 17.0만-23.8만 | 7.0만-15.6만 | 1.05만-2.34만 | 1.54만-4.68만 |
| **5개국/지역 합계** | **54.5만** | **27.3만-38.2만** | **11.2만-25.1만** | **1.7만-3.8만** | **2.5만-7.5만** |

> `T1`과 `T2`는 서로 독립 모집단이 아니며 크기 역전도 가능하다. `T1`은 한 시점의 severity proxy, `T2`는 치료 과정 중 추가치료 event proxy이기 때문이다. 두 값을 더하거나 funnel의 연속 단계로 사용하지 않는다.

### 7.2 IGF-1R inhibition

**현재 신호:** Teprotumumab, veligrotug/Lumvoa 및 중국 IBI311이 승인 축을 형성하고, linsitinib, MHB018A, VRDN-003 등 후기 자산이 active/chronic TED를 확장하고 있다. 이 class는 pipeline에서 가장 성숙한 TED 경쟁축이다.[15,16,17]

| 평가축 | 판단 |
|---|---|
| 가능한 positioning | Active moderate-to-severe TED의 proptosis/diplopia 중심 systemic backbone; chronic/inactive TED의 비수술 structural-improvement option; IV/SC/oral 및 dosing convenience 경쟁 |
| Priority population | `T1` 연 1.7만-3.8만 명. 미국 0.26만-0.57만, EU5 0.24만-0.56만, 한국 0.04만-0.09만, 일본 0.09만-0.21만, 중국 1.05만-2.34만 |
| Broad ceiling | Label과 근거가 activity/duration을 넓힐 경우 `T0` 연 11.2만-25.1만 명. 모든 mild TED가 약물치료 대상이라는 뜻은 아님 |
| Address하기 어려운 영역 | GD hyperthyroidism 자체, hearing/metabolic/IBD risk로 부적합한 환자, class nonresponder, DON emergency, fixed deficit 중 약물 비가역 영역 |
| Class-intrinsic risk | IGF-1R biology 관련 safety와 GD thyroid endpoint 부재; class 내 efficacy가 유사해지면 가격, route, cycle length와 durability가 경쟁축으로 이동 |
| Asset differentiation | Shorter course, SC/oral, hearing/glucose risk 완화, inactive-specific evidence, retreatment rule, surgery-avoidance endpoint |
| 2036 market role | **TED backbone 가능성 높음.** 다만 단일 독점보다 phenotype, activity, route별 다자 경쟁 구조 예상 |
| Confidence | **중간-높음**, 승인/후기 randomized evidence는 강하나 10년 sequencing과 장기 durability는 불확실 |

### 7.3 FcRn inhibition

**현재 신호:** Efgartigimod는 inadequately controlled GD Phase 3이 active인 반면 TED Phase 3 두 건은 terminated됐다. Imeroprubart는 GD Phase 2 축이다. 따라서 GD와 TED를 반드시 분리해 평가한다.[15,18]

| 평가축 | 판단 |
|---|---|
| 가능한 positioning | ATD에 inadequately controlled인 GD의 add-on/ATD-sparing; 빠른 total IgG/TRAb 감소가 필요한 pre-definitive line |
| Priority population | `G1` 연 27.3만-38.2만 명. 미국 4.1만-5.7만, EU5 4.0만-5.5만, 한국 0.77만-1.07만, 일본 1.5만-2.1만, 중국 17.0만-23.8만 |
| Broad ceiling | Newly diagnosed add-on까지 성공하면 `G0` 연 54.5만 명이나, ATD 단독 대비 incremental benefit과 반복투여 필요성을 입증해야 함 |
| Address하기 어려운 영역 | TED는 class extrapolation 불가; fixed orbital fibrosis, structural goiter, post-ablation thyroid endpoint, infection/high-risk IgG-lowering 부적합군 |
| Class-intrinsic risk | Protective IgG까지 낮추는 비선택성, infection/monitoring, IgG/autoantibody rebound와 chronic dosing |
| Asset differentiation | Albumin/IgG selectivity, 깊이와 회복속도, SC convenience, finite-course remission, baseline IgG/TRAb 기반 stopping rule |
| 2036 market role | **GD의 broad upstream competitor 가능성 중간.** ATD-free durability가 없으면 chronic add-on niche에 머물 수 있음 |
| Confidence | **중간**, GD 후기개발은 존재하나 efficacy result와 durable remission 미확립 |

### 7.4 Pan-IgG depletion/degradation

**현재 신호:** BHV-1300은 GD Phase 3과 biomarker study가 진행 중이며 anti-TSHR 선택적 제거가 아닌 pan-IgG extracellular degradation으로 분류된다.[15,19]

| 평가축 | 판단 |
|---|---|
| 가능한 positioning | FcRn과 유사한 post-ATD inadequate-control line; rapid/deep IgG reduction이 차별화될 경우 rescue-like finite induction |
| Priority population | `G1`과 동일한 연 27.3만-38.2만 명의 line-level ceiling. FcRn/anti-TSHR/TSHR blockade와 완전히 중복하므로 합산 금지 |
| Address하기 어려운 영역 | TED 독립 근거 없음, fixed fibrosis, true antibody-independent disease, protective IgG 감소가 위험한 환자 |
| Class-intrinsic risk | Pathogenic/non-pathogenic IgG 비선택성, infection와 rebound, 반복투여 시 cumulative immune burden |
| Asset differentiation | Depletion depth/onset, FcRn 대비 IgG recovery profile, finite dosing, infection signal, vaccine-response 보존, TRAb-to-total-IgG PD ratio |
| 2036 market role | **FcRn과 동일 GD segment를 두고 경쟁하는 high-efficacy/high-monitoring option.** superior finite-course durability가 없으면 차별화가 약함 |
| Confidence | **중간**, Phase 3 registry는 강한 개발 신호이나 결과 미확립 |

### 7.5 TSHR direct blockade/antagonism

**현재 신호:** GenSci098/YB-101은 GD P2/TED P1, K1-70은 GD 초기 임상이며 다수 preclinical TSHR program이 존재한다. Receptor-level pharmacology이므로 antibody titer와 무관하게 signaling을 차단할 잠재력이 있다.[15]

| 평가축 | 판단 |
|---|---|
| 가능한 positioning | GD의 ATD add-on 또는 대체, rapid biochemical control; anti-TSHR 제거제가 epitope escape를 보이는 환자의 대안; TED는 early active exploratory line |
| Priority population | GD는 `G1` 연 27.3만-38.2만 명; 성공적인 safety/route 확보 시 `G0` 54.5만 명까지 확장 가능 |
| Address하기 어려운 영역 | Fixed inactive TED, structural goiter/malignancy, DON emergency, post-thyroidectomy hyperthyroidism endpoint |
| Class-intrinsic risk | Native TSH signaling도 막아 hypothyroid pharmacology/hormone replacement 가능; disease driver를 제거하지 않아 drug-off rebound 가능 |
| Asset differentiation | Partial vs full antagonism, TSH/TSAb bias, oral/SC exposure, thyroid-selective distribution, titratability, treatment-free remission 또는 clean on/off control |
| 2036 market role | **GD의 receptor-level precision control niche.** 장기 약리 차단제로 자리잡거나 safety가 우수하면 ATD 대체 가능 |
| Confidence | **낮음-중간**, P2 이하이며 human durability/TED efficacy 부족 |

### 7.6 Plasma-cell/B-cell targeting

**현재 신호:** Felzartamab은 GD P2에서 CD38 plasma-cell depletion을, Cizutamig는 TED P1에서 BCMA x CD3 접근을 평가한다. Allogeneic/in-vivo CD19/BCMA CAR-T는 GD early P1이나 치료강도가 현 SoC와 크게 다르다.[15,20]

| 평가축 | 판단 |
|---|---|
| 가능한 positioning | 반복 재발/high-TRAb GD에서 autoantibody source를 줄이는 remission-directed 2차; steroid/IGF-1R refractory TED의 high-severity niche |
| Priority population | GD upper line은 `G1` 연 27.3만-38.2만 명이나 실제 benefit-risk 적합군은 훨씬 작을 가능성. TED는 `T2` 연 2.5만-7.5만 명의 refractory proxy가 상단 |
| Address하기 어려운 영역 | Mild/self-limited disease, 감염/혈액학적 위험이 큰 환자, fixed fibrosis, emergency decompression 필요군 |
| Class-intrinsic risk | Broad B/plasma-cell depletion, infection, hypogammaglobulinemia, cytokine-release/lymphodepletion 등 modality별 치료강도; antibody가 아닌 downstream pathology는 잔존 |
| Asset differentiation | Antigen-specific vs broad depletion, outpatient feasibility, immune reconstitution, vaccine response, finite-course remission, no-lymphodepletion platform |
| 2036 market role | **고위험 refractory niche 또는 finite-course remission class.** 안전성이 크게 개선되지 않으면 broad first-line은 어려움 |
| Confidence | **낮음**, P2/P1/early P1이며 GD/TED human outcome 미확립 |

### 7.7 IL-6/IL-6R blockade

**현재 신호:** Satralizumab은 TED regulatory-review 축, TOUR006은 P2이며, tocilizumab은 steroid-resistant TED의 off-label/연구 근거를 제공한다. 주된 가치는 orbital inflammation control이다.[13,15,21]

| 평가축 | 판단 |
|---|---|
| 가능한 positioning | Active moderate-to-severe TED의 steroid-sparing alternative; steroid-resistant/intolerant 환자; IGF-1R 부적합 또는 접근 제한 환자의 mechanism switch |
| Priority population | Broad systemic proxy `T1` 연 1.7만-3.8만 명. Refractory focus는 `T2` 연 2.5만-7.5만 명이나 두 proxy는 중복되고 직접 funnel이 아님 |
| Address하기 어려운 영역 | GD hyperthyroidism, inactive fixed proptosis/diplopia, DON에서 decompression 지연, infection/hepatic/neutropenia risk군 |
| Class-intrinsic risk | Inflammation은 낮춰도 structural response와 durable drug-free remission이 제한될 수 있음; chronic immune blockade/monitoring |
| Asset differentiation | Proptosis/diplopia 동반효과, SC convenience, steroid-sparing design, flare prevention, infection/liver/neutrophil safety, IGF-1R head-to-head |
| 2036 market role | **TED의 non-IGF-1R systemic alternative.** 가격/route/safety 우위가 있으면 second backbone, 아니면 refractory niche |
| Confidence | **중간**, 후기개발과 임상 신호가 있으나 최종 authorization/access 및 장기 positioning 변동 가능 |

### 7.8 IGF-1R/TSHR dual targeting

**현재 신호:** IBI3031은 TED Phase 1이고 VBS-102는 preclinical이다. 두 receptor 축을 동시에 겨냥하지만 dual blockade가 임상적으로 단일 IGF-1R보다 우월하다는 근거는 없다.[15,22]

| 평가축 | 판단 |
|---|---|
| 가능한 positioning | Active moderate-to-severe TED에서 inflammation/structural phenotype과 TSHR-driven biology를 동시에 겨냥; GD+TED 동반 subgroup의 통합 endpoint 탐색 |
| Priority population | TED `T1` 연 1.7만-3.8만 명. GD biochemical benefit이 입증되기 전에는 `G1`을 포함하지 않음 |
| Address하기 어려운 영역 | Inactive fixed fibrosis, seronegative/antibody-independent TED, DON emergency, dual-pathway safety 부적합군 |
| Class-intrinsic risk | 두 target 차단에 따른 safety/PK/PD 복잡성, 어느 component가 benefit을 만드는지 불명확, single-target 대비 개발비/증분효과 입증 부담 |
| Asset differentiation | Balanced potency, tissue exposure, receptor-specific PD, component-contribution design, GD/TED dual endpoint, IGF-1R safety 개선 |
| 2036 market role | **IGF-1R crowded market의 premium differentiation bet.** 명확한 superior efficacy 또는 GD 동시효과 없이는 자리 확보가 어려움 |
| Confidence | **매우 낮음**, P1/preclinical 중심 |

### 7.9 BTK inhibition

**현재 신호:** Rilzabrutinib은 adult GD P2이며 TED 독립 임상 단계로 계수하지 않는다. Oral immune signaling modulation이라는 사용 편의 잠재력이 있다.[15,23]

| 평가축 | 판단 |
|---|---|
| 가능한 positioning | ATD inadequate-control GD의 oral add-on; biologic 주사를 원치 않는 환자; B-cell/innate signaling phenotype의 precision option |
| Priority population | `G1` 연 27.3만-38.2만 명의 상단 line. Biomarker-defined responsive fraction은 미확인 |
| Address하기 어려운 영역 | TED structural disease, fixed fibrosis, structural goiter, definitive control이 긴급한 환자 |
| Class-intrinsic risk | Target가 TSHR-specific하지 않고 chronic systemic kinase inhibition 안전성/상호작용 부담; drug-off durability 불확실 |
| Asset differentiation | Reversible/covalent profile, selectivity, oral dose, bleeding/infection/hepatic safety, TSAb/TRAb response enrichment, finite-course 가능성 |
| 2036 market role | **편의성 중심 oral GD niche.** ATD보다 명확한 remission/안전성 우위가 없으면 add-on에 제한 |
| Confidence | **낮음**, 단일 P2 축이며 efficacy result 미확립 |

### 7.10 CD40L blockade

**현재 신호:** Frozen JHA-73에는 Lu AG22515 P1/2가 포함됐으나 2026-08 공개 후속정보에서는 TED 개발 중단이 보고됐다. 따라서 현재 시장형성 자산이 아니라 **target validation lesson**으로 취급한다.[15,24]

| 평가축 | 판단 |
|---|---|
| 가능한 positioning | 재진입 시 active TED의 upstream T-cell/B-cell costimulation modulation, steroid/IGF-1R alternative |
| Priority population | 활성 자산이 없으므로 **현재 evidence-based addressable flow는 0으로 처리**. 이론적 재진입 ceiling은 `T1`이나 시장 추정에 사용하지 않음 |
| Address하기 어려운 영역 | Fixed fibrosis, emergency DON, GD biochemical control; target modulation이 임상효과로 연결되지 않는 responder-selection 문제 |
| Class-intrinsic risk | Broad immune costimulation 조절, 감염/면역 risk, historical anti-CD40L thrombosis concern과 construct engineering 부담 |
| Asset differentiation | Fc-effector 제거, thrombotic risk 관리, target engagement-response biomarker, responder enrichment, 다른 적응증의 platform validation |
| 2036 market role | **Watchlist/재진입 option.** 신규 자산 또는 biomarker breakthrough 없이는 GD/TED 시장 비중 낮음 |
| Confidence | **낮음**, 해당 자산의 TED 중단과 class-wide 결론을 동일시할 수 없음 |

### 7.11 JAK/mTOR 및 기타 면역조절

**현재 신호:** Tofacitinib은 glucocorticoid-resistant/intolerant active TED P2, sirolimus는 active moderate-to-severe TED P2 investigator-led 축이다. Approved-in-other-disease repurposing은 개발속도 이점이 있지만 TED-specific benefit-risk가 별도로 필요하다.[15,25]

| 평가축 | 판단 |
|---|---|
| 가능한 positioning | Steroid-resistant/intolerant active TED의 oral/repurposed rescue; access가 제한된 시장의 off-label 또는 lower-cost alternative 가능성 |
| Priority population | `T2` 연 2.5만-7.5만 명의 refractory proxy. 실제 eligibility는 infection, age, comorbidity로 감소 |
| Address하기 어려운 영역 | Fixed inactive fibrosis, DON emergency, GD durable remission, 강한 structural response가 필요한 proptosis/diplopia |
| Class-intrinsic risk | Pleiotropic immunosuppression과 class별 infection/metabolic/thrombotic monitoring; TED-specific target selectivity 부족 |
| Asset differentiation | Short-course regimen, local/orbital delivery, biomarker-selected inflammation, comparative steroid-sparing trial, generic/access advantage |
| 2036 market role | **지역/access 기반 refractory niche.** Large registrational evidence가 없으면 premium targeted class와 직접 경쟁하기 어려움 |
| Confidence | **낮음**, 소규모/단일기관 또는 investigator-led P2 중심 |

### 7.12 Emerging/표적미공개 자산의 처리

IL-11R은 JHA-73 frozen matrix에 active asset이 없고, KHN939/SCTT11은 phase는 확인되지만 target이 공개 검증되지 않았다. 이들은 asset watchlist에는 포함하되 mechanism class별 10년 positioning 또는 환자 수에 배분하지 않는다. 표적을 임의 추정하면 class coverage를 이중계수할 위험이 있기 때문이다.[15]

## 8. 2036 종합 비교와 시장구조

### 8.1 Class positioning 비교표

| Class | 주 질환/우선 line | 연간 5개국 priority flow | 10년 가능한 역할 | 구조적으로 어려운 영역 | 핵심 승부처 | Confidence |
|---|---|---:|---|---|---|---|
| IGF-1R | TED systemic, active 및 chronic 확장 | `T1` 1.7만-3.8만 | TED backbone, phenotype/route별 다자경쟁 | GD control, class nonresponder, emergency DON | Durability, hearing/metabolic safety, route, inactive evidence | 중간-높음 |
| FcRn | GD post-ATD/add-on | `G1` 27.3만-38.2만 | Broad upstream GD competitor | TED 외삽, protective IgG 감소 | Finite-course remission, infection, rebound | 중간 |
| Pan-IgG 제거 | GD post-ATD/add-on | `G1` 27.3만-38.2만 | FcRn 대체/경쟁 high-depletion option | TED 근거, 비선택성 | Depletion/recovery profile, durability | 중간 |
| Anti-TSHR AAb 제거 | GD post-ATD, TED 탐색 | `G1` 27.3만-38.2만 | Pathogen-selective thyroid-preserving class | 진성 seronegative, fixed fibrosis | Polyclonal breadth, B-cell source/rebound, SC | 낮음 |
| TSHR blockade | GD biochemical control | `G1` 27.3만-38.2만 | Precision receptor-control niche/ATD 대체 | Fixed TED, native TSH blockade | Biased/partial antagonism, oral/SC, titration | 낮음-중간 |
| Plasma/B-cell | Refractory GD/TED | GD `G1`, TED `T2` 상단 | Finite-course remission 또는 high-risk niche | Mild disease, infection-risk, fibrosis | Antigen specificity, immune reconstitution, outpatient use | 낮음 |
| IL-6/IL-6R | Active systemic/refractory TED | `T1` 1.7만-3.8만 | Non-IGF-1R second backbone | GD, fixed structural deficit | Steroid sparing, route, structural response | 중간 |
| IGF-1R/TSHR dual | Active TED, GD+TED 탐색 | `T1` 1.7만-3.8만 | Premium differentiated TED option | Fibrosis, emergency, complexity | Component contribution, superior efficacy | 매우 낮음 |
| BTK | GD oral add-on | `G1` 27.3만-38.2만 | Convenience-driven oral niche | TED structure, definitive need | Selectivity, safety, remission vs ATD | 낮음 |
| CD40L | 현재 active market asset 없음 | 0 | Watchlist/biomarker 기반 재진입 | Target validation, fibrosis | Safety engineering, responder biomarker | 낮음 |
| JAK/mTOR/기타 | Refractory active TED | `T2` 2.5만-7.5만 | Access/repurposing 기반 niche | GD remission, fixed TED | Short course, comparative data, affordability | 낮음 |

> 각 행의 patient flow는 **경쟁 class가 공유하는 동일 환자 pool**이다. 예를 들어 GD `G1`을 FcRn, pan-IgG, anti-TSHR, TSHR blockade, B/plasma-cell, BTK에 각각 배정한 뒤 합산하면 동일 환자를 여러 번 세는 오류가 된다.

### 8.2 10년 시장 형성 시나리오

| Scenario | 시장 구조 | 승자 조건 | 뒤처질 가능성이 큰 접근 |
|---|---|---|---|
| **Base case: phenotype별 다중 backbone** | TED는 IGF-1R backbone + IL-6/기타 rescue, GD는 ATD 뒤 복수 immune/TSHR class 경쟁 | 승인 efficacy, manageable safety, 편한 route, 명확한 sequencing | 초기단계에서 biomarker/endpoint 차별화가 없는 me-too |
| **Durable-remission case** | GD에서 finite-course로 ATD-free remission을 만드는 class가 post-ATD line을 통합 | 6-12개월 이상 drug-free durability, rebound 억제, thyroid 보존 | Chronic dosing만 가능하고 RAI/수술 대비 lifetime burden이 큰 class |
| **Precision-segmentation case** | Functional TSAb, TRAb, activity, fibrosis, hearing/metabolic risk로 시장 세분화 | Companion biomarker와 responder enrichment | Broad immunosuppression이나 target-negative 환자를 구분하지 못하는 개발 |
| **Combination/sequencing case** | Upstream antibody/B-cell class 뒤 downstream IGF-1R/IL-6 또는 반대 순서 | 비중복 toxicity, additive endpoint, 짧은 총 치료기간 | 같은 독성을 중첩하거나 component contribution을 설명하지 못하는 병용 |
| **Access-driven case** | 고가 biologic은 미국/중국 일부 중심, repurposed/oral/SC가 지역별 share 확보 | SC/oral, 짧은 cycle, 낮은 monitoring, reimbursement evidence | Infusion-heavy chronic regimen, specialist-center 의존 class |
| **Failure/consolidation case** | 후기 실패와 safety로 IGF-1R/SoC 중심 시장 유지 | Hard clinical outcome과 real-world durability | Biomarker 개선만 있고 proptosis/diplopia/euthyroidism으로 연결되지 않는 class |

### 8.3 임상 + 시장구조 관점의 우선순위

1. **TED:** IGF-1R은 가장 높은 시장형성 확률, IL-6는 가장 가까운 non-IGF 대안, dual/B-cell/JAK-mTOR는 differentiation 또는 refractory niche
2. **GD:** 가장 큰 미충족 flow는 `G1`이나 여섯 class가 같은 pool을 경쟁. 승부는 초기 biochemical response보다 **finite-course ATD-free durability와 thyroid preservation**
3. **공통:** 단일 class가 GD thyroid function, TED inflammation, inactive fibrosis를 모두 해결할 가능성은 낮아 sequencing/combination 시장이 기본 case
4. **Asset differentiation:** 같은 target 내에서는 efficacy만이 아니라 route, treatment duration, retreatment, safety monitoring, regional reimbursement가 share를 결정
5. **수치 해석:** 이 절은 환자 수 forecast나 매출 추정이 아니다. 국가별 diagnosis/treatment/access/price/share 데이터가 추가되기 전에는 clinical opportunity ceiling으로만 사용

## 9. Legacy Section C6 통합본

Legacy report는 동결하고, C6의 다섯 항목을 아래와 같이 현재 결과에 통합한다.

| Legacy C6 항목 | JHA-70/71/72/73 교차 후 통합 판정 | 후속 데이터 요구 |
|---|---|---|
| Teprotumumab 이후 비용/청각 AE/durability | IGF-1R class는 active TED의 중요한 축이나 hearing impairment, hyperglycemia 등 safety와 nonresponse/relapse 후 경로가 남음. 다른 IGF-1R 후기 자산의 존재만으로 class gap 해소 판정 불가 | 독립 장기 추적, standardized relapse, retreatment, class-switch, 지역 access |
| Legacy의 inactive TED systemic option 부재 주장 | **현재 기준으로 교정:** 미국 teprotumumab/veligrotug는 activity/duration 무관 승인이고 EU/UK teprotumumab 및 중국 IBI311도 현재 systemic coverage를 제공한다. 수술 재활은 고정 deficit에 여전히 중요하며, 잔여 gap은 지역 access, IGF-1R 부적합/무반응, durability/retreatment 및 surgery-avoidance 근거 부족이다.[13,15,16,26] | Region/activity별 access, fixed-deficit functional outcome, 수술 회피, 장기 durability |
| TRAb 음성 TED | 9.4% assay discordance는 진단 gap을 지지하나 seronegative prevalence 5-10%는 미확인 상태 유지 | 복수 assay와 imaging을 쓴 prospective prevalence, target-positive tissue/response 분석 |
| GD 재발/장기관리/임신 | RAI/수술/장기 low-dose ATD 경로는 있으나 비침습적 durable disease modification과 special-population evidence 부족 | Off-treatment remission, TSAb/TRAb-stratified response, pregnancy/pediatric safety |
| TED 진행 및 active-inactive 전환 예측 | 치료 전 activity/phenotype 분류는 가능하지만 진행/재활성화/섬유화 전환을 예측하는 검증 biomarker 부족 | Longitudinal biomarker-imaging cohort, transition/relapse endpoint 표준화 |

## 10. 개발 및 연구 우선순위

1. **GD:** `ATD-free euthyroidism`뿐 아니라 치료 중단 후 durability, TRAb/TSAb rebound, TED outcome을 함께 측정
2. **Inactive TED:** 수술 회피, diplopia/function, proptosis, QoL 및 장기 재활성화를 별도 endpoint로 측정
3. **TRAb 음성 TED:** assay panel, imaging, phenotype 및 치료반응을 묶은 prospective subgroup 정의
4. **Failure-state trial:** Primary nonresponse, partial response, taper flare, post-treatment relapse, inactive residual deficit을 분리
5. **교차 적응증:** GD biochemical control과 TED activity/structure를 동시에 추적하며 한쪽 개선을 다른 쪽 cure로 표현하지 않음
6. **Special population:** Pregnancy/lactation, pediatric, diabetes, IBD, hearing impairment, infection risk별 안전성/대체기전 자료 확보

## 11. 해석 한계와 QA 상태

- 본 분석은 class의 기전상 가능성과 임상적으로 입증된 coverage를 구분한다. Preclinical/P1 자산은 환자군 coverage로 계수하지 않았다.
- 지역별 authorization/reimbursement가 `unresolved`인 경우 비승인/비급여로 단정하지 않았다.
- `soc_outcomes_v2.csv`의 special-population 행은 guideline 기반 경로 확인에 사용했으며 환자 비중 산출에는 사용하지 않았다.
- 상 tier인 역학 원 수치는 baseline 문서 값을 재사용했다. 신규 DOI 3건의 metadata는 Crossref로 대조했지만 역학 원 수치의 독립 cross-model QA와 원문 direct-quote 대조는 수행하지 않았으므로 그 절차가 끝날 때까지 `draft`를 유지한다.
- 가설 단계의 TSAb-IgG sweeping을 MER511/LCA-0321/BHV-1300 또는 다른 임상 class의 실증으로 간주하지 않았다.

## 12. 참고문헌

1. Biomni. *Graves' Disease 및 Thyroid Eye Disease 경쟁환경 조사: 역학, 진단, 병기, 표준치료*. 2026-09-14. `00_baseline_biomni/epi_soc_run_260914/report_graves_ted_landscape.md`.
2. Villagelin D, et al. A 2023 International Survey of Clinical Practice Patterns in the Management of Graves Disease: A Decade of Change. *J Clin Endocrinol Metab.* 2024. DOI: [10.1210/clinem/dgae222](https://doi.org/10.1210/clinem/dgae222).
3. Azizi F, et al. Risk of recurrence at withdrawal of short- or long-term methimazole therapy in Graves' hyperthyroidism. *Endocrine.* 2024;84:577-588. PMID: [38165576](https://pubmed.ncbi.nlm.nih.gov/38165576/).
4. Chin YH, et al. Prevalence of thyroid eye disease in Graves' disease: A meta-analysis and systematic review. *Clin Endocrinol.* 2020. DOI: [10.1111/cen.14296](https://doi.org/10.1111/cen.14296).
5. Watanabe M, et al. Prevalence, Incidence, and Clinical Characteristics of Thyroid Eye Disease in Japan. *J Endocr Soc.* 2023. DOI: [10.1210/jendso/bvad148](https://doi.org/10.1210/jendso/bvad148).
6. Kahaly GJ, et al. 2018 European Thyroid Association Guideline for the Management of Graves' Hyperthyroidism. *Eur Thyroid J.* 2018;7:167-186. DOI: [10.1159/000490384](https://doi.org/10.1159/000490384).
7. Lycia Therapeutics. [Programs: LCA-0321](https://lyciatx.com/pipeline/programs/). 확인일: 2026-09-10.
8. Clinical Trials Information System. [2025-524053-14-00, LCA-0321-01](https://ctis.eu/trial/2025-524053-14-00). Frozen record: 2026-09-10.
9. Merida Biosciences. [Pipeline & Programs: MER511](https://meridabio.com/pipeline-programs/). 확인일: 2026-09-29.
10. ClinicalTrials.gov. [NCT07305818, NEXUS](https://clinicaltrials.gov/study/NCT07305818). 확인일: 2026-09-29.
11. Merida Biosciences. Specific and Deep Depletion of anti-TSHR Autoantibodies for the Treatment of Graves' and Thyroid Eye Disease. *J Endocr Soc.* 2025;9(Suppl 1). DOI: [10.1210/jendso/bvaf149.2238](https://doi.org/10.1210/jendso/bvaf149.2238).
12. JHA-70. *Graves' disease 치료 line-of-therapy*. `01_competitive_landscape/gd_line_of_therapy.md`.
13. JHA-71. *TED 치료 line-of-therapy*. `01_competitive_landscape/ted_line_of_therapy.md`.
14. JHA-72. *GD/TED class별 핵심 한계 비교표*. `01_competitive_landscape/class_limitation_matrix.md`.
15. JHA-73. *GD/TED MoA class x indication-specific 개발단계 통합 매트릭스*. `01_competitive_landscape/moa_phase_matrix_extended.md`.
16. US FDA. [LUMVOA (veligrotug-vvze) Prescribing Information](https://www.accessdata.fda.gov/drugsatfda_docs/label/2026/761530Orig1s000lbl.pdf). 2026.
17. ClinicalTrials.gov. [NCT06989918, MHB018A in active TED](https://clinicaltrials.gov/study/NCT06989918); [NCT07753603, linsitinib Phase 3](https://clinicaltrials.gov/study/NCT07753603). Frozen/live cross-confirm은 JHA-73 참조.
18. ClinicalTrials.gov. [NCT07570316, efgartigimod in GD](https://clinicaltrials.gov/study/NCT07570316); [NCT06307613, terminated TED study](https://clinicaltrials.gov/study/NCT06307613). Frozen/live cross-confirm은 JHA-73 참조.
19. ClinicalTrials.gov. [NCT07661056, BHV-1300 Phase 3 GD](https://clinicaltrials.gov/study/NCT07661056); [NCT06980649, biomarker study](https://clinicaltrials.gov/study/NCT06980649).
20. ClinicalTrials.gov. [NCT07722546, felzartamab in GD](https://clinicaltrials.gov/study/NCT07722546); [NCT07597200, cizutamig in TED](https://clinicaltrials.gov/study/NCT07597200).
21. ClinicalTrials.gov. [NCT05987423](https://clinicaltrials.gov/study/NCT05987423) and [NCT06106828](https://clinicaltrials.gov/study/NCT06106828), satralizumab Phase 3 TED.
22. ClinicalTrials.gov. [NCT07622368, IBI3031 Phase 1 TED](https://clinicaltrials.gov/study/NCT07622368).
23. ClinicalTrials.gov. [NCT06984627, rilzabrutinib Phase 2 GD](https://clinicaltrials.gov/study/NCT06984627).
24. JHA-80. *R1b 자산 식별 및 CD40L 적응증 분석*. `03_mechanism_deepdive/r1b_asset_identification.md`.
25. ClinicalTrials.gov. [NCT07547930, tofacitinib in refractory/intolerant TED](https://clinicaltrials.gov/study/NCT07547930); [NCT04936854, sirolimus in active TED](https://clinicaltrials.gov/study/NCT04936854).
26. US National Library of Medicine DailyMed. [TEPEZZA (teprotumumab-trbw) current prescribing information](https://dailymed.nlm.nih.gov/dailymed/drugInfo.cfm?setid=3e6c54a1-cefd-4a5b-a855-ab9f268b6cce). Regulator/NLM label repository; 확인일: 2026-09-10.

## 13. 검증 로그

| 점검 항목 | Tier | 방법 | 결과 | 일자 |
|---|---|---|---|---|
| JHA-70/71/72/73 반영 | 하 | 네 산출물의 line, class 한계, indication-specific phase를 수동 교차 | PASS | 2026-09-30 |
| Legacy C6 통합 | 하 | C6 다섯 bullet을 9절에서 1:1 대조 | PASS | 2026-09-30 |
| 5개국/지역 pool 산술 | 상 | baseline 1.2/2.2 표의 표시값 단순 합산 | PASS, 독립 QA/direct quote 대조 대기 | 2026-09-30 |
| 잔여군 정량 과장 방지 | 하 | TRAb 음성/ATD relapse/중복 subgroup의 전 population 외삽 금지 확인 | PASS | 2026-09-30 |
| 신규 참고문헌 DOI metadata | 상/중 | Crossref API에서 DOI 3건 title/author/year 대조 | PASS | 2026-09-30 |
| 10년 class scope | 하 | JHA-73 active matrix의 주요 10개 class + emerging watchlist 대조 | PASS | 2026-09-30 |
| 지역별 scenario 산술 | 상 | 5개 지역 G0/G1/T0/T1/T2 산식과 합계 재계산 | PASS, 원 비율의 독립 QA 대기 | 2026-09-30 |
| Chronic/inactive TED 현재 coverage | 상 | JHA-71 authorization table, US teprotumumab/veligrotug label scope 및 JHA-73 IBI311 status 대조 | PASS, 지역 access unresolved 유지 | 2026-09-30 |
| 가운뎃점 미사용 | 하 | 문자 검색 | PASS | 2026-09-30 |
