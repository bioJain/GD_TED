# Graves’ disease 및 thyroid eye disease 치료·R&D landscape v2

**Data cut:** 2026-09-10 (frozen; later registry/regulatory changes excluded). <!-- claim:DOC-CONTROL-001 -->
**범위:** United States, EU/EEA, United Kingdom, South Korea, Japan을 포함하며 adults가 primary이고 pediatrics, pregnancy/lactation, older adults, relapsed/refractory populations는 분리한다. <!-- claim:DOC-CONTROL-002 -->
**분석 원칙:** Quantitative meta-analysis, naïve pooling, cross-trial efficacy ranking을 수행하지 않으며 R&D potential과 evidence confidence를 분리한다. <!-- claim:DOC-CONTROL-003 -->
**QA 방식:** Claim QA는 동일 coordinator의 stance-hidden second pass이며 independent third-party validation이 아니다. <!-- claim:QA-METHOD-001 -->

## Executive summary

- Frozen ClinicalTrials.gov query는 324개 record를 포함했다. <!-- claim:METHOD-001 -->
- 최종 clinical trial inventory에는 168개 unique trial이 포함되었다. <!-- claim:METHOD-003 -->
- 포함 trial 중 25개에 data cut 시점 posted results가 있었다. <!-- claim:METHOD-004 -->
- United States Lumvoa authorization: approved by FDA on 2026-06-26; BLA 761530; TED regardless of activity or duration [373, 726] <!-- claim:REG-US-LUMVOA-AUTH -->
- CTIS 2025-524053-14-00/LCA-0321-01은 Phase 1 first-in-human SAD/MAD이며 frozen cut에서 ongoing, recruiting이었다. [2] <!-- claim:DIRECT-LCA-PHASE-STATUS -->
- NEXUS NCT07305818은 18–55세 adult GD에서 IV/SC MER511 SAD/MAD를 평가하는 placebo-controlled Phase 1 first-in-human study이며 frozen cut에서 recruiting이었다. [7, 898] <!-- claim:DIRECT-MER-PHASE-STATUS -->
- Cure는 정상 thyroid function, pathogenic autoimmunity의 지속적 소실, 무치료 durability를 함께 요구하는 강한 표현이며 본 release의 investigational direct anti-TSHR 프로그램에는 적용하지 않는다. <!-- claim:ENDPOINT-007 -->

## 1. Methods 및 audit boundary

- 사전 정의된 scope로 193개 record를 audit triage했다. <!-- claim:METHOD-002 -->
- Baseline과 frozen cut 사이 tracked registry drift는 0건이었다. <!-- claim:METHOD-005 -->
- Randomized trials with posted participant flow: 17개; n_randomized는 first-period participant-flow STARTED 합계로 정의했다. <!-- claim:METHOD-015 -->
- Randomized trials without posted participant flow: 108개; Enrollment를 randomized N으로 대체하지 않고 NR로 유지했다. <!-- claim:METHOD-016 -->
- Nonrandomized or allocation-NA trials: 43개; n_randomized를 NA로 유지했다. <!-- claim:METHOD-017 -->
- 25개 result-bearing trial의 n_analyzed는 endpoint-specific이며 enrollment 또는 randomized flow N으로 대체하지 않았다. <!-- claim:METHOD-018 -->
- TERMINATED 11개, WITHDRAWN 5개, SUSPENDED 1개 trial과 target-unverified/registry-unspecified asset 4개를 inventory에 유지했다. <!-- claim:METHOD-019 -->
- Claim QA는 동일 coordinator의 stance-hidden second pass이며 independent third-party validation이 아니다. <!-- claim:QA-METHOD-001 -->

### 1.1 Included-trial status distribution

| Overall status | Trials | Claim |
|---|---:|---|
| COMPLETED | 66 | <!-- claim:METHOD-006 --> |
| RECRUITING | 39 | <!-- claim:METHOD-007 --> |
| UNKNOWN | 22 | <!-- claim:METHOD-008 --> |
| NOT_YET_RECRUITING | 14 | <!-- claim:METHOD-009 --> |
| TERMINATED | 11 | <!-- claim:METHOD-010 --> |
| ACTIVE_NOT_RECRUITING | 8 | <!-- claim:METHOD-011 --> |
| WITHDRAWN | 5 | <!-- claim:METHOD-012 --> |
| ENROLLING_BY_INVITATION | 2 | <!-- claim:METHOD-013 --> |
| SUSPENDED | 1 | <!-- claim:METHOD-014 --> |

## 2. Disease and endpoint framework

- Biochemical control은 치료 중 FT4/FT3가 정상화된 상태이며 off-treatment remission과 동일하지 않다. <!-- claim:ENDPOINT-001 -->
- ATD-sparing response는 ATD 증량 없이 normalization 또는 ATD dose 감소를 뜻하며 durable remission을 자동 의미하지 않는다. <!-- claim:ENDPOINT-002 -->
- Off-ATD normalization은 특정 시점에 ATD 없이 FT3/FT4가 정상인 상태이며, 충분한 추적이 없으면 durable remission으로 부르지 않는다. <!-- claim:ENDPOINT-003 -->
- Durable off-treatment remission은 사전 정의된 추적 기간 동안 치료 없이 euthyroidism이 지속되고 relapse가 없는 상태다. <!-- claim:ENDPOINT-004 -->
- Relapse는 ATD 중단 후 재발을 뜻하며 RAI 후 persistent hyperthyroidism과 별도 failure state로 기록한다. <!-- claim:ENDPOINT-005 -->
- RAI 또는 thyroidectomy에 의한 thyroid-source control은 pathogenic autoimmunity나 TED의 소실을 의미하지 않는다. <!-- claim:ENDPOINT-006 -->
- Cure는 정상 thyroid function, pathogenic autoimmunity의 지속적 소실, 무치료 durability를 함께 요구하는 강한 표현이며 본 release의 investigational direct anti-TSHR 프로그램에는 적용하지 않는다. <!-- claim:ENDPOINT-007 -->
- TED의 PRR, CAS, diplopia, GO-QOL, overall response 및 imaging endpoint는 GD biochemical remission과 교환 가능하지 않다. <!-- claim:ENDPOINT-008 -->

## 3. Regional standard of care

- Regional SoC matrix는 5개 region 각각에 15개 category를 유지해 총 75개 row를 포함한다. <!-- claim:SOC-FRAME-001 -->
- GD의 Adult ATD, Adult RAI, Adult thyroidectomy는 각 region에서 별도 pathway로 유지되며 biochemical control, destructive/surgical control, remission을 합치지 않는다. <!-- claim:SOC-FRAME-002 -->
- Pediatrics, pregnancy, lactation, older adults, relapsed/refractory GD 및 relapsed/refractory TED는 adult primary pathway와 분리했다. <!-- claim:SOC-FRAME-003 -->

### 3.1 Authorization과 access를 분리한 regional status

unresolved는 documented official-source pass에서 positive official evidence를 확정하지 못했다는 뜻이며 ‘not authorized’ 또는 ‘not reimbursed’를 의미하지 않는다. <!-- claim:SOC-FRAME-004 -->

| Region | Tepezza authorization | Tepezza reimbursement/access | Lumvoa authorization | Lumvoa reimbursement/access |
|---|---|---|---|---|
| United States | approved in the United States; labeled for TED regardless of activity or duration [728] <!-- claim:REG-US-TEPEZZA-AUTH --> | unresolved (본 curated source set에서 region-wide reimbursement/coverage를 공식 근거로 확정하지 않음; 개별 payer·기관 확인 필요)  <!-- claim:REG-US-TEPEZZA-ACCESS --> | approved by FDA on 2026-06-26; BLA 761530; TED regardless of activity or duration [373, 726] <!-- claim:REG-US-LUMVOA-AUTH --> | unresolved (본 curated source set에서 region-wide reimbursement/coverage를 공식 근거로 확정하지 않음; 개별 payer·기관 확인 필요)  <!-- claim:REG-US-LUMVOA-ACCESS --> |
| EU/EEA | EU marketing authorization valid throughout the EU from 2025-06-19 for adults with moderate-to-severe TED [729] <!-- claim:REG-EU-TEPEZZA-AUTH --> | Member-State-specific; EU-wide reimbursement claim을 하지 않으며 status는 국가별 unresolved [751] <!-- claim:REG-EU-TEPEZZA-ACCESS --> | unresolved (no relevant official EMA product record identified in the documented search; this does not prove non-authorization) [747] <!-- claim:REG-EU-LUMVOA-AUTH --> | unresolved  <!-- claim:REG-EU-LUMVOA-ACCESS --> |
| United Kingdom | MHRA approved on 2025-05-07 for adults with moderate-to-severe TED [731] <!-- claim:REG-UK-TEPEZZA-AUTH --> | unresolved for NHS access; NICE appraisal status in progress at the cutoff [732, 733] <!-- claim:REG-UK-TEPEZZA-ACCESS --> | unresolved (no relevant official UK product or appraisal record identified; this does not prove non-authorization) [749] <!-- claim:REG-UK-LUMVOA-AUTH --> | unresolved [749] <!-- claim:REG-UK-LUMVOA-ACCESS --> |
| South Korea | unresolved (no relevant official MFDS/NEDrug product record identified; this does not prove non-authorization) [745] <!-- claim:REG-KR-TEPEZZA-AUTH --> | unresolved (no relevant official HIRA reimbursement record identified; this does not prove non-reimbursement) [746] <!-- claim:REG-KR-TEPEZZA-ACCESS --> | unresolved (no relevant official Korean product record identified; this does not prove non-authorization) [750] <!-- claim:REG-KR-LUMVOA-AUTH --> | unresolved (no relevant official Korean reimbursement record identified; this does not prove non-reimbursement) [750] <!-- claim:REG-KR-LUMVOA-ACCESS --> |
| Japan | approved in Japan on 2024-09-24 for active thyroid eye disease [735, 736] <!-- claim:REG-JP-TEPEZZA-AUTH --> | unresolved (official reimbursement/price-list locator not verified in this pass) [752] <!-- claim:REG-JP-TEPEZZA-ACCESS --> | unresolved (no relevant official PMDA/MHLW product record identified; this does not prove non-authorization) [748] <!-- claim:REG-JP-LUMVOA-AUTH --> | unresolved  <!-- claim:REG-JP-LUMVOA-ACCESS --> |

### 3.2 반드시 유지할 source conflicts와 special-population timing

- Korean RAI Recommendation 5.3은 narrative의 ‘may be considered’와 Table 3의 ‘Steroid prophylaxis recommended’를 모두 보존하며, strength discrepancy를 conclusion-neutral Severity 3로 공개한다. [28] <!-- claim:SOC-CONFLICT-KR-RAI -->
- NICE appraisal는 expected publication date TBC, status In progress이며, 2026-09 consultation 및 2027-01 committee 일정은 provisional이고 draft는 final guidance가 아니다. [732, 733] <!-- claim:SOC-CONFLICT-NICE -->
- Japan FCQ1의 MMI avoidance interval은 임신 5w0d–9w6d이다. [741, 743] <!-- claim:SOC-CONFLICT-JP-FCQ1 -->
- Japan BCQ2의 broader first-choice exception은 임신 4w0d–15w6d이며 FCQ1 avoidance interval과 병합하지 않는다. [741] <!-- claim:SOC-CONFLICT-JP-BCQ2 -->

## 4. Clinical-trial landscape와 result interpretability

Result-bearing 25개 trial을 positive/negative 이분법으로 축약하지 않고 disposition, efficacy, safety, durability와 caveat를 분리했다. <!-- claim:TRIAL-FRAME-001 -->

### 4.1 Complete result-bearing interpretation inventory

| Trial | Disposition | Bounded interpretation | Evidence |
|---|---|---|---|
| NCT00595335 | negative_randomized | 6개월 CAS 변화와 failure rate에서 rituximab이 methylprednisolone 대비 우월하지 않았다. | [762] <!-- claim:TRIAL-001-INTERPRETATION --> |
| NCT01114503 | terminated_uninterpretable | n=2로 효능 해석이 불가능하며 dose 이해를 기다리며 종료되었다. | [767] <!-- claim:TRIAL-002-INTERPRETATION --> |
| NCT01269749 | no_posted_efficacy | pediatric RAI/ATD 연구지만 posted outcome-measurement row가 없어 efficacy 또는 remission을 추론할 수 없다. | [769] <!-- claim:TRIAL-003-INTERPRETATION --> |
| NCT01868997 | positive_randomized | active TED에서 teprotumumab은 Week 24 composite response와 proptosis를 유의하게 개선했다. | [780] <!-- claim:TRIAL-004-INTERPRETATION --> |
| NCT01950260 | negative_primary | RAI 후 조기 levothyroxine은 8주 overt hypothyroidism primary endpoint를 유의하게 줄이지 못했다. | [782] <!-- claim:TRIAL-005-INTERPRETATION --> |
| NCT02378298 | nonrandomized_descriptive | 선택된 rescue cohorts에서 rituximab/MTX 후 CAS 감소가 관찰됐지만 causal 비교는 불가하다. | [791] <!-- claim:TRIAL-006-INTERPRETATION --> |
| NCT02713256 | single_arm_weak | iscalimab 단일군에서 Week 12 TSH normalization은 0%였다. | [796] <!-- claim:TRIAL-007-INTERPRETATION --> |
| NCT02845336 | terminated_infeasible | poor enrollment로 종료되어 feasibility 실패이며 efficacy 판단 근거가 아니다. | [798] <!-- claim:TRIAL-008-INTERPRETATION --> |
| NCT02973802 | exploratory_single_arm | ATX-GD-59 Phase 1에서 thyroid/antibody biomarker 개선 신호가 있었지만 remission proof는 아니다. | [800] <!-- claim:TRIAL-009-INTERPRETATION --> |
| NCT02993302 | negative_biomarker | PTU+alfacalcidol은 prespecified immune biomarkers를 개선하지 못했다. | [801] <!-- claim:TRIAL-010-INTERPRETATION --> |
| NCT03298867 | positive_randomized | OPTIC에서 teprotumumab은 Week 24 proptosis response를 크게 높였다. | [807] <!-- claim:TRIAL-011-INTERPRETATION --> |
| NCT03461211 | open_label_extension | OPTIC-X는 prior-placebo crossover와 selected retreatment/nonresponder cohorts에서 추가 response를 보였다. | [809] <!-- claim:TRIAL-012-INTERPRETATION --> |
| NCT03922321 | single_arm_pd | RVT-1401 pilot은 strong IgG PD를 보였으나 clinical efficacy inference는 약하다. | [812] <!-- claim:TRIAL-013-INTERPRETATION --> |
| NCT03938545 | negative_primary_pd_positive | ASCEND GO-2의 Week 13 clinical primary comparisons는 nonsignificant였지만 IgG/anti-TSHR PD는 dose-related였다. | [813] <!-- claim:TRIAL-014-INTERPRETATION --> |
| NCT04583735 | positive_randomized | chronic/low-activity TED에서도 teprotumumab은 Week 24 proptosis를 유의하게 개선했다. | [817] <!-- claim:TRIAL-015-INTERPRETATION --> |
| NCT04737330 | negative_futility | secukinumab은 futility로 종료되었고 Week 16 response가 관찰되지 않았다. | [819] <!-- claim:TRIAL-016-INTERPRETATION --> |
| NCT05176639 | positive_randomized | THRIVE에서 veligrotug은 Week 15에 큰 proptosis/overall response 효과를 보였다. | [829] <!-- claim:TRIAL-017-INTERPRETATION --> |
| NCT05276063 | positive_high_dose | linsitinib high dose는 Week 24 PRR와 overall response를 유의하게 개선했으나 low dose primary comparison은 유의하지 않았다. | [831] <!-- claim:TRIAL-018-INTERPRETATION --> |
| NCT05907668 | single_arm_biochemical | batoclimab+background ATD에서 biochemical control 및 ATD reduction 신호가 있었지만 remission/cure 증거는 아니다. | [843] <!-- claim:TRIAL-019-INTERPRETATION --> |
| NCT05987423 | negative_primary_secondary_signals | SatraGO-1 active-TED Week 24 primary PRR는 실패했다. | [844] <!-- claim:TRIAL-020-INTERPRETATION --> |
| NCT06021054 | positive_randomized | THRIVE-2에서 chronic TED Week 15 PRR가 크게 개선되었다. | [845] <!-- claim:TRIAL-021-INTERPRETATION --> |
| NCT06106828 | positive_randomized | SatraGO-2는 active-TED Week 24 primary PRR를 충족했다. | [849] <!-- claim:TRIAL-022-INTERPRETATION --> |
| NCT06179875 | selected_open_label | feeder-trial nonresponders의 open-label treatment 결과이며 randomized comparative efficacy로 해석할 수 없다. | [852] <!-- claim:TRIAL-023-INTERPRETATION --> |
| NCT06226545 | mixed_small_randomized | LASN01은 Week 37 CAS response 신호를 보였지만 PRR는 placebo와 유사했다. | [853] <!-- claim:TRIAL-024-INTERPRETATION --> |
| NCT06384547 | active_dose_uncontrolled | STRIVE는 placebo 없는 active-dose safety comparison으로 efficacy 또는 dose response를 확립하지 못한다. | [859] <!-- claim:TRIAL-025-INTERPRETATION --> |

### 4.2 Selected efficacy, null, and stopped results

Displayed trial values는 각 trial 내부 comparator와 endpoint에만 적용하며 trial 간 수치 ranking 또는 pooling을 하지 않는다. <!-- claim:TRIAL-FRAME-002 -->

| Trial | Result | Evidence |
|---|---|---|
| NCT00595335 | CAS change −1.2 (n=13) vs −1.5 (n=12), p=0.73; failure 69% vs 75%, p=0.75. | [762] <!-- claim:TRIAL-001-EFFICACY --> |
| NCT01868997 | Composite response 29/42 vs 9/45, p<0.001; OR 8.86 (95% CI 3.293–23.825); proptosis LS change −2.46 vs −0.15 mm. | [780] <!-- claim:TRIAL-004-EFFICACY --> |
| NCT02713256 | 13 evaluable: TSH normalization 0%; total T3 below ULN 38.5%; FT4 below ULN 30.8%. | [796] <!-- claim:TRIAL-007-EFFICACY --> |
| NCT02973802 | Week 22: TBII −0.6602 IU/L; TSAb −54 %SRR; FT3 −14.19%; FT4 −14.54%; TSH +0.309 mIU/L. | [800] <!-- claim:TRIAL-009-EFFICACY --> |
| NCT03298867 | PRR 82.9% vs 9.5%, p<0.001; RD 73.45 points; overall response 78.0% vs 7.1%; CAS 0/1 58.5% vs 21.4%. | [807] <!-- claim:TRIAL-011-EFFICACY --> |
| NCT03938545 | PRR: 680 mg 30.0% (p=0.1993), 340 mg 30.8% (p=0.1016), 255 mg 0% (p=0.2963), placebo 8.3%. | [813] <!-- claim:TRIAL-014-EFFICACY --> |
| NCT04583735 | LS change −2.41 vs −0.92 mm; difference −1.48 (95% CI −2.28 to −0.69), p=0.0004. | [817] <!-- claim:TRIAL-015-EFFICACY --> |
| NCT04737330 | Overall response 0/14 vs 0/14; CAS response 0/14 vs 3/14; PRR 0/14 vs 0/14. | [819] <!-- claim:TRIAL-016-EFFICACY --> |
| NCT05176639 | PRR 70.0% vs 5.26%, p<0.0001; proptosis LS change −2.90 vs −0.48 mm; overall response 66.83% vs 5.26%; diplopia response 59.07% vs 19.89%. | [829] <!-- claim:TRIAL-017-EFFICACY --> |
| NCT05276063 | PRR 150 mg BID 51.7% vs 18.8%, p=0.01, RD 0.345 (95% CI 0.098–0.593); 75 mg 38.9%, p=0.090; GO-QOL difference +10.776, p=0.002. | [831] <!-- claim:TRIAL-018-EFFICACY --> |
| NCT05907668 | Week 24 biochemical response without ATD increase 68.8% (95% CI 50.0–83.9); normalized FT3/FT4 with ATD ≤50% baseline 53.1%; off ATD with normalized FT3/FT4 31.3% (95% CI 16.1–50.0). | [843] <!-- claim:TRIAL-019-EFFICACY --> |
| NCT05987423 | Active PRR 49.0% vs 31.2%, p=0.0715; RD 17.9 points (95.03% CI −1.6 to 37.3). Some secondary activity endpoints nominally positive. | [844] <!-- claim:TRIAL-020-EFFICACY --> |
| NCT06021054 | PRR 57.28% vs 8.22%, p<0.0001; RD 49.06 points (95% CI 37.71–60.40); proptosis LS change −2.35 vs −0.46 mm; diplopia response 55.57% vs 24.70%. | [845] <!-- claim:TRIAL-021-EFFICACY --> |
| NCT06106828 | Active PRR 52.9% vs 23.4%, p=0.0011; RD 28.9 points (95.03% CI 11.5–46.2); adjusted proptosis difference −1.02 mm, p=0.0027. | [849] <!-- claim:TRIAL-022-EFFICACY --> |
| NCT06226545 | CAS response 15/17 (88.2%) vs 4/9 (44.4%), p=0.028; PRR 6/17 (35.3%) vs 3/9 (33.3%). | [853] <!-- claim:TRIAL-024-EFFICACY --> |

### 4.3 Selected safety observations

| Trial | Safety observation | Evidence |
|---|---|---|
| NCT04583735 | SAE 1/41 vs 1/20; hyperglycemia 6/41 vs 2/20; hearing impairment 9/41 vs 2/20; muscle spasms 17/41 vs 2/20. | [817] <!-- claim:TRIAL-015-SAFETY --> |
| NCT05176639 | SAE 7/75 vs 0/38; muscle spasms 34/75 vs 3/38; infusion reaction 13/75 vs 2/38; hearing-related symptoms present. | [829] <!-- claim:TRIAL-017-SAFETY --> |
| NCT05276063 | SAE 2/29 high, 0/30 low, 1/31 placebo; high-dose GI/fatigue/transaminase signals. | [831] <!-- claim:TRIAL-018-SAFETY --> |
| NCT06021054 | Through Week 52: death 1/125 vs 0/63; SAE 10/125 vs 3/63; registry는 death cause/relatedness 미기재. | [845] <!-- claim:TRIAL-021-SAFETY --> |
| NCT06106828 | SAE 2/64 vs 3/62; ALT 6/64 vs 1/62, AST 4/64 vs 1/62, neutrophils decreased 4/64 vs 1/62. | [849] <!-- claim:TRIAL-022-SAFETY --> |
| NCT06384547 | Week 52 TEAE 159/173 vs 55/58; SAE 10/173 vs 3/58; deaths 0; class-like muscle spasm/hearing/reproductive events. | [859] <!-- claim:TRIAL-025-SAFETY --> |

### 4.4 Durability boundaries

| Trial | Durability statement | Evidence |
|---|---|---|
| NCT02973802 | Full paper에서 2명이 1년 off-ATD euthyroid였으나 uncontrolled spontaneous remission 대안이 큼. | [800] <!-- claim:TRIAL-009-DURABILITY --> |
| NCT03461211 | Crossover responders 중 Week 48 PRR maintenance 29/32. | [809] <!-- claim:TRIAL-012-DURABILITY --> |
| NCT05176639 | Week 52에서 initial responders의 70%가 PRR 유지; evaluable follow-up subset 21/30. | [829] <!-- claim:TRIAL-017-DURABILITY --> |
| NCT05907668 | Off-ATD normalization은 해당 시점의 상태이며 durable remission 추적 아님. | [843] <!-- claim:TRIAL-019-DURABILITY --> |
| NCT06021054 | Efficacy durability beyond Week 15 not posted. | [845] <!-- claim:TRIAL-021-DURABILITY --> |

## 5. Direct TSHR/anti-TSHR programs

### 5.1 LCA-0321

- LCA-0321은 anti-TSHR autoantibodies를 선택적으로 결합·제거하도록 설계된 LYTAC degrader이며, sponsor는 general immunosuppression 없이 driver 제거를 목표로 설명한다. [1] <!-- claim:DIRECT-LCA-MECHANISM -->
- CTIS 2025-524053-14-00/LCA-0321-01은 Phase 1 first-in-human SAD/MAD이며 frozen cut에서 ongoing, recruiting이었다. [2] <!-- claim:DIRECT-LCA-PHASE-STATUS -->
- LCA-0321 Phase 1의 planned enrollment는 48명이며 analyzed N으로 대체할 수 없다. [2] <!-- claim:DIRECT-LCA-PLANNED-N -->
- Frozen evidence package에는 LCA-0321의 human efficacy, immunogenicity, autoantibody rebound, normal TSH physiology preservation, TED–biochemical concordance 또는 off-treatment durability를 확립한 human result가 포함되지 않았다. [1, 2] <!-- claim:DIRECT-LCA-EVIDENCE-BOUNDARY -->

### 5.2 MER511

- MER511은 anti-TSHR autoantibodies를 neutralize/clear하고 antigen-specific B-cell function을 억제하도록 설계된 TSHR-IgG Fc fusion precision biologic이다. [6, 8] <!-- claim:DIRECT-MER-MECHANISM -->
- NEXUS NCT07305818은 18–55세 adult GD에서 IV/SC MER511 SAD/MAD를 평가하는 placebo-controlled Phase 1 first-in-human study이며 frozen cut에서 recruiting이었다. [7, 898] <!-- claim:DIRECT-MER-PHASE-STATUS -->
- MER511의 TSH non-binding, TSH-signaling preservation 및 total-IgG sparing은 sponsor/preclinical claim이며 사람에서 검증되지 않았다. [6, 8] <!-- claim:DIRECT-MER-TSH-SPARING -->
- NEXUS protocol objectives는 safety, tolerability, PK, PD, immunogenicity이며 frozen registry record에는 posted results가 없다; clinical efficacy와 durable remission은 미확정이다. [7, 898] <!-- claim:DIRECT-MER-EVIDENCE-BOUNDARY -->

### 5.3 Other direct approaches

| Asset | Target, stage, status, trial linkage | Evidence |
|---|---|---|
| GenSci098 / YB-101 | target=TSHR; highest_stage=Phase 2; status=Active development; trial_ids=NCT06569758; NCT07286656; NCT07682896. | [541, 870, 897, 915] <!-- claim:DIRECT-OTHER-01 --> |
| K1-70 | target=TSHR; highest_stage=Phase 1; status=Early clinical; trial_ids=NCT02904330; Japanese Phase 1 publication. | [164, 799] <!-- claim:DIRECT-OTHER-02 --> |
| ATX-GD-59 | target=TSHR-reactive T cells; highest_stage=Phase 1 completed; status=Completed; follow-on WP1302 suspended; trial_ids=NCT02973802; NCT06240455. | [253, 800, 854] <!-- claim:DIRECT-OTHER-03 --> |
| IBI3031 | target=IGF-1R and TSHR; highest_stage=Phase 1; status=Recruiting/early; trial_ids=NCT07622368. | [619, 913] <!-- claim:DIRECT-OTHER-04 --> |
| WP1302 | target=TSHR-reactive T cells; highest_stage=Highest registered phase: PHASE2; status=Registered statuses: SUSPENDED; trial_ids=NCT06240455. | [854] <!-- claim:DIRECT-OTHER-05 --> |

## 6. R&D potential과 evidence confidence

R&D potential은 driver proximity, potential durability, selectivity, translational/PD tractability, developability를 합성한 hypothesis-weighted 0–3 score이며 임상 성공 확률, 투자 등급 또는 cross-trial efficacy ranking이 아니다. <!-- claim:RND-FRAME-001 -->

| Asset | R&D potential (0–3) | Evidence confidence | Claim |
|---|---:|---|---|
| LCA-0321 | 2.35 | Low | <!-- claim:POTENTIAL-01 --> |
| MER511 | 2.75 | Low–moderate | <!-- claim:POTENTIAL-02 --> |
| GenSci098 / YB-101 | 2.05 | Moderate | <!-- claim:POTENTIAL-03 --> |
| K1-70 | 2.05 | Moderate | <!-- claim:POTENTIAL-04 --> |
| ATX-GD-59 | 2.5 | Low–moderate | <!-- claim:POTENTIAL-05 --> |
| IBI3031 | 1.6 | Low | <!-- claim:POTENTIAL-06 --> |

## 7. Complete asset inventory

- Asset tier 분포는 Core 5, Core-adjacent 1, Comparator 5, Adjacent 6, Watchlist 3, Completeness 28였다. <!-- claim:ASSET-SUMMARY-TIERS -->
- Publicly or registry-unverified target label을 가진 asset 4개도 inventory에 유지했다: KHN939, SCTT11, Technetium-99 methylene diphosphonate (99Tc-MDP), Unspecified immunosuppressive agent. <!-- claim:ASSET-SUMMARY-TARGET-UNKNOWN -->

Complete asset inventory의 각 row는 canonical table에서 직접 렌더링한다; stage/status는 data cut source state이고 tier/evidence confidence는 efficacy ranking이 아니다. <!-- claim:ASSET-RENDER-001 -->

| Asset | Indication | Target | Highest stage | Status | Tier | Evidence confidence | Evidence |
|---|---|---|---|---|---|---|---|
| Aflibercept | Active TED | VEGF-A/PlGF | Highest registered phase: PHASE2 | Registered statuses: COMPLETED | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [815] <!-- claim:ASSET-001 --> |
| Allogeneic CD19/BCMA CAR-T | GD / autoimmune hyperthyroidism | CD19/BCMA | Highest registered phase: EARLY_PHASE1 | Registered statuses: RECRUITING | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [884, 893] <!-- claim:ASSET-002 --> |
| AMG 732 | TED | IGF-1R | Phase 2 | Active | Comparator | Low | [862, 903] <!-- claim:ASSET-003 --> |
| ATX-GD-59 | GD | TSHR-reactive T cells | Phase 1 completed | Completed; follow-on WP1302 suspended | Core | Low–moderate | [253, 800, 854] <!-- claim:ASSET-004 --> |
| Batoclimab | GD; TED | FcRn | Phase 2 | Completed/earlier program interrupted | Adjacent | Moderate | [683, 812, 813, 824, 836, 837, 838, 843] <!-- claim:ASSET-005 --> |
| BHV-1300 | GD / autoimmune hyperthyroidism | IgG/extracellular degradation pathway | Highest registered phase: PHASE3 | Registered statuses: RECRUITING | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [879, 914] <!-- claim:ASSET-006 --> |
| Celecoxib | Active TED | COX-2 | Highest registered phase: PHASE2 | Registered statuses: TERMINATED | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [798] <!-- claim:ASSET-007 --> |
| Cizutamig (CND106) | Autoantibody-mediated disease; relevance to GD/TED | BCMA×CD3 | Phase 1 | Early clinical | Adjacent | Low | [564, 645, 909] <!-- claim:ASSET-008 --> |
| Efgartigimod PH20 SC | Active moderate-to-severe TED; GD / autoimmune hyperthyroidism | FcRn | Highest registered phase: PHASE3 | Registered statuses: TERMINATED; RECRUITING | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [857, 858, 906, 908] <!-- claim:ASSET-009 --> |
| Felzartamab | GD / autoimmune hyperthyroidism | CD38 | Highest registered phase: PHASE2 | Registered statuses: RECRUITING | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [918] <!-- claim:ASSET-010 --> |
| GenSci098 / YB-101 | GD | TSHR | Phase 2 | Active development | Core | Moderate | [541, 870, 897, 915] <!-- claim:ASSET-011 --> |
| HN2301 in-vivo CAR-T | GD / autoimmune hyperthyroidism | CD19/BCMA | Highest registered phase: EARLY_PHASE1 | Registered statuses: RECRUITING | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [900] <!-- claim:ASSET-012 --> |
| Hydroxychloroquine | Mild TED | Pleiotropic immune pathways | Highest registered phase: PHASE4 | Registered statuses: RECRUITING | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [828] <!-- claim:ASSET-013 --> |
| IBI3031 | TED | IGF-1R and TSHR | Phase 1 | Recruiting/early | Core-adjacent | Low | [619, 913] <!-- claim:ASSET-014 --> |
| IBI311 | Active TED; Active moderate-to-severe TED; Chronic/inactive TED; TED, active and chronic/inactive cohorts | IGF-1R | Highest registered phase: PHASE4 | Registered statuses: COMPLETED; RECRUITING | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [842, 851, 856, 866, 883, 886, 887, 888] <!-- claim:ASSET-015 --> |
| IMVT-1402 | GD / autoimmune hyperthyroidism | FcRn | Highest registered phase: PHASE2 | Registered statuses: RECRUITING; ENROLLING_BY_INVITATION | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [875, 882, 896] <!-- claim:ASSET-016 --> |
| Iscalimab (CFZ533) | GD / autoimmune hyperthyroidism | CD40 | Highest registered phase: PHASE2 | Registered statuses: COMPLETED | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [796] <!-- claim:ASSET-017 --> |
| K1-70 | GD; TED | TSHR | Phase 1 | Early clinical | Core | Moderate | [164, 799] <!-- claim:ASSET-018 --> |
| Kamuvudine-9 (K9) | TED | P2X7/NLRP3 axis | Phase 2 terminated | Terminated for low enrollment | Adjacent | Low | [864] <!-- claim:ASSET-019 --> |
| KHN939 | TED | Not publicly verified | Clinical | Registered | Watchlist | Very low | [916, 917] <!-- claim:ASSET-020 --> |
| Lanreotide | Active TED | Somatostatin receptors | Highest registered phase: PHASE2 | Registered statuses: TERMINATED | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [758] <!-- claim:ASSET-021 --> |
| LASN01 | TED | IL-11R | Phase 2 | Completed | Adjacent | Low–moderate | [422, 521, 832, 853] <!-- claim:ASSET-022 --> |
| LCA-0321 | GD; TED | anti-TSHR autoantibodies | Phase 1 | Ongoing, recruiting | Core | Low | [1, 2] <!-- claim:ASSET-023 --> |
| Linsitinib | TED | IGF-1R/insulin receptor kinase | Phase 3 | ORBIT recruiting | Comparator | Moderate | [714, 715, 831, 850, 919] <!-- claim:ASSET-024 --> |
| Lonigutamab | Active TED | IGF-1R | Highest registered phase: PHASE1; PHASE2 | Registered statuses: COMPLETED | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [840] <!-- claim:ASSET-025 --> |
| Lu AG22515 | TED | CD40L | Phase 1/2 | Clinical development | Adjacent | Low | [868] <!-- claim:ASSET-026 --> |
| MER511 | GD; potential TED | anti-TSHR autoantibodies and cognate B-cell sources | Phase 1 | Recruiting | Core | Low–moderate | [6, 7, 8, 898] <!-- claim:ASSET-027 --> |
| MHB018A | Active moderate-to-severe TED; Chronic/inactive TED; TED, active and chronic/inactive cohorts | IGF-1R | Highest registered phase: PHASE3 | Registered statuses: RECRUITING; NOT_YET_RECRUITING | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [459, 460, 461, 881, 892, 894, 910, 911, 912] <!-- claim:ASSET-028 --> |
| NTB003 / BCG009 | TED, active and chronic/inactive cohorts | IGF-1R | Highest registered phase: PHASE1; PHASE2 | Registered statuses: NOT_YET_RECRUITING | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [404, 495, 904] <!-- claim:ASSET-029 --> |
| Otelixizumab | Active TED | CD3 | Highest registered phase: PHASE2 | Registered statuses: TERMINATED | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [767] <!-- claim:ASSET-030 --> |
| Rabbit anti-thymocyte globulin | Active moderate-to-severe TED | T lymphocytes | Highest registered phase: NA | Registered statuses: UNKNOWN | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [830] <!-- claim:ASSET-031 --> |
| Rilzabrutinib | Active TED | BTK | Highest registered phase: PHASE2 | Registered statuses: RECRUITING | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [880] <!-- claim:ASSET-032 --> |
| Rituximab | Active TED; Active moderate-to-severe TED; GD / autoimmune hyperthyroidism | CD20 | Highest registered phase: PHASE4 | Registered statuses: COMPLETED | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [755, 760, 762, 791] <!-- claim:ASSET-033 --> |
| Satralizumab | TED | IL-6R | Regulatory review US | Pending at cutoff; not FDA-approved for TED | Adjacent | Moderate | [675, 699, 701, 844, 849] <!-- claim:ASSET-034 --> |
| SCTT11 | TED | Not publicly verified | Clinical | Registered | Watchlist | Very low | [876] <!-- claim:ASSET-035 --> |
| Secukinumab | Active moderate-to-severe TED | IL-17A | Highest registered phase: PHASE3 | Registered statuses: TERMINATED | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [819] <!-- claim:ASSET-036 --> |
| SHR-1314 | Active moderate-to-severe TED | IL-6 pathway | Highest registered phase: PHASE2 | Registered statuses: TERMINATED | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [833] <!-- claim:ASSET-037 --> |
| Sirolimus (rapamycin) | Active moderate-to-severe TED | mTOR | Highest registered phase: PHASE2 | Registered statuses: UNKNOWN; RECRUITING | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [818, 822, 839] <!-- claim:ASSET-038 --> |
| Technetium-99 methylene diphosphonate (99Tc-MDP) | Active moderate-to-severe TED | Not registry-specified | Highest registered phase: PHASE4 | Registered statuses: COMPLETED | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [814] <!-- claim:ASSET-039 --> |
| Teprotumumab | TED (US) | IGF-1R | Approved US | Approved | Comparator | High for TED | [190, 191, 274, 780, 807, 809, 817, 823, 855, 860, 869, 873, 885, 895, 899, 907] <!-- claim:ASSET-040 --> |
| Tocilizumab | Active TED; Active moderate-to-severe TED; Sight-threatening TED / dysthyroid optic neuropathy; TED, activity/severity not registry-specified | IL-6R | Highest registered phase: PHASE4 | Registered statuses: UNKNOWN; RECRUITING; COMPLETED; WITHDRAWN | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [772, 821, 847, 878] <!-- claim:ASSET-041 --> |
| Tofacitinib | Active moderate-to-severe TED | JAK family | Highest registered phase: PHASE2 | Registered statuses: RECRUITING | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [905] <!-- claim:ASSET-042 --> |
| TOUR006 | Active moderate-to-severe TED | IL-6 pathway | Highest registered phase: PHASE2 | Registered statuses: ACTIVE_NOT_RECRUITING | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [848] <!-- claim:ASSET-043 --> |
| Unspecified immunosuppressive agent | TED, activity/severity not registry-specified | Not registry-specified | Highest registered phase: NA | Registered statuses: UNKNOWN | Watchlist | Low (registry-level completeness row; not an efficacy judgment) | [826] <!-- claim:ASSET-044 --> |
| Veligrotug (Lumvoa) | TED regardless of activity or duration (US) | IGF-1R | Approved US | FDA approved 2026-06-26 | Comparator | High for TED | [230, 373, 726, 727, 829, 845, 852, 859] <!-- claim:ASSET-045 --> |
| VRDN-003 | Active moderate-to-severe TED; Chronic/inactive TED; TED, any CAS / mixed activity | IGF-1R | Highest registered phase: PHASE3 | Registered statuses: ACTIVE_NOT_RECRUITING; COMPLETED | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [871, 872, 877, 889, 891] <!-- claim:ASSET-046 --> |
| WP1302 | GD / autoimmune hyperthyroidism | TSHR-reactive T cells | Highest registered phase: PHASE2 | Registered statuses: SUSPENDED | Completeness | Low (registry-level completeness row; not an efficacy judgment) | [854] <!-- claim:ASSET-047 --> |
| ZB001 | TED | IGF-1R | Phase 1/2 | Clinical | Comparator | Low | [841] <!-- claim:ASSET-048 --> |

## 8. Special populations와 sequencing boundaries

- Pediatrics는 adult primary pathway와 분리하고 remission assumptions, RAI age/dose constraints 및 prolonged ATD strategy를 별도 기록한다. <!-- claim:POP-PEDIATRIC-001 -->
- Pregnancy/lactation은 adult primary pathway와 분리하고 trimester-specific ATD choice, fetal/infant risk 및 maternal biochemical control을 별도 기록한다. <!-- claim:POP-PREGNANCY-001 -->
- Older adults는 adult primary pathway와 분리하고 cardiovascular comorbidity 및 drug/procedural toxicity modifiers를 별도 기록한다. <!-- claim:POP-OLDER-002 -->
- Relapsed/refractory populations에서는 post-ATD relapse, post-RAI persistence, TED primary nonresponse, partial response, flare 및 post-treatment relapse를 별도 state로 기록한다. <!-- claim:POP-RELAPSED-002 -->

## 9. Limitations

1. Registry landscape는 미등록 preclinical assets, unpublished failures 및 비공개 sponsor changes를 포착하지 못할 수 있다. <!-- claim:LIMIT-001 -->
2. 일부 direct-program evidence는 congress abstract, sponsor 또는 registry source이며 peer-reviewed full-paper human outcome evidence가 아니다. [1, 2, 6, 7, 8] <!-- claim:LIMIT-002 -->
3. Query-level negative search는 authorization 또는 reimbursement 부재를 입증하지 않으므로 해당 status를 unresolved로 유지했다. <!-- claim:LIMIT-003 -->
4. Complete asset table의 R&D potential과 evidence confidence는 서로 다른 축이며 clinical efficacy 또는 probability로 해석할 수 없다. <!-- claim:LIMIT-004 -->
5. Stance-hidden QA는 within-agent bias-reduction이며 independent validation이 아니다. <!-- claim:LIMIT-005 -->

## 10. Conclusions

IGF-1R class에는 randomized TED trial evidence와 US, EU/EEA, UK, Japan의 regulatory authorization evidence가 존재하지만, 이를 GD pathogenic autoimmunity 제거 또는 durable off-treatment remission의 증거로 전환하지 않는다. [728, 729, 731, 735, 780] <!-- claim:CONCLUSION-001 -->
LCA-0321과 MER511은 anti-TSHR autoantibody axis를 직접 겨냥하는 Phase 1 programs이며, canonical analytic table의 evidence confidence는 각각 Low와 Low–moderate다. [1, 2, 6, 7, 8, 898] <!-- claim:CONCLUSION-002 -->
Near-term analytical monitoring priorities는 safety/PK/PD, TRAb/TSI/TSAb kinetics, thyroid hormones, immunogenicity, total-IgG preservation, B-cell pharmacology 및 off-treatment durability다. <!-- claim:CONCLUSION-004 -->
