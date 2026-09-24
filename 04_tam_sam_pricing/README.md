---
title: "Cluster 4: TAM/SAM 및 약가"
linear_parent: JHA-67
milestone: cluster-4-tam-sam-pricing
created: 2026-09-24
status: active
---

# Cluster 4: TAM/SAM 및 약가

## 산출물(Linear 이슈 대응)

| 이슈 | 산출물 |
|---|---|
| JHA-81 | `teprotumumab_veligrotug_pricing.md` |
| JHA-82 | `tam_sam_revision.md` (JHA-81 반영) |

## 입력 파일

- 기존 TAM/SAM: `00_legacy_unsorted/GD_TED_market_sizing_report.md` (FLOOR/PREMIUM, TSAb-IgG coverage, Section 2.3 실매출 anchor), `00_legacy_unsorted/GD_TED_market_sizing_plan.md`
- 환자 pool(2024 인구 기준): `00_baseline_biomni/epi_soc_run_260914/report_graves_ted_landscape.md` 1.2, 2.2장
- 지역별 authorization/reimbursement/access status: `00_baseline_biomni/landscape_v2/soc_outcomes_v2.csv` (`reimbursement_access`, `authorization_status_scope`, `guideline_position` 컬럼), `00_baseline_biomni/landscape_v2/report_graves_ted_landscape_v2.md` 3.1장, 3.2장
- 임상 규모/승인 자산: `00_baseline_biomni/landscape_v2/pipeline_assets_v2.csv`

## 주의

- v2에는 가격 데이터가 없다. WAC/list price와 보험수가는 신규 조사 대상이며, 출처와 as-of 날짜를 반드시 병기한다.
- 한국 teprotumumab authorization/reimbursement는 v2에서 unresolved다(QA2 S3-REGIONAL-STATUS-GAPS). 한국 가격 비교는 공식 출처(MFDS/HIRA)를 먼저 확인하고, 없으면 unresolved로 남긴다.
- 약가 수치는 report-deck-style 기준 Evidence grade C(2차 자료) 이하가 될 수 있으므로 등급을 기록한다.
