---
title: "Cluster 1: 경쟁약물 Line/Class 정리"
linear_parent: JHA-64
milestone: cluster-1-competitive-landscape
created: 2026-09-24
status: active
---

# Cluster 1: 경쟁약물 Line/Class 정리

## 산출물(Linear 이슈 대응)

| 이슈 | 산출물 | 
|---|---|
| JHA-70 | `gd_line_of_therapy.md` |
| JHA-71 | `ted_line_of_therapy.md` |
| JHA-72 | `class_limitation_matrix.md` |
| JHA-73 | `moa_phase_matrix_extended.md` |
| JHA-87 | `addressable_population_crosscheck.md` (JHA-70, 71, 72, 73 완료 후) |

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
