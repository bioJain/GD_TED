---
linear_issue: JHA-72
created: 2026-09-29
source: manual
milestone: cluster-1-competitive-landscape
status: in-review
inputs:
  - 00_legacy_unsorted/GD_TED_report.md
  - 00_baseline_biomni/landscape_v2/pipeline_assets_v2.csv
  - 00_baseline_biomni/landscape_v2/report_graves_ted_landscape_v2.md
  - 01_competitive_landscape/moa_phase_matrix_extended.md
  - 05_etpd_molecular_design/benchmark_spec_deepdive.md
---

# GD/TED class별 핵심 한계 비교표

**기준일:** 2026-09-29

**읽기 범위:** class 간 효능 순위가 아니라 각 접근의 대표적 제약을 한 장에 요약한 표. 개발단계는 JHA-73의 indication-specific 매트릭스를 참조하며, `on-treatment control`, `off-treatment normalization`, `durable remission`을 같은 endpoint로 간주하지 않는다.

## 8개 class 비교

| Class, 통일 명칭 | 적용 맥락 | 핵심 한계, 1~2줄 | 근거 수준 / 내부 근거 |
|---|---|---|---|
| **ATD** | GD, biochemical control | 복용 중 조절이 자가면역의 소실이나 durable remission을 보장하지 않아 중단 후 relapse와 장기 복용 부담이 남음. 드물지만 중대한 agranulocytosis/hepatotoxicity와 임신 시 약제별 fetal risk 때문에 모니터링과 선택 제약 존재. | **높음**, guideline/임상 outcome. `soc_outcomes_v2.csv`의 Adult ATD/pregnancy 행; legacy C1/C6 |
| **RAI** | GD, definitive thyroid-source control | 흔히 영구 hypothyroidism과 replacement를 수반하며 pathogenic autoimmunity 자체를 제거하지 않음. TED 발생/악화 위험 때문에 active moderate-to-severe TED에서는 회피하고 위험군은 steroid prophylaxis가 필요하며, 임신/수유에는 사용 불가. | **높음**, guideline. `soc_outcomes_v2.csv`의 Adult RAI 행; legacy C1/C6 |
| **수술(Thyroidectomy)** | GD, 신속한 definitive thyroid-source control | 침습적이며 recurrent laryngeal nerve 손상, hypoparathyroidism, 출혈/마취 위험과 숙련 surgeon/access 의존성이 있음. 갑상선 제거 후 평생 hormone replacement가 필요하고 자가면역/TED 자체의 직접 치료는 아님. | **높음**, guideline/메타분석. `soc_outcomes_v2.csv`의 Adult thyroidectomy 행; legacy C1 |
| **IVMP** | active moderate-to-severe TED, inflammation 중심 | Activity/inflammation에는 유용하지만 proptosis, diplopia, inactive fibrotic deficit을 일관되게 해결하지 못하며 poor response/재발 시 대안이 필요함. 누적 용량에 따른 hepatic/cardiovascular/metabolic toxicity, 감염 위험으로 반복 투여에 제약. | **높음**, guideline. `soc_outcomes_v2.csv`의 TED active moderate-to-severe/relapsed 행 |
| **IGF-1R 억제** | TED, proptosis/diplopia 중심 | Hearing impairment, hyperglycemia, muscle spasm, infusion reaction 등 class/asset safety 부담과 투여/access 부담이 있음. 반응 후 durability/재치료 기준이 충분히 확정되지 않았고 GD의 thyroid hyperfunction 자체를 교정하지 않음. | **중간~높음**, 승인 label/임상시험/실사용. v2 4.3장; legacy C3/C5/C6 |
| **FcRn 억제** | GD 중심의 broad IgG lowering | 병원성 TSAb뿐 아니라 보호성 IgG도 비선택적으로 감소시키므로 감염/장기 반복투여와 IgG rebound 관리가 핵심 부담임. TED에서는 efgartigimod Phase 3 두 건이 futility로 종료돼 GD 신호를 TED class 효과로 외삽할 수 없음. | **중간**, class 임상/indication-specific registry. JHA-73 3.1/5.1; `benchmark_spec_deepdive.md` 6절 |
| **TSHR 직접 차단/길항** | GD/TED, receptor-level blockade | 정상 TSH signaling도 함께 막아 hypothyroid pharmacology와 hormone replacement 가능성이 있으며, 현 임상 근거는 소규모/초기 단계 중심임. 장기 안전성, off-treatment durability, TED 효능은 미확립. | **중간~낮음**, 초기 임상/전임상. JHA-73 2/3절; `benchmark_spec_deepdive.md` 5절 |
| **TSAb-IgG sweeping(eTPD)** | GD 우선의 pathogen-selective concept | **개념 단계로 v2 임상 자산 없음.** 환자 간 polyclonal TSAb epitope 이질성, 결합 domain의 선택성, total IgG/정상 TSH signaling 보존, tissue delivery와 재생산/rebound를 사람에서 입증해야 함. TED에서는 TSAb 제거만으로 orbital pathology가 충분히 조절될지도 불확실. | **낮음/가설**, 설계 가설과 인접 플랫폼 근거의 외삽. legacy Section E; `benchmark_spec_deepdive.md` 4/7/8절 |

## 해석 메모

- **직접 비교 금지:** 서로 다른 질환, 병기, endpoint를 다루므로 표의 행 순서는 우열이나 권고 순위가 아니다. GD의 biochemical control과 TED의 CAS/proptosis response도 상호 대체 가능한 endpoint가 아니다.
- **개발단계 연결:** pipeline class와 indication-specific 단계는 [`moa_phase_matrix_extended.md`](./moa_phase_matrix_extended.md)를 단일 기준으로 사용한다. 특히 FcRn 억제는 GD와 TED의 개발 결과를 분리한다.
- **근거등급 의미:** `높음`은 guideline/승인 후 임상 근거, `중간`은 제한된 질환 임상 근거, `낮음/가설`은 early clinical, preclinical 또는 설계 추론을 뜻한다. 이는 GRADE 판정이 아니라 본 표의 의사결정용 상대 표기다.

## JHA-73 class 명칭 대응표

| 본 문서 명칭 | JHA-73 / v2 대응 | legacy 표기 | 정규화 메모 |
|---|---|---|---|
| ATD | SoC, pipeline matrix 비대상 | ATD(anti-thyroid drugs) | 약물 class 약어 유지 |
| RAI | SoC, pipeline matrix 비대상 | RAI(I-131) | 약어 유지 |
| 수술(Thyroidectomy) | SoC, pipeline matrix 비대상 | Thyroidectomy | 한영 병기 |
| IVMP | SoC, pipeline matrix 비대상 | IV methylprednisolone | 약어 유지 |
| IGF-1R 억제 | `IGF-1R 억제` | IGF-1R 억제제 계열 | JHA-73 명칭 채택 |
| FcRn 억제 | `FcRn 억제` | FcRn 억제제 계열 | JHA-73 명칭 채택 |
| TSHR 직접 차단/길항 | `TSHR 직접 차단/길항` | TSHR 직접 길항/차단 | JHA-73 어순 채택 |
| TSAb-IgG sweeping(eTPD) | 임상 자산 없음, 인접 class는 `anti-TSHR autoantibody 제거/항원특이 면역조절` 및 `pan-IgG 제거` | TSAb/IgG 스위핑/분해(Degrader) | eTPD concept을 MER511/LCA-0321/BHV-1300과 동일 class로 계수하지 않음 |

## 문서 한계

- `pipeline_assets_v2.csv` 현 schema에는 `mechanism_class` 열이 없으므로 JHA-73에서 검증/정규화한 class 명칭을 우선했다. CSV의 `critical_risks`, `key_unmet_need`, `safety_hypothesis`는 자산별 보조 근거로만 사용했다.
- TSAb-IgG sweeping(eTPD)은 후보물질의 임상 안전성/효능을 설명하는 행이 아니라 target product concept의 미해결 조건을 정리한 행이다. 인접 자산의 성과를 eTPD의 실증으로 간주하지 않는다.
- 표는 핵심 한계만 압축하므로 환자별 contraindication, 지역별 access/reimbursement 및 전체 AE 목록을 대체하지 않는다.

## 검증 로그

| 점검 항목 | Tier | 방법 | 결과 | 일자 |
|---|---|---|---|---|
| 8개 class 포함 및 명칭 정합성 | 하 | 이슈 목록과 JHA-73 표제어 수동 대조 | PASS, 8/8 | 2026-09-29 |
| SoC 한계 | 중 | legacy C1/C6와 v2 `soc_outcomes_v2.csv` risk/endpoint 행 교차 대조 | PASS | 2026-09-29 |
| Pipeline class 한계 | 중 | v2 4.3/5~6장, JHA-73, 자산 CSV `critical_risks` 대조 | PASS | 2026-09-29 |
| eTPD 근거등급 | 하/가설 | legacy Section E와 분자설계 benchmark의 evidence gap 대조 | PASS, 임상 자산 없음과 외삽 한계 명시 | 2026-09-29 |

> 독립 QA/cross-model 검증을 수행했다는 의미는 아니다. 본 표는 정성적 class 한계 요약이며, 향후 수치나 승인/단계 claim을 추가할 경우 `_shared/GD_TED_qa_checklist.md`의 상 tier 절차를 별도로 적용해야 한다.
