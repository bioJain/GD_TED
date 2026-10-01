---
linear_issue: JHA-86
created: 2026-10-01
source: claude-code
milestone: cluster-6-deck
status: draft
style: report-deck-style v0.4
data_cut: 2026-09-10 (frozen registry) / 2026-09-24~2026-10-01 (cluster 재검증)
inputs:
  - 00_legacy_unsorted/GD_TED_deck_outline_260914.md
  - 00_legacy_unsorted/GD_TED_report.md
  - 00_legacy_unsorted/GD_TED_market_sizing_report.md
  - 01_competitive_landscape/gd_line_of_therapy.md
  - 01_competitive_landscape/ted_line_of_therapy.md
  - 01_competitive_landscape/class_limitation_matrix.md
  - 01_competitive_landscape/moa_phase_matrix_extended.md
  - 01_competitive_landscape/addressable_population_crosscheck.md
  - 02_ted_fcrn_strategy/fcrn_entry_strategy_ir_review.md
  - 02_ted_fcrn_strategy/placebo_competitive_summary.md
  - 03_mechanism_deepdive/tshr_igf1r_crosstalk_deepdive.md
  - 03_mechanism_deepdive/igf1r_class_effect_ae.md
  - 03_mechanism_deepdive/igf1r_autoantigen_review.md
  - 03_mechanism_deepdive/orbital_fibroblast_igf1r_maturity.md
  - 03_mechanism_deepdive/r1b_asset_identification.md
  - 04_tam_sam_pricing/tam_sam_revision.md
  - 04_tam_sam_pricing/teprotumumab_veligrotug_pricing.md
  - 05_etpd_molecular_design/benchmark_spec_deepdive.md
  - 05_etpd_molecular_design/tshr_shedding_rate.md
  - _shared/deck_style.md
---

# GD/TED report deck outline

> 이 문서는 슬라이드 자체가 아니라 **렌더링 전 outline**이다. report-deck-style v0.4의 outline 포맷을 따르며, 승인 후 pptx 또는 Slides로 렌더링한다. 모든 내용은 repo 자료만을 근거로 하며 신규 사실 수집은 수행하지 않았다. 공백은 숨기지 않고 슬라이드 안에 명시한다.

---

## 0. 덱 메타

| 항목 | 값 |
|---|---|
| deck_short_title | GD/TED Landscape & eTPD |
| date | 2026-10-01 |
| audience | 내부 의사결정 회의(연구/전략), 발표자 없이 단독 열람 |
| question | GD/TED의 치료 현황과 경쟁 지형에서 eTPD(TSAb-selective extracellular degradation)가 들어갈 자리가 있는가, 있다면 어느 적응증과 어느 환자군인가 |
| language | 한국어 본문, 영어 기술 용어 유지 |
| length_target | 본문 49 + Appendix/Sources 4 = 53 slides |
| as-of 규칙 | frozen registry cut 2026-09-10을 기본으로 하고, cluster 재검증(2026-09-24~10-01) 결과가 다르면 재검증본 우선. 두 날짜를 source line에 병기 |
| evidence 규칙 | A 동료심사/규제문서/완료시험 primary endpoint, B 회사 공시, C 2차 자료, D 추론/추정. 슬라이드 footer는 그 슬라이드의 최저 등급 |

### 미완료 영역 표기 원칙

JHA-85(clone competitiveness 평가기준), JHA-88(eTPD 분자 스펙 초안)은 2026-10-01 기준 미착수다. 해당 내용에 의존하는 슬라이드(S6-4, S6-5)는 결론을 쓰지 않고 **결정 대기 변수와 판정 gate**만 제시하며, 각 슬라이드 하단에 `미확정 - JHA-85/88 진행 중` 표기를 둔다.

---

## 1. Key Takeaways

### Key Takeaways (1/3): 지형 - 두 질환의 미충족은 서로 다른 축에 있다

- **GD의 공백은 durability다. ATD는 복용 중 조절만 하고 RAI/수술은 자가면역이 아니라 hormone source를 없앤다** (→ slide 17, 18) [A]
  - ➢ MMI 통상기간 투여 후 **84개월 relapse 56%**, 장기투여군 **17%**(단일 RCT, n 제한)
  - ➢ RAI 1년 thyroid-source control **81%**, 그중 **61.8%가 hypothyroidism**으로 replacement 필요
  - ➢ 승인된 disease-modifying GD 약물은 **0건**
- **TED의 공백은 phenotype과 durability다. IGF-1R 억제가 proptosis를 바꾸지만 고정 deficit과 재발은 남는다** (→ slide 22, 24) [A]
  - ➢ Teprotumumab OPTIC Week 24 **PRR 82.9% vs placebo 9.5%**
  - ➢ 같은 자산의 장기 성적이 시험 추적과 real-world에서 갈림: pooled Week 72 proptosis response **38/56**, 독립 단일기관 series는 initial responder **17명 중 8명(47%) reactivation**
- **두 질환을 한 class가 동시에 해결한다는 근거는 없다** (→ slide 30) [B]
  - ➢ Efgartigimod는 **GD Phase 3 active / TED Phase 3 terminated**로 적응증별 운명이 갈림

### Key Takeaways (2/3): 기회 - TSAb 선택적 제거의 적합도는 GD에서 높고 TED에서 미확정

- **TSAb는 GD에서 확립된 driver, TED에서는 proposed co-driver다** (→ slide 12, 14) [A]
  - ➢ TSHR 유전자면역만 TED 동물모델을 재현하고 **IGF-1R 면역화는 재현하지 못함**
  - ➢ TSHR-IGF-1R crosstalk의 분자배치는 ARRB1 scaffold와 직접결합 두 모델이 병존하는 **proposed** 상태
  - ➢ 2025년 두 독립 코호트의 혈청 anti-IGF-1R 항체는 **억제/보호 방향**으로 보고되어 IGF-1R 독립 자가항원 가설을 지지하지 않음
- **mechanism coverage는 GD 약 90-95%, TED는 serology proxy 약 90%이나 임상 coverage는 정량 불가** (→ slide 41, 42) [D]
  - ➢ GD mechanism SAM 단순환산 FLOOR **$2.80B-$2.96B** E, PREMIUM **$4.54B-$4.79B** E
  - ➢ TED는 response-based haircut이 없어 **금액 SAM 제시 보류(NR)**
- **비선택적 IgG 제거는 TED에서 두 번 실패했다. 이것이 선택적 제거의 가설을 지우지는 않는다** (→ slide 29) [A]
  - ➢ Batoclimab ASCEND GO-2 전 용량 **primary 미유의**, efgartigimod UplighTED 2건 **interim futility 종료**

### Key Takeaways (3/3): 우리 판단 - 진입은 GD 우선, 승부처는 선택성 입증

- **Our view: eTPD의 1차 적응증은 GD, TED는 selective depletion이 structural endpoint를 움직인다는 근거가 나온 뒤 검토 대상이다** (→ slide 44) [D]
- **Benchmark는 FcRn이 아니라 MER511과 LCA-0321이다. 둘 다 임상 결과 전이고 공개 spec은 patent candidate 수준이다** (→ slide 46) [B]
  - ➢ MER511은 WO2025030009A1의 TSHR ectodomain/FcγRIIB candidate를 공개하나 **final construct 미특정**
  - ➢ LCA-0321은 WO2025207934A1 example에서 코드가 명시되고 mouse 4시간 serum anti-TSHR **70.5% clearance**를 보고
- **설계 선행조건 하나가 아직 비어 있다. TSHR ectodomain shedding rate는 수치가 확인되지 않았다** (→ slide 45) [A]
  - ➢ 사람 in vivo shedding rate, soluble A-subunit 반감기, 재현된 혈중 농도 **모두 미확인**
  - ➢ `낮다`로 전제하지 않고 **wide sensitivity range + empirical gate**로 처리

---

## 2. Contents

| # | 섹션 | 한 줄 결론 |
|---|---|---|
| S1 | 질환과 환자 | GD와 TED는 연동되지만 endpoint가 다른 두 질환이다 |
| S2 | 병리기전 | TSHR이 유일한 확립 autoantigen이고 IGF-1R은 증폭 branch다 |
| S3 | 치료 현황 | 모든 현행 class가 control을 제공하고 durability를 남긴다 |
| S4 | 파이프라인과 경쟁 | IGF-1R은 TED에 밀집, GD는 IgG 제거 축으로 재편 중이다 |
| S5 | 시장과 약가 | TAM range는 넓고 price anchor는 course 단위로만 공개됐다 |
| S6 | eTPD 포지셔닝 | GD 우선 진입이 타당하나 선택성과 shedding이 미결 gate다 |

---

## 3. 섹션별 슬라이드

### S1 divider (slide 6) — 질환과 환자

> 결론: TED는 GD에 동반되지만 평가 endpoint와 치료 목표가 분리된다.

| # | Title (assertion) | Archetype | Exhibit banner | Evidence | Source(s) | Devices/notes |
|---|---|---|---|---|---|---|
| 7 | TED의 약 90%는 GD 맥락에서 발생하나 GD 없이 발생하는 TED가 최대 10% 남는다 | T6 | 그림 1. GD-TED 관계와 발현 시점, 문헌 종합 | A | legacy report A1/A3, legacy outline slide 3 | **구조 레벨 그림 슬롯 1**: 벤 다이어그램 + 시간축(hyperthyroidism 1년 이내 TED 동반 61%, TED 선행 약 20%) |
| 8 | GD 유병은 지역별로 자릿수가 다르고 7MM 개별국가 수치는 학술근거로 확보되지 않았다 | T4 | 그림 2. GD prevalence/incidence, 확인 가능한 지역만, as of 2026-09-14 | A/C | legacy report A2, addressable crosscheck 5.1 | 중국 성인 450/100,000, 한국 NHIS 40세 이상 4.6/10,000 PY. **미확보 callout**: DE/FR/UK/IT/ES 개별 수치는 상업 forecast만 존재하여 채택 안 함 |
| 9 | TED는 GD 환자의 약 40%에서 보고되지만 중증 비율은 23%에 그친다 | T7 | 그림 3. TED 동반률과 중증도 분포, pooled 연구 기준 | A | legacy report A2/A3 | 4패널: pooled 40%(57개 연구/26,804명), 지역 Europe 38%/Asia 44%/N.America 27%/Oceania 58%, 중증도 77/22/1%, Olmsted incidence 여 16.0 남 2.9/100,000/yr |
| 10 | GD에는 공식 staging이 없고 TED만 CAS와 EUGOGO로 활동성과 중증도를 이원 평가한다 | T5 | 표 1. GD/TED 진단과 병기 체계 대조 | A | legacy report A5/A6, ted_line_of_therapy 1절 | CAS 7점(초진)+3점(추적)=10점, CAS≥3 active. TRAb bioassay vs binding assay **9.4% 불일치** 각주 |

### S2 divider (slide 11) — 병리기전

> 결론: TSHR이 primary autoantigen이고 IGF-1R은 자가항원이 아니라 증폭 경로다.

| # | Title (assertion) | Archetype | Exhibit banner | Evidence | Source(s) | Devices/notes |
|---|---|---|---|---|---|---|
| 12 | TSHR 유전자면역만 TED 모델을 재현한다. IGF-1R 면역화는 재현하지 못한다 | T6 | 그림 4. GD 병인 핵심 회로, TSAb-TSHR-Gs-cAMP | A | igf1r_autoantigen_review 2.2, legacy B3 | **조직 레벨 그림 슬롯 2**: 갑상선 조직과 안와 조직의 TSHR/IGF-1R 상대 발현 대비 |
| 13 | 안와 섬유모세포의 두 분화 운명 중 IGF-1R 근거는 adipocyte 쪽만 B, myofibroblast 쪽은 C다 | T11 | 표 2. OF 분화경로별 IGF-1R evidence grade, 2026-09-27 검색 기준 | A | orbital_fibroblast_igf1r_maturity | **세포 레벨 그림 슬롯 3**: Thy-1+/Thy-1- 분기 도식 + grade 뱃지. 3컬럼(경로/직접 human in vitro/in vivo) |
| 14 | TSHR-IGF-1R crosstalk는 기능적으로 지지되지만 분자배치는 세 가설이 경쟁 중이다 | T6 | 그림 5. 경쟁가설 3종의 signaling chain | A | tshr_igf1r_crosstalk_deepdive 3-5절, 8절 panel spec | **signaling 레벨 그림 슬롯 4**: 3-panel(ARRB1 scaffold / ECD 직접결합 / 항체가설 반박). 실선=perturbation 지지, 점선=proposed, 적색 X=근거 부족. legend 필수 |
| 15 | IGF-1R 자가항체는 존재하나 방향은 자극이 아니라 억제로 보고됐다 | T4 | 그림 6. 혈청 anti-IGF-1R 항체와 GO 중증도, 2025년 독립 2개 코호트 | A | igf1r_autoantigen_review 2.1 | Pisa n=147: non-GO 29.3 vs GO 19.8 ng/mL, P=0.005. Katowice n=47+20: sight-threatening군이 non-TO군보다 유의하게 낮음, P=0.004. **Our view 박스**: 독립 섹션 신설 불요, B4 서술 보강으로 충분 |
| 16 | 같은 crosstalk라도 thyrocyte는 NIS/TPO/TG, OF는 HA로 출력이 갈린다 | T5 | 표 3. 세포유형별 receptor 비율과 출력 | A | tshr_igf1r_crosstalk_deepdive 6절 | HA를 adipogenesis/fibrosis의 대리변수로 쓰지 말 것을 각주로 명시 |

### S3 divider (slide 17) — 치료 현황 (심층)

> 결론: 현행 치료는 control을 제공하고 durability와 phenotype을 남긴다.

| # | Title (assertion) | Archetype | Exhibit banner | Evidence | Source(s) | Devices/notes |
|---|---|---|---|---|---|---|
| 18 | GD 치료는 3단계지만 2차는 ATD 뒤에만 오는 것이 아니라 초기 선택지이기도 하다 | T5 | 표 4. GD line-of-therapy, ATA 2016/ETA 2018 기준 | A | gd_line_of_therapy 2절 | 5열: 단계/진입조건/치료와 기간/평가 endpoint/미충족. MMI 12-18개월, 지속 고 TRAb 시 추가 12개월 |
| 19 | 세 modality의 숫자는 같은 endpoint가 아니다. relapse 2.41%와 56%를 나란히 두면 안 된다 | T4 | 그림 7. GD modality별 결과와 endpoint 정의, 연구별 | A | gd_line_of_therapy 3절, 6절 | 좌: 수평 막대(ATD 84개월 relapse 56% vs 17%; RAI 1년 control 81%, hypothyroid 61.8%; 수술 relapse 2.41% vs RAI 19.53% vs ATD 75.60%). 우: endpoint taxonomy 5행 박스. **적색 점선 1개**: thyroid-source control ≠ autoimmune remission |
| 20 | 특수 환자군에서 표준 경로가 먼저 끊긴다. 임신, 소아, active TED 동반이 대표적이다 | T5 | 표 5. GD 특수 환자군과 경로 이탈 | A | gd_line_of_therapy 4절 | 임신 1분기 PTU/이후 MMI, RAI 금기; 5세 미만 RAI 회피; active/severe TED에서 RAI 회피. 지역별 ATD duration은 US/EU/UK/KR/JP 공통 12-18개월 |
| 21 | TED는 직선형 line이 아니다. 치료 전에 severity, activity, phenotype, 시력위협을 먼저 분기한다 | T11 | 표 6. TED 환자 상태별 첫 경로, EUGOGO/지역 guideline | A | ted_line_of_therapy 1절 | 4컬럼(mild active / active moderate-to-severe / sight-threatening DON / chronic inactive), 동일 행 라벨(첫 경로, 다음 분기, 실패 시) |
| 22 | TED 1차는 IVMP 누적 4.5g, 승인 표적치료는 자동으로 그 다음 line이 아니다 | T5 | 표 7. TED line-of-therapy 0-4단계와 emergency pathway | A | ted_line_of_therapy 2절 | IVMP 0.5g x6주 후 0.25g x6주, cycle 8g 이하. 4.5g RCT 3개월 composite response 77% vs oral 51%. Teprotumumab 8회/약 21주, veligrotug 5회/약 12주 |
| 23 | 승인은 전국 급여와 동의어가 아니다. 한국은 authorization과 reimbursement 모두 unresolved다 | T5 | 표 8. 승인 IGF-1R 치료의 지역별 authorization vs access, as of 2026-09-10 | A/C | ted_line_of_therapy 3절 | 2x5 매트릭스(teprotumumab/veligrotug × US/EU/UK/KR/JP). **범례 필수**: `unresolved`는 비승인/비급여의 증거가 아님. US 2026-06-26 veligrotug 승인, EU 2025-06-19, UK 2025-05-07, JP 2024-09-24 |
| 24 | response는 remission이 아니다. teprotumumab 장기 성적은 추적 집단에 따라 17.9%와 47%로 갈린다 | T7 | 그림 8. 반응과 지속성의 분모 비교, 시험 추적 vs 독립 real-world | A | ted_line_of_therapy 4절 | 4패널: OPTIC Week 24 PRR 82.9% vs 9.5% / pooled Week 72 proptosis response 38/56 / 최종 dose 후 99주 내 추가 TED 치료 19/106(17.9%) / 단일기관 n=21 중 initial responder 17명 중 8명(47%) reactivation. 각 패널에 n과 정의 병기 |
| 25 | 8개 class 중 어느 것도 control, phenotype, durability, 안전성을 동시에 충족하지 않는다 | T5 | 표 9. GD/TED class별 핵심 한계, 2026-09-29 기준 | A/D | class_limitation_matrix | 8행(ATD/RAI/수술/IVMP/IGF-1R/FcRn/TSHR 직접차단/TSAb-IgG sweeping). 근거수준 열에 색 scale + 범례. eTPD 행은 `낮음/가설`로 표기하고 임상 자산 없음을 명시 |

### S4 divider (slide 26) — 파이프라인과 경쟁 (심층)

> 결론: TED는 IGF-1R에 밀집하고 GD는 IgG 제거 축으로 재편 중이며, 적응증을 섞으면 판정이 틀린다.

| # | Title (assertion) | Archetype | Exhibit banner | Evidence | Source(s) | Devices/notes |
|---|---|---|---|---|---|---|
| 27 | 자산이 아니라 자산 x 적응증으로 세야 지형이 보인다 | T5m | 표 10. MoA class x indication-specific 개발단계 통합 매트릭스, registry cut 2026-09-10 | A | moa_phase_matrix_extended 2절 | 14행(class) x 5열(Approved/RR, P3, P2, P1, PC). 셀에 `GD P2 / TED P1` 병기. category tint + public/private 범례 |
| 28 | Highest Status를 그대로 쓰면 efgartigimod는 TED 자산으로 잘못 분류된다 | T4 | 그림 9. indication-specific 재판정으로 분류가 바뀐 자산 | A | moa_phase_matrix_extended 2절, 6절 | 좌: before/after 비교 4건(efgartigimod GD P3 유지/TED 제외, rilzabrutinib CSV `Active TED`→GD P2 교정, KHN939/SCTT11 IGF-1R→표적 미공개, MER511 receptor 길항→AAb 제거). 우: 판정 규칙 4줄 |
| 29 | placebo 대비 재현된 성공은 IGF-1R 축에 몰려 있고, 다른 면역 class는 일관되지 않는다 | T5 | 표 11. TED placebo-controlled 주요 결과, 결과 공개 25건 기준 | A | placebo_competitive_summary 2.1 | 12행. 성공/부분성공/실패를 색으로 구분하고 범례. OPTIC 82.9 vs 9.5, THRIVE 70.0 vs 5.26, THRIVE-2 57.28 vs 8.22, chronic TED -2.41 vs -0.92 mm, linsitinib 150mg 51.7 vs 18.8(75mg P=0.090), SatraGO-1 49.0 vs 31.2 P=0.0715(실패) vs SatraGO-2 52.9 vs 23.4 P=0.0011(성공), batoclimab 전 용량 미유의, secukinumab 0/14 vs 0/14, LASN01 PRR 차이 없음/CAS P=0.028, UplighTED 수치 미공개. **cross-trial 비교 금지 각주** |
| 30 | 같은 분자, 다른 적응증. satralizumab과 efgartigimod가 한 class 결론을 막는다 | T4 | 그림 10. 적응증/시험별로 갈린 동일 자산 결과 | A | placebo_competitive_summary 3.2/3.3, fcrn_entry_strategy_ir_review 1절 | 좌: satralizumab replicate Phase 3 쌍(실패/성공) 막대. 우: efgartigimod TED terminated vs GD Phase 3 recruiting. **적색 점선 없음**(이미 slide 19에서 1회 사용) |
| 31 | 이 시험들의 placebo는 SoC add-on이 아니다. 대부분 matched inactive infusion이다 | T5 | 표 12. 주요 TED 시험의 placebo arm 실제 투여물과 공통 background | A | placebo_competitive_summary 2.3 | 15행. `normal saline` 명시 시험(teprotumumab Ph2/OPTIC)과 조성 미기재를 구분. placebo PRR가 9.5%(OPTIC), 18.8%(linsitinib), 31.2%(SatraGO-1)로 갈리는 점을 commentary에 |
| 32 | 중단 17건 중 efficacy futility는 4건이다. 중단을 실패로 읽으면 지형을 과소평가한다 | T5 | 표 13. TERMINATED/WITHDRAWN/SUSPENDED 17건 전수와 사유 | A | placebo_competitive_summary 5절 | 사유를 efficacy futility / recruitment / funding / drug access / commercial / preliminary efficacy 확인으로 분류한 범주 fill + 범례 |
| 33 | TED 승인 3건은 모두 IGF-1R이고 Phase 3 3건도 같은 축이다. 차별화는 제형과 population에서 일어난다 | T5 | 표 14. IGF-1R 계열 자산별 투여 regimen, population, 상태 | A | moa_phase_matrix_extended 3.2, ted_line_of_therapy 2절 | Teprotumumab(A), IBI311(A 중국), Veligrotug(A 미국), Linsitinib/MHB018A/VRDN-003(P3), AMG 732/NTB003(P2), IBI3031(P1 dual) |
| 34 | 반복 관찰되는 class 신호는 muscle spasm, 청각, 혈당 셋이고 자산별 특이 신호는 따로 있다 | T5 | 표 15. IGF-1R 계열 AE 비교, 시험별 관찰기간 상이 | A | igf1r_class_effect_ae 2절 | 7행. muscle spasm teprotumumab 41.5%, veligrotug 45.3%/44.5%, linsitinib 6.7-10.3%. 청각은 단일 PT 아님을 각주(hypoacusis 9.8%, tinnitus 12.0%, ear discomfort 12.0%). linsitinib 특이 GI/transaminase. **`미보고`≠0 범례 필수** |
| 35 | FcRn의 GD 선택은 기전 논리이고, 상업 논리를 명시한 곳은 Immunovant뿐이다 | T4 | 그림 11. FcRn 개발사의 GD/TED 진입 논리, 공개 공시 기준 | B | fcrn_entry_strategy_ir_review 3절, 6절 | 좌: 2x2(기전 명시 여부 x 상업 논리 명시 여부)에 Immunovant/argenx 배치. 우: 근거 수준 표. **Our view 박스**: GD 진입을 gMG/CIDP 처방기반 재사용으로 읽는 해석은 공시와 불일치 |
| 36 | Spotlight - Immunovant: imeroprubart는 hormone control이 아니라 drug-free remission을 겨냥한 설계다 | T12 | 표 16. Immunovant GD 프로그램의 설계와 endpoint | A/B | fcrn_entry_strategy_ir_review 2절, 4절 | fact 박스: batoclimab=IMVT-1401, imeroprubart=IMVT-1402(별개 분자), batoclimab 전 적응증 중단. 데이터: GD POC Week 24 composite 68.8%, 순수 정상화 53.1%, off-ATD 31.3%(n=32 단일군). 설계: NCT06727604 26주 후 placebo 전환, NCT07018323 2 dose vs placebo. **Our view**: 68.8%만 인용하면 POC 효능 과대평가 |
| 37 | Spotlight - argenx: TED에서 실패한 기전으로 GD에 다시 들어갔고 공개된 선택 논리는 기전까지다 | T12 | 표 17. argenx TED/GD 프로그램 대조 | A/B | fcrn_entry_strategy_ir_review 3.2, NCT07570316 | fact 박스: UplighTED 2건 interim futility 종료, safety 사유 아님. GD Phase 3 VitaliThy(NCT07570316) recruiting, n=230, primary는 Week 24 euthyroid off-ATD, secondary에 TRAb seronegativity. **Our view**: 상업 논리는 공시에서 확인되지 않으며 추론으로만 표기 |
| 38 | TSHR/자가항체 축은 전부 P1 이하이고 유일한 P3는 선택적이지 않은 pan-IgG 제거다 | T5m | 표 18. TSHR/자가항체 표적 자산의 선택성과 단계 | A/B | moa_phase_matrix_extended 2/3.1, benchmark_spec_deepdive | 2축: 선택성(pan-IgG / anti-TSHR AAb 선택 / receptor 직접차단) x 단계. BHV-1300(GD P3, pan-IgG), MER511(GD P1), LCA-0321(GD/TED P1), BHV-1440(PC), GenSci098(GD P2/TED P1), K1-70(관찰목록), IBI3031(TED P1 dual) |
| 39 | CD40L은 TED에서 자가항체를 낮췄지만 임상 효과로 이어지지 않아 중단됐다 | T4 | 그림 12. Lu AG22515 TED 프로그램 경과, 2024-09~2026-08 | B/C | r1b_asset_identification | 타임라인: Phase 1a 완료 2023-08 → Phase 1b 개시 2024-09(NCT06557850, 단일군 비맹검, 실제 등록 20명) → 중간신호 2025-11(proptosis 약 2.06mm 감소, TRAb 저하) → 2026-08-19 TED 적응증 중단. **Considerations 박스**: 단일군이므로 인과 확정 불가, TRAb 감소는 distal PD biomarker. 교훈 - autoantibody 감소가 structural endpoint를 보장하지 않음 |

### S5 divider (slide 40) — 시장과 약가

> 결론: TAM range는 scope 이질성이 크고, 가격 anchor는 course 단위로만 공개됐다.

| # | Title (assertion) | Archetype | Exhibit banner | Evidence | Source(s) | Devices/notes |
|---|---|---|---|---|---|---|
| 41 | GD top-down TAM은 약 $3.11B에서 $5.04B, TED는 $4.53B에서 $8.09B이나 원자료 범위가 32배 벌어진다 | T4 | 그림 13. GD/TED TAM FLOOR-PREMIUM과 원자료 분산, 상업 report 기준 | D | tam_sam_revision 0절, 1.2 | 좌: FLOOR/PREMIUM 수평 막대 + 원자료 점. 우: 주의 3줄(TED base 범위 약 32.4배, $8.09B는 scope-adjusted 대표값, GD+TED 합산 금지). 모든 수치에 **E 접미** |
| 42 | TSAb coverage는 GD에서 90-95%로 환산 가능하고 TED에서는 금액 환산을 보류해야 한다 | T7 | 그림 14. mechanism SAM과 therapy-line SAM, 두 축 분리 | D | tam_sam_revision 3절, 4.3/4.4 | 4패널: GD serology 90-95%(3세대 TSI sensitivity 93.3%, TRAb 88.9%) / GD mechanism SAM $2.80-2.96B E, $4.54-4.79B E / TED serology proxy 90%이나 실질 coverage NR / 미국 GD post-ATD 비관해-재발 연 2.48만/3.54만/4.06만 명 E와 TSAb 교집합 2.23만-3.85만 명 E. **패널당 30 단어 이하** |
| 43 | Lumvoa의 $450,000은 vial 가격이 아니라 course parity다. unit price를 동일 적용하면 안 된다 | T5 | 표 19. Tepezza vs Lumvoa 가격과 코드, as of 2026-09-27 | A/C | teprotumumab_veligrotug_pricing | 행: FDA 상태, 제형, 권장 과정(8회 vs 5회), 공개 WAC, HCPCS(J3241 vs 미확인), CMS 2026 Q4 payment limit($381.627/10mg vs 미확인). Tepezza FY2025 매출 $1.903B를 관측 anchor로 표기. **$450,000은 grade C 경영진 인용 보도**임을 각주 |

### S6 divider (slide 44) — eTPD 포지셔닝

> 결론: GD 우선 진입이 타당하나 선택성과 shedding이 미결 gate다.

| # | Title (assertion) | Archetype | Exhibit banner | Evidence | Source(s) | Devices/notes |
|---|---|---|---|---|---|---|
| 45 | 현행 class와 후기 pipeline을 모두 합쳐도 7개 환자군이 남는다 | T5h | 표 20. 환자 상태 x class coverage map, frozen cut 2026-09-10 | A/D | addressable_population_crosscheck 1절, 3절 | 환자상태 10행 x 판정(부분 포괄/조건부/durability/biomarker/경로/교차적응증). 우선 잔여군 2개(ATD 불응-재발 GD, chronic/inactive TED)에 **적색 점선 1개**. 범례: `잔여`는 치료 부재가 아니라 핵심 목표 미충족 |
| 46 | TSAb 제거 설계의 선행조건 하나가 비어 있다. TSHR shedding rate는 수치가 없다 | T6 | 그림 15. cargo 선택과 soluble antigen sink, 확인/미확인 구분 | A | tshr_shedding_rate | 좌: 도식(membrane TSHR / shed A-subunit / circulating TSAb) 위에 확인(실선)과 미확인(점선) 표기. 우: 미확인 4항목(사람 shedding 분율, production/clearance rate, 반감기, 재현된 혈중 농도). **Considerations 박스**: `낮다`로 전제하지 않고 wide sensitivity range + spike-in assay gate로 처리 |
| 47 | Benchmark는 MER511과 LCA-0321이며 공개된 것은 patent candidate이지 최종 spec이 아니다 | T5 | 표 21. 경쟁/benchmark 분자 공개 spec 대조, 검색 2026-09-27/10-01 | A/B | benchmark_spec_deepdive | 8행 x 5열(construct/affinity/developability/human data/근거수준). K1-70 Ka 4x10^10 L/mol(apparent KD 약 25 pM), GenSci098 EC50 1.11 nM, cAMP IC50 2.3 nM, LCA-0321 mouse 70.5% clearance, efgartigimod 총 IgG 평균 75% 감소. **`검색 범위에서 미확인`과 `비공개 명시`를 별도 기호로 구분** |
| 48 | FcRn 대비 차별화는 선택성에서만 나온다. 그 선택성을 입증할 gate는 아직 정의 중이다 | T11 | 표 22. FcRn 억제 vs TSHR 직접차단 vs TSAb 선택 제거, 동일 행 비교 | A/D | class_limitation_matrix, benchmark_spec_deepdive, tshr_igf1r_crosstalk_deepdive | 3컬럼 동일 행 라벨(표적/보존해야 할 것/확인된 liability/필요 입증). FcRn=보호 IgG 동반 감소와 rebound, TSHR 직접차단=정상 TSH signaling 차단(K1-70 rat/monkey T3/T4 저하, Phase 1 고용량 L-thyroxine 보조), TSAb 선택 제거=polyclonal epitope 이질성. **미확정 - JHA-85 진행 중** 표기 |
| 49 | 분자 스펙 확정 전에 결정해야 할 변수는 다섯이고 현재 답이 있는 것은 없다 | T8 | 표 23. eTPD 설계 결정 대기 변수와 판정 gate | D | benchmark_spec_deepdive 'Proposed JHA-88 design/assay gates', tshr_shedding_rate | 3열(변수 / 현재 상태 / 판정 gate): cargo binding, native TSH signaling 보존, Fc routing, selectivity 비율, human PD/durability. 모든 행 `미확정`. **Considerations 박스**: 본 슬라이드는 결론이 아니라 JHA-85/88 산출물의 입력 명세 |

---

## 4. 마무리 슬라이드

| # | Title | Archetype | 내용 | Evidence |
|---|---|---|---|---|
| 50 | Scenarios: GD Phase 3 두 축의 결과가 eTPD의 진입 조건을 바꾼다 | T8 | 3컬럼(bear/base/bull) x 3행(가정 / 결과 / 신호). bear=FcRn/pan-IgG가 GD에서 durable remission을 입증 → 선택성만으로는 차별화 불충분. base=biochemical control은 보이나 off-treatment durability 미흡 → 선택적 제거의 공간 유지. bull=broad IgG 제거가 안전성/rebound로 제약 → 선택성 가치 상승. 모든 셀 hedged 문장 | D |
| 51 | Catalysts: 2026년 4분기부터 TED/GD 양쪽에서 판정이 나온다 | T9 | 6열(Company/Agent/Target/Indication/Potential catalyst/Est. timing). satralizumab 규제 결정 예정 2026-10-15, Lumvoa 공식 HCPCS/CMS 등재, imeroprubart GD Phase 2 readout, VitaliThy Phase 3 primary completion 2028-06, MER511 NEXUS 결과. 모든 시점에 **E**. 고영향 행만 pale-yellow + 범례 | B/C |
| 52 | Limitations: 이 자료가 답하지 못하는 9가지를 먼저 밝힌다 | T10 | ① 7MM 개별국가 GD/TED 수치 ② TED Th1/Th2 전환 문헌 ③ TSHR shedding 정량치와 PMID 1497642 전문 ④ TED 직접 TSAb-positive cohort ⑤ Lumvoa 공식 unit WAC/HCPCS ⑥ 2026 Tepezza unit WAC ⑦ MER511/LCA-0321 final construct ⑧ JHA-85 clone competitiveness 기준 ⑨ JHA-88 분자 스펙. 각 항목에 해소 경로 1줄 | D |
| 53-54 | Appendix | T10 | A1 용어/endpoint 정의(on-treatment control, off-ATD normalization, durable remission, thyroid-source control, PRR, CAS). A2 제외 자산 목록(stopped 10건, NDR/관찰 10건). A3 legacy와 v2 자산집합 대조와 차이 사유. A4 as-of 이원화와 조정 규칙 | A |
| 55 | Sources | T10 | 번호 출처 전체. PubMed 15건 + ClinicalTrials.gov + 규제문서(FDA label/approval letter, EMA, MHRA, PMDA) + CMS 파일 + 특허 3건 + 회사 공시(10-K, 20-F, 8-K) + repo 산출물 경로 | A |

실제 장수: 본문 49 + Appendix 2 + Sources 1 = **52 slides** (Appendix를 1장으로 묶으면 51).

---

## 5. 그림 슬롯 점검 (JHA-86 완료조건)

| 레벨 | 슬롯 | 배치 | 근거 문서 |
|---|---|---|---|
| 구조 | 안와 해부와 GD-TED 관계 | slide 7 | legacy report A1/A3 |
| 조직 | 갑상선 vs 안와 조직의 receptor 분포 | slide 12 | tshr_igf1r_crosstalk_deepdive 6절 |
| 세포 | Thy-1+/- 분화와 IGF-1R evidence grade | slide 13 | orbital_fibroblast_igf1r_maturity |
| Signaling | TSHR-IGF-1R crosstalk 3가설 | slide 14 | tshr_igf1r_crosstalk_deepdive 8절 3-panel spec |

네 레벨 모두 배치됨. 기존 Biomni v2 figure 6종은 본 덱의 assertion 구조와 맞지 않아 그대로 쓰지 않고, 필요 시 figure 3(mechanism x phase heatmap)만 slide 27의 보조 자료로 재사용 검토한다.

---

## 6. 렌더링 전 확인 사항

1. **repo 쓰기 권한**: 본 세션은 읽기 전용 clone이므로 push는 별도 수행 필요.
2. **스타일 버전**: `_shared/deck_style.md`는 v0.3 요약본이고 본 outline은 v0.4 기준이다. archetype 코드(T1-T13), outline 포맷, 렌더 경로 항목을 v0.4로 갱신 권장.
3. **한국어 제목 길이**: v0.4 기준 약 45자 이내. 위 제목 중 slide 19, 24, 29, 39, 43은 재단이 필요할 수 있어 렌더링 시 재확인.
4. **적색 점선**: 슬라이드당 1개 이하 규칙에 따라 slide 19와 slide 45에만 배치했다.
5. **미완료 표기**: slide 48, 49에 `미확정 - JHA-85/88 진행 중` 표기 유지.
