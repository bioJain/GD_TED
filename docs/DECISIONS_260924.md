---
title: DECISIONS_260924
created: 2026-09-24
source: claude-code
---

# 결정 기록 (2026-09-24, repo 초기 구성)

사용자 결정과 이를 반영한 구성 변경. HANDOFF 문서 §5 열린 질문에 대한 답.

| # | 질문 | 결정 | 근거/비고 |
|---|---|---|---|
| 1 | Repo 가시성 | **public** (`bioJain/GD_TED`) | 사용자 지정. 아래 "공개 범위 점검" 참조 |
| 2 | 로컬 Obsidian vault 폴더의 역할 | repo가 원본. 별도 경로(`C:\Users\jain\repos\GD_TED`)에 clone하고 파일은 **복사** | vault 폴더(OneDrive 동기화)는 원본 스냅샷으로 남김. OneDrive 안에서 git 작업을 하지 않기 위함 |
| 3 | PPTX 정책 | Google Drive 외부 저장 + 링크 | `.gitignore`에 `*.pptx`; `docs/EXTERNAL_ASSETS.md`, `00_baseline_biomni/external_assets_hashes.csv` |
| 4 | deck architecture 문서 | `deck_architecture_and_scoring_framework.md`는 **가져오지 않고** deck 구성 규칙은 report-deck-style 스킬 사용 | `_shared/deck_style.md`. **미결**: 이 문서에 있는 Gate G1~G6 *scoring* 프레임(JHA-85, JHA-88이 참조)을 계속 쓸지는 사용자 확인 필요. 그동안 JHA-85/88은 자체 정의 평가축으로 진행하도록 이슈에 명시 |
| 5 | Biomni 폴더 처리 | `00_baseline_biomni/`로 편입(동결), 아래 변경점 참조 | |
| 6 | cluster 구조 | HANDOFF 3.2안 유지(6 cluster 병렬) + `00_baseline_biomni/` 추가 | 실제 작업 몇 건 후 재평가(HANDOFF §5-5) |

## HANDOFF 3.2안 대비 변경점

1. `00_baseline_biomni/` 신설: Biomni 산출물 3개 bundle(`epi_soc_run_260914`, `landscape_v1`, `landscape_v2`). v2를 canonical, v1은 superseded로 표시.
   - bundle 내부 경로는 바꾸지 않았다(v2 `release_manifest_v2.csv` 해시 무결성 유지).
2. `_shared/`에는 `GD_TED_reference.md`, `GD_TED_qa_checklist.md`를 원래 파일명 그대로 둠(HANDOFF의 `reference.md`, `qa_checklist.md` 개명 안 함: report 내 상호 참조 보존). `deck_architecture_and_scoring_framework.md` 대신 `deck_style.md` 추가.
3. `00_legacy_unsorted/`는 md 7건으로 축소(나머지 2건은 `_shared/`로 이동).
4. `docs/` 신설: HANDOFF 원문, 결정 기록, 작성 규칙, 외부 자산 목록.
5. git 제외(Drive): pptx 2건, slide PNG 15장, `worker-0.ipynb`(8 MB). `execution_trace/PLAN.md`(v2 `plan2.md`와 동일)는 중복이라 제외.

## Biomni 산출물 검토 결과(구성에 영향을 준 사실)

- 3개 bundle은 서로 대체/보완 관계다: 09-10 v1 -> 09-11 v2(대체), 09-14 epi_soc_run은 별개 주제(역학/환자 pool)라 v2에 없는 내용을 담고 있음.
- v2가 legacy report보다 나은 점: 지역별 SoC 분리(75행), trial-asset crosswalk(339행), claim별 blind QA(202 claim), R&D potential/evidence confidence 분리. 반대로 legacy에만 있는 것: Section B(기전) 서술, market sizing, eTPD 시사점(Section E), Cortellis 파생 72건 파이프라인.
- **자산 집합 불일치**: legacy C4(72건, active 51건) vs v2(48건). 범위 정의가 달라 JHA-73에서 명시적 재정합 필요.
- v2 알려진 gap: 한국 teprotumumab authorization/reimbursement unresolved, Tepezza 2026 SPL, Lilly/Merida closing, KHN939/SCTT11 target 미상. JHA-81, 84에 영향.
- 두 개의 인용 번호 체계(legacy `[n]`, v2 `[N]`)가 공존. 통합하지 않고 병기 규칙만 정함(`repo_conventions.md`).

## 공개 범위 점검 (public repo)

push 전에 사용자 확인이 필요한 항목:

- `00_legacy_unsorted/GD_TED_report.md` C4 표와 `GD_TED_reference.md` [48]은 Cortellis(상업 DB) 파생 자료를 전재하거나 서술한다. 라이선스상 재배포 제한이 있을 수 있음.
- `meeting_notes_organized_260922.md`, `GD_TED_execution_log.md`, `docs/HANDOFF...`에는 내부 논의(벤더 "프로티나", 에이프릴바이오 단서, 내부 eTPD 프로그램 맥락, 미팅 코멘트 원문)가 있음.
- eTPD 분자설계 전략(Cluster 5)은 자산 전략 성격의 내용이다.

## Linear 반영 (2026-09-24)

- 자식 19개 이슈: 'Repo 산출물 경로 및 입력' 절 추가, 'Repo 미연결' 문구를 repo 경로 안내로 교체.
- JHA-84 산출물명 `benchmark_spec_deepdive.md`로 변경(이슈 제목에 맞춤).
- 상위 6개 이슈(JHA-64~69): cluster 폴더 안내 추가.
- 미반영: 프로젝트 P-JHA-4의 GitHub 연동(Linear 워크스페이스 설정, API 미지원), 프로젝트 resource 링크.
