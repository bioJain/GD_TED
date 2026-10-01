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

# Visual Slot Review

본 draft에는 4개의 도판 검토 슬롯이 있다. 내용, 위치와 source selection을 검토한 후 최종 raw 도판/page를 확보하고 재작도한다. 현재 후보는 evidence document 수준이며 논문 figure 번호와 PDF page는 확정 전이다.

| Slide | Level | Placeholder exact text | 확인할 관계 |
|---|---|---|---|
| 11 | 구조 | [FIGURE: 안와 해부  /  03_mechanism_deepdive/orbital_fibroblast_igf1r_maturity.md; EUGOGO/ATA-ETA consensus 원도판 선택] | 외안근과 안와 지방의 체적 변화가 proptosis, diplopia와 DON의 서로 다른 출력을 만든다. |
| 12 | 조직 | [FIGURE: 안와 조직과 OF heterogeneity  /  03_mechanism_deepdive/orbital_fibroblast_igf1r_maturity.md#Thy-1; PMID 14507638] | TSHR 및 IGF1R 기능, 면역세포 신호와 fibroblast heterogeneity가 병태 출력을 조절한다. |
| 13 | 세포 운명 | [FIGURE: Thy-1+/− 세포 운명  /  PMID 14507638, 23219871; 03_mechanism_deepdive/orbital_fibroblast_igf1r_maturity.md] | OF fate별로 receptor-specific perturbation과 downstream intervention을 분리해야 한다. |
| 16 | Signaling | [FIGURE: TSHR–IGF1R 3가설  /  PMID 31127272, 39821041, 34788857; 03_mechanism_deepdive/tshr_igf1r_crosstalk_deepdive.md] | 기능적 의존성은 지지되지만 환자 조직에서의 단일 복합체 구조와 독점적 연결 방식은 확정되지 않았다. |

## 검토 요청

1. 구조 → 조직 → 세포 운명 → signaling의 순서와 페이지 배치
2. 각 그림의 범위 및 근거 source 후보
3. 현재 표의 정보량과 body/appendix 경계

## 승인 후 작업

원도판의 source_doc, page, extraction metadata를 보존하고, 확정된 도판만 재작업하며 `derived_from` metadata를 기록한다. 최종 그림은 native diagram/source-derived vector 등 허용된 방식으로 제작. Draft 슬롯을 완성된 도판으로 표현하지 않는다.
