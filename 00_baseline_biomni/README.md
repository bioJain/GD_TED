---
title: 00_baseline_biomni
created: 2026-09-24
status: frozen
---

# 00_baseline_biomni: 1차 공유용 Biomni 산출물 (동결)

후속 피드백(2026-09-22 미팅) 이전에 1차 공유를 위해 Biomni lab에서 만든 리서치 산출물. **수정하지 않는다.** v2 bundle은 `release_manifest_v2.csv`로 무결성이 고정되어 있어, 파일을 고치면 manifest와 어긋난다. 보완/재해석은 cluster 폴더의 신규 파일에서 한다.

## 구성

| 폴더 | 생성 | 내용 | 위치 |
|---|---|---|---|
| `epi_soc_run_260914/` | 2026-09-14 | 역학(GD/TED, 5개국 환자 pool), 진단, 병기(CAS/EUGOGO), 병기별 SoC, 파이프라인 요약. 한국어 보고서 + xlsx | 후속 cluster 1, 4의 입력 |
| `landscape_v1/` | 2026-09-10 | 임상시험/자산/SoC landscape 1차본(168 trial, 19 asset, 20 SoC row, 31 claim). **v2로 대체됨(superseded)** | provenance 보존용. 새 작업은 v1을 인용하지 않는다 |
| `landscape_v2/` | 2026-09-11 | v1의 5개 release blocker 해소본(168 trial, 48 asset, 75 SoC row, 202 claim, 지역별 SoC 분리, claim별 blind QA, 15 slide deck). **canonical** | 모든 cluster의 1차 데이터 입력 |

## 어느 것을 쓰나

- 임상시험/자산/지역별 SoC 수치: `landscape_v2/*_v2.csv` (v1 CSV는 사용하지 않음).
- 역학/환자 pool, EUGOGO 병기별 SoC 서술: `epi_soc_run_260914/report_graves_ted_landscape.md` (v2에는 역학 섹션이 없음).
- 인용 번호: v2 `[N]`은 `landscape_v2/reference_v2.md`. epi_soc_run의 `[n]`은 보고서 말미 참고문헌 목록 기준이며 둘은 서로 다른 번호 체계다.

## 주의사항

- **Data cut 2026-09-10.** ClinicalTrials.gov live 결과와 섞지 않는다.
- v2 QA는 same-coordinator stance-hidden second pass로, 독립 검증이 아니다(`landscape_v2/QA2.md`).
- 알려진 gap(QA2 Severity 3): 한국 teprotumumab authorization/reimbursement unresolved; Tepezza 2026 SPL 미확인; Lilly/Merida closing 미확인; KHN939/SCTT11 target 미상(임의 분류하지 않고 watchlist 유지).
- **파이프라인 자산 집합이 legacy report(C4, Cortellis 파생 72건, active 51건)와 v2(48건, registry 기반)에서 서로 다르다.** 범위 정의가 다르므로 그대로 합치지 않는다. 재정합은 JHA-73에서 수행한다.
- v2 R&D potential 점수(0~3)는 evidence confidence와 분리된 축이며 clinical efficacy 확률이 아니다.

## git에서 제외된 파일

pptx 2건, slide 렌더 PNG 15장, `worker-0.ipynb`(8 MB)는 Google Drive 보관. 해시는 `external_assets_hashes.csv`, 링크는 `../docs/EXTERNAL_ASSETS.md`.
`execution_trace/PLAN.md`(v2 bundle 내 `plan2.md`와 동일 파일)는 중복이라 넣지 않았다.
