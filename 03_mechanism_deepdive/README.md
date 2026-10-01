---
title: "Cluster 3: Mechanism 딥다이브"
linear_parent: JHA-66
milestone: cluster-3-mechanism-deepdive
created: 2026-09-24
status: done
completed: 2026-10-01
---

# Cluster 3: Mechanism 딥다이브

## 산출물(Linear 이슈 대응)

| 이슈 | 산출물 | 완료 여부 | 핵심 결론 |
|---|---|---|---|
| JHA-76 | `igf1r_class_effect_ae.md` | 완료 | 6개 지정 자산과 master의 IGF-1R 관련 자산을 대조함. TED에서 반복 관찰된 muscle spasm, hearing-related AE, hyperglycemia 패턴과 자산별 신호를 구분하고 `미보고`와 0건을 분리함 |
| JHA-77 | `igf1r_autoantigen_review.md` | 완료 | 독립 section 신설보다 기존 B4 보강을 권고함. 2025년 자가항체 보고는 존재 가능성을 지지하지만 directly-stimulating/pathogenic 가설을 확립하지 않음 |
| JHA-78 | `orbital_fibroblast_igf1r_maturity.md` | 완료 | adipocyte 경로는 **B, lower confidence**, myofibroblast 경로는 **C**로 판정함. target-specific in vivo attribution은 아직 제한적임 |
| JHA-79 | `tshr_igf1r_crosstalk_deepdive.md` | 완료 | crosstalk의 기능적 관찰과 세부 분자배치를 구분함. ARRB1 scaffold, ectodomain 직접결합은 `proposed`, directly-stimulating IGF-1R autoantibody는 가장 약한 가설로 유지함 |
| JHA-80 | `r1b_asset_identification.md` | 완료 | "R1b"를 APB-A1/Lu AG22515의 TED Phase 1b를 가리킨 표기로 추정함. 타겟은 CD40L이며 TED 적응증 개발 중단을 확인함 |

## 상위 이슈 종결 판정

- **JHA-66 완료 조건 충족:** 자식 이슈 5건의 산출물과 결론이 모두 존재함. 각 문서의 검증 로그에 2026-10-01 독립 QA/fact-check 결과를 기록함.
- **B4 반영 방식:** `00_legacy_unsorted/GD_TED_report.md`는 legacy 원본이므로 수정하지 않고, JHA-77/78/79 신규 문서를 B4 보강용 canonical addendum으로 사용함. JHA-77의 5절에 실제 B4 반영용 문안을 제공함.
- **잔여 불확실성의 처리:** IGF-1R-selective in vivo lineage attribution, agonistic anti-IGF-1R antibody, crosstalk의 정확한 molecular architecture는 미확립 상태로 남음. 이는 문서에 각각 한계/`proposed`로 표기되어 있으며 이슈 종결을 막는 미완료 작업은 아님.

## 입력 파일

- JHA-76: `00_baseline_biomni/landscape_v2/clinical_trials_v2.csv` (safety_results, IGF-1R 자산 행), `00_baseline_biomni/landscape_v2/pipeline_assets_v2.csv` (mechanism_class 기준 IGF-1R), `00_baseline_biomni/landscape_v2/report_graves_ted_landscape_v2.md` 4.3장(safety); figure 4(selected PRR, descriptive only); `00_legacy_unsorted/GD_TED_report.md` Section C3
- JHA-77, 78, 79: `00_legacy_unsorted/GD_TED_report.md` Section B4(Thy-1 fibroblast 분화, 3가설); 문헌 anchor는 `00_baseline_biomni/landscape_v2/source_anchors_v2.csv`, `00_baseline_biomni/landscape_v2/reference_catalog_v2.csv`
- JHA-80: 입력 파일 없음(공개 파이프라인 조사)

## 주의

- 안전성 비교표는 서로 다른 population/endpoint/timepoint의 관찰을 나열하는 것이며 발생률 순위를 만들지 않는다.
- 2024~2026 문헌 재검색 결과는 PubMed ID/DOI와 as-of 날짜를 기록한다.
