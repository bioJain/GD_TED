---
linear_issue: JHA-75
created: 2026-09-28
source: claude-code
milestone: cluster-2-ted-fcrn-strategy
status: draft
inputs:
  - 00_baseline_biomni/landscape_v2/result_trial_curation_v2.csv
  - 00_baseline_biomni/landscape_v2/clinical_trials_v2.csv
  - 00_baseline_biomni/landscape_v2/trial_result_evidence_anchors_v2.csv
  - 00_baseline_biomni/landscape_v2/frozen_trial_registry_documents_v2.jsonl
  - 00_baseline_biomni/landscape_v2/report_graves_ted_landscape_v2.md
  - 00_legacy_unsorted/GD_TED_report.md
---

# Placebo 대비 성공/실패 자산 요약표

## 1. 범위와 판독 원칙

- **Data cut:** Biomni v2 frozen cut인 **2026-09-10**. 결과 수치는 `result_trial_curation_v2.csv`의 승인된 25개 result-bearing trial을 기준으로 하고, 설계/arm/eligibility는 `clinical_trials_v2.csv`와 frozen ClinicalTrials.gov record를 대조함.
- **두 개의 모수:** (1) 결과 공개 25건은 결과 유무와 무관하게 전수 목록화, (2) 168개 trial master에서 `TERMINATED`, `WITHDRAWN`, `SUSPENDED`인 17건은 별도 전수 목록화. 따라서 UplighTED처럼 결과가 게시되지 않은 중단 시험도 누락하지 않음.
- **성공/실패 정의:** `성공`은 prespecified primary comparison이 placebo 대비 통계적으로 유의한 경우, `실패`는 유의하지 않거나 futility인 경우. `부분 성공`은 다중 용량 중 일부만 primary comparison에 성공한 경우. 결과 미게시, active comparator, single-arm, open-label extension, feasibility/운영상 중단은 성공/실패로 억지 분류하지 않음.
- **비교 금지:** 아래 수치는 각 trial 내부 비교에만 유효함. 모집단(activity, disease duration), endpoint 정의, 평가 시점, 투여 방식이 달라 **cross-trial pooling, naive ranking, meta-analysis를 하지 않음**.
- **Evidence 표기:** `[N]`은 Biomni v2 `reference_v2.md`의 source ID이며, 각 trial의 frozen registry record와 연결된 `trial_result_evidence_anchors_v2.csv` anchor임.

## 2. Executive summary: placebo-controlled 주요 결과

### 2.1 TED 질환조절 후보

| Class / 자산 | Trial / 모집단 | Arm / primary endpoint | Placebo 대비 결과 | 판정 |
|---|---|---|---|---|
| IGF-1R mAb / teprotumumab | NCT01868997, Phase 2; active TED, onset <9개월, CAS ≥4; n=87 | IV teprotumumab 8회 vs saline, q3W; Week 24 composite responder | 29/42 vs 9/45; p<0.001; proptosis LS change −2.46 vs −0.15 mm | **성공** [780] |
| IGF-1R mAb / teprotumumab, OPTIC | NCT03298867, Phase 3; active moderate-to-severe TED, onset ≤9개월, CAS ≥4; n=83 | 10 mg/kg 1회 후 20 mg/kg IV q3W 7회 vs placebo; Week 24 PRR | 82.9% vs 9.5%; p<0.001; RD 73.45%p | **성공** [807] |
| IGF-1R mAb / teprotumumab | NCT04583735, Phase 4; chronic/inactive TED 2-10년, CAS ≤1; n=62 | 동일 8회 IV regimen vs placebo; Week 24 proptosis change | −2.41 vs −0.92 mm; difference −1.48 mm, 95% CI −2.28 to −0.69; p=0.0004 | **성공** [817] |
| IGF-1R mAb / veligrotug, THRIVE | NCT05176639, Phase 3; active moderate-to-severe TED, onset ≤15개월, CAS ≥3; n=113 | 10 mg/kg IV q3W 5회 vs placebo; Week 15 PRR | 70.0% vs 5.26%; p<0.0001 | **성공** [829] |
| IGF-1R mAb / veligrotug, THRIVE-2 | NCT06021054, Phase 3; chronic TED, onset >15개월, any CAS; n=188 | 10 mg/kg IV q3W 5회 vs matched placebo; Week 15 PRR | 57.28% vs 8.22%; p<0.0001; RD 49.06%p | **성공** [845] |
| IGF-1R/insulin receptor TKI / linsitinib | NCT05276063, Phase 2/3; active moderate-to-severe TED, onset ≤12개월, CAS ≥4; n=90 | PO BID 150 mg 또는 75 mg vs placebo; Week 24 PRR | 150 mg 51.7% vs 18.8%, p=0.01; 75 mg 38.9%, p=0.090 | **부분 성공: high dose만 유의** [831] |
| IL-6R mAb / satralizumab, SatraGO-1 | NCT05987423, Phase 3; moderate-to-severe TED; n=131 | SC q4W vs placebo; active-TED Week 24 PRR | 49.0% vs 31.2%; p=0.0715; 95.03% CI of RD −1.6 to 37.3%p | **실패: primary 미충족** [844] |
| IL-6R mAb / satralizumab, SatraGO-2 | NCT06106828, Phase 3; moderate-to-severe TED; n=127 | SC q4W vs placebo; active-TED Week 24 PRR | 52.9% vs 23.4%; p=0.0011; RD 28.9%p | **성공** [849] |
| FcRn mAb / batoclimab, ASCEND GO-2 | NCT03938545, Phase 2; active moderate-to-severe TED, onset ≤9개월, CAS ≥4; n=65 | SC 680/340/255 mg weekly vs placebo, 12주; Week 13 PRR | 30.0%/30.8%/0% vs 8.3%; 각각 p=0.1993/0.1016/0.2963 | **실패: 모든 용량 primary 미유의** [813] |
| IL-17A mAb / secukinumab | NCT04737330, Phase 3; active moderate-to-severe TED, onset <12개월, CAS ≥4; n=28 | 300 mg SC vs placebo; Week 16 overall response 또는 PRR | overall response 0/14 vs 0/14; PRR 0/14 vs 0/14; blinded futility | **실패/futility** [819] |
| IL-11R mAb / LASN01 | NCT06226545, Phase 2; active moderate-to-severe TED; randomized subset n=26 | low/high-dose IV vs placebo, anti-IGF-1R-naive stratum; PRR와 safety | PRR 6/17 vs 3/9; 35.3% vs 33.3%. CAS response는 88.2% vs 44.4%, p=0.028 | **혼재: PRR 차이 없음, CAS 신호** [853] |
| FcRn fragment / efgartigimod PH20 SC, UplighTED | NCT06307613 및 NCT06307626, Phase 3; active moderate-to-severe TED, onset ≤12개월 | SC active vs matched PH20 placebo; Week 24 PRR | 결과 미게시. 사전 정의 중간분석에서 intended efficacy 입증 가능성이 낮아 두 시험 조기 종료; safety 사유 아님 | **실패/futility, 수치 미공개** [857, 858] |

### 2.2 GD/요법 최적화 placebo 결과

| 자산 | Trial / 설계 | Primary endpoint / 결과 | 판정 |
|---|---|---|---|
| Rituximab | NCT00595335; active moderate-to-severe TED, rituximab vs saline, n=25 | 6개월 CAS change −1.2 vs −1.5, p=0.73; failure 69% vs 75%, p=0.75 | **실패** [762] |
| 조기 levothyroxine after RAI | NCT01950260; GD, levothyroxine vs placebo, n=61 | Week 8 overt hypothyroidism 11/30 vs 17/31, p=0.23 | **실패** [782] |
| Alfacalcidol + PTU | NCT02993302; GD, alfacalcidol+PTU vs placebo+PTU, n=25 | CD80 p=0.48, CD206 p=0.47, IL-12/IL-10 p=0.53 | **실패: biomarker primary** [801] |

### 2.3 각 시험에서 `placebo`가 실제로 의미하는 것

**결론부터 말하면, 두 설계가 모두 존재하지만 TED 신약 시험의 대부분은 `SoC+placebo` 대 `SoC+신약`이 아니다.** Active TED 시험에서는 대체로 시험약과 외형/투여경로/일정이 맞는 inactive control만 투여하고, 갑상선기능 관리와 허용된 supportive care를 유지한다. 반면 GD 요법 최적화 시험인 NCT01950260은 양 군 모두 RAI 후 상태이고, NCT02993302는 양 군 모두 PTU를 투여하므로 명확한 background therapy 위 add-on 비교이다.

`placebo`라는 label만으로 생리식염수인지 formulation vehicle인지 알 수는 없다. Registry가 `normal saline`이라고 명시한 경우에만 saline으로 적었고, 단지 `matched placebo` 또는 `placebo`라고 기록한 경우 조성을 임의 추정하지 않았다.

| Trial / 자산 | Active arm이 받은 것 | Placebo arm이 실제로 받은 것 | 공통 background / 설계 해석 |
|---|---|---|---|
| NCT00595335 / rituximab | Rituximab 1,000 mg IV 2회, 각 투여 전 methylprednisolone 100 mg IV | Saline IV 2회, 각 투여 전에도 saline premedication | SoC add-on 설계가 아님. Active arm에만 steroid premedication이 포함되어 rituximab 단독 차이로만 해석하기 어려움 [762] |
| NCT01868997 / teprotumumab Phase 2 | Teprotumumab IV q3W 8회 | **Normal saline IV** q3W 8회 | TED disease-modifying SoC add-on 아님. Local supportive measures와 제한된 과거 steroid만 허용한 efficacy trial [780] |
| NCT03298867 / teprotumumab OPTIC | Teprotumumab 10 mg/kg 1회 후 20 mg/kg IV q3W 7회 | **Normal saline IV**, active arm과 동일한 infusion volume/일정 | TED disease-modifying SoC add-on 아님. Thyroid function은 controlled 상태로 유지 [807] |
| NCT04583735 / teprotumumab chronic TED | 동일 teprotumumab 8회 IV regimen | Teprotumumab-matching placebo IV q3W 8회, 공개 registry에 vehicle 조성 미기재 | Chronic/inactive TED의 direct placebo comparison. Double-masked 기간 후 nonresponder는 open-label teprotumumab 선택 가능 [817] |
| NCT03938545 / batoclimab | 680/340/255 mg SC weekly, 12주 | SC placebo weekly, 공개 registry에 vehicle 조성 미기재 | SoC add-on으로 명시되지 않음. 최근 steroid/biologic therapy를 배제 [813] |
| NCT04737330 / secukinumab | 300 mg SC, Baseline/Week 1/2/3/4/8/12 | SC placebo, active arm과 동일 일정; 조성 미기재 | SoC add-on 아님. Non-sight-threatening active TED 대상 [819] |
| NCT05176639 / veligrotug THRIVE | 10 mg/kg IV q3W 5회 | Veligrotug-matched placebo IV q3W 5회; 조성 미기재 | SoC add-on 아님. 최근 systemic steroid/면역억제제를 배제 [829] |
| NCT06021054 / veligrotug THRIVE-2 | 10 mg/kg IV q3W 5회 | Veligrotug-matched placebo IV q3W 5회; 조성 미기재 | Chronic TED direct placebo comparison [845] |
| NCT05276063 / linsitinib | 150 mg 또는 75 mg oral BID | Oral placebo BID | SoC add-on 아님. Prior IGF-1R therapy와 일정 수준 이상의 최근 glucocorticoid를 배제 [831] |
| NCT05987423 / satralizumab SatraGO-1 | Satralizumab SC q4W | SC placebo q4W, 조성 미기재 | Part I direct placebo comparison 후 Part II는 proptosis response 기반 individualized treatment [844] |
| NCT06106828 / satralizumab SatraGO-2 | Satralizumab SC q4W | SC placebo q4W, 조성 미기재 | SatraGO-1과 같은 구조의 direct placebo comparison [849] |
| NCT06226545 / LASN01 | Randomized low/high-dose LASN01 IV | IV placebo, anti-IGF-1R-naive randomized stratum; 조성 미기재 | Post-teprotumumab 환자는 별도 open-label arm이며 placebo comparison에 포함하지 않음 [853] |
| NCT06307613/626 / efgartigimod UplighTED | Efgartigimod PH20 SC, prefilled syringe | Registry 명칭상 **Placebo PH20 SC**, prefilled syringe; 상세 formulation 미공개 | SoC add-on으로 명시되지 않은 direct placebo comparison [857, 858] |
| NCT01950260 / early levothyroxine | RAI 후 Week 4부터 levothyroxine 25 μg/day, 이후 50 μg/day | RAI 후 Week 4부터 placebo capsule, Week 8에 levothyroxine 필요성 평가 | **공통 background가 RAI**인 regimen-timing 비교 [782] |
| NCT02993302 / alfacalcidol | PTU 300 mg/day + alfacalcidol 1.5 μg/day, 8주 | **PTU 300 mg/day + placebo tablet**, 8주 | **SoC에 가까운 공통 ATD 위 add-on** 비교 [801] |

#### Placebo 기간에 질환 진행을 어떻게 다루는가

- Placebo가 active TED를 치료하는 것은 아니며 placebo response도 자연경과, 측정 변동, concomitant supportive care 등의 영향을 받을 수 있음. 실제로 placebo PRR가 OPTIC 9.5%, linsitinib trial 18.8%, SatraGO-1 31.2%처럼 시험마다 달라 자연경과가 동일하다고 가정할 수 없음. [807, 831, 844]
- 주요 active TED 시험은 **sight-threatening disease, optic neuropathy, refractory corneal disease 또는 immediate surgery가 필요한 환자**를 배제해 관찰 가능한 risk 범위를 제한함. Euthyroid 또는 제한된 mild thyroid dysfunction을 요구하고 thyroid treatment는 안정화/유지하지만, 이는 TED disease-modifying SoC add-on과 다른 의미임.
- Trial별 protocol에는 prohibited medication, discontinuation, rescue 또는 open-label 전환 규칙이 있을 수 있음. Frozen public registry에 rescue regimen이 구체적으로 공개되지 않은 경우 이를 추정하지 않음. 따라서 `placebo arm=아무 의료관리도 받지 않음`도, `placebo arm=모두 IVMP SoC를 받음`도 일반화하면 안 됨.
- 특히 teprotumumab pivotal trial의 비교 질문은 대체로 **controlled thyroid status/supportive management 하에서 teprotumumab 자체가 matched inactive infusion보다 나은가**이며, **IVMP+teprotumumab 대 IVMP 단독** 질문이 아님.

## 3. Class별 임상 디자인 검토

### 3.1 IGF-1R pathway

- **Active TED enrichment:** teprotumumab Phase 2/OPTIC은 CAS ≥4, 증상 onset ≤9개월; linsitinib은 CAS ≥4, onset ≤12개월; THRIVE는 CAS ≥3, onset ≤15개월로 정의가 다름. 모두 sight-threatening disease/immediate surgery 필요 환자를 배제하고, euthyroid 또는 제한된 mild thyroid dysfunction을 허용하는 구조임.
- **Chronic population:** NCT04583735는 TED 진단 2-10년, 양안 CAS ≤1 및 1년 이상 안정성을 요구한 반면 THRIVE-2는 onset >15개월과 any CAS를 허용함. 두 chronic trial 수치를 동일 population의 반복 결과로 간주할 수 없음.
- **Arm/노출:** teprotumumab은 8회 IV(첫 10 mg/kg, 이후 20 mg/kg q3W), veligrotug은 10 mg/kg IV q3W 5회, linsitinib은 oral BID high/low dose의 3-arm 설계. PRR 평가시점도 Week 24와 Week 15로 다름.
- **Prior therapy:** THRIVE/THRIVE-2는 prior anti-IGF-1R을 배제했고, linsitinib도 prior IGF-1R inhibitor와 prior orbital irradiation/surgery를 배제함. LASN01은 anti-IGF-1R-naive randomized cohort와 post-teprotumumab open-label cohort를 의도적으로 분리함.

### 3.2 FcRn inhibition

- **Batoclimab ASCEND GO-2:** 3개 active SC dose와 placebo, double-blind Phase 2. CAS ≥4, onset ≤9개월의 active moderate-to-severe GD-associated TED를 선별하고 최근 steroid, 최근 biologic immunomodulation, prior orbital irradiation/surgery, low baseline IgG를 배제함. Clinical primary PRR는 전 용량 미유의였지만 IgG/anti-TSHR PD는 dose-related였음. Program-wide review에 따른 premature unblinding 때문에 종료되었으므로 결과는 negative clinical comparison으로 보존하되 순수한 target invalidation으로 확대하지 않음. [813]
- **Efgartigimod UplighTED:** 두 개의 parallel Phase 3 모두 active moderate-to-severe autoimmune-thyroid-associated TED, onset ≤12개월, controlled thyroid function을 대상으로 efgartigimod PH20 SC와 matched placebo를 비교함. Optic neuropathy, refractory corneal disease, prior orbital irradiation/surgery 등을 배제함. 두 시험 모두 같은 interim futility 사유로 종료되었고 결과값은 공개되지 않아 effect size를 추정할 수 없음. [857, 858]
- **해석 경계:** batoclimab의 PRR 실패와 UplighTED futility는 TED에서 FcRn clinical efficacy가 입증되지 않았다는 근거이나, 서로 다른 molecule/regimen의 결과를 pooling하거나 GD biochemical efficacy로 외삽하지 않음.

### 3.3 Cytokine blockade

- **IL-6R/satralizumab:** SatraGO-1/2는 동일한 SC q4W active/placebo 구조와 Week 24 active-population PRR를 사용했지만 한 시험은 primary 실패, 다른 시험은 성공함. Registry 공개 eligibility는 clinical diagnosis based on CAS, immediate surgery/irradiation 필요 환자와 screening-to-baseline spontaneous improvement 환자 배제를 명시함. Replicate 결과 불일치는 하나의 pooled estimate나 class 순위로 축약하지 않음. [844, 849]
- **IL-17A/secukinumab:** 300 mg SC loading 후 Week 4/8/12 투여 vs placebo. CAS ≥4, onset <12개월의 active moderate-to-severe TED를 선별했으며 Week 16 response가 양 군에서 거의 관찰되지 않아 efficacy futility로 종료됨. Safety concern에 의한 종료가 아님. [819]
- **IL-11R/LASN01:** anti-IGF-1R-naive 대상의 randomized low/high-dose/placebo와 post-teprotumumab open-label high-dose arm이 공존함. 따라서 공개 결과의 randomized n=26만 placebo comparison에 사용해야 하며, CAS response와 PRR가 서로 다른 결론을 보여 endpoint별로 분리 해석함. [853]

## 4. 결과 공개 25건 completeness ledger

`result_trial_curation_v2.csv` 25/25건을 아래에 표시함. `Placebo 판정`이 `해당 없음`인 행도 결과 공개 trial completeness를 위해 유지함.

| Trial | 자산 / indication | Disposition | Primary 결과 요약 | Placebo 판정 |
|---|---|---|---|---|
| NCT00595335 | Rituximab / active TED | negative_randomized | 6개월 CAS 및 failure rate 우월성 없음 | 실패 [762] |
| NCT01114503 | Otelixizumab / active TED | terminated_uninterpretable | n=2, efficacy 해석 불가; dose-development 사유 종료 | 해당 없음 [767] |
| NCT01269749 | RAI/ATD / pediatric GD | no_posted_efficacy | Outcome measurement row 없음 | 해당 없음 [769] |
| NCT01868997 | Teprotumumab / active TED | positive_randomized | Week 24 composite response 유의 | 성공 [780] |
| NCT01950260 | Levothyroxine / GD after RAI | negative_primary | Week 8 overt hypothyroidism 미유의 | 실패 [782] |
| NCT02378298 | Rituximab/MTX rescue / active TED | nonrandomized_descriptive | 비동등 selected cohort의 CAS 관찰값 | 해당 없음 [791] |
| NCT02713256 | Iscalimab / GD | single_arm_weak | Week 12 TSH normalization 0% | 해당 없음 [796] |
| NCT02845336 | Celecoxib / active TED | terminated_infeasible | poor enrollment, efficacy 판단 불가 | 해당 없음 [798] |
| NCT02973802 | ATX-GD-59 / GD | exploratory_single_arm | n=12 biomarker signal, remission proof 아님 | 해당 없음 [800] |
| NCT02993302 | Alfacalcidol+PTU / GD | negative_biomarker | immune biomarker primary 미유의 | 실패 [801] |
| NCT03298867 | Teprotumumab / active TED | positive_randomized | OPTIC Week 24 PRR 유의 | 성공 [807] |
| NCT03461211 | Teprotumumab / active TED | open_label_extension | prior-placebo crossover/selected retreatment response | 해당 없음 [809] |
| NCT03922321 | Batoclimab / active TED | single_arm_pd | n=7 IgG PD, clinical efficacy inference 제한 | 해당 없음 [812] |
| NCT03938545 | Batoclimab / active TED | negative_primary_pd_positive | Week 13 PRR 전 용량 미유의, PD signal | 실패 [813] |
| NCT04583735 | Teprotumumab / chronic TED | positive_randomized | Week 24 proptosis change 유의 | 성공 [817] |
| NCT04737330 | Secukinumab / active TED | negative_futility | Week 16 response 부재, futility | 실패 [819] |
| NCT05176639 | Veligrotug / active TED | positive_randomized | THRIVE Week 15 PRR 유의 | 성공 [829] |
| NCT05276063 | Linsitinib / active TED | positive_high_dose | high dose PRR 유의, low dose 미유의 | 부분 성공 [831] |
| NCT05907668 | Batoclimab+ATD / GD | single_arm_biochemical | biochemical control/ATD reduction signal | 해당 없음 [843] |
| NCT05987423 | Satralizumab / moderate-to-severe TED | negative_primary_secondary_signals | SatraGO-1 active PRR primary 실패 | 실패 [844] |
| NCT06021054 | Veligrotug / chronic TED | positive_randomized | THRIVE-2 Week 15 PRR 유의 | 성공 [845] |
| NCT06106828 | Satralizumab / moderate-to-severe TED | positive_randomized | SatraGO-2 active PRR 유의 | 성공 [849] |
| NCT06179875 | Veligrotug / feeder nonresponders | selected_open_label | selected open-label cohort | 해당 없음 [852] |
| NCT06226545 | LASN01 / active TED | mixed_small_randomized | PRR 유사, CAS response signal | 혼재/primary PRR 미입증 [853] |
| NCT06384547 | Veligrotug / active TED | active_dose_uncontrolled | placebo 없는 dose safety comparison | 해당 없음 [859] |

## 5. Negative/stopped trial completeness ledger

Master 168건 중 frozen status가 `TERMINATED`, `WITHDRAWN`, `SUSPENDED`인 **17/17건**. 결과 공개 여부를 함께 표시해 `중단=효능 실패` 오독을 방지함.

| Trial | 자산 / indication | Status / 결과 게시 | Registry 중단 사유 | 해석 |
|---|---|---|---|---|
| NCT00288522 | Lanreotide / active TED | TERMINATED / No | 사유 미보고 | 실패 원인 판정 불가 |
| NCT01114503 | Otelixizumab / active TED | TERMINATED / Yes | 다른 연구에서 유효 dose 이해를 기다리며 종료 | n=2, uninterpretable [767] |
| NCT01379196 | Azithromycin / active TED | WITHDRAWN / No | 환자 등록 의향 부족 | Recruitment failure |
| NCT01893450 | Methimazole/bromocriptine/pentoxifylline / active TED | TERMINATED / No | Preliminary analysis에서 efficacy 확인 | Negative로 분류 금지 |
| NCT02393183 | Selenium / active TED | WITHDRAWN / No | Drug access 불가 | Operational |
| NCT02845336 | Celecoxib / active TED | TERMINATED / Yes | Poor enrollment | Feasibility failure [798] |
| NCT05517447 | Batoclimab feeder extension / active TED | TERMINATED / No | Feeder studies primary efficacy 미충족으로 benefit-risk 변경; new safety finding 없음 | Upstream efficacy failure 연동 |
| NCT06467435 | Kamuvudine-9 / active TED | TERMINATED / No | Low enrollment | Recruitment failure |
| NCT02422368 | Methylprednisolone/selenium / active moderate-to-severe TED | WITHDRAWN / No | Drug access 불가 | Operational |
| NCT03938545 | Batoclimab / active moderate-to-severe TED | TERMINATED / Yes | Program review로 premature unblinding | Primary negative이나 termination 자체는 mechanistic failure 아님 [813] |
| NCT04737330 | Secukinumab / active moderate-to-severe TED | TERMINATED / Yes | Primary 달성 가능성 낮은 blinded futility; safety concern 없음 | Efficacy futility [819] |
| NCT05394857 | SHR-1314 / active moderate-to-severe TED | TERMINATED / No | Sponsor commercial considerations | Commercial, efficacy 판정 불가 |
| NCT06307613 | Efgartigimod PH20 SC / active moderate-to-severe TED | TERMINATED / No | Interim analysis efficacy futility; safety concern 없음 | UplighTED efficacy futility [857] |
| NCT06307626 | Efgartigimod PH20 SC / active moderate-to-severe TED | TERMINATED / No | Interim analysis efficacy futility; safety concern 없음 | UplighTED efficacy futility [858] |
| NCT06240455 | WP1302+methimazole / GD | SUSPENDED / No | Suitable subject recruitment 불가능 | Recruitment feasibility |
| NCT02112643 | Selenium / mild TED | WITHDRAWN / No | Funding 부족 | Operational |
| NCT06087731 | Tocilizumab / TED | WITHDRAWN / No | Personal reasons | Operational/불명확 |

## 6. 결론과 사용 시 주의점

1. **재현된 positive signal은 주로 IGF-1R pathway에서 확인:** active와 chronic TED에서 여러 placebo-controlled trial이 각자의 primary endpoint를 충족했으나, 서로 다른 drug, exposure, eligibility, Week 15/24 timepoint 때문에 효과크기 순위를 만들 수 없음.
2. **다른 면역 class는 일관되지 않음:** satralizumab은 replicate Phase 3 결과가 갈렸고, FcRn clinical program은 batoclimab PRR 미유의와 efgartigimod futility, IL-17A는 futility, IL-11R은 endpoint별 혼재 결과임.
3. **Endpoint가 결론을 바꿈:** LASN01의 CAS response와 PRR, batoclimab의 PD와 PRR처럼 activity/biomarker 개선이 structural proptosis efficacy를 대신하지 않음. Primary endpoint를 우선하고 secondary/nominal signal을 구분해야 함.
4. **중단 사유를 efficacy failure와 동일시하지 않음:** 17개 stopped trial에는 efficacy futility뿐 아니라 recruitment, funding, drug access, commercial decision, preliminary efficacy 확인까지 포함됨.
5. **GD와 TED를 분리:** TED의 PRR/CAS 결과는 GD biochemical remission 근거가 아니며, GD single-arm biochemical control 역시 TED efficacy 근거가 아님.

## 7. 검증 로그

| Claim | Tier | 검증 방법 | 결과 | 일자 |
|---|---|---|---|---|
| Result-bearing trial 25건 completeness | 중 | `result_trial_curation_v2.csv` trial_id 전수 대조 | 25/25 포함 | 2026-09-28 |
| Stopped status completeness | 상: phase/status 포함 | `clinical_trials_v2.csv`에서 TERMINATED/WITHDRAWN/SUSPENDED 전수 필터 | 17/17 포함 | 2026-09-28 |
| Primary endpoint/result/significance | 중 | Curation row와 evidence anchor, frozen registry result 연결 대조 | 표 수치/판정 일치 | 2026-09-28 |
| Arm/eligibility | 중 | `clinical_trials_v2.csv` arms와 frozen registry eligibility module 대조 | 주요 placebo class 요약 완료 | 2026-09-28 |
| Placebo composition/background therapy | 중 | 각 placebo-controlled trial의 registry arm/intervention text 전수 대조 | 15개 trial/program의 saline, matched placebo, 공통 RAI/PTU 및 미공개 조성을 구분 | 2026-09-28 |
| UplighTED futility | 중 | 두 frozen registry `why_stopped` 및 legacy Section E2 대조 | efficacy futility, safety 비관련 문구 일치 | 2026-09-28 |

> **QA 상태:** 작성 세션 내 deterministic completeness/format 검사는 완료. `docs/repo_conventions.md`가 요구하는 독립 QA session 및 상 tier cross-model/direct-quote 검증은 별도 절차이므로 본 문서 상태를 `draft`로 유지함.
