---
linear_issue: JHA-81
created: 2026-09-27
source: manual
milestone: cluster-4-tam-sam-pricing
status: done
inputs:
  - 00_legacy_unsorted/GD_TED_market_sizing_report.md
  - 00_baseline_biomni/landscape_v2/soc_outcomes_v2.csv
  - 00_baseline_biomni/landscape_v2/pipeline_assets_v2.csv
  - 00_baseline_biomni/landscape_v2/report_graves_ted_landscape_v2.md
---

# Teprotumumab vs veligrotug 약가 비교

**조사 기준일: 2026-09-27, 미국 우선.** WAC는 제조사가 설정한 도매취득가로 실제 순가격, 보험자 허용액, 환자 본인부담금과 다름. `확인 불가`는 가격이 없다는 뜻이 아니라 공개 공식 자료에서 검증하지 못했다는 뜻임.

## 1. 결론

- **두 제품의 unit price를 동일 적용하면 안 됨.** Viridian CCO가 Fierce Pharma에 밝힌 Lumvoa의 75 kg 환자 기준 WAC는 **약 $450,000/course**이며, 산정 기준은 Tepezza와의 **course-of-therapy parity**임.[9] 이는 5회 Lumvoa 과정 전체를 8회 Tepezza 과정과 유사하게 책정한 value-based positioning이지 vial당 또는 mg당 가격 parity가 아님.
- **보험수가 구조도 동일하다고 볼 수 없음.** Tepezza에는 영구 HCPCS `J3241`과 2026년 4분기 CMS payment limit이 있음. 같은 CMS 파일과 NDC-HCPCS crosswalk에서 Lumvoa/veligrotug 및 NDC `85166-001-01`은 확인되지 않아, Lumvoa의 영구 HCPCS와 CMS 별도 payment limit은 **미확인**임. 코드 부재는 Medicare 비급여 판정이 아니며, CMS도 파일 등재 여부와 coverage 결정을 구분함.[1][2]
- **Anchor 처리:** 당장은 Tepezza FY2025 실매출 $1.903B를 관측 anchor로 유지함. Lumvoa에는 C-grade 공개 WAC signal을 가격 scenario로 반영할 수 있으나, 제품별 HCPCS/CMS payment limit과 누적 매출이 관측되기 전까지 실매출 anchor로 합산하지 않음.

## 2. 미국 가격 및 코드

| 항목 | Teprotumumab-trbw (Tepezza) | Veligrotug-vvze (Lumvoa) | 근거 수준 |
|---|---|---|---|
| FDA 상태 | 승인, TED activity/duration과 무관 | 2026-06-26 승인, TED activity/duration과 무관, BLA 761530 | A, FDA label/approval letter [3][4] |
| 제형 | 500 mg single-dose vial | 500 mg/10 mL single-dose vial, NDC `85166-001-01` | A, FDA label [3][5] |
| 권장 과정 | 10 mg/kg 1회 후 20 mg/kg Q3W 7회, 총 8회 | 10 mg/kg Q3W 5회, 총 5회 | A, FDA label [3][5] |
| 공개 WAC/list price | **출시 WAC $14,900/vial**. 2020년 ICER가 보고한 역사값이며 2026년 현재 WAC로 간주하지 않음 | **약 $450,000/course**, 75 kg 평균 환자 기준. Viridian CCO가 `course of therapy basis`로 Tepezza와 parity라고 설명. 공식 unit price list는 미확인 | 양쪽 C, 2차 자료 [6][9] |
| HCPCS | **J3241**, injection, teprotumumab-trbw, 10 mg | 영구 제품별 코드 **미확인** | A, CMS [1][2] |
| Medicare 2026 Q4 payment limit | **$381.627/10 mg**, coinsurance 20% 표시. 2026-10-01~12-31 적용, 2026 Q2 ASP 기반 | 제품별 payment limit **미확인** | A, CMS [1] |
| 보험 접근 | 지역 단위 일괄 급여 여부는 unresolved, 개별 payer/contractor 판단 필요 | 지역 단위 일괄 급여 여부는 unresolved, 개별 payer/contractor 판단 필요 | 기존 v2 `reimbursement_access`; CMS 주석 [1] |

### 2.1 체중별 dose, vial 및 CMS 산술

- **Tepezza, 70 kg:** 총 투여량 10,500 mg이나 single-dose 500 mg vial을 infusion별로 올림하면 23 vials, 11,500 mg를 개봉함. 역사적 출시 WAC 기준 약 **$342,700**(23 x $14,900)이나 이는 2026년 견적이 아님. 2026 Q4 CMS payment limit 적용 시 투여량만 계산하면 **$400,708.35**(1,050 units), 개봉량 전체를 계산하면 **$438,871.05**(1,150 units)임. 실제 discarded-drug 청구에는 CMS JW/JZ modifier 및 payer 규칙이 적용되므로 두 값 모두 단순 산술이며 환자 본인부담액이 아님.[1][10]
- **Tepezza, 75 kg:** 총 투여량 11,250 mg, infusion별 올림 시 역시 23 vials, 11,500 mg를 개봉함. 따라서 2026 Q4 CMS 개봉량 환산값은 70 kg 예시와 동일한 **$438,871.05**이며, Fierce Pharma가 설명한 약 $450,000 course parity와 방향 및 규모가 부합함. 이는 Lumvoa WAC를 CMS가 정했다는 의미가 아니라 회사의 comparator positioning을 해석하는 보조 검산임.
- **Lumvoa, 70 kg 및 75 kg:** 총 투여량은 각각 3,500 mg 및 3,750 mg이나 두 체중 모두 회당 2 vials, 과정당 10 vials를 개봉함. 보도된 $450,000가 10-vial acquisition cost를 뜻한다면 두 체중의 gross course WAC는 같을 수 있으나, 공식 unit WAC가 없으므로 70 kg 가격으로 단정하지 않음.
- 용량 및 vial 수 차이 때문에 향후 vial당 가격이 같더라도 과정당 약제비는 같지 않음. 폐기량, vial sharing, 계약 할인, site of care, payer policy에 따라 실제 청구 및 순가격이 달라짐.

### 2.2 Lumvoa $450,000 WAC의 산정 기준

#### 공개자료 검색 결과

- Fierce Pharma는 Viridian CCO Tony Casciano를 직접 인용해, 평균 체중 75 kg 환자의 Lumvoa WAC가 $450,000이며 Tepezza와 `course of therapy basis`에서 parity라고 보도함. 기사 자체가 산출한 analyst estimate가 아니라 **회사 임원이 제공한 course-level WAC 설명을 trade press가 보도한 값**임.[9]
- 기준은 infusion 수 비례가 아님. Lumvoa 5회가 Tepezza 8회보다 적더라도 전체 치료과정 가격을 대략 같게 둔다는 상업적 포지셔닝임. 따라서 기존의 `짧은 regimen이므로 더 저렴할 것`이라는 가정은 기각함.
- Viridian 승인 press release와 2026 Q2 Form 10-Q는 immediate launch, payer engagement, insurance support 및 patient assistance를 설명하지만 숫자 가격은 제시하지 않음.[7][8] 즉 $450,000의 공개 근거는 현재 Fierce Pharma의 경영진 인터뷰 보도이며, 공식 manufacturer price sheet나 compendia unit WAC로 교차검증되지는 않음.

#### 75 kg 기준 산술 해석

- FDA label 용량 10 mg/kg을 적용하면 75 kg 환자는 회당 750 mg, 5회 총 **3,750 mg** 투여함.[3]
- Lumvoa는 500 mg single-dose vial이므로 vial sharing이 없으면 회당 2 vials, 과정당 **10 vials**를 개봉함.[3]
- 10 vials의 acquisition cost 기준으로 해석하면 **$45,000/vial**이 역산됨. $450,000을 실제 투여량 3,750 mg로 나눈 **$120/administered mg**는 course 총액을 dose로 나눈 산술 비율일 뿐, single-dose vial의 가격 구조를 설명하는 unit WAC로 사용하면 안 됨. 기사는 package/unit WAC, 폐기분 청구 또는 반올림 규칙을 공개하지 않음.
- 따라서 모델에는 가장 직접적으로 보도된 **$450,000/75 kg course**를 입력하고, $45,000/vial은 `implied, not compendia-verified`, $120/administered mg는 `descriptive ratio only`로 표시함. WAC는 실제 net price, payer payment allowance 또는 환자 본인부담금이 아님.

#### 참고용 시나리오 산정

아래 값은 보도된 $450,000 WAC와 비교하기 위한 **comparator 기반 산술 시나리오**임. 첫 두 행은 Lumvoa 가격 관측치가 아니며 sensitivity 용도로만 사용함.

| 시나리오 | 계산 | 과정당 금액 | Evidence grade | 해석 제한 |
|---|---|---:|---|---|
| Tepezza 역사적 출시 WAC와 vial parity | Lumvoa 10 vials x $14,900 | **$149,000/course** | D, 추론 | 2020년 Tepezza 역사값을 2026년 경쟁제품에 전이한 값. Lumvoa WAC 추정치가 아님 |
| Tepezza 2026 Q4 CMS vial-equivalent와 parity | $381.627/10 mg x 500 mg x 10 vials | **$190,813.50/course** | D, 추론 | CMS payment limit을 Lumvoa에 적용한 가상값. WAC, ASP 또는 Lumvoa Medicare 허용액이 아님 |
| 회사 설명의 course-price parity | Viridian CCO가 밝힌 75 kg course WAC | **약 $450,000/course** | C, 경영진 인용 2차 보도 | 공식 unit price list로 미교차검증, 실제 순가격 아님 [9] |

결론적으로 $450,000은 단순 기사 자체의 추정치가 아니라 회사가 제시한 WAC signal이므로 Lumvoa pricing scenario의 중심값으로 사용할 수 있음. 다만 evidence grade C를 유지하고, unit WAC와 실제 net price는 `NR`로 둠. $149,000 및 $190,813.50은 기존 comparator parity가 실제 회사 포지셔닝을 크게 과소평가했음을 보여주는 보조 sensitivity로만 유지함.

#### 추가 review point

1. **Tepezza 비교가격 시점 불일치:** 확인된 $14,900/vial은 2020년 출시 WAC이고 Lumvoa $450,000은 2026년 signal임. 두 수치를 직접 비교한 할인율 또는 premium 계산은 금지함. 2026 Tepezza unit WAC 확보 필요.
2. **Gross-to-net 미확인:** $450,000은 gross WAC이며 rebates, discounts, patient assistance 및 payer mix가 반영된 net price가 아님. TAM/SAM 매출 계산에는 별도의 gross-to-net sensitivity가 필요함.
3. **Discarded drug 처리:** weight-based single-dose vial 제품은 투여량보다 개봉량이 중요할 수 있음. Medicare JW/JZ 및 commercial payer rules를 확인하지 않은 채 administered mg만 곱하면 과소추정 위험이 있음.
4. **코드와 coverage 분리:** Lumvoa 전용 HCPCS 부재는 noncoverage를 의미하지 않으며, temporary/NOC billing과 payer policy를 별도 추적해야 함.

## 3. 미국 외 확인

| 지역 | Tepezza | Lumvoa | 가격 결론 |
|---|---|---|---|
| EU/EEA | 2025-06-19 허가, 국가별 reimbursement unresolved | 허가/reimbursement unresolved | 공식 list price 미확인 |
| United Kingdom | 2025-05-07 MHRA 허가, 조사 입력 cutoff에서 NICE 진행 중 | 허가/reimbursement unresolved | 공식 list price 미확인 |
| Japan | 2024-09-24 active TED 허가, reimbursement unresolved | 허가/reimbursement unresolved | 공식 약가 미확인 |
| South Korea | MFDS/NEDrug positive product record 미확인, HIRA reimbursement record 미확인으로 **unresolved** | authorization/reimbursement 모두 **unresolved** | 원화 공식 약가 **미확인** |

지역별 상태는 v2의 `soc_outcomes_v2.csv` 및 report 3.1을 유지했음. 공식 포털의 음성 검색 결과를 미승인 또는 비급여의 증거로 바꾸지 않음.

## 4. 추가 승인 IGF-1R 항체

- 미국에서는 조사 기준일 현재 FDA 자료와 v2 승인 자산에서 Tepezza와 Lumvoa 외 추가 승인 IGF-1R antibody를 확인하지 못함.
- `IBI311`은 v2에 Phase 4를 포함한 등록시험 자산으로 존재하지만, 해당 행은 `Highest registered phase`이며 규제 승인 근거가 아님. 중국 승인 및 공식 가격을 이번 공식-source 확인으로 확정하지 못했으므로 추가 가격 anchor에 포함하지 않음. Legacy §5의 `중국 biosimilar` 표현도 현재 입력으로 검증되지 않으므로 답습하지 않음.

## 5. Section 2.3 후속 업데이트

Legacy report는 동결 상태이므로 아래 내용을 Section 2.3 후속 해석으로 사용함.

1. FY2025 Tepezza 매출 $1.903B는 계속 **관측 실매출 anchor**로 사용.
2. Lumvoa는 2026-06-26 승인됐고 75 kg 기준 약 $450,000/course WAC가 경영진 인용 보도로 확인됐으나, 제품별 CMS payment limit과 누적 매출이 아직 검증되지 않은 **미성숙 비교 anchor**로 분리.
3. 모델에서 unit price parity는 사용하지 않음. 가격 scenario에는 회사가 설명한 **course-price parity, $450,000/75 kg course, grade C**를 우선 사용하고, 실제 net price로 오인하지 않음.
4. 향후 업데이트 trigger는 (a) Lumvoa 공식 WAC 또는 유통 가격 공시, (b) HCPCS quarterly update 또는 CMS ASP file 등재, (c) Viridian 분기 제품매출, (d) 미국 외 공식 약가 등재임.

이는 기존 §5 한계 5번의 방향을 유지하면서, 단순히 승인 자산 수를 늘리는 것이 아니라 **검증된 가격/수가/매출이 있는 자산만 정량 anchor에 편입**하는 기준을 추가한 것임.

## 참고문헌

1. CMS. [October 2026 Medicare Part B Payment Limit Files](https://www.cms.gov/files/zip/october-2026-medicare-part-b-payment-limit-files-final.zip), final file 2026-09-17. `J3241`, 10 mg, payment limit $381.627; 파일 주석상 등재 여부는 coverage 판정이 아님.
2. CMS. [October 2026 NDC-HCPCS Crosswalk](https://www.cms.gov/files/zip/october-2026-ndc-hcpcs-crosswalk-final.zip), final file 2026-09-17. Tepezza NDC와 `J3241` 연결 확인.
3. FDA. [LUMVOA prescribing information](https://www.accessdata.fda.gov/drugsatfda_docs/label/2026/761530Orig1s000lbl.pdf), 2026-06.
4. FDA. [LUMVOA BLA 761530 approval letter](https://www.accessdata.fda.gov/drugsatfda_docs/appletter/2026/761530Orig1s000ltr.pdf), 2026-06-26.
5. DailyMed. [TEPEZZA current prescribing information](https://dailymed.nlm.nih.gov/dailymed/drugInfo.cfm?setid=3e6c54a1-cefd-4a5b-a855-ab9f268b6cce), accessed 2026-09-27.
6. Institute for Clinical and Economic Review. *Teprotumumab for Thyroid Eye Disease: Effectiveness and Value*, 2020. 출시 WAC $14,900/500 mg vial을 보고한 2차 평가자료.
7. Viridian Therapeutics. [Form 10-Q for the quarter ended June 30, 2026](https://www.sec.gov/Archives/edgar/data/1590750/000159075026000018/vrdn-20260630.htm), filed 2026-08-06. 미국 commercial launch, payer engagement 및 patient-support 접근을 기술하나 제품 가격은 제시하지 않음.
8. Viridian Therapeutics. [Lumvoa FDA approval press release, Form 8-K Exhibit 99.1](https://www.sec.gov/Archives/edgar/data/1590750/000119312526286273/d164211dex991.htm), 2026-06-26. Immediate launch, payer 협업 및 access-support program을 설명하나 가격은 제시하지 않음.
9. Fierce Pharma. [Viridian set for 1-on-1 vs. Amgen after FDA approval of Lumvoa](https://www.fiercepharma.com/pharma/look-out-amgen-here-comes-viridian-fda-nod-ted-med-lumvoa), 2026-06-29, updated 2026-06-29. Viridian CCO Tony Casciano를 인용해 75 kg 환자 WAC 약 $450,000 및 Tepezza와의 course-of-therapy parity를 보도.
10. CMS. [New JZ Claims Modifier for Certain Medicare Part B Drugs](https://www.cms.gov/files/document/mm13056-new-jz-claims-modifier-certain-medicare-part-b-drugs.pdf), MLN Matters MM13056, 2023. Single-dose container의 discarded amount에 JW, 폐기량이 없을 때 JZ modifier를 사용하는 청구 기준.
