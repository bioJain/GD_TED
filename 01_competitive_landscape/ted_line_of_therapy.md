---
linear_issue: JHA-71
created: 2026-09-24
source: claude-code
milestone: cluster-1-competitive-landscape
status: in-review
inputs:
  - 00_baseline_biomni/landscape_v2/soc_outcomes_v2.csv
  - 00_baseline_biomni/landscape_v2/pipeline_assets_v2.csv
  - 00_baseline_biomni/landscape_v2/report_graves_ted_landscape_v2.md
  - 00_baseline_biomni/epi_soc_run_260914/report_graves_ted_landscape.md
  - 00_legacy_unsorted/GD_TED_report.md
---

# TED 치료 line-of-therapy

> **Data cut:** 2026-09-10. 이 문서는 임상 처방 지침이 아니라, severity/activity/phenotype과 지역별 authorization/access를 분리한 경쟁환경 요약이다. `unresolved`는 공식 근거를 이번 source set에서 확정하지 못했다는 뜻이며, 비승인 또는 비급여를 뜻하지 않는다. 아래 `[N]`은 별도 표시가 없는 한 Biomni v2 참고문헌 번호다.

## 1. 먼저 분기해야 하는 환자 상태

TED는 하나의 직선형 line으로 치료하지 않는다. 치료 전에 EUGOGO severity, activity, 주된 phenotype, 시력 위협 여부를 함께 분류한다. CAS는 초진 7개 항목 중 3점 이상이면 active로 보되, 낮은 CAS만으로 inactive를 확정하지 않는다. EUGOGO severity는 mild, moderate-to-severe, sight-threatening의 3단계다 [135, 139].

| 임상 상태 | 첫 경로 | 다음 분기 | 근거 키 |
|---|---|---|---|
| Mild active | 국소 안구표면 관리, 금연/갑상선기능 정상화 등 risk-factor control, selenium 결핍 지역의 selected selenium | 진행하거나 QoL 영향이 커지면 activity/severity/phenotype 재평가 후 systemic pathway | `SOC-US/EU/UK/KR/JP-TED-MILD-ACTIVE`; [135, 139, 742] |
| Active moderate-to-severe, 즉각적 시력 위협 없음 | IV glucocorticoid(IVGC/IVMP) 기반 또는 지역/phenotype에 따른 approved targeted therapy | 6주 전후 반응 불충분, 불내약, flare, 재발이면 active refractory pathway | `SOC-US/EU/UK/KR/JP-TED-ACTIVE-MODERATE-SEVERE`; [127, 135, 139, 742] |
| Sight-threatening DON/각막 위협 | 아래 line을 건너뛰고 emergency IVMP, 조기 orbital decompression | 1~2주 내 시기능 회복이 불충분하거나 악화하면 urgent decompression | `SOC-US/EU/UK/KR/JP-TED-DON`; [127, 135, 139] |
| Chronic/inactive 잔여 병변 | 안정된 inactive/euthyroid 상태에서 decompression, strabismus, eyelid surgery의 staged rehabilitation | 재활 단계 사이 residual phenotype 평가, 재활성화 시 active pathway 복귀 | `SOC-US/EU/UK/KR/JP-TED-CHRONIC-INACTIVE`; [135, 139, 742] |

## 2. 단계별 line-of-therapy 표

| 단계 | 대상과 치료 | 기간/평가 시점 | 확인된 response/remission 수치 | 놓치는 환자군/미충족 수요 | 실패 시 다음 단계 |
|---|---|---|---|---|---|
| **0. 모든 line의 기반 관리** | 안구 윤활/노출 보호, 금연, thyroid dysfunction 교정, 필요 시 prism 등. Mild active에서는 selenium selenite 100 μg BID 6개월을 고려하되 selenium-insufficient region 중심 | Selenium 6개월 | Legacy RCT(n=159)에서는 QoL/안구 소견/중증 진행이 모두 유의하게 개선(P≤0.01). 다만 본 v2 source set에는 endpoint별 절대 response 비율이 없어 remission 수치로 환산하지 않음 [139]; legacy [44] | Selenium 충분 지역, 임신/소아, 빠르게 진행하는 환자, 뚜렷한 proptosis/diplopia, moderate-to-severe disease를 단독으로 address하지 못함 | 진행/QoL 악화 시 재분류 후 systemic therapy |
| **1. Conventional first-line** | Active moderate-to-severe TED의 inflammation-predominant phenotype: IVMP 0.5 g weekly x 6주 후 0.25 g weekly x 6주, 누적 4.5 g. EUGOGO 경로에서는 mycophenolate sodium 0.72 g/day 24주 병용. 더 심한 diplopia/proptosis에는 고용량 IVMP 단독 대안 | IVMP 12주, mycophenolate 24주. 6주 poor response 시 지속 여부 재평가. 단일 cycle 누적 IVGC는 8 g 이하 | 입력 자료에는 동일 정의의 IVMP 절대 response/remission 비율이 없음. 따라서 수치 미확인으로 명시하며 targeted-therapy trial과 간접 비교하지 않음 [135, 139] | Steroid contraindication/intolerance, hepatic/cardiometabolic risk, steroid-resistant disease, proptosis/diplopia 우세 phenotype, chronic/inactive structural deficit, IV infusion 접근성이 낮은 환자 | 반응/내약성/phenotype 및 지역 access를 재평가해 approved targeted therapy 또는 stage 3 옵션 |
| **2. Approved targeted therapy, 지역/phenotype 기반** | IGF-1R inhibitor. Teprotumumab 또는, 미국에서는 veligrotug. 이는 모든 지역에서 자동으로 IVMP 다음 line이라는 뜻이 아니며 authorization, reimbursement, guideline position을 별도 판단 | Teprotumumab: 10 mg/kg 첫 IV 후 20 mg/kg Q3W x 7, 총 8회/약 21주. Veligrotug: 10 mg/kg IV Q3W x 5, 총 약 12주 | Teprotumumab OPTIC Week 24 PRR 82.9% vs 9.5%, overall response 78.0% vs 7.1%, CAS 0/1 58.5% vs 21.4% [807]. OPTIC-X crossover responder 중 Week 48 PRR 유지 29/32 [809]. Veligrotug THRIVE Week 15 PRR 70.0% vs 5.26%, overall response 66.83% vs 5.26%, diplopia response 59.07% vs 19.89% [829]; initial responder 중 Week 52 PRR 유지 21/30(70%) [829] | 비급여/접근 제한, 소아, 임신, hearing impairment 위험, hyperglycemia/IBD 등 label-specific 위험, class nonresponder. Response는 proptosis/CAS/diplopia endpoint이지 면역학적 cure나 durable off-treatment remission이 아님 | 불충분 반응, flare, 재발 시 primary nonresponse/partial response/post-treatment relapse를 구분해 stage 3 또는 surgery. Teprotumumab selected retreatment cohort는 작아 일반화 제한 |
| **3. 재발/무반응 active disease의 후속 옵션** | 재평가 후 second IVMP course, prednisone+cyclosporine/azathioprine, mycophenolate/기타 immunomodulation, orbital RT+GC, phenotype에 맞는 targeted therapy. GC-resistant active disease에서는 off-label rituximab 또는 tocilizumab 고려 | Regimen은 option별/지역별 상이. 누적 steroid exposure와 감염, HBV, hepatic/metabolic risk를 재평가 | Rituximab RCT NCT00595335: 6개월 CAS 변화 -1.2 vs -1.5, p=0.73; failure 69% vs 75%, p=0.75로 methylprednisolone 대비 우월성 없음 [762]. Legacy steroid-resistant tocilizumab RCT(n=32): Week 16 CAS 2점 이상 감소 93.3% vs 58.8%, CAS<3 86.7% vs 35.2%, exophthalmos -1.5 vs 0.0 mm [legacy 41]. 서로 다른 population/endpoint이므로 직접 순위화하지 않음 | 장기 inactive fibrosis, 고정 diplopia/proptosis, 반복 면역억제 부적합, 감염 고위험, biologic/RT 접근 제한. Rituximab evidence는 상충하고 tocilizumab 대규모 confirmatory RCT는 부족 | Active가 남으면 alternate modality/clinical trial. Inactive residual deficit이면 stage 4. 시력 위협이면 즉시 emergency pathway |
| **4. Chronic/inactive rehabilitation** | 안정된 inactive/euthyroid 상태에서 orbital decompression, 이후 strabismus surgery, 이후 eyelid correction | 안정성 확인 후 staged procedure, 단일 고정 기간 없음 | 염증 response/remission endpoint를 적용하지 않음. 수술 목적은 잔여 functional/cosmetic deficit 교정 [135, 139, 742] | 수술 부적합, activity가 불안정한 환자, systemic inflammation의 재활성화, 전문 수술 접근 제한 | 재활성화 시 active pathway, 안정된 residual deficit은 다음 staged procedure |
| **별도 emergency pathway** | DON: 즉시 고용량 IVMP 0.5~1 g daily x 3일 연속 또는 격일, 필요 시 두 번째 주. 각막 파열은 즉시 수술 | 1~2주 이내 시기능 평가 | 일반 TED composite response를 사용하지 않고 visual acuity/color vision/field/RAPD와 decompression 필요성으로 평가. 입력 자료에 단일 pooled response 비율 없음 [127, 135, 139] | 치료 지연 시 irreversible vision loss. Biologic/RT가 definitive decompression을 지연해서는 안 됨 | 반응 불충분/악화 시 urgent orbital decompression |

### 해석상 핵심

1. **IVMP/selenium은 같은 환자군의 1차제가 아님:** selenium은 주로 recent-onset mild active disease의 supportive option이고, IVMP는 active moderate-to-severe disease의 systemic first-line 축이다 [135, 139].
2. **승인과 치료 순서는 동의어가 아님:** 미국 label의 activity/duration 범위가 넓어도 특정 환자에서 first-line 우위를 자동 확립하지 않으며, EU/UK/Japan의 label 범위와 local guideline/access를 따른다 [728, 729, 731, 735].
3. **재발/무반응을 하나의 endpoint로 합치지 않음:** primary nonresponse, partial response, taper 중 flare, post-treatment relapse, inactive residual deficit은 서로 다른 상태다. 일본 draft에서 추가치료 필요 비율 22~30%가 제시되지만 cross-trial efficacy estimate로 사용하지 않는다 [742].
4. **response와 remission을 구분:** PRR, CAS, diplopia, GO-QOL은 서로 대체할 수 없고, 특정 방문의 response는 durable remission 또는 cure가 아니다. 현재 입력에서 수치가 있는 durability는 selected follow-up subset에 한정된다 [809, 829].

## 3. 승인 표적치료의 지역별 authorization와 reimbursement/access

| 지역 | Teprotumumab authorization | Teprotumumab reimbursement/access | Veligrotug authorization | Veligrotug reimbursement/access |
|---|---|---|---|---|
| US | 승인, TED regardless of activity or duration [728] | unresolved, 개별 payer 확인 필요 | 2026-06-26 FDA 승인, TED regardless of activity or duration [373, 726, 727] | unresolved, 개별 payer 확인 필요 |
| EU/EEA | 2025-06-19 EU marketing authorization, adult moderate-to-severe TED [729, 730] | Member State별, 국가별 unresolved [751] | unresolved, 공식 EMA product record 미확인. 비승인의 증거는 아님 [747] | unresolved |
| UK | 2025-05-07 MHRA 승인, adult moderate-to-severe TED [731, 734] | NHS access unresolved, NICE appraisal in progress [732, 733] | unresolved, 공식 UK product/appraisal record 미확인. 비승인의 증거는 아님 [749] | unresolved [749] |
| South Korea | **unresolved**, 공식 MFDS/NEDrug product record 미확인. 비승인의 증거는 아님 [745] | **unresolved**, 공식 HIRA record 미확인. 비급여의 증거는 아님 [746] | unresolved, 공식 Korean product record 미확인. 비승인의 증거는 아님 [750] | unresolved [750] |
| Japan | 2024-09-24 승인, active TED [735, 736, 737] | unresolved, 공식 reimbursement/price-list locator 미검증 [752] | unresolved, 공식 PMDA/MHLW product record 미확인. 비승인의 증거는 아님 [748] | unresolved [748] |

## 4. 수치 확인표와 evidence boundary

| 치료/질문 | 확인 결과 | 사용 가능한 수치 | 근거 |
|---|---|---|---|
| Selenium duration | 확인 | 100 μg BID, 6개월 | `SOC-US-TED-MILD-ACTIVE`, `SOC-EU-TED-MILD-ACTIVE`; [135, 139] |
| Selenium response/remission | 부분 확인 | legacy RCT에서 주요 outcome P≤0.01, 절대 response/remission 비율은 v2 입력에 없음 | legacy [44] |
| IVMP duration | 확인 | 12주, 누적 4.5 g 표준축, cycle 8 g 이하 | `SOC-EU/KR-TED-ACTIVE-MODERATE-SEVERE`; [127, 135] |
| IVMP response/remission | 미확인 | 본 입력에 비교 가능한 절대 비율 없음 | 입력 gap |
| Teprotumumab response | 확인 | Week 24 PRR 82.9%, overall response 78.0%, CAS 0/1 58.5% | NCT03298867; [807] |
| Teprotumumab durability | 제한적 확인 | OPTIC-X crossover responder 29/32가 Week 48 PRR 유지 | NCT03461211; [809] |
| Teprotumumab population relapse rate | **미확인** | legacy에 언급된 약 25%는 원저 직접 확인 실패, 본 표에 사용하지 않음 | legacy C5 evidence boundary |
| Veligrotug response | 확인 | Week 15 PRR 70.0%, overall response 66.83%, diplopia response 59.07% | NCT05176639; [829] |
| Veligrotug durability | 제한적 확인 | evaluable initial responder 21/30(70%)가 Week 52 PRR 유지 | NCT05176639; [829] |
| Rituximab response | 상충/부정적 RCT 확인 | NCT00595335에서 CAS change와 failure 모두 유의차 없음 | [762] |
| Tocilizumab response | 제한적 확인 | steroid-resistant RCT n=32, Week 16 CAS response 93.3% vs 58.8% | legacy [41] |
| Refractory/relapse 추가치료 부담 | 지역 맥락에서 확인 | 일본 draft 약 22~30%, efficacy estimate 아님 | `SOC-JP-TED-RELAPSED-REFRACTORY`; [742] |

## 5. 단계별 미충족 환자군 요약

| 미충족 환자군 | 현재 경로의 한계 | 필요한 데이터/옵션 |
|---|---|---|
| Steroid-resistant/intolerant active TED | IVMP first-line의 효과/안전성 한계, 후속 option 간 직접 비교 부족 | phenotype-stratified head-to-head, 표준화된 nonresponse 정의 |
| Chronic/inactive이나 수술을 원치 않거나 부적합 | systemic trial evidence와 authorization가 지역별로 다르고 수술 외 durable option 제한 | 장기 active/inactive 별 response, 재치료, 수술 회피 endpoint |
| IGF-1R inhibitor nonresponder/relapser | 작은 selected retreatment cohort 외 population-level relapse/durability 불명확 | 분모가 명확한 장기 추적, flare/relapse 정의 통일 |
| Hearing loss, diabetes, IBD, pregnancy, pediatric 환자 | IGF-1R class의 label-specific risk/근거 공백, steroid 또한 독성 부담 | special-population safety와 대체기전 데이터 |
| DON/각막 위협 | 치료 지연 시 비가역 손상, routine biologic sequence 적용 불가 | 신속한 referral와 decompression access, vision-specific outcome |
| 한국 환자 | Teprotumumab/Lumvoa authorization와 reimbursement 모두 v2에서 unresolved | MFDS/NEDrug 및 HIRA positive official record 재검증 |

## 6. 출처와 추적 가능성

- Regional SoC, regimen, authorization/access: `00_baseline_biomni/landscape_v2/soc_outcomes_v2.csv`의 위 표에 적은 `soc_id`, `source_ids`, `anchor_ids`.
- Trial efficacy/safety/durability: `00_baseline_biomni/landscape_v2/report_graves_ted_landscape_v2.md` 4.2~4.4장과 `reference_v2.md`의 [762], [807], [809], [829].
- Asset identity/status: `00_baseline_biomni/landscape_v2/pipeline_assets_v2.csv`의 Teprotumumab, Veligrotug (Lumvoa), Rituximab, Tocilizumab 행.
- Severity/activity별 EUGOGO pathway: `00_baseline_biomni/epi_soc_run_260914/report_graves_ted_landscape.md` 4.2~4.3장.
- Legacy 보조 수치: `00_legacy_unsorted/GD_TED_report.md` C2/C3/C5의 [41], [44]. Legacy 번호는 `_shared/GD_TED_reference.md`를 따르며 Biomni v2 번호와 혼용하지 않았다.

## 7. QA 결론

- [x] 1차/승인 표적치료/재발 또는 무반응 옵션을 단계별로 정리함.
- [x] Mild, active moderate-to-severe, sight-threatening, chronic/inactive를 선분기함.
- [x] 각 단계의 미충족 환자군을 명시함.
- [x] Duration/response/durability 수치의 확인, 부분 확인, 미확인을 구분함.
- [x] 모든 제시 수치에 source number와 trial 또는 `soc_id`를 연결함.
- [x] Authorization와 reimbursement/access를 별도 열로 유지하고 한국 status를 unresolved로 보존함.
- [x] 가운뎃점을 사용하지 않고 마케팅 표현과 근거 없는 cross-trial ranking을 배제함.
