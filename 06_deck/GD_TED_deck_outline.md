---
linear_issue: JHA-86
created: 2026-10-01
source: codex
milestone: cluster-6-deck
status: in-review
inputs:
  - 01_competitive_landscape/gd_line_of_therapy.md
  - 01_competitive_landscape/ted_line_of_therapy.md
  - 01_competitive_landscape/class_limitation_matrix.md
  - 01_competitive_landscape/moa_phase_matrix_extended.md
  - 01_competitive_landscape/addressable_population_crosscheck.md
  - 02_ted_fcrn_strategy/fcrn_entry_strategy_ir_review.md
  - 02_ted_fcrn_strategy/placebo_competitive_summary.md
  - 03_mechanism_deepdive/igf1r_class_effect_ae.md
  - 03_mechanism_deepdive/igf1r_autoantigen_review.md
  - 03_mechanism_deepdive/orbital_fibroblast_igf1r_maturity.md
  - 03_mechanism_deepdive/tshr_igf1r_crosstalk_deepdive.md
  - 03_mechanism_deepdive/r1b_asset_identification.md
  - 04_tam_sam_pricing/tam_sam_revision.md
  - 04_tam_sam_pricing/teprotumumab_veligrotug_pricing.md
  - 05_etpd_molecular_design/benchmark_spec_deepdive.md
  - 05_etpd_molecular_design/tshr_shedding_rate.md
---

# GD/TED Research Report Deck v0.1

R&D 내부 공유용 standalone report. 근거 기준일 2026-10-01. 63쪽, 도판 검토 슬롯 4개.

대분류 1–4 완료 근거 및 대분류 5의 검증된 benchmark/shedding 결과를 반영. JHA-85/88은 설계 제안만 포함. 기존 frozen 원자료와 ref namespace 변경 없음. 모든 표는 native editable table.

## 슬라이드 개요

| Slide | Part | Supported title | Evidence | Inputs | Figure slot |
|---|---|---|---|---|---|
| 1 | 표지 | GD와 TED의 치료 공백 및 eTPD 연구 방향 | D | D01, D11, D15 | — |
| 2 | 핵심 판단 | GD와 TED는 같은 자가항체 축에서 다른 치료 공백을 보인다 | D | D01, D09, D11, D15 | — |
| 3 | 핵심 판단 | 임상 성공 기준은 항체 감소보다 지속적인 질환 개선이다 | D | D04, D06, D13, D15, P02, P03 | — |
| 4 | 읽는 법 | 질환에서 설계 판단까지 여섯 단계로 연결한다 | D | D01, D15 | — |
| 5 | 근거 관리 | 근거 등급과 분모를 모든 핵심 주장에 붙인다 | D | D13 | — |
| 6 | 질환 | GD의 호르몬 과다와 TED의 조직 변화는 분리 평가한다 | A | D01, D02, D11 | — |
| 7 | 질환 | 진단과 trial eligibility를 같은 기준으로 보지 않는다 | A | D01, D02, D11 | — |
| 8 | 질환 | TED는 활동성과 중증도 두 축으로 치료가 갈린다 | A | D02 | — |
| 9 | 환자 분모 | 역학 수치는 일반 인구와 GD 환자 분모를 구분해야 한다 | A | D05 | — |
| 10 | 환자 분모 | 지역별 pool은 수요의 상한이며 치료 적격군이 아니다 | D | D05, D13 | — |
| 11 | 구조 | 안와 공간의 변화는 돌출과 압박 위험으로 연결된다 | A | D02, D10 | 안와 해부  /  03_mechanism_deepdive/orbital_fibroblast_igf1r_maturity.md; EUGOGO/ATA-ETA consensus 원도판 선택 |
| 12 | 조직 | Orbital fibroblast는 염증과 조직 변화의 연결점이다 | A | D10, D11 | 안와 조직과 OF heterogeneity  /  03_mechanism_deepdive/orbital_fibroblast_igf1r_maturity.md#Thy-1; PMID 14507638 |
| 13 | 세포 운명 | 지방화와 섬유화의 IGF1R 인과 근거는 다르다 | A | D10 | Thy-1+/− 세포 운명  /  PMID 14507638, 23219871; 03_mechanism_deepdive/orbital_fibroblast_igf1r_maturity.md |
| 14 | 세포 운명 | Adipogenesis 근거는 있어도 fibrosis 검증은 남아 있다 | A | D10 | — |
| 15 | Signaling | TSHR의 조직별 출력은 같은 항체에도 달라질 수 있다 | A | D11, D15 | — |
| 16 | Signaling | TSHR–IGF1R 연계에는 경쟁하는 세 가지 설명이 있다 | A | D11, D09 | TSHR–IGF1R 3가설  /  PMID 31127272, 39821041, 34788857; 03_mechanism_deepdive/tshr_igf1r_crosstalk_deepdive.md |
| 17 | Signaling | ARRB1 지지는 독점적 물리적 bridge의 증명과 다르다 | A | D11 | — |
| 18 | 자가항체 | Anti-IGF1R 항체의 관찰 결과는 agonist 가설을 확정하지 않는다 | A | D09 | — |
| 19 | 기전에서 치료로 | TSAb 제거는 입력을 줄이고 IGF1R 차단은 분기를 억제한다 | D | D11, D15, D06 | — |
| 20 | GD SoC | GD 초기 치료는 지역과 환자 맥락에 따라 선택한다 | A | D01 | — |
| 21 | GD SoC | 호르몬 조절과 autoimmune remission은 다른 결과다 | A | D01 | — |
| 22 | TED SoC | Active TED에서는 염증과 돌출 목표를 함께 설정한다 | A | D02 | — |
| 23 | TED SoC | DON과 chronic stable TED는 별도 경로가 필요하다 | A | D02, P01 | — |
| 24 | 치료 한계 | 질환별 미충족 수요는 같은 클래스에서도 다르다 | D | D03, D15 | — |
| 25 | 경쟁 지형 | GD pipeline은 항체 조절과 호르몬 조절로 나뉜다 | B | D04, D15, P05 | — |
| 26 | 경쟁 지형 | TED pipeline은 IV에서 SC 및 경구 방식으로 확장된다 | B | D04, P01, P02, P03, P04, P07, P08 | — |
| 27 | 경쟁 지형 | 개발 중단 신호는 질환과 프로그램 단위로 읽어야 한다 | B | D12, P06, P07 | — |
| 28 | 임상 해석 | Proptosis responder라도 시간점과 복합 조건이 다르다 | A | D07, D01 | — |
| 29 | TED 효능 | Active TED의 IGF1R RCT는 돌출 개선을 입증했다 | A | D07 | — |
| 30 | TED 효능 | Chronic TED에도 proptosis 개선 증거가 있다 | B | D07, P03 | — |
| 31 | TED 효능 | Elegrobart topline은 투여 경로의 확장을 보여준다 | B | P02, P03 | — |
| 32 | TED 효능 | Non-IGF1R 전략의 결과는 endpoint별로 혼재한다 | A | D02, D07, P04 | — |
| 33 | 임상 해석 | Placebo 설계는 endpoint와 윤리적 맥락에 의존한다 | D | D07, D02, P03 | — |
| 34 | 지속성 | Responder 유지율은 전체 환자 성공률과 다르다 | A | D02, D07 | — |
| 35 | FcRn 전략 | TED 실패와 GD 개발 지속은 표적의 질환 맥락을 보여준다 | D | D06, P06, P07 | — |
| 36 | GD 임상 | GD Phase 3는 off-ATD 정상 기능과 지속성을 묻는다 | A | D04, P05 | — |
| 37 | GD 임상 | Batoclimab 단일군 결과는 randomized remission 증거가 아니다 | A | D06, D07 | — |
| 38 | 안전성 | Teprotumumab AE는 event별 분모를 유지한다 | A | D08 | — |
| 39 | 안전성 | Veligrotug는 efficacy와 별개로 hearing/glucose 감시가 필요하다 | A | D08, P01 | — |
| 40 | 안전성 | 미보고 AE를 0건 또는 안전성 우위로 읽지 않는다 | D | D08, P02, P03 | — |
| 41 | 가격 | 미국 course 가격과 CMS payment는 같은 수치가 아니다 | C | D14, P01 | — |
| 42 | 가격 | 동일 체중에서도 administered dose와 opened vial이 다르다 | D | D14 | — |
| 43 | 시장 | Commercial TAM은 범위 점검용이며 투자 가치가 아니다 | D | D13 | — |
| 44 | 시장 | TSAb 양성률은 mechanism ceiling이고 치료 반응률이 아니다 | D | D13 | — |
| 45 | 시장 | US annual flow는 발생률에서 출발한 시나리오다 | D | D13 | — |
| 46 | 시장 | TED 유병 pool에 추가 필터와 중복 제거가 필요하다 | D | D13, D05 | — |
| 47 | eTPD benchmark | Benchmark는 neutralization과 clearance 경로가 다르다 | B | D15, P05 | — |
| 48 | eTPD benchmark | Affinity, cellular potency와 모델 제거율은 비교 가능한 단위가 아니다 | A | D15 | — |
| 49 | eTPD benchmark | 특허는 설계 선택지를 보여주지만 최종 CMC를 확정하지 않는다 | D | D15 | — |
| 50 | TSHR shedding | Shedding의 존재와 인간 in vivo flux는 별도 질문이다 | A | D16 | — |
| 51 | 설계 판단 | eTPD의 첫 gate는 선택성과 정상 기능 보존이다 | D | D15, D16 | — |
| 52 | 다음 실험 | 단계별 실험으로 제거와 기능 억제를 분리한다 | D | D15, D16, D10, D11 | — |
| 53 | 다음 결정 | eTPD 차별화는 네 가지 조건을 동시에 통과해야 한다 | D | D15, D16, D11 | — |
| 54 | 업데이트 항목 | 2026–2027 이벤트는 예정과 결과를 구분해 추적한다 | B | D04, D15, P04, P02, P05 | — |
| 55 | 미해결 과제 | 미완료 자료는 결론의 한계로 명시한다 | D | D15, D16, D13 | — |
| 56 | 부록 A | 허가 범위와 시험 phenotype은 다를 수 있다 | A | P01, P04, P08, D14 | — |
| 57 | 부록 B | 최근 등록부 상태를 원자료와 함께 보관했다 | A | D04 | — |
| 58 | 부록 C | Patent 날짜와 sequence mapping을 분리 기록한다 | A | D15 | — |
| 59 | 부록 D | 기전 원문을 hypothesis별로 추적할 수 있다 | A | D09, D10, D11, D16 | — |
| 60 | 출처 색인 | 출처 색인 1: 문서와 최신 원출처 | A | D01, D02, D03, D04, D05, D06 | — |
| 61 | 출처 색인 | 출처 색인 2: 문서와 최신 원출처 | A | D07, D08, D09, D10, D11, D12 | — |
| 62 | 출처 색인 | 출처 색인 3: 문서와 최신 원출처 | A | D13, D14, D15, D16, P01, P02 | — |
| 63 | 출처 색인 | 출처 색인 4: 문서와 최신 원출처 | A | P03, P04, P05, P06, P07, P08 | — |

## 출처

Source ID는 본 덱만의 namespace. legacy/Biomni reference 번호와 통합하지 않음. 전체 row-level 출처는 `slide_source_map_20261001.csv`, `source_index_20261001.md` 참조. Speaker notes에도 URL 포함.

## 최신 자료 처리

- ClinicalTrials.gov API v2: 21개 등록부를 2026-10-01 조회. 최신 enrollment, phase, status 및 results posted 구분.
- Elegrobart REVEAL-1/2 회사 공개 topline 추가. Registry에 결과가 없다는 이유로 공개 결과 전체가 없다고 하지 않음.
- Satralizumab TED sBLA는 review 중, 예정 PDUFA 2026-10-15. 승인 전 표시.
- Lu AG22515 TED sponsor stop과 registry Active not recruiting를 병기.
- Tepro muscle spasm placebo 3/20 사용. 중복 hearing event 합산 금지.
- GD/TED TAM 합산 금지. TSAb serology ceiling와 clinical SAM 분리.

## QA 및 남은 단계

- Package integrity, geometry/font, native table 확인 및 전 페이지 visual review. 상세 로그는 `deck_qa_20261001.md`.
- 독립 세션/cross-model QA는 별도 미수행. 기존 repo QA와 이번 원출처 대조를 반영했지만 독립 QA 통과라고 표기하지 않음.
- 도판은 repo convention의 draft → layout 확정 → 재작업 → 배치 순서를 따름.
