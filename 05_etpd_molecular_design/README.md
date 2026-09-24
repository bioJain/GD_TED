---
title: "Cluster 5: eTPD 분자설계 전략"
linear_parent: JHA-68
milestone: cluster-5-etpd-molecular-design
created: 2026-09-24
status: active
---

# Cluster 5: eTPD 분자설계 전략

## 산출물(Linear 이슈 대응)

| 이슈 | 산출물 | 순서 |
|---|---|---|
| JHA-83 | `tshr_shedding_rate.md` | 1(High, 선행조건) |
| JHA-84 | `benchmark_spec_deepdive.md` | 2(High) |
| JHA-85 | `clone_competitiveness_criteria.md` | 2(Medium) |
| JHA-88 | `molecule_spec_draft.md` | 3(JHA-83, 84, 85 완료 후) |

## 입력 파일

- JHA-83: 입력 파일 없음(PubMed 조사). 참고 배경 `00_legacy_unsorted/GD_TED_report.md` Section E(eTPD 시사점)
- JHA-84: `00_baseline_biomni/landscape_v2/pipeline_assets_v2.csv` 의 `construct`, `target`, `mechanism`, `preclinical_models`, `preclinical_results`, `dosing_developability`, `biomarker_pd_strategy` 컬럼; direct-TSHR/autoantibody 프로그램(LCA-0321, MER511, K1-70 등) 근거 `00_baseline_biomni/landscape_v2/direct_source_documents_v2.jsonl`, `00_baseline_biomni/landscape_v2/claim_evidence_anchors_v2.csv`, `00_baseline_biomni/landscape_v2/report_graves_ted_landscape_v2.md` 5장
- JHA-85: 5장 서술과 `00_legacy_unsorted/GD_TED_report.md` Section E. **Gate G4/G1~G6 프레임 문서(deck_architecture_and_scoring_framework.md)는 현재 repo에 없다**(deck 스타일 대체 결정과 별개로, scoring 프레임 사용 여부는 미결. docs/DECISIONS_260924.md). 확정 전에는 평가축(epitope 독립성, FTO/특허, engineerability, differentiation)을 이 폴더에서 자체 정의한다.
- JHA-88: 위 3건 결과 + `00_legacy_unsorted/meeting_notes_organized_260922.md` 1-E

## 주의

- KHN939, SCTT11 등 target 미상 자산은 임의로 기전을 부여하지 않는다.
- v2의 LCA-0321/MER511 evidence confidence는 Low, Low-moderate이며 preclinical 주장은 sponsor 유래가 많다. 스펙 수치는 출처 유형(특허/IR/포스터/논문)을 표기한다.
- "프로티나" 벤더 feasibility는 이 클러스터 이슈에 포함되지 않는다(사용자 벤더 컨택 진행 여부에 의존).
