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
---

# GD/TED address 가능 환자군 교차분석

> **분석 기준일:** pipeline/SoC frozen data cut 2026-09-10. JHA-73의 별도 live cross-confirm은 2026-09-29 기준이다. 이 문서는 JHA-70/71/72/73 결과와 legacy Section C6를 교차한 환자군 gap map이며, 치료 권고나 시장 규모 산출물이 아니다.

## 1. 결론

현재 class 조합이 가장 잘 address하는 영역은 GD의 **thyroid hormone source control**과 TED의 **active inflammation/proptosis**다. 반대로 아래 환자군은 하나의 승인 또는 후기개발 class가 질환 상태, phenotype, 내약성, durability를 동시에 해결하지 못한다.

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

아래 합계는 baseline report 1.2/2.2장의 2024 인구 기반 값을 단순 합산한 **질환 전체 pool**이다. 환자 중복, 진단률, 치료 적격성 또는 잔여군 비율을 반영하지 않는다.

| 질환 | 미국 + EU5 + 한국 + 일본 + 중국 합계 | 계산 | 사용 가능 범위 |
|---|---:|---|---|
| GD 유병 | 약 **1,152만 명** | 170 + 164 + 10 + 62 + 746만 | 상단 disease pool context만 가능 |
| GD 연간 신규 | 약 **60.6만 명/년** | 9.1 + 8.8 + 1.7 + 3.3 + 37.7만 | incidence context만 가능 |
| TED 유병, 인구기반 저/고 시나리오 | 약 **55.6만-146.5만 명** | 국가별 24.65/10만 및 65/10만 시나리오 합계 | TED 전체 시나리오, 잔여군 규모 아님 |
| TED 연간 신규, 저/고 시나리오 | 약 **11.2만-25.1만 명/년** | baseline 표의 반올림 수치 합계 | TED 전체 시나리오, 잔여군 규모 아님 |
| TED, GD 동반률 연동 추정 | 약 **467.5만 명** | 지역별 GD pool x 메타분석 동반률의 baseline 합계 | 경증/일과성 포함, 인구기반 pool과 합산 금지 |

> **근거등급 주의:** 위 환자 pool은 문헌 rate x 2024 인구의 추정치로, 본 이슈에서 **D 성격의 planning estimate**로 취급한다. 특히 TED의 인구기반 시나리오와 GD 연동 추정은 case definition과 포착 방식이 달라 서로 더하거나 평균내지 않는다.

### 5.2 산출 가능한 제한적 예시와 산출 금지 항목

- 일본 자료는 TED 유병 2.5만-3.9만 명, 비활성 약 74%를 함께 보고한다. 같은 연구 맥락의 단순 곱은 약 **1.85만-2.89만 명**의 inactive TED를 시사하지만, severity, residual deficit, 치료 의향, 수술 적합성을 반영하지 않은 탐색적 상한 context다. 이를 일본의 addressable market으로 사용하지 않는다.
- ATD conventional-duration RCT relapse 56%를 전체 GD pool에 적용하지 않는다. 치료기간, 중단 eligibility, 추적, 지역 practice가 다르다.
- TRAb-seronegative TED의 검증된 분모/rate가 없으므로 환자 수를 제시하지 않는다.
- Steroid/IGF-1R nonresponder, 수술 부적합, special population은 서로 중복 가능하므로 합산하지 않는다.

## 6. Legacy Section C6 통합본

Legacy report는 동결하고, C6의 다섯 항목을 아래와 같이 현재 결과에 통합한다.

| Legacy C6 항목 | JHA-70/71/72/73 교차 후 통합 판정 | 후속 데이터 요구 |
|---|---|---|
| Teprotumumab 이후 비용/청각 AE/durability | IGF-1R class는 active TED의 중요한 축이나 hearing impairment, hyperglycemia 등 safety와 nonresponse/relapse 후 경로가 남음. 다른 IGF-1R 후기 자산의 존재만으로 class gap 해소 판정 불가 | 독립 장기 추적, standardized relapse, retreatment, class-switch, 지역 access |
| Inactive TED systemic option 부족 | 수술 재활이 SoC. Inactive/chronic 개발은 존재하나 지역별 승인/장기 수술 회피 근거가 제한적 | Activity별 trial, functional outcome, 수술 회피, 장기 durability |
| TRAb 음성 TED | 9.4% assay discordance는 진단 gap을 지지하나 seronegative prevalence 5-10%는 미확인 상태 유지 | 복수 assay와 imaging을 쓴 prospective prevalence, target-positive tissue/response 분석 |
| GD 재발/장기관리/임신 | RAI/수술/장기 low-dose ATD 경로는 있으나 비침습적 durable disease modification과 special-population evidence 부족 | Off-treatment remission, TSAb/TRAb-stratified response, pregnancy/pediatric safety |
| TED 진행 및 active-inactive 전환 예측 | 치료 전 activity/phenotype 분류는 가능하지만 진행/재활성화/섬유화 전환을 예측하는 검증 biomarker 부족 | Longitudinal biomarker-imaging cohort, transition/relapse endpoint 표준화 |

## 7. 개발 및 연구 우선순위

1. **GD:** `ATD-free euthyroidism`뿐 아니라 치료 중단 후 durability, TRAb/TSAb rebound, TED outcome을 함께 측정
2. **Inactive TED:** 수술 회피, diplopia/function, proptosis, QoL 및 장기 재활성화를 별도 endpoint로 측정
3. **TRAb 음성 TED:** assay panel, imaging, phenotype 및 치료반응을 묶은 prospective subgroup 정의
4. **Failure-state trial:** Primary nonresponse, partial response, taper flare, post-treatment relapse, inactive residual deficit을 분리
5. **교차 적응증:** GD biochemical control과 TED activity/structure를 동시에 추적하며 한쪽 개선을 다른 쪽 cure로 표현하지 않음
6. **Special population:** Pregnancy/lactation, pediatric, diabetes, IBD, hearing impairment, infection risk별 안전성/대체기전 자료 확보

## 8. 해석 한계와 QA 상태

- 본 분석은 class의 기전상 가능성과 임상적으로 입증된 coverage를 구분한다. Preclinical/P1 자산은 환자군 coverage로 계수하지 않았다.
- 지역별 authorization/reimbursement가 `unresolved`인 경우 비승인/비급여로 단정하지 않았다.
- `soc_outcomes_v2.csv`의 special-population 행은 guideline 기반 경로 확인에 사용했으며 환자 비중 산출에는 사용하지 않았다.
- 상 tier인 역학 원 수치는 baseline 문서 값을 재사용했다. 본 작성 세션에서 새로운 외부 검증을 수행하지 않았으므로 독립 cross-model QA와 원문 direct-quote 대조 전까지 `draft`를 유지한다.
- 가설 단계의 TSAb-IgG sweeping을 MER511/LCA-0321/BHV-1300 또는 다른 임상 class의 실증으로 간주하지 않았다.

### 검증 로그

| 점검 항목 | Tier | 방법 | 결과 | 일자 |
|---|---|---|---|---|
| JHA-70/71/72/73 반영 | 하 | 네 산출물의 line, class 한계, indication-specific phase를 수동 교차 | PASS | 2026-09-30 |
| Legacy C6 통합 | 하 | C6 다섯 bullet을 6절에서 1:1 대조 | PASS | 2026-09-30 |
| 5개국/지역 pool 산술 | 상 | baseline 1.2/2.2 표의 표시값 단순 합산 | PASS, 독립 QA/direct quote 대조 대기 | 2026-09-30 |
| 잔여군 정량 과장 방지 | 하 | TRAb 음성/ATD relapse/중복 subgroup의 전 population 외삽 금지 확인 | PASS | 2026-09-30 |
| 가운뎃점 미사용 | 하 | 문자 검색 | PASS | 2026-09-30 |
