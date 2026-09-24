---
title: "Cluster 2: TED 임상경쟁 및 FcRn 항체 전략"
linear_parent: JHA-65
milestone: cluster-2-ted-fcrn-strategy
created: 2026-09-24
status: active
---

# Cluster 2: TED 임상경쟁 및 FcRn 항체 전략

## 산출물(Linear 이슈 대응)

| 이슈 | 산출물 |
|---|---|
| JHA-74 | `fcrn_entry_strategy_ir_review.md` |
| JHA-75 | `placebo_competitive_summary.md` |

## 입력 파일

- Placebo-controlled 결과 exact result 25건: `00_baseline_biomni/landscape_v2/result_trial_curation_v2.csv`, 시험 상세 `00_baseline_biomni/landscape_v2/clinical_trials_v2.csv` (design, arms, eligibility, primary/secondary endpoints, efficacy_results, safety_results), 근거 anchor `00_baseline_biomni/landscape_v2/trial_result_evidence_anchors_v2.csv`, `00_baseline_biomni/landscape_v2/trial_registry_sources_v2.csv`
- 서술: `00_baseline_biomni/landscape_v2/report_graves_ted_landscape_v2.md` 4.2장(efficacy/null/stopped), 6장; figure 6 (result interpretability)
- Negative/stopped(UplighTED, VitaliThy 등) 원문 대조: `00_legacy_unsorted/GD_TED_report.md` Section D, E2
- FcRn 자산(v2 기준 Efgartigimod PH20 SC, Batoclimab, IMVT-1402) 필터: `00_baseline_biomni/landscape_v2/asset_trial_crosswalk_v2.csv`

## 주의

- cross-trial pooling, naive ranking, meta-analysis 금지(v2 정책). 표에는 population, endpoint 정의, timepoint 차이를 명시한다.
- JHA-74는 IR/press release/학회 자료 조사라 v2 data cut(2026-09-10) 이후 자료를 쓸 수 있다. 이 경우 as-of 날짜를 병기하고 v2 수치와 구분한다.
- 명칭 확인 필요: JHA-74 원문은 "imeroprubart(舊 batoclimab RVT-1401 계열)"로 적었으나 v2 자산 목록에는 Batoclimab과 IMVT-1402가 별개 행이다. 조사 시작 시 Immunovant 자산명/코드 대응을 먼저 확정한다.
