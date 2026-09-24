---
title: GD_TED_qa_checklist
목적: report.md 완성 후 별도 QA 세션에 공급할 검토 체크리스트 (GD_TED_plan.md §6.2 원문)
---

# QA Checklist — Graves' Disease & TED 종합 분석

## QA 에이전트 시스템 프롬프트 (별도 세션 실행 시 사용)

```
You are a scientific quality assurance agent reviewing a comprehensive disease analysis report on Graves' Disease (GD) and Thyroid Eye Disease (TED).

Your task: systematically evaluate the attached report.md against the provided qa_checklist.md.

For EACH checklist item:
- Mark: PASS / FAIL / PARTIAL
- If FAIL or PARTIAL: quote the exact problematic text; explain the specific error; suggest a concrete correction
- Do not give benefit of the doubt on factual inaccuracies

Standards:
- Scientific rigor: no unqualified claims; uncertain mechanisms labeled as "proposed" or "under investigation"
- Citation integrity: every factual claim has [x] in-line citation; [x] matches reference.md numbering
- No marketing language ("revolutionary", "breakthrough", "game-changing")
- Language: Korean body text; English technical terms preserved; no middle dots (·)
- Pipeline scope: preclinical + active only; no discontinued/NDR assets included
- eTPD content: confined to Section E only; not present in Sections A-D

Output format: table (checklist item | PASS/FAIL/PARTIAL | comment/correction)
```

## 체크리스트

**[A] 질환 구분/개념 정확성**
- [ ] A1: GD와 TED를 별개 질환으로 구분하면서 연관성 명시 (TED ≠ GD, but ~90-95% TED is GD-associated)
- [ ] A2: TED가 GD 없이도 발생 가능함을 기술 (~5-10% TED: euthyroid or hypothyroid)
- [ ] A3: GD 환자에서 TED 발생 비율 올바르게 기술 (mild orbital changes ~50%; clinically significant TED ~20-25%)

**[B] 역학 수치 정확성**
- [ ] B1: GD incidence와 prevalence 수치가 registry/cohort study 이상 근거에서 인용됨
- [ ] B2: TED epidemiology는 GD 대비 비율 또는 독립 수치로 명확히 제시됨
- [ ] B3: 7MM 국가별 수치 — 단일 출처 의존 시 명기됨; 복수 출처 교차확인 권장
- [ ] B4: Incidence와 prevalence 혼동 없이 구분 제시

**[C] Staging/Severity 정확성**
- [ ] C1: CAS 체계 정확히 기술 — 7점 (첫 방문) vs. 10점 (추적 방문) 구분
- [ ] C2: EUGOGO 3 tier 각 기준 구체적 수치 포함하여 정확히 기술
- [ ] C3: NOSPECS 7 class 개요 정확히 기술
- [ ] C4: GD 자체에 대한 공식 staging system 부재 사실 명기

**[D] 병리기전 정확성**
- [ ] D1: TSAb (stimulating) vs. TBAb (blocking) vs. neutral TRAb 구분 정확히 기술
- [ ] D2: TSHR-IGF-1R 복합체 가설 — 확립된 사실이 아닌 "proposed" / "under investigation" 명기
- [ ] D3: Thy-1+ (myofibroblast 분화) vs. Thy-1- (adipocyte 분화) fibroblast 운명 정확히 기술
- [ ] D4: RAI가 TED 악화 위험을 가질 수 있다는 사실 기술; 흡연 동반 시 위험 증가 포함
- [ ] D5: TED active phase (Th1 dominant) vs. inactive/fibrotic phase (Th2/TGF-β dominant) cytokine milieu 차이 기술
- [ ] D6: 흡연이 TED #1 modifiable risk factor임을 명시

**[E] 치료제 정보 정확성**
- [ ] E1: Teprotumumab FDA 승인일 (2020년 1월) 및 적응증 (moderate-to-severe active TED) 정확
- [ ] E2: Teprotumumab 주요 AE — 청각 관련 (hearing loss, hyperacusis, tinnitus) 명기; reversibility 불확실성 포함
- [ ] E3: IVMP가 active TED 1차 SoC로 기술 (EUGOGO guideline 근거)
- [ ] E4: ATD 재발률 수치 출처 명시됨
- [ ] E5: RAI 후 TED 악화 예방을 위한 prednisolone 투여 권고 기술
- [ ] E6: 파이프라인 각 자산의 임상 단계가 indication-specific으로 확인됨 (Highest Status trap 적용 여부 확인)
- [ ] E7: Discontinued/NDR 자산이 포함되지 않음 (본 작업 범위 명시 기준)

**[F] 인용/참고문헌 정확성**
- [ ] F1: report.md 본문 모든 사실 claim에 [x] in-line citation 존재
- [ ] F2: [x] 번호가 reference.md 번호와 전수 일치
- [ ] F3: reference.md 중복 항목 없음
- [ ] F4: 무작위 샘플 5개 이상 PMID 실존 검증
- [ ] F5: 마케팅 언어 없음
- [ ] F6: 불확실한 mechanism/claim에 근거 수준 표현 사용 ("suggested", "proposed", "under investigation", "in vitro only" 등)

**[G] eTPD 섹션 분리 원칙**
- [ ] G1: eTPD 관련 내용이 Section A-D에 없고 Section E에만 기술됨
- [ ] G2: eTPD 시사점에서 speculative 항목에 근거 수준 명기
- [ ] G3: FcRn inhibitor vs. eTPD TSAb-selective 접근의 차별화 포인트 명확히 기술

**[H] 언어/형식**
- [ ] H1: 영어 기술 용어 (TSHR, IGF-1R, TSAb, CAS, EUGOGO, TRAb, FcRn 등) 영문 유지
- [ ] H2: 가운뎃점(·) 미사용 — 슬래쉬(/), 쉼표(,), 세미콜론(;) 적절 사용
- [ ] H3: 개조식(명사 종결형) 문체 유지
