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
---

# GD/TED address 가능 환자군 교차분석

> **분석 기준일:** pipeline/SoC frozen data cut 2026-09-10. JHA-73의 별도 live cross-confirm은 2026-09-29 기준이다. 이 문서는 JHA-70/71/72/73 결과와 legacy Section C6를 교차한 환자군 gap map이며, 치료 권고나 시장 규모 산출물이 아니다.

## 1. 결론

여기서 **현재 class 조합**은 JHA-72의 8개 행을 단순히 모두 병용한다는 뜻이 아니다. **SoC 4개 class(ATD, RAI, thyroidectomy, IVMP)와 JHA-73에서 확인한 active/approved pipeline class를 환자 여정에서 순차 또는 대안으로 사용할 수 있는 전체 선택지 집합**을 뜻한다. JHA-72의 `TSAb-IgG sweeping(eTPD)`은 임상 자산이 없는 concept이므로 현재 coverage에는 포함하지 않았고, JHA-73의 P1/preclinical 자산도 실제 환자 coverage로 계수하지 않았다.[12,13,14,15]

이 선택지 집합이 가장 잘 address하는 영역은 GD의 **thyroid hormone source control**과 TED의 **active inflammation/proptosis**다. 반대로 아래 환자군은 하나의 승인 또는 후기개발 class가 질환 상태, phenotype, 내약성, durability를 동시에 해결하지 못한다.

1. **ATD 장기불응/불내성 또는 중단 후 재발 GD 중 RAI/수술을 원치 않거나 부적합한 환자**
2. **Chronic/inactive TED의 고정 diplopia/proptosis/eyelid deficit 중 수술을 원치 않거나 부적합한 환자**
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
| Chronic/inactive TED, 고정 구조 이상 | Staged decompression/strabismus/eyelid surgery | IBI311 approved(중국) 및 inactive 시험; MHB018A P3의 chronic/inactive 연구 | 비수술 systemic option의 지역별 승인/근거가 제한되고 수술 부적합/거부 환자의 durable option 부족 | **우선 잔여군** |
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

- 현재 표준 경로는 안정된 inactive/euthyroid 상태에서 decompression, strabismus surgery, eyelid correction 순의 staged rehabilitation이다.
- IVMP는 inactive fibrotic deficit을 일관되게 해결하지 못하고 반복 독성이 있다. IGF-1R class는 inactive/chronic 연구가 확대 중이지만 지역별 authorization와 장기 수술 회피 효과가 균일하게 확립된 것으로 볼 수 없다.
- JHA-73은 IBI311의 active/inactive 시험과 MHB018A의 chronic/inactive P3을 포착한다. 이는 gap에 직접 대응하는 개발 신호이나, `class 전체가 inactive TED를 포괄`한다는 뜻은 아니다.

**잔여 정의:** 수술을 원치 않거나 마취/수술 위험, 활동성 불안정, 전문 surgeon 접근 제한이 있으면서 durable systemic/비침습 교정 옵션이 필요한 환자.

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

## 7. Legacy Section C6 통합본

Legacy report는 동결하고, C6의 다섯 항목을 아래와 같이 현재 결과에 통합한다.

| Legacy C6 항목 | JHA-70/71/72/73 교차 후 통합 판정 | 후속 데이터 요구 |
|---|---|---|
| Teprotumumab 이후 비용/청각 AE/durability | IGF-1R class는 active TED의 중요한 축이나 hearing impairment, hyperglycemia 등 safety와 nonresponse/relapse 후 경로가 남음. 다른 IGF-1R 후기 자산의 존재만으로 class gap 해소 판정 불가 | 독립 장기 추적, standardized relapse, retreatment, class-switch, 지역 access |
| Inactive TED systemic option 부족 | 수술 재활이 SoC. Inactive/chronic 개발은 존재하나 지역별 승인/장기 수술 회피 근거가 제한적 | Activity별 trial, functional outcome, 수술 회피, 장기 durability |
| TRAb 음성 TED | 9.4% assay discordance는 진단 gap을 지지하나 seronegative prevalence 5-10%는 미확인 상태 유지 | 복수 assay와 imaging을 쓴 prospective prevalence, target-positive tissue/response 분석 |
| GD 재발/장기관리/임신 | RAI/수술/장기 low-dose ATD 경로는 있으나 비침습적 durable disease modification과 special-population evidence 부족 | Off-treatment remission, TSAb/TRAb-stratified response, pregnancy/pediatric safety |
| TED 진행 및 active-inactive 전환 예측 | 치료 전 activity/phenotype 분류는 가능하지만 진행/재활성화/섬유화 전환을 예측하는 검증 biomarker 부족 | Longitudinal biomarker-imaging cohort, transition/relapse endpoint 표준화 |

## 8. 개발 및 연구 우선순위

1. **GD:** `ATD-free euthyroidism`뿐 아니라 치료 중단 후 durability, TRAb/TSAb rebound, TED outcome을 함께 측정
2. **Inactive TED:** 수술 회피, diplopia/function, proptosis, QoL 및 장기 재활성화를 별도 endpoint로 측정
3. **TRAb 음성 TED:** assay panel, imaging, phenotype 및 치료반응을 묶은 prospective subgroup 정의
4. **Failure-state trial:** Primary nonresponse, partial response, taper flare, post-treatment relapse, inactive residual deficit을 분리
5. **교차 적응증:** GD biochemical control과 TED activity/structure를 동시에 추적하며 한쪽 개선을 다른 쪽 cure로 표현하지 않음
6. **Special population:** Pregnancy/lactation, pediatric, diabetes, IBD, hearing impairment, infection risk별 안전성/대체기전 자료 확보

## 9. 해석 한계와 QA 상태

- 본 분석은 class의 기전상 가능성과 임상적으로 입증된 coverage를 구분한다. Preclinical/P1 자산은 환자군 coverage로 계수하지 않았다.
- 지역별 authorization/reimbursement가 `unresolved`인 경우 비승인/비급여로 단정하지 않았다.
- `soc_outcomes_v2.csv`의 special-population 행은 guideline 기반 경로 확인에 사용했으며 환자 비중 산출에는 사용하지 않았다.
- 상 tier인 역학 원 수치는 baseline 문서 값을 재사용했다. 신규 DOI 3건의 metadata는 Crossref로 대조했지만 역학 원 수치의 독립 cross-model QA와 원문 direct-quote 대조는 수행하지 않았으므로 그 절차가 끝날 때까지 `draft`를 유지한다.
- 가설 단계의 TSAb-IgG sweeping을 MER511/LCA-0321/BHV-1300 또는 다른 임상 class의 실증으로 간주하지 않았다.

## 10. 참고문헌

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

## 11. 검증 로그

| 점검 항목 | Tier | 방법 | 결과 | 일자 |
|---|---|---|---|---|
| JHA-70/71/72/73 반영 | 하 | 네 산출물의 line, class 한계, indication-specific phase를 수동 교차 | PASS | 2026-09-30 |
| Legacy C6 통합 | 하 | C6 다섯 bullet을 7절에서 1:1 대조 | PASS | 2026-09-30 |
| 5개국/지역 pool 산술 | 상 | baseline 1.2/2.2 표의 표시값 단순 합산 | PASS, 독립 QA/direct quote 대조 대기 | 2026-09-30 |
| 잔여군 정량 과장 방지 | 하 | TRAb 음성/ATD relapse/중복 subgroup의 전 population 외삽 금지 확인 | PASS | 2026-09-30 |
| 신규 참고문헌 DOI metadata | 상/중 | Crossref API에서 DOI 3건 title/author/year 대조 | PASS | 2026-09-30 |
| 가운뎃점 미사용 | 하 | 문자 검색 | PASS | 2026-09-30 |
