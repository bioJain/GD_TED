---
linear_issue: JHA-70
created: 2026-09-24
source: claude-code
milestone: cluster-1-competitive-landscape
status: in-review
inputs:
  - 00_baseline_biomni/landscape_v2/soc_outcomes_v2.csv
  - 00_baseline_biomni/landscape_v2/source_anchors_v2.csv
  - 00_baseline_biomni/landscape_v2/report_graves_ted_landscape_v2.md
  - 00_baseline_biomni/epi_soc_run_260914/report_graves_ted_landscape.md
  - 00_legacy_unsorted/GD_TED_report.md
---

# Graves' disease 치료 line-of-therapy

## 1. 범위와 해석 원칙

- 대상: 성인 Graves' hyperthyroidism의 일반 경로와 재발, 임신, 소아 등 별도 환자군
- 근거 시점: Biomni v2 data cut인 2026-09-10. 미확인 수치 보완을 위한 PubMed live search는 별도로 2026-09-24 수행하고 해당 참고문헌에 확인일 명시
- 아래의 `1차 -> 2차 -> 재발/불응`은 실무용 순서화. 모든 환자에게 강제되는 보편적 단계 규칙은 아님
- 미국 ATA는 overt GD의 초기 치료로 ATD, RAI, thyroidectomy를 모두 허용. 유럽 ETA는 newly diagnosed GD에서 ATD를 기본으로 두되 환자 선호에 따라 RAI 또는 thyroidectomy도 초기 선택 가능[1,2]
- 따라서 `2차`는 주로 ATD 실패 후의 위치를 뜻하며, RAI와 thyroidectomy가 반드시 ATD 뒤에만 가능하다는 의미가 아님

## 2. 3단계 line-of-therapy 표

| 실무 단계 | 대상/진입 조건 | 치료와 기간 | 평가 endpoint | 다음 선택 | 놓치는 환자군/미충족 수요 | remission/지속성 수치 |
|---|---|---|---|---|---|---|
| **1차: ATD** | Newly diagnosed 성인 GD. 대부분 MMI/CMZ 선택. 임신 제1삼분기는 PTU 예외 | MMI 약 **12-18개월**. TSH와 TRAb/TSHR-Ab 정상 시 중단 고려. 지속 고 TRAb이면 MMI를 **추가 12개월** 지속하거나 definitive therapy 선택[1,2] | 복용 중 biochemical control, off-ATD normalization, durable off-treatment remission을 분리. 중단 전 TRAb로 remission 가능성 평가 | 중단 후 relapse, 약물 불내성, poor control이면 RAI 또는 thyroidectomy. 환자 선호 시 장기 low-dose MMI 가능[1,2] | 12-18개월 후 비관해/재발, agranulocytosis/hepatotoxicity 위험, adherence 불량, 큰 goiter/압박, 빠른 definitive control 필요, 임신/임신 계획 | 성인 RCT에서 MMI 중단 후 **84개월 relapse-free 44%**(통상군, median 18개월 치료) 대 **83%**(장기군, 60-120개월 치료). 재발은 각각 **56%**와 **17%**[8]. 특정 단일 RCT 결과이며 전체 guideline population의 고정 remission 비율로 일반화하지 않음 |
| **2차: definitive therapy, RAI** | ATD 후 relapse/poor control, ATD 부작용, 또는 초기부터 definitive therapy 선호. Pregnancy/lactation 및 TED 위험 별도 평가 | 미국 기준 통상 **10-15 mCi 단회**, 첫 **1-2개월** 평가 후 **4-6주** 간격으로 **6개월** 또는 안정화까지 monitoring[1] | Euthyroidism, hypothyroidism, persistent hyperthyroidism, retreatment를 구분. Destructive thyroid-source control을 autoimmune remission 또는 TED cure로 표현하지 않음 | **6개월** 후 persistent hyperthyroidism이면 repeat RAI 고려. Minimal response이면 선택적으로 **3개월**부터 추가 RAI 고려. 상황에 따라 surgery/ATD[1] | 임신/수유에서는 금기. Active/severe TED 또는 TED 악화 고위험군, 방사선 회피 선호, 큰 goiter/압박, 신속한 control 필요 환자에서 부적합 가능[2] | 단일기관 370 MBq cohort(n=160)에서 **1년 thyroid-source control 81%**, 이 중 **61.8%가 hypothyroidism**으로 replacement 필요[9]. 이는 euthyroid와 hypothyroid를 합한 연구 정의상 `cure`이며 durable autoimmune remission 아님 |
| **2차: definitive therapy, thyroidectomy** | ATD 후 relapse/poor control/불내성, RAI 부적합, 큰 goiter/압박 또는 malignancy 의심, 빠른 control 필요, 또는 초기 수술 선호 | Total 또는 near-total thyroidectomy. 수술 전 ATD와 필요 시 beta-blockade로 euthyroid 상태 유도, 수술 직전 KI-containing preparation[1,2] | 신속한 thyroid-source control, 수술 합병증, 이후 thyroid hormone replacement. Autoimmune remission/TED outcome과 분리 | 수술 부적합이면 RAI 또는 ATD. Persistent biochemical disease이면 진단과 잔존 조직 재평가 | High-volume surgeon 접근 제한, hypoparathyroidism, recurrent laryngeal nerve injury, 출혈/마취 위험, 평생 replacement 부담 | 홍콩 population cohort(n=6,385, median follow-up 90개월)의 first-line treatment 비교에서 relapse **2.41%**(수술), **19.53%**(RAI), **75.60%**(ATD)[10]. 비무작위 후향 cohort이므로 selection bias 가능성이 있고 autoimmune remission 수치가 아님 |
| **재발/불응: prior-therapy-specific rescue** | ATD 중단 후 relapse, ATD intolerance/poor control, RAI 후 persistence를 서로 다른 failure state로 분류 | Post-ATD relapse: RAI 또는 thyroidectomy, 선호 시 장기 low-dose MMI. Post-RAI persistence: repeat RAI, surgery 또는 ATD[1,2] | ATD relapse와 RAI persistence를 하나의 반응률로 합치지 않음. 현재 biochemical control과 치료 중단 후 durability도 분리 | 이전 modality, adverse event, TED, goiter, 임신 계획, comorbidity, 환자 선호에 따라 alternate modality | 반복 ATD toxicity, 반복 RAI/수술 위험, persistent thyrotoxicosis의 cardiovascular risk. 기존 치료로 durable remission에 도달하지 못한 환자 | **통합 remission 비율: 산출하지 않음.** Failure state, 후속 modality, endpoint가 이질적이므로 단일 수치보다 위의 modality별 결과를 사용 |

## 3. Endpoint taxonomy

| 용어 | 본 문서의 사용 범위 | 혼동 금지 항목 |
|---|---|---|
| On-treatment biochemical control | ATD 복용 중 FT4/FT3 정상화 | Off-treatment remission 아님 |
| Off-ATD normalization | 특정 평가 시점에 ATD 없이 FT3/FT4 정상 | 충분한 추적이 없으면 durable remission 아님 |
| Durable off-treatment remission | 사전 정의된 추적 기간 동안 치료 없이 euthyroidism 유지, relapse 없음 | RAI/수술 후 hypothyroidism과 다름 |
| Relapse | ATD 중단 후 hyperthyroidism 재발 | RAI 후 persistent hyperthyroidism과 다름 |
| Thyroid-source control | RAI 또는 수술로 thyroid hormone source를 제거/파괴 | Pathogenic autoimmunity 소실 또는 TED cure 아님 |

## 4. 특수 환자군과 경로 이탈

| 환자군 | 일반 경로에서 놓치는 지점 | 별도 경로/미충족 수요 | 근거 |
|---|---|---|---|
| 임신/임신 계획 | MMI와 RAI를 일반 성인과 동일하게 적용 불가 | Overt GD에는 ATD 사용. 제1삼분기는 PTU, 제1삼분기 이후 새로 ATD를 시작하면 MMI. RAI 사용 금지. 약물 불내성/poor control이면 multidisciplinary assessment와 임신 시기에 적합한 수술 검토 | ATA R80, ETA R21/R35[1,2] |
| 수유 | RAI 사용 불가. 모체 control만 평가하면 infant exposure 누락 | 최저 유효 ATD와 infant thyroid safety 병행. 미국 전용 lactation anchor는 curated set에서 미확인되어 ETA 권고를 contextual evidence로만 사용 | ETA R21/R42/R43[2] |
| Active/severe TED 또는 TED 악화 위험 | RAI가 안과 질환을 악화시킬 수 있어 단순 2차 선택 곤란 | Thyroid control과 TED activity/severity를 함께 평가. RAI 회피 또는 risk-adapted steroid prophylaxis/대체 modality 검토 | ETA guideline의 GO 관련 권고[2] |
| ATD 불응/불내성 | 12-18개월 완주 또는 장기 저용량 유지 불가 | RAI와 thyroidectomy 적합성 비교. Agranulocytosis/hepatotoxicity 의심 시 안전성 우선 평가 | ATA R23, ETA R13[1,2] |
| 큰 goiter/압박, malignancy 의심 | 반복 ATD나 RAI가 구조적 문제를 해소하지 못할 수 있음 | 숙련된 high-volume surgeon의 thyroidectomy 우선 검토. 수술 접근성과 합병증 부담이 미충족 요인 | ATA R24, ETA R24[1,2] |
| 소아/청소년 | 성인 12-18개월 duration과 RAI 기준을 그대로 적용 불가 | MMI **1-2년** 후 저용량에서 remission 평가 또는 연장. 관해가 없으면 RAI/thyroidectomy 고려. **5세 미만** RAI 회피와 연령/선량 제한 적용[1,4] | ATA R58 corrected/R66/R67[1,4] |
| 고령/심혈관 comorbidity | Thyrotoxicosis 악화가 AF, heart failure, ischemia를 유발할 위험 | RAI 전 high-risk 환자에서 MMI pretreatment, RAI 후 **3-7일** 선택적 재개 고려. Frailty와 procedural risk가 높고 mild/stable이면 장기 low-dose MMI 고려 | ATA R5/R6, ETA R44/R45[1,2] |

## 5. 지역별 line/status 요약

> `authorization`은 ATD/RAI/thyroidectomy라는 표준 modality에 제품 단위 허가 판정을 적용하지 않아 `NA`로 표기. 공식 근거가 확보되지 않은 region-wide reimbursement는 추정하지 않고 `unresolved` 유지.

| 지역 | Adult initial/continued medical therapy | Definitive option/재발 후 경로 | 특이사항 | Authorization/reimbursement |
|---|---|---|---|---|
| US | MMI 약 12-18개월, 임신 제1삼분기 PTU | RAI 또는 thyroidectomy는 초기 선택 또는 ATD 실패 후 선택. Post-RAI **6개월** persistence에서 repeat RAI 고려 | ATA evidence-graded guideline 기반 | NA/unresolved |
| EU | Newly diagnosed GD에서 ATD 기본. 12-18개월 후 TSH/TSHR-Ab 정상 시 중단 | 첫 ATD course 후 relapse이면 RAI/thyroidectomy 권고, 선호 시 long-term low-dose MMI | Pregnancy/breastfeeding에서 RAI 금기 | NA/unresolved |
| UK | Remission 가능성과 definitive therapy 적합성에 따라 carbimazole **12-18개월** | 적합한 성인에서 RAI가 first-line definitive option 가능. Persistent/relapsed이면 RAI 또는 surgery | NICE 기반. Adult pathway를 일률적 ATD-first로 표현하지 않음[5] | NA/unresolved |
| KR | 국내 입력은 RAI 중심 guideline. ATD duration은 ETA 12-18개월 framework를 international context로 사용 | ATD remission 후 recurrence 또는 적절한 ATD에도 poor control이면 RAI 고려. Surgery는 RAI 부적합/poor-control 맥락 | Korean national ATD pathway로 과장하지 않음[6] | NA/unresolved |
| JP | Untreated 환자는 일반적으로 drug therapy 대상. Pregnancy 예외 외 MMI first choice | Withdrawal 기준 미충족/relapse이면 RAI 또는 surgery 평가 | ATD withdrawal은 low-dose alternate-day 상태에서 **6개월 이상** 정상 기능 시 고려. 국내 입력의 exact guideline wording 사용[7] | NA/unresolved |

## 6. 수치 사용에 대한 결론

- 확인된 duration: 성인 ATD 12-18개월, persistent high TRAb에서 추가 12개월 선택, RAI 후 6개월까지 monitoring과 persistence 평가[1,2]
- ATD: MMI 통상 치료군의 84개월 relapse-free 44%와 장기 치료군의 83%를 확인. 장기 투여가 통상 투여보다 재발을 낮춘 RCT 결과이나, 연구 대상과 protocol을 벗어난 일반화는 제한[8]
- RAI: 1년 thyroid-source control 81%를 확인. 61.8%가 hypothyroidism이므로 이를 durable off-treatment remission으로 부르지 않음[9]
- Thyroidectomy: 장기 real-world cohort의 relapse 2.41%를 확인. 비무작위 치료 선택에 따른 confounding 가능성이 있어 modality 간 인과 비교로 해석하지 않음[10]
- 재발/불응 전체를 포괄하는 단일 remission 비율과 thyroidectomy 후 autoimmune remission 비율: **자료 미확인/단일 산출 부적절**. 서로 다른 endpoint와 추적기간을 합산하지 않음

## 7. PubMed 보완 검색 기록

| 검색일 | 검색 경로/검색어 | 채택 근거 | 제외 또는 해석 제한 |
|---|---|---|---|
| 2026-09-24 | PubMed E-utilities: `Graves methimazole randomized trial long term remission recurrence` | 성인 randomized trial의 치료기간별 장기 relapse 수치 채택[8] | Conventional duration과 long-term regimen의 추적조건이 달라 guideline 전체 비율로 확대 금지 |
| 2026-09-24 | PubMed E-utilities: `Graves radioactive iodine treatment success cohort hypothyroidism` | 최신 단일기관 cohort의 1년 euthyroid/hypothyroid composite와 hypothyroidism 비율 채택[9] | 단일기관, retrospective, 연구 정의상 cure가 autoimmune remission과 다름 |
| 2026-09-24 | PubMed E-utilities: DOI `10.1097/SLA.0000000000004828` | 세 modality를 비교한 population-based long-term cohort의 relapse 수치 채택[10] | First-line observational comparison으로 indication/selection confounding 가능 |
| 2026-09-24 | PubMed E-utilities: `Graves total thyroidectomy recurrence systematic review` | Total thyroidectomy가 subtotal thyroidectomy보다 recurrent hyperthyroidism을 낮춘 방향성 확인[11] | OR 중심 meta-analysis로 현재 표의 절대 relapse 수치에는 cohort[10] 사용 |

## 8. 근거 추적

주요 행 키: `SOC-US-GD-ADULT-ATD`, `SOC-US-GD-ADULT-RAI`, `SOC-US-GD-ADULT-THYROIDECTOMY`, `SOC-US-GD-RELAPSE-REFRACTORY`, `SOC-EU-GD-ADULT-ATD`, `SOC-EU-GD-RELAPSE-REFRACTORY`, `SOC-UK-GD-*`, `SOC-KR-GD-*`, `SOC-JP-GD-*`.

1. American Thyroid Association. 2016 American Thyroid Association Guidelines for Diagnosis and Management of Hyperthyroidism and Other Causes of Thyrotoxicosis. Source ID 26. Anchors US-ATA2016-R3/R5/R6/R8/R11/R12/R13/R21/R22/R23/R24/R80. https://www.liebertpub.com/doi/pdf/10.1089/thy.2016.0229 (확인일: 2026-09-10)
2. European Thyroid Association. 2018 European Thyroid Association Guideline for the Management of Graves' Hyperthyroidism. Source ID 39. Anchors EU-ETA2018-R5/R7/R8/R9/R13/R19/R21/R24/R35/R42/R43/R44/R45. PMID: 30283735. https://pmc.ncbi.nlm.nih.gov/articles/PMC6140607/ (확인일: 2026-09-10)
3. Li J, Cai Y, Sun X, Yao D, Xia J. MiR-346 and TRAb as Predicative Factors for Relapse in Graves' Disease Within One Year. Horm Metab Res. 2017;49(3):180-184. PMID: 28192819.
4. American Thyroid Association. Correction to Recommendation 58. Source ID 744. Anchors US-ATA2017-R58-CORRECTED/R58-ONLINE-CORRECTED. DOI: 10.1089/thy.2016.0229 (확인일: 2026-09-10)
5. National Institute for Health and Care Excellence. Thyroid disease: assessment and management, NG145. Anchors UK-NICE-NG145-1.6.10/1.6.11/1.6.12/1.6.13/1.6.14/1.6.22/1.6.26/1.7.1/1.7.11. https://www.nice.org.uk/guidance/ng145 (확인일: 2026-09-10)
6. Korean Thyroid Association. 2025 Korean Thyroid Association Management Guidelines for Radioactive Iodine Therapy in Patients with Hyperthyroidism. Source ID 28. https://www.e-enm.org/upload/pdf/enm-2025-2464.pdf (확인일: 2026-09-10)
7. Japan Thyroid Association. バセドウ病治療ガイドライン2019, guideline at a glance. Source ID 40. Anchors JP-JTA2019-BCQ1/BCQ2/BCQ6/BCQ7/BCQ26/BCQ28/BCQ30/BCQ32/BCQ33/BCQ34/BCQ35/BCQ36/FCQ1/FCQ4/FCQ5. https://www.jstage.jst.go.jp/article/naika/111/11/111_2279/_pdf (확인일: 2026-09-10)
8. Azizi F, et al. Risk of recurrence at the time of withdrawal of short- or long-term methimazole therapy in patients with Graves' hyperthyroidism: a randomized trial and a risk-scoring model. Endocrine. 2024;84(2):577-588. PMID: 38165576. https://pubmed.ncbi.nlm.nih.gov/38165576/ (확인일: 2026-09-24)
9. Montebello A, et al. Factors predicting cure at one year after administration of radioactive iodine to patients with Graves' disease. Hellenic J Nucl Med. 2025;28(3):196-199. PMID: 41389254. https://pubmed.ncbi.nlm.nih.gov/41389254/ (확인일: 2026-09-24)
10. Liu X, et al. Outcomes of Graves' Disease Patients Following Antithyroid Drugs, Radioactive Iodine, or Thyroidectomy as the First-line Treatment. Ann Surg. 2021;273(6):1197-1206. PMID: 33914484. https://pubmed.ncbi.nlm.nih.gov/33914484/ (확인일: 2026-09-24)
11. Feroci F, et al. A systematic review and meta-analysis of total thyroidectomy versus bilateral subtotal thyroidectomy for Graves' disease. Surgery. 2014;155(3):529-540. PMID: 24230962. https://pubmed.ncbi.nlm.nih.gov/24230962/ (확인일: 2026-09-24)
