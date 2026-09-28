---
linear_issue: JHA-76
created: 2026-09-27
source: claude-code
milestone: cluster-3-mechanism-deepdive
status: in-review
inputs:
  - 00_baseline_biomni/landscape_v2/pipeline_assets_v2.csv
  - 00_baseline_biomni/landscape_v2/clinical_trials_v2.csv
  - 00_baseline_biomni/landscape_v2/report_graves_ted_landscape_v2.md
  - 00_baseline_biomni/landscape_v2/frozen_trial_registry_documents_v2.jsonl
  - 00_baseline_biomni/landscape_v2/reference_catalog_v2.csv
  - 00_baseline_biomni/landscape_v2/source_anchors_v2.csv
  - 00_legacy_unsorted/GD_TED_report.md
  - _shared/GD_TED_qa_checklist.md
data_cut: 2026-09-10
---

# IGF-1R 계열 자산의 adverse event 비교

## 1. 결론과 읽는 법

- TED에서 두 개 이상 IGF-1R 억제 자산에 관찰된 반복 신호는 **muscle spasm, hearing-related AE, hyperglycemia/increased blood glucose**임. 다만 이는 관찰된 계열 패턴이며, 각 사건이 모두 IGF-1R 억제에 의해 발생한다는 인과성 또는 모든 계열 자산에서 발생한다는 의미는 아님.[1-5]
- Teprotumumab과 veligrotug의 공개 무작위시험에서 위 세 신호가 반복되고, IBI311 RESTORE-1도 세 범주의 발생과 mild/moderate severity를 보고함. Linsitinib에서는 muscle spasm이 보고됐지만, 공개 결과의 5% reporting threshold 아래 사건은 표에 나타나지 않을 수 있어 hearing AE나 hyperglycemia가 **0건이었다고 해석할 수 없음**.[2-5,10]
- Linsitinib의 상대적 특징은 high-dose에서 더 뚜렷한 GI/fatigue/transaminase 신호임. 이는 insulin receptor kinase도 함께 억제하는 oral small molecule이라는 차이를 고려해 해석할 사항이나, 현재 자료만으로 표적별 인과성을 분리할 수 없음.[1,5]
- Elegrobart는 `pipeline_assets_v2.csv`의 **VRDN-003**에 해당함. Elegrobart와 MHB-018A는 data cut 현재 공개된 수치형 AE 결과가 없어 **미보고**로 표시함. 반면 IBI311은 registry 결과가 미게시 상태여도 RESTORE-1 RCT 논문이 있으므로 해당 논문의 공개 safety 결과를 반영함. 미보고는 0건과 다름.[1,6,10]
- 이슈에 지정된 6개 자산 외에도 현재 `pipeline_assets_v2.csv`에서 target에 IGF-1R이 포함된 IBI3031, AMG 732, ZB001, lonigutamab, NTB003/BCG009를 scope reconciliation 표에 포함함. 따라서 master의 IGF-1R 관련 11개 자산을 누락 없이 확인하되, 상세 AE 표는 공개 수치가 있는 3개 자산과 이슈 지정 3개 미보고 자산을 중심으로 구성함.[1]
- 아래 수치는 population, dose, 투여경로, 관찰기간, AE 수집 및 coding threshold가 다른 시험의 병렬 기술임. **발생률 순위, 간접비교, pooled estimate로 사용하지 않음.** Figure 4의 selected PRR은 efficacy의 descriptive plot이므로 안전성 비교 근거로 사용하지 않음.

### 용어 규칙

| 표기 | 의미 |
|---|---|
| `n/N (%)` | 해당 시험군에서 사건이 보고된 참여자 수/위험집단 수; 소수점 첫째 자리 계산 |
| 미보고 | 확인한 공개 source에 사건별 수치가 없음. 사건 0건을 뜻하지 않음 |
| 0/N | source가 실제 0명을 명시한 경우만 사용 |
| SAE | serious adverse event를 1건 이상 경험한 참여자. 개별 SAE의 치료 관련성은 별도 명시가 없는 한 판단하지 않음 |
| class-common | 이 문서에서는 서로 다른 IGF-1R 억제 자산 2개 이상에서 관찰된 반복 신호라는 운영적 분류. 확정된 pharmacologic class effect 선언이 아님 |

## 2. 자산별 비교표

**공통 AE 열은 class-common 후보를, 마지막 열은 투여법 또는 분자 특성과 함께 두드러진 자산별 신호를 표시함.** Teprotumumab과 veligrotug 수치는 비교 가능한 하나의 공통 timepoint가 아니라 각각 아래에 적은 시험별 관찰기간의 값임.

| 자산 / 근거 집단 | 고혈당 / 혈당상승 | 청각 관련 AE | Muscle spasm | 전체 중증도 지표 | 자산별 특이 또는 두드러진 AE |
|---|---|---|---|---|---|
| **Teprotumumab**, chronic/low-activity TED, NCT04583735, Week 24, 41 vs placebo 20 | hyperglycemia **6/41 (14.6%)** vs **2/20 (10.0%)**; grade 미보고 | hearing impairment **9/41 (22.0%)** vs **2/20 (10.0%)**. 별도 preferred term tinnitus **2/41 (4.9%)** vs **2/20 (10.0%)**; grade 미보고 | **17/41 (41.5%)** vs **3/20 (15.0%)**; grade 미보고 | SAE **1/41 (2.4%)** vs **1/20 (5.0%)** | fatigue **9/41 (22.0%)** vs **2/20 (10.0%)**; diarrhoea **8/41 (19.5%)** vs **4/20 (20.0%)**; infusion-related reaction **2/41 (4.9%)** vs **3/20 (15.0%)**. 개별 event grade 미보고. 공개 label은 hearing loss가 severe하거나 일부 permanent일 수 있음을 경고함.[2,7] |
| **Veligrotug (Lumvoa)**, active TED THRIVE, NCT05176639, baseline-Week 52, 75 vs placebo 38 | blood glucose increased **7/75 (9.3%)** vs **1/38 (2.6%)**; hyperglycaemia **2/75 (2.7%)** vs **2/38 (5.3%)**. 서로 다른 preferred term이므로 합산하지 않음; grade 미보고 | ear discomfort **9/75 (12.0%)** vs **1/38 (2.6%)**; tinnitus **9/75 (12.0%)** vs **4/38 (10.5%)**. 서로 중복 가능하므로 합산하지 않음; grade 미보고 | **34/75 (45.3%)** vs **3/38 (7.9%)**; grade 미보고 | SAE **7/75 (9.3%)** vs **0/38 (0%)** | infusion-related reaction **13/75 (17.3%)** vs **2/38 (5.3%)**; alopecia **11/75 (14.7%)** vs **4/38 (10.5%)**; amenorrhoea **3/34 (8.8%)** vs **0/12 (0%)**. 개별 event grade 미보고.[3] |
| **Veligrotug**, dose-ranging NCT06384547, baseline-Week 52, 10 mg/kg 173 vs 3 mg/kg 58 | blood glucose increased **10/173 (5.8%)** vs **3/58 (5.2%)**; grade 미보고 | ear discomfort **17/173 (9.8%)** vs **2/58 (3.4%)**; hypoacusis **5/173 (2.9%)** vs **3/58 (5.2%)**; tinnitus **21/173 (12.1%)** vs **8/58 (13.8%)**. preferred term 간 중복 가능; grade 미보고 | **77/173 (44.5%)** vs **17/58 (29.3%)**; grade 미보고 | SAE **10/173 (5.8%)** vs **3/58 (5.2%)**; death **0/173 vs 0/58** | amenorrhoea **23/70 (32.9%)** vs **5/26 (19.2%)**; alopecia **30/173 (17.3%)** vs **6/58 (10.3%)**; infusion-related reaction **14/173 (8.1%)** vs **5/58 (8.6%)**, 이 중 serious **1/173 vs 0/58**. 그 외 event grade 미보고.[4] |
| **Linsitinib**, active moderate-to-severe TED LIDS, NCT05276063, AE 수집 consent-Week 120, placebo 31 / 75 mg BID 30 / 150 mg BID 29 safety set | 미보고, 공개 AE 표의 5% threshold 아래 사건은 배제될 수 있음 | 미보고, 공개 AE 표의 5% threshold 아래 사건은 배제될 수 있음 | placebo **1/31 (3.2%)**; 75 mg **2/30 (6.7%)**; 150 mg **3/29 (10.3%)** | SAE **1/31 (3.2%)**, **0/30 (0%)**, **2/29 (6.9%)**; death 각 군 **0** | dose별 placebo/75/150 mg: diarrhoea **2/31 (6.5%)/4/30 (13.3%)/6/29 (20.7%)**; nausea **1/31 (3.2%)/3/30 (10.0%)/6/29 (20.7%)**; fatigue **2/31 (6.5%)/6/30 (20.0%)/5/29 (17.2%)**; ALT increased **0/31/3/30 (10.0%)/4/29 (13.8%)**; AST increased **0/31/2/30 (6.7%)/3/29 (10.3%)**. 150 mg SAE는 abnormal ECG T wave와 Guillain-Barré syndrome 각 1명이며 relatedness 미판단.[5] |
| **Elegrobart (VRDN-003)**, SC IGF-1R mAb, Phase 3 | 미보고 | 미보고 | 미보고 | 미보고 | 공개 수치형 AE 결과 미보고. NCT06812325와 NCT07155668은 TEAE incidence를 endpoint로 두지만 data cut 현재 posted result 없음.[1,6] |
| **MHB-018A (MHB018A)**, SC IGF-1R mAb, Phase 3 | 미보고 | 미보고 | 미보고 | 미보고 | 공개 수치형 AE 결과 미보고. 등록시험은 protocol 수준이며 결과 미게시.[1,6] |
| **IBI311**, active moderate-to-severe TED RESTORE-1, NCT05795621, Week 24, randomized 54 vs placebo 28 | 발생 확인; event별 `n/N` 미보고; mild/moderate | 발생 확인; event별 `n/N` 미보고; mild/moderate | 발생 확인; event별 `n/N` 미보고; mild/moderate | IBI311군 SAE **0/54 (0%)**, death **0/54 (0%)**; placebo군 SAE/death 수치는 abstract에 미보고 | Infusion reaction 및 nausea/diarrhea도 발생 확인; event별 `n/N` 미보고; 모두 mild/moderate. 이는 RESTORE-1 논문 abstract에서 확인되는 범위이며, 8개 registry record의 posted-results 부재만으로 자산 전체 safety를 미보고 처리하지 않음.[10] |

### 2.1 Pipeline master scope reconciliation

아래 5개 자산은 이슈에 열거된 6개에는 없지만 current master에서 target 문자열에 IGF-1R이 포함되므로 전체 자산 확인 범위에 추가함. `미보고`는 이 문서가 확인한 TED 공개 자료에서 event-level 수치를 찾지 못했다는 뜻이며 전 적응증 안전성 문헌의 체계적 부재 증명이 아님.

| 추가 자산 | Target / master 상태 | TED 수치형 AE 결과 | 처리 |
|---|---|---|---|
| IBI3031 | IGF-1R and TSHR / recruiting, early | 미보고 | Early dual-target asset로 별도 추적 |
| AMG 732 | IGF-1R / active | 미보고 | Registered trial 결과 게시 시 갱신 |
| ZB001 | IGF-1R / clinical | 미보고 | Registered trial 결과 게시 시 갱신 |
| Lonigutamab | IGF-1R / registered status completed | 미보고 | 완료 상태와 결과 공개를 구분하여 추적 |
| NTB003 / BCG009 | IGF-1R / not yet recruiting | 미보고 | Protocol-only 자산으로 유지 |

## 3. Class-common 후보와 자산별 차이

| 구분 | 관찰 근거 | 해석 경계 |
|---|---|---|
| **Class-common 후보: muscle spasm** | Teprotumumab 41.5%, veligrotug 45.3% 및 44.5%, linsitinib 6.7-10.3%에서 보고. IBI311에서도 발생했으나 event별 빈도는 abstract에 미보고.[2-5,10] | 네 자산에서 반복되지만 대조군, dose, 기간이 다름. 단순 백분율로 자산 간 위험 순위를 만들 수 없음 |
| **Class-common 후보: hearing-related AE** | Teprotumumab hearing impairment 22.0%; veligrotug에서 ear discomfort 9.8-12.0%, tinnitus 12.0-12.1%, hypoacusis 2.9%가 보고됨. IBI311에서도 hearing impairment가 발생했으나 event별 빈도는 abstract에 미보고. Teprotumumab/veligrotug label은 severe/permanent hearing impairment 가능성과 치료 전/중/후 평가를 경고.[2-4,7,8,10] | `ear discomfort`, `hearing impairment`, `hypoacusis`, `tinnitus`, audiometric loss는 동일 endpoint가 아니며 환자 중복 가능성이 있어 합산하지 않음. Linsitinib 및 다른 개발 mAb의 미보고는 0건이 아님 |
| **Class-common 후보: hyperglycemia / blood glucose increased** | Teprotumumab hyperglycemia 14.6%; veligrotug에서 blood glucose increased 5.8-9.3% 및 hyperglycaemia 2.7%. IBI311에서도 hyperglycemia가 발생했으나 event별 빈도는 abstract에 미보고. Veligrotug label은 임상시험 전체 hyperglycemia 12%와 그중 절반의 baseline diabetes/impaired glucose tolerance를 명시.[2-4,8,10] | MedDRA preferred term을 임의 합산하지 않음. 기저 diabetes와 검사 빈도의 영향을 받는 신호이며 시험 간 직접비교 불가 |
| **반복되지만 투여경로 영향도 가능한 신호: infusion reaction** | IV teprotumumab과 IV veligrotug에서 보고.[2-4] | IGF-1R 표적 자체보다 IV biologic 투여 관련 가능성을 분리할 수 없음. Oral linsitinib 또는 SC 개발자산에 일반화하지 않음 |
| **Teprotumumab/veligrotug에서 반복: alopecia, GI, reproductive/menstrual event** | Veligrotug에서 alopecia와 amenorrhoea 수치 확인; teprotumumab의 pivotal/label 및 chronic trial에서 alopecia/GI/menstrual event 계열이 알려져 있음.[2-4,7] | 성별 위험집단 denominator와 coding이 다름. 계열 전체 공통으로 확정하기에는 공개 자산 수가 제한적 |
| **Linsitinib에서 두드러짐: GI/fatigue/transaminase** | 150 mg BID에서 diarrhoea와 nausea 각 20.7%, ALT increased 13.8%, AST increased 10.3%; placebo는 각각 6.5%, 3.2%, 0%, 0%.[5] | small molecule의 IGF-1R/insulin receptor kinase dual activity, oral exposure와 연관 가능성은 가설 수준. mAb와 직접 비교 불가 |

## 4. 데이터 공백과 후속 안전성 확인 항목

1. **Elegrobart/VRDN-003 명칭 고정:** 자산 master에는 VRDN-003으로만 존재하므로 본 문서에서 elegrobart와 같은 자산으로 처리함. 향후 source가 두 이름을 다르게 정의하면 crosswalk 수정 필요.[1,6]
2. **미보고 또는 부분 보고 자산:** Elegrobart와 MHB-018A는 첫 posted results, 학회 포스터 또는 CSR 공개 시 사건별 `n/N`, grade, serious/relatedness, discontinuation을 갱신해야 함. IBI311은 RESTORE-1 full-text safety table을 직접 확보하면 abstract에 없는 event별 `n/N`과 placebo SAE/death를 보완해야 함.[10]
3. **청각 endpoint 표준화:** 증상 설문, MedDRA hearing impairment/tinnitus, baseline-adjusted audiometry를 분리 수집해야 함. Teprotumumab real-world cohort의 높은 증상 또는 audiometric 빈도는 trial 표와 별도 근거층으로 유지함.[9]
4. **대사 위험 층화:** baseline diabetes/impaired glucose tolerance, HbA1c, rescue medication 및 회복 여부를 함께 기록해야 함.
5. **생식 안전성:** amenorrhoea와 menstrual irregularity는 female-at-risk denominator를 사용하고, pregnancy/fetal risk warning과 임상 AE를 혼합하지 않아야 함.
6. **중증도:** 현재 공개 registry는 많은 사건에 CTCAE grade와 treatment-relatedness를 제공하지 않음. 이 경우 빈도가 있어도 grade는 **미보고**이며, SAE 여부만 별도 제시함.

## 5. Source notes

1. `pipeline_assets_v2.csv`, asset keys `Teprotumumab`, `Veligrotug (Lumvoa)`, `Linsitinib`, `VRDN-003`, `MHB018A`, `IBI311`, `IBI3031`, `AMG 732`, `ZB001`, `Lonigutamab`, `NTB003 / BCG009`; data cut 2026-09-10. 자산, target, 개발단계, trial crosswalk에 사용.
2. `clinical_trials_v2.csv`, trial_id `NCT04583735`, `safety_results`; frozen ClinicalTrials.gov result record `NCT04583735`. Week 24 teprotumumab 결과.
3. `clinical_trials_v2.csv`, trial_id `NCT05176639`, `safety_results`; frozen ClinicalTrials.gov result record `NCT05176639`; Biomni v2 sources [230], [713], [829]. THRIVE Week 52 결과.
4. `clinical_trials_v2.csv`, trial_id `NCT06384547`, `safety_results`; frozen ClinicalTrials.gov result record `NCT06384547`; Biomni v2 source [859]. Dose-ranging Week 52 결과.
5. `clinical_trials_v2.csv`, trial_id `NCT05276063`, `safety_results`; frozen ClinicalTrials.gov result record `NCT05276063`; Biomni v2 sources [714], [715], [831]. LIDS 결과와 5% AE reporting threshold.
6. `clinical_trials_v2.csv`, trial_id `NCT06625398`, `NCT06625411`, `NCT06812325`, `NCT07155668`, `NCT07211776` (VRDN-003); `NCT06989918`, `NCT07257185`, `NCT07262476`, `NCT07620405`, `NCT07622108`, `NCT07622121` (MHB018A); `NCT05795621`, `NCT06126783`, `NCT06269393`, `NCT06525506`, `NCT07113262`, `NCT07152340`, `NCT07152366`, `NCT07152392` (IBI311). 모두 data cut에서 수치형 posted safety result 미확인.
7. DailyMed/FDA prescribing information, TEPEZZA, Biomni v2 source [728], anchors `US-TEPEZZA-LABEL-HEARING`, `US-TEPEZZA-LABEL-HYPERGLYCEMIA`. https://dailymed.nlm.nih.gov/dailymed/drugInfo.cfm?setid=3e6c54a1-cefd-4a5b-a855-ab9f268b6cce
8. FDA prescribing information, LUMVOA, Biomni v2 source [373], anchors `US-LUMVOA-LABEL-HEARING`, `US-LUMVOA-LABEL-HYPERGLYCEMIA`, `US-LUMVOA-LABEL-IBD`. https://www.accessdata.fda.gov/drugsatfda_docs/label/2026/761530Orig1s000lbl.pdf
9. `00_legacy_unsorted/GD_TED_report.md`, Section C3, refs [45-47]. Teprotumumab 실사용 청각 AE의 측정법 및 reversibility 불확실성 맥락.
10. Zhang H, et al. IGF-1R Inhibitor IBI311 for the Treatment of Active Thyroid Eye Disease in Chinese Patients: The RESTORE-1 Randomized Clinical Trial. JAMA Ophthalmology. 2025;143(11):964-971. PMID 41066129; DOI 10.1001/jamaophthalmol.2025.3350; Biomni v2 source [231]. Structured abstract는 IBI311 54명/placebo 28명과 AE of interest의 mild/moderate severity, IBI311군 SAE/death 부재를 보고하지만 event별 빈도는 제공하지 않음. https://doi.org/10.1001/jamaophthalmol.2025.3350

## 6. QA self-check

- [x] 요청된 6개 자산(teprotumumab, linsitinib, veligrotug, elegrobart/VRDN-003, MHB-018A, IBI311)과 current master의 추가 IGF-1R 관련 5개 자산 모두 확인
- [x] class-common 후보와 자산별 신호를 분리하고 class 인과성의 불확실성 명시
- [x] 공개된 AE는 `n/N (%)`, 관찰기간, comparator/dose와 함께 제시
- [x] 수치가 없는 경우 `미보고`로 표시하고 `0건`과 구분
- [x] 서로 다른 population/endpoint/timepoint의 순위, 간접비교, pooling 미실시
- [x] 중증도 grade가 없으면 미보고로 처리하고 SAE만 별도 제시
- [x] 한국어 본문, English technical terms 유지, 가운뎃점 미사용
