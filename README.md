# GD_TED

Graves' disease(GD) / thyroid eye disease(TED) 리서치와 eTPD(extracellular targeted protein degradation) 분자설계 후속 작업 저장소.

- 작업 추적: Linear 프로젝트 P-JHA-4 "eTPD GD/TED 후속 리서치 (2026-09-22 미팅 액션아이템)" (team JHa_Res, issue JHA-64 ~ JHA-88)
- 시작 배경: [docs/HANDOFF_eTPD_GD_TED_260924.md](docs/HANDOFF_eTPD_GD_TED_260924.md)
- 구조 결정 기록: [docs/DECISIONS_260924.md](docs/DECISIONS_260924.md)
- 작성 규칙(frontmatter, 인용, 바이너리 정책): [docs/repo_conventions.md](docs/repo_conventions.md)

## 폴더 구조

| 폴더 | 역할 | 수정 정책 |
|---|---|---|
| `00_baseline_biomni/` | 1차 공유용으로 만든 Biomni 리서치 산출물(2026-09-10 data cut). `landscape_v2/`가 canonical 데이터 | **동결**, 수정 금지(manifest hash 보존). 보완은 cluster 폴더에서 |
| `00_legacy_unsorted/` | claude.ai Project "6T_review_26_H2"에서 가져온 원본 md 7건(report, plan, market sizing, deck outline, execution log, meeting notes) | 동결. 내용을 갱신할 때는 cluster 폴더에 새 파일로 |
| `_shared/` | cluster 공통 참조자료(참고문헌, QA 체크리스트, deck 스타일 규칙) | 갱신 가능 |
| `01_competitive_landscape/` | Cluster 1, JHA-64 (70, 71, 72, 73, 87) | 활성 |
| `02_ted_fcrn_strategy/` | Cluster 2, JHA-65 (74, 75) | 활성 |
| `03_mechanism_deepdive/` | Cluster 3, JHA-66 (76, 77, 78, 79, 80) | 활성 |
| `04_tam_sam_pricing/` | Cluster 4, JHA-67 (81, 82) | 활성 |
| `05_etpd_molecular_design/` | Cluster 5, JHA-68 (83, 84, 85, 88) | 활성 |
| `06_deck/` | Cluster 6, JHA-69 (86). pptx 본체는 Google Drive | 활성 |

각 cluster 폴더의 README에 **대응 Linear 이슈별 산출물 경로**와 **입력으로 참조할 기존 파일**이 있다.

## 핵심 참조 데이터(모두 `00_baseline_biomni/landscape_v2/`)

| 파일 | 내용 | 규모 |
|---|---|---|
| `clinical_trials_v2.csv` | ClinicalTrials.gov 2026-09-10 snapshot 기반 GD/TED 시험 | 168 trial |
| `pipeline_assets_v2.csv` | 승인/개발 자산 + direct-TSHR preclinical, R&D potential 점수 | 48 asset |
| `asset_trial_crosswalk_v2.csv` | trial 내 intervention 단위 asset 매핑 | 339 행 |
| `soc_outcomes_v2.csv` | 지역(US/EU/UK/KR/JP) x 질환/병기 x line SoC, authorization/reimbursement/guideline 분리 | 75 행 |
| `result_trial_curation_v2.csv` | 결과 공개 임상 exact-result curation | 25 trial |
| `evidence_claims_v2.csv` | claim 단위 근거 anchor와 blind verdict | 202 claim |
| `reference_v2.md`, `reference_catalog_v2.csv` | 인용 번호 체계 `[N]`(v2) | |
| `report_graves_ted_landscape_v2.md` | v2 본문 보고서 | |
| `figures_v2/` | figure 6종 (SVG + PNG) | |

주의: v2 QA는 same-coordinator stance-hidden 방식이며 **독립 검증이 아니다**(QA2.md 참조). 알려진 gap: 한국 teprotumumab authorization/reimbursement unresolved, Tepezza 2026 SPL 미확인, Lilly/Merida closing 미확인, KHN939/SCTT11 target 미상.

## 외부 저장(Google Drive)

pptx와 대용량 실행 노트북은 git에 넣지 않는다. 파일명, 크기, SHA-256은 `00_baseline_biomni/external_assets_hashes.csv`, Drive 링크는 [docs/EXTERNAL_ASSETS.md](docs/EXTERNAL_ASSETS.md)에 기록한다.
