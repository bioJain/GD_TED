---
name: GD_TED_market_sizing_plan
description: GD/TED 시장성(TAM/SAM range) 및 TSAb-IgG targeting coverage 분석 작업 개요 — market-sizing-multitrack 스킬을 경량 모드로 적용
sources: [chat]
aliases: [GD TED market sizing, TSAb coverage, market sizing plan, market-sizing-multitrack 적용]
---

# Graves' Disease & TED — Market Sizing 작업 개요 (Plan)

> 작성일: 2026-09-14
> 기존 GD_TED_plan.md(질적 disease landscape 분석)와 별개 트랙, 동일 프로젝트(6T_review_26_H2)에 귀속
> 사용자 승인 완료 파라미터 기준 확정

---

## 1. 목적

- GD, TED 각각 독립적으로 총 예상 가능 시장(TAM) 및 mechanism-narrowed SAM range 파악
- TSAb-IgG-targeting 접근 시 각 적응증의 환자 coverage(= TSAb가 질환을 실제로 driving하는 환자 비율) 정량화 — NSCLC EGFR C797S 유사 개념
- 재무모델(bottom-up epi×price) 자체 구축은 차선책; 공개 마켓 리포트 초록/샘플 기반 range 확보가 1차 목표

## 2. market-sizing-multitrack 스킬 적합성 평가

| 항목 | 평가 |
|---|---|
| 2x2 트랙 프레임(top-down/bottom-up × current/premium) | 그대로 적합 — range(FLOOR/PREMIUM) 산출 목적에 정확히 부합 |
| Step 0 mechanism causality gate (Driver/Co-driver/Epiphenomenon) | 이번 TSAb coverage 질문에 정확히 대응하는 틀 — GD/TED 각각 verdict 판정이 곧 이번 작업의 핵심 산출물 |
| Step 7 기본 산출물(Excel 라이브수식 모델 + CSV + 리포트) | 과설계 — 이번엔 Excel 풀모델 생략, 경량 표/CSV + 한글 요약 리포트로 축소 |
| Track C/D(bottom-up epi×price) 전체 구축 | 이번엔 보조/sanity-check 용도로만 경량 사용, 별도 재무모델 미구축 |
| Biomarker bottom-up track | 이번 작업의 실질적 핵심 — TSAb seropositivity/driving 비율 기반 mechanism-eligible 인구 산출에 활용 |

결론: 스킬의 방법론(2x2 프레임 + causality gate)은 이번 작업에 적합하게 설계되어 있음. 다만 Step 7 산출물 스펙은 그대로 쓰지 않고 경량화하여 적용.

## 3. 확정 파라미터 (승인 완료)

| 항목 | 결정 |
|---|---|
| 작업 깊이 | Range 우선 경량 방식 — Track A/B(top-down) 우선 수집, Track C/D는 보조 |
| 지역 범위 | Global + 7MM (US/DE/FR/UK/IT/ES/JP) — 기존 GD_TED_plan.md 역학 범위 재사용 |
| TSAb 프레이밍 | TSAb-targeting 계열 전체 광의 정의 (FcRn inhibitor, TSHR-blocking Ab, eTPD/sweeping-Ab 등 modality 무관 — "TSAb가 질환을 driving하는 환자 비율" 자체를 계산) |
| 작업 귀속 | 기존 6T_review_26_H2 프로젝트(019ff321)에 통합 — GD_TED_plan.md의 역학 계획과 연계, 중복 수집 방지 |

## 4. Step -1/0 스킬 적용 매핑

- 자산/메커니즘 지정 여부: Yes (TSAb-targeting 계열, 광의) → TAM + SAM 모두 산출
- 적응증 개수: 2개(GD, TED) 각각 독립 산정하되, TED의 ~90-95%가 GD 맥락에서 발생하는 population overlap 존재 → cross-indication 합산 수행하지 않고 overlap을 별도 명시 (스킬 Step 5.6 원칙 준용)
- Step 0 causality gate 예비 가설 (문헌 확인 후 확정):
  - GD: TSAb = **Driver** (TSHR 자극 → 갑상선호르몬 과다생성의 직접 기전; 확립된 사실)
  - TED: TSAb = **Co-driver** (가능성) — IGF-1R 경로의 독립적/공동 관여 논쟁 존재; TRAb-negative TED(~5-10%, 기존 GD_TED_plan.md A2 메모) 존재가 "TSAb 비의존적 TED subset"의 근거 → coverage가 100% 미만일 가능성 높음, 정확한 수치는 문헌 확인 필요

## 5. Track 설계 (경량 모드)

| Track | 방법 | 우선순위 |
|---|---|---|
| A. Top-down/current | 공개 마켓 리포트 executive summary/PR (DelveInsight, GlobalData, GrandView, Coherent, IMARC 등) 수집, median+range | 최우선 |
| B. Top-down/premium | 동일 소스의 peak/premium 매출 전망치 | 최우선 |
| C. Bottom-up/current | 역학 cascade(유병률→진단→치료) × 현행가 — sanity check | 보조 |
| D. Bottom-up/premium | 역학 cascade × premium anchor(teprotumumab 등) — sanity check | 보조 |
| Biomarker bottom-up | TSAb-driving 비율(seropositivity/causality 문헌) 기반 mechanism-eligible 인구 산출 | 핵심 (coverage 질문 직접 답변) |

## 6. 데이터 수집 계획

- Track A/B: Web search로 GD/TED market size 공개 리포트 executive summary/press release 수집 (paywall 리포트는 초록 수준만); teprotumumab(TEPEZZA) 실매출(Amgen 실적발표)을 real-world anchor로 보완
- Coverage 계산용 역학: PubMed — GD에서 TRAb/TSAb seropositivity rate, TED에서 TSAb 양성률 vs TRAb-negative TED 비율, IGF-1R pathway 독립 기여 문헌 — 기존 GD_TED_plan.md Section A2/B3/B4 query와 중복되므로 그 결과 재사용 가능
- ClinicalTrials.gov: 이번 market sizing 작업 범위에서는 불필요 (파이프라인은 기존 GD_TED_plan.md Section C/D에서 별도 진행)

## 7. 산출물

- Market sizing 요약 리포트 (한글, 개조식): GD/TED 각각 TAM/SAM range(FLOOR/PREMIUM), TSAb-driving coverage %(evidence grade 포함), GD-TED overlap 설명, 출처 quality flag, limitations
- 수집 원자료 경량 표/CSV

## 8. 다음 단계

승인된 개요 기준으로 Work 세션(데이터 수집 및 산출물 작성) 진행 대기
