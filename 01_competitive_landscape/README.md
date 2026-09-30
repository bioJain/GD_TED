---
title: "Cluster 1: 경쟁약물 Line/Class 정리"
linear_parent: JHA-64
milestone: cluster-1-competitive-landscape
created: 2026-09-24
status: in-review
---

# Cluster 1: 경쟁약물 Line/Class 정리

## 산출물(Linear 이슈 대응)

| 이슈 | 산출물 | 
|---|---|
| JHA-70 | `gd_line_of_therapy.md` |
| JHA-71 | `ted_line_of_therapy.md` |
| JHA-72 | `class_limitation_matrix.md` |
| JHA-73 | `moa_phase_matrix_extended.md` |
| JHA-87 | `addressable_population_crosscheck.md` |

## 통합 결론

- **GD 치료 순서:** ATD를 기본 1차 치료로 사용하되 지역 guideline, 환자 선호, 임신 계획, goiter/TED 상태에 따라 RAI 또는 thyroidectomy를 초기 definitive option으로 선택할 수 있다. ATD 중단 후 재발과 불내성에서는 RAI, thyroidectomy, 장기 low-dose ATD를 구분해 검토한다.
- **TED 치료 순서:** 단일 직선형 line이 아니라 severity, activity, phenotype, 시력 위협 여부를 먼저 분기한다. Mild active disease는 국소 관리와 selected selenium, active moderate-to-severe disease는 IVMP 기반 치료 또는 지역별 승인 표적치료, 불응/재발은 phenotype별 표적치료나 off-label 면역조절, chronic/inactive deficit은 재활수술이 중심이다.
- **Class 한계:** 기존 SoC는 durable autoimmune remission, 반복치료 독성, 영구 hypothyroidism 또는 구조적 deficit을 동시에 해결하지 못한다. IGF-1R, FcRn, TSHR 직접 차단도 각각 safety/access, broad IgG suppression, 초기 임상근거라는 제약이 있으며 TSAb-IgG sweeping은 아직 임상 자산이 없는 가설 단계다.
- **개발단계:** 자산 전체의 최고 단계를 적응증별 단계로 오인하지 않도록 GD와 TED trial을 따로 판정했다. Active/approved 자산은 본표, stopped/failed 자산은 부표, 후속 개발이 확인되지 않은 completed-only 자산은 관찰 목록으로 분리했다.
- **잔여 환자군:** ATD 장기불응/불내성 GD, IGF-1R 부적합/무반응 chronic-inactive TED, TRAb 음성 또는 assay-discordant TED, steroid-resistant active TED, 주요 class의 독성 고위험군, DON/각막 위협 환자가 핵심 gap이다. 환자 pool 수치는 시장규모가 아니라 clinical opportunity ceiling으로만 해석한다.

## 완료조건 추적

| 상위 완료조건 | 반영 위치 | 상태 |
|---|---|---|
| GD 1차/2차/재발 line, duration/remission, 미충족군 | `gd_line_of_therapy.md` 2절, 4절, 7절 | 작성 완료, review 중 |
| TED 상태 분기, 단계별 line, 지역별 승인/급여, 미충족군 | `ted_line_of_therapy.md` 1절, 2절, 3절, 5절 | 작성 완료, review 중 |
| 8개 class 한계와 통일 명칭 | `class_limitation_matrix.md` 8개 class 표, 명칭 대응표 | 작성 완료, review 중 |
| GD/TED indication-specific phase 통합 및 legacy/v2 대조 | `moa_phase_matrix_extended.md` 2절부터 6절, 별도 QA 보고서 | 작성 및 독립 QA 완료, review 중 |
| 네 산출물 교차, 잔여 환자군, legacy C6 통합 | `addressable_population_crosscheck.md` 2절부터 10절 | 작성 완료, 상 tier 수치 독립 QA 대기 |

상위 이슈는 다섯 산출물이 모두 마련돼 **통합 review 단계**다. Linear 상태를 Done으로 전환하기 전 `addressable_population_crosscheck.md` 11절과 13절에 명시한 역학 원 수치의 독립 QA/direct-quote 대조를 완료해야 한다.

## 입력 파일

- 지역별 SoC, line, authorization/reimbursement/guideline: `00_baseline_biomni/landscape_v2/soc_outcomes_v2.csv` (75행, US/EU/UK/KR/JP), `00_baseline_biomni/landscape_v2/report_graves_ted_landscape_v2.md` 3장, 8장(special populations)
- 병기별 SoC(EUGOGO 2021 중증도 x 활성도), 진단/병기 기준: `00_baseline_biomni/epi_soc_run_260914/report_graves_ted_landscape.md` 3~4장
- 자산, MoA, phase: `00_baseline_biomni/landscape_v2/pipeline_assets_v2.csv` (48 asset), `00_baseline_biomni/landscape_v2/asset_trial_crosswalk_v2.csv`, `00_baseline_biomni/landscape_v2/clinical_trials_v2.csv`; figure 2, 3 (`00_baseline_biomni/landscape_v2/figures_v2/`)
- 기존 서술: `00_legacy_unsorted/GD_TED_report.md` Section C1~C6
- 환자군 규모(JHA-87): `00_baseline_biomni/epi_soc_run_260914/report_graves_ted_landscape.md` 1~2장 환자 pool

## 주의

- JHA-73: legacy C4(Cortellis 파생 72건, active 51건)와 v2(48건)의 자산 집합이 다르다. 두 목록을 대조해 차이(누락/추가/중단 판정)를 명시하고, indication-specific 개발단계로 재확인한다("Highest Status trap").
- SoC의 endpoint 용어(on-treatment control, off-ATD normalization, durable remission, relapse, cure)를 v2 taxonomy대로 구분한다.
- v2 지역 status gap(한국 teprotumumab 등)은 표에 unresolved로 표기하고 추정으로 채우지 않는다.
