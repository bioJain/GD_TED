---
title: HANDOFF_eTPD_GD_TED
목적: claude.ai 세션에서 진행한 eTPD GD/TED 리서치를 Claude Code(로컬/저장소) 세션에서 이어가기 위한 인수인계 문서
작성일: 2026-09-24
작성 세션: claude.ai Project "6T_review_26_H2" (Project ID: 019ff321-e837-70af-bff8-3eadcbf93ece)
대상 GitHub repo: https://github.com/bioJain/GD_TED (아직 미생성/미설정)
---

# Handoff — eTPD GD/TED 리서치 → GitHub Repo 설정

> 이 문서는 Claude Code 세션이 **처음 읽어야 할 파일**입니다. 지금까지의 작업 맥락, 이 폴더에 함께 복사된 9개 원본 파일의 성격, 그리고 앞으로 만들 GitHub repo(`bioJain/GD_TED`)의 구조 설계와 설정 체크리스트를 담고 있습니다.

---

## 0. 지금 이 폴더에 있는 것 (인벤토리)

이 폴더(`eTPD_GD,TED/`)에는 이 문서 외에 claude.ai Project "6T_review_26_H2"에서 복사해온 9개 원본 마크다운 파일이 함께 있습니다.

| 파일명 | 원래 위치 | 성격 |
|---|---|---|
| `GD_TED_plan.md` | claude.ai 메모리(Project 전용, `/projects/019ff321.../GD_TED_plan.md`) | 최초 작업 계획서 — 분석 범위/섹션 구조(A-E)/QA 프레임워크 원안 |
| `GD_TED_market_sizing_plan.md` | 상동(메모리) | 시장성 분석 트랙의 별도 작업 개요(market-sizing-multitrack 스킬 경량 적용) |
| `GD_TED_report.md` | claude.ai Project 문서(`claude/GD_TED_report.md`) | 본문 보고서 — Section A(역학) ~ E(eTPD 시사점), in-line 인용 포함 |
| `GD_TED_reference.md` | 상동 | 참고문헌 목록 — report.md의 [n] 번호와 1:1 대응 |
| `GD_TED_market_sizing_report.md` | 상동 | TAM/SAM 시장성 분석 + TSAb-IgG coverage 분석 |
| `GD_TED_execution_log.md` | 상동 | 전체 작업 세션의 도구 호출/발견/의사결정 상세 로그 |
| `GD_TED_deck_outline_260914.md` | 상동 | 내부 공유용 20슬라이드 deck 개요(eTPD 시사점 제외, 순수 리서치 요약용) |
| `GD_TED_qa_checklist.md` | 상동 | QA 에이전트용 체크리스트(A-H 카테고리, ~30개 항목) + QA 시스템 프롬프트 원문 |
| `meeting_notes_organized_260922.md` | 상동 | 2026-09-22 미팅에서 나온 후속 리서치 요청을 정리한 문서 — 현재 Linear 프로젝트의 직접 소스 |

**주의(스코프 관련 고지)**:
- `GD_TED_plan.md`, `GD_TED_market_sizing_plan.md` 두 파일은 claude.ai Project의 "claude/" 문서 폴더가 아니라 **claude.ai 메모리**(Project-scoped)에서 가져온 것입니다. 사용자의 원래 지시("claude 폴더 중 GD, TED 관련 md 파일들")를 문자 그대로 보면 대상이 아니지만, `GD_TED_report.md`와 `GD_TED_market_sizing_report.md`가 본문에서 각각 이 두 계획서를 명시적으로 인용하고 있어("계획서: GD_TED_plan.md", "연계 문서: GD_TED_market_sizing_plan.md") 맥락 손실을 막기 위해 포함했습니다.
- 다음 문서들은 **의도적으로 제외**했습니다 — 확인이 필요하면 알려주시기 바랍니다.
  - `claude/followup_task_breakdown_260827.md`, `followup_priority_matrix_260827.md`, `etpd_과제표_원안정합성진단_260827.md`, `eTPD_변화혁신과제_매칭_초안_20260826.md`/`_20260827.md`, `eTPD_변화혁신과제_ExecutiveSummary_20260826.md`/`_20260827.md`, `etpd_통합_한일_최종성과_260827.md`, `change_innovation_task_mapping_260826.md` — 별도의 "eTPD 변화혁신과제"(내부 조직 프로그램) 관련 문서로 판단, GD/TED 질환 리서치와 직접 관련 없음
  - `AL_amyloidosis_epidemiology_market_sizing_260826.md` — 다른 질환(AL amyloidosis)
  - `target_review_status_260824.md`, `deck_architecture_and_scoring_framework.md` — GD/TED 전용 문서는 아니지만 **cross-target 공통 프레임워크**로서 GD_TED_report.md Section E와 meeting_notes의 1-E(eTPD 분자설계 전략)에서 직접 참조되고 있음(예: Gate G1-G6 프레임, Clone competitiveness 기준 G4). 이 폴더에는 복사하지 않았으나, 필요 시 claude.ai Project에서 별도로 가져와 `_shared/`에 추가하는 것을 권장(§3 참조)
  - `DW_eTPD_Target_DeepDive_*.pptx`(v8/v9), `DW_eTPD_Crosscut_Draft_260824.pptx` — PPTX 파일(비-md), 슬라이드 레이아웃 참고용으로 한 번 사용된 적 있음(execution_log 16:05 참조)

---

## 1. 지금까지의 작업 흐름 요약

1. **2026-09-11**: Plan 세션에서 `GD_TED_plan.md` 확정 (Section A-E 구조, Global+7MM 역학, preclinical 포함 active pipeline, eTPD를 Section E로 분리)
2. **2026-09-11~14**: Work 세션에서 Section A(역학) → B(기전) → C(치료 지형, C4 파이프라인은 사용자의 Cortellis export 제공 후 완료) → D(핵심 임상시험) → E(eTPD 시사점) 순차 작성, 독립 QA 에이전트 리뷰로 5개 FAIL 항목 수정
3. **2026-09-14**: 내부 공유용 20슬라이드 deck 개요 작성 후 실제 pptx(29슬라이드) 제작·전달(`GD_TED_deck_260914.pptx`, 이 폴더에는 미포함 — 필요 시 claude.ai Project에서 별도 확보)
4. **2026-09-14(별도 세션)**: Market Sizing & TSAb-IgG Coverage 분석 트랙 진행 — `GD_TED_market_sizing_report.md` 완성
5. **2026-09-22**: 미팅에서 나온 후속 리서치 요청들을 정리(`meeting_notes_organized_260922.md`) — eTPD/GD-TED 트랙(Part 1, §1-A~1-F)과 B cell TCE 트랙(Part 2, 이 repo와 무관)으로 분리
6. **2026-09-23**: `meeting_notes_organized_260922.md`의 Part 1 액션아이템 + Google Drive `260922_meeting_action_tracker` 시트의 `eTPD_GD_TED` 시트 내용을 기반으로 **Linear 프로젝트 신규 생성**(아래 §2)
7. **2026-09-24(현재 작업)**: 위 9개 파일 + 본 handoff 문서를 로컬 폴더에 정리, GitHub repo 구조 설계 착수(본 문서)

---

## 2. Linear 프로젝트 현황 (이미 생성 완료)

- **Team**: JHa_Res (`74b3b53e-947e-4a21-8690-7ea69b79b0b3`)
- **Project**: P-JHA-4 "eTPD GD/TED 후속 리서치 (2026-09-22 미팅 액션아이템)"
  - URL: `https://linear.app/jha-res/project/etpd-gdted-후속-리서치-2026-09-22-미팅-액션아이템-287e3afb456e`
  - Lead: jain ha
  - 연결 리소스: Google Drive `260922_meeting_action_tracker` 시트
- **구조**: 대분류(cluster)마다 별도 상위 이슈 + 하위 이슈를 행 단위 1:1 매핑 — GitHub repo는 아직 연결되지 않음(repo 생성 후 연결 필요, §4 참조)
- 모든 이슈 설명에는 "산출물은 현재 claude.ai Project 문서로 가되, repo 경로는 미확정"이라는 caveat이 명시되어 있음 — **repo가 준비되면 각 이슈의 산출물 경로를 실제 repo 상대경로로 업데이트해야 함**(Linear 이슈 자체를 다시 열어 설명을 수정하는 작업, 아래 §5 Step 4)

### 2.1 6개 Milestone / Parent Issue (Cluster) 매핑

| Cluster # | Milestone명 | Parent Issue | meeting_notes 대응 섹션 |
|---|---|---|---|
| 1 | 경쟁약물 Line/Class 정리 | JHA-64 | Part 1, §1-A |
| 2 | TED 임상경쟁 및 FcRn 항체 전략 | JHA-65 | Part 1, §1-B |
| 3 | Mechanism 딥다이브 | JHA-66 | Part 1, §1-C |
| 4 | TAM/SAM 및 약가 | JHA-67 | Part 1, §1-D |
| 5 | eTPD 분자설계 전략 | JHA-68 | Part 1, §1-E |
| 6 | Deck 제작 | JHA-69 | Part 1, §1-F |

### 2.2 19개 Child Issue 전체 목록

| Issue | 제목 | Cluster | 비고 |
|---|---|---|---|
| JHA-70 | GD Line-of-therapy 표 작성 | 1 | |
| JHA-71 | TED Line-of-therapy 표 작성 | 1 | |
| JHA-72 | Class별 한계 비교표 작성 | 1 | |
| JHA-73 | MoA×Phase 매트릭스 확장 | 1 | |
| JHA-87 | Address 가능 환자군 교차분석 | 1 | `blockedBy: JHA-70, 71, 72, 73` |
| JHA-74 | FcRn 항체 GD/TED 진입 전략 조사(argenx/Immunovant IR 자료) | 2 | |
| JHA-75 | Placebo 대비 성공/실패 경쟁구도 요약표 | 2 | |
| JHA-76 | IGF-1R class-effect 부작용 비교표 | 3 | |
| JHA-77 | IGF-1R autoantigen-autoantibody 섹션 검토 | 3 | |
| JHA-78 | Orbital fibroblast 내 IGF-1R 기능적 evidence 성숙도 정리 | 3 | |
| JHA-79 | TSHR-IGF1R crosstalk 딥다이브(최신 문헌 2024-2026) | 3 | |
| JHA-80 | "R1b"(에이프릴바이오 discontinued asset) 확인 | 3 | 근거 단서 약함, 낮은 우선순위 |
| JHA-81 | Teprotumumab vs veligrotug 약가 비교 | 4 | |
| JHA-82 | TAM/SAM 재검토(약가 비교 반영) | 4 | |
| JHA-83 | TSHR ectodomain shedding rate 문헌 확인 | 5 | **High priority**, eTPD 분자설계의 선행조건 |
| JHA-84 | 경쟁사 pipeline × biological data 교차분석(공통 패턴 추출) | 5 | |
| JHA-85 | Clone competitiveness 평가기준 정의 | 5 | `deck_architecture_and_scoring_framework.md` Section 4.1 인용 |
| JHA-88 | eTPD 분자 스펙 초안 작성 | 5 | `blockedBy: JHA-83, 84, 85` |
| JHA-86 | Deck 시각자료 슬롯 확인(구조/조직/세포/signaling) | 6 | |

**"프로티나" 벤더 feasibility 확인**(meeting_notes §1-E-2)과 **B cell TCE 트랙 전체**(meeting_notes Part 2)는 각각 사용자의 벤더 컨택 진행 여부에 의존하거나 이 repo와 무관한 별도 트랙이라 Linear 이슈로 만들지 않았습니다(원 AskUserQuestion 답변: "이번엔 제외").

---

## 3. GitHub Repo 구조 제안

### 3.1 이전 세션 논의(b-cell-targeting repo) 대비 이 프로젝트의 차이

과거 다른 프로젝트(b-cell-targeting) 논의에서 제안됐던 4가지 아이디어를 이 프로젝트에 어떻게 적용할지 정리합니다:

| 아이디어 | b-cell-targeting 맥락 | GD/TED 이 프로젝트 적용 |
|---|---|---|
| `00_legacy_unsorted/` | 기존 산발적 파일을 일단 모아두는 폴더 | **그대로 적용** — 이 폴더의 9개 원본 파일은 repo 생성 시 우선 `00_legacy_unsorted/`에 넣고, 시간 날 때 아래 cluster 폴더로 재배치 권장(억지로 지금 당장 완벽 분류할 필요 없음) |
| Top-level 축 선택(milestone-based 추천, 1:1 Linear 매핑) | 순차적 M0-M5 마일스톤 | 이 프로젝트는 **순차적이지 않고 6개 병렬 cluster**(§2.1) 구조 — "milestone-based"의 정신(Linear 구조에 1:1 대응)은 유지하되, 순번이 아니라 **cluster 축**으로 적용. 아래 3.2 참조 |
| `_shared/` 공통 참조자료 폴더 | 여러 이슈가 공유하는 자료 | **그대로 적용** — `GD_TED_report.md`/`GD_TED_reference.md`/`GD_TED_qa_checklist.md`는 모든 cluster가 공통으로 참조하므로 `_shared/`에 위치 |
| Frontmatter 필수 필드(Linear ID/생성일/Source tool·session/Milestone·status) | 세션 파편화 방지 | **그대로 적용** — 각 cluster 산출물 파일에 아래 3.3 템플릿 사용 권장 |

### 3.2 제안 폴더 구조

```
GD_TED/
├── README.md                          # repo 목적, 이 handoff 문서로의 링크, Linear 프로젝트 링크
├── 00_legacy_unsorted/                # 이번에 복사한 9개 원본 파일 우선 착지 지점
│   ├── GD_TED_plan.md
│   ├── GD_TED_market_sizing_plan.md
│   ├── GD_TED_report.md
│   ├── GD_TED_reference.md
│   ├── GD_TED_market_sizing_report.md
│   ├── GD_TED_execution_log.md
│   ├── GD_TED_deck_outline_260914.md
│   ├── GD_TED_qa_checklist.md
│   └── meeting_notes_organized_260922.md
├── _shared/                           # cluster 무관 공통 참조자료 (legacy에서 승격 또는 신규 링크)
│   ├── reference.md                   # GD_TED_reference.md 승격본 — 신규 산출물도 이 번호체계에 이어서 인용
│   ├── qa_checklist.md                # GD_TED_qa_checklist.md 승격본
│   └── deck_architecture_and_scoring_framework.md   # (선택) claude.ai Project에서 별도 확보 시 추가 — G1-G6 Gate 프레임, JHA-85가 직접 참조
├── 01_competitive_landscape/          # Cluster 1 — JHA-64 (+70,71,72,73,87)
│   ├── README.md                      # cluster 목적, 대응 Linear issue 목록
│   ├── gd_line_of_therapy.md          # JHA-70
│   ├── ted_line_of_therapy.md         # JHA-71
│   ├── class_limitation_matrix.md     # JHA-72
│   ├── moa_phase_matrix_extended.md   # JHA-73
│   └── addressable_population_crosscheck.md  # JHA-87
├── 02_ted_fcrn_strategy/              # Cluster 2 — JHA-65 (+74,75)
│   ├── README.md
│   ├── fcrn_entry_strategy_ir_review.md   # JHA-74
│   └── placebo_competitive_summary.md     # JHA-75
├── 03_mechanism_deepdive/             # Cluster 3 — JHA-66 (+76,77,78,79,80)
│   ├── README.md
│   ├── igf1r_class_effect_ae.md       # JHA-76
│   ├── igf1r_autoantigen_review.md    # JHA-77
│   ├── orbital_fibroblast_igf1r_maturity.md  # JHA-78
│   ├── tshr_igf1r_crosstalk_deepdive.md      # JHA-79
│   └── r1b_asset_identification.md    # JHA-80
├── 04_tam_sam_pricing/                # Cluster 4 — JHA-67 (+81,82)
│   ├── README.md
│   ├── teprotumumab_veligrotug_pricing.md    # JHA-81
│   └── tam_sam_revision.md            # JHA-82
├── 05_etpd_molecular_design/          # Cluster 5 — JHA-68 (+83,84,85,88)
│   ├── README.md
│   ├── tshr_shedding_rate.md          # JHA-83 (선행조건, High priority)
│   ├── competitor_pipeline_pattern_analysis.md  # JHA-84
│   ├── clone_competitiveness_criteria.md        # JHA-85
│   └── molecule_spec_draft.md         # JHA-88 (JHA-83/84/85 완료 후)
└── 06_deck/                           # Cluster 6 — JHA-69 (+86)
    ├── README.md
    ├── visual_slot_review.md          # JHA-86
    └── (완성 pptx는 git 대신 별도 저장 권장 — 3.4 참조)
```

### 3.3 산출물 파일 Frontmatter 템플릿

각 cluster 폴더의 산출물 `.md` 파일은 다음 frontmatter를 필수로 포함할 것을 권장합니다(과거 b-cell-targeting 논의에서 나온 "6개 독립 세션 파편화 방지" 원칙 재사용):

```yaml
---
linear_issue: JHA-70          # 대응 Linear 이슈 번호 (필수)
created: 2026-09-24            # 작성일 (필수)
source: claude-code             # 작성 도구/세션 종류 — claude-code | claude-ai | manual 등 (필수)
milestone: cluster-1-competitive-landscape   # 대응 cluster (필수)
status: draft                   # draft | in-review | done — Linear 이슈 status와 동기화 권장 (필수)
---
```

### 3.4 PPTX/바이너리 파일 정책

`GD_TED_deck_260914.pptx`(29슬라이드, claude.ai Project에 저장됨)처럼 큰 바이너리 산출물은 git repo에 직접 커밋하기보다:
- Git LFS를 쓰거나
- `06_deck/`에는 outline/README만 두고 실제 pptx는 claude.ai Project 또는 별도 파일 저장소에 두고 링크만 남기는 방식

중 하나를 repo 생성 시점에 정해야 합니다(아래 §5 Step 3, 열린 질문).

---

## 4. Repo 생성 및 초기 설정 체크리스트

Claude Code 세션에서 다음을 순서대로 진행하면 됩니다.

1. **Repo 생성 확인/초기화**
   - `https://github.com/bioJain/GD_TED`가 이미 존재하는지 확인 (`gh repo view bioJain/GD_TED` 또는 웹 확인)
   - 없다면 생성: `gh repo create bioJain/GD_TED --private` (private 여부는 사용자 확인 필요 — 미확정)
   - README.md, LICENSE(필요 시), .gitignore(node_modules, .DS_Store 등) 기본 세팅

2. **폴더 구조 생성**
   - §3.2의 폴더 구조를 로컬에 먼저 만들고, 이 폴더(`eTPD_GD,TED/`)의 9개 파일을 `00_legacy_unsorted/`로 이동(복사 아닌 이동 — 이 로컬 Obsidian vault 폴더가 원본 보관처가 아니라 repo가 원본이 되어야 함, 단 이 판단은 사용자 확인 필요 — §6 참조)
   - `_shared/`, `01_`~`06_` 각 cluster 폴더에 README.md 스텁 생성(각 cluster의 목적 1-2문장 + 대응 Linear issue 링크)

3. **PPTX 정책 결정 및 반영**(§3.4의 열린 질문 — 사용자 확인 후 진행)

4. **Linear 프로젝트에 GitHub repo 연결**
   - Linear 프로젝트 P-JHA-4에 GitHub 통합이 설정되어 있는지 확인, 없다면 워크스페이스 설정에서 GitHub 연동 활성화
   - 25개 이슈(6 parent + 19 child) 각각의 설명 중 "repo 경로는 미확정"이라고 되어 있는 부분을 실제 repo 상대경로(§3.2 파일 매핑 표 기준)로 업데이트 — `mcp__Linear__save_issue`로 description 수정
   - 예: JHA-70 설명의 산출물 경로를 `claude.ai Project 문서 (임시)` → `01_competitive_landscape/gd_line_of_therapy.md`로 갱신

5. **첫 커밋**
   - `00_legacy_unsorted/`의 9개 파일 + 본 handoff 문서 + 폴더 구조 스텁을 초기 커밋으로 push
   - 커밋 메시지 예: `"Initial import: GD/TED research corpus from claude.ai Project + Linear project handoff"`

6. **작업 시작**
   - Linear 이슈 우선순위대로 작업(JHA-83 TSHR shedding rate가 High priority + JHA-88의 선행조건이므로 우선 착수 권장)
   - 각 이슈 완료 시: 해당 cluster 폴더에 frontmatter 포함 산출물 저장 → git commit → Linear 이슈를 상응 status로 업데이트(가능하면 GitHub-Linear 연동으로 커밋 메시지에 `JHA-70` 언급 시 자동 링크되도록 활용)

---

## 5. 열린 질문 (사용자 확인 필요 — Claude Code 세션이 임의로 결정하지 말 것)

1. **Repo 가시성**: `bioJain/GD_TED`를 private로 생성할지 public으로 생성할지 미확정
2. **로컬 Obsidian vault 폴더의 역할**: 이 폴더(`C:\Users\jain\OneDrive\Obs_Vault1\D50_sources\public\eTPD_GD,TED`)가 앞으로도 원본 보관처로 남을지, 아니면 GitHub repo가 유일한 원본(source of truth)이 되고 이 폴더는 스냅샷/백업 성격으로만 남을지 — repo 생성 후 파일을 "이동"할지 "복사 유지"할지가 여기 달림
3. **PPTX/바이너리 저장 정책**(§3.4): Git LFS vs 외부 저장 + 링크
4. **`_shared/deck_architecture_and_scoring_framework.md`, `target_review_status_260824.md` 포함 여부**: 이 두 문서는 GD/TED 전용이 아닌 cross-target 공통 프레임워크지만 JHA-85 등 일부 이슈가 직접 참조함 — repo `_shared/`에 사본을 둘지, 아니면 claude.ai Project 링크만 남길지
5. **폴더 구조 자체의 최종 승인**: §3.2 제안은 초안입니다 — 6-cluster 병렬 구조가 실제 작업 진행 중 사용성이 떨어진다고 판단되면(예: 여러 cluster에 걸치는 산출물이 많아지는 경우) output-type 축(예: `epidemiology/`, `mechanism/`, `pipeline/`, `market/` 등 GD_TED_report.md의 Section A-E 축)으로 재구성하는 대안도 있음 — 실제 작업 몇 건 진행 후 재평가 권장

---

## 6. 참고 — 이 문서를 만든 claude.ai 세션 정보

- claude.ai Project: "6T_review_26_H2" (설명: "reviewing the candidate targets for extracellular degradation")
- 사용자: joehalee@gmail.com
- 이 handoff는 사용자가 "GD, TED 관련 md 파일들 copy + Claude Code 세션 이어가기용 handoff 작성"을 요청한 데 따른 산출물입니다(원 요청: "해당 폴더에 현재 프로젝트 claude 폴더 중, GD, TED 관련 md 파일들 copy해서 복사해놓기 바람. 그리고 난 다음에 이 세션을 claude code에서 이어하기 위한 handoff 작성해서 해당 폴더에 함께 저장. - github repo용 자료 구조 짜고, 설정해야하는 것 등.")
- 가운뎃점(·) 미사용 원칙이 사용자 서식 선호로 지정되어 있어 본 문서 및 위 9개 원본 파일 전체에 적용/유지되어 있습니다.
