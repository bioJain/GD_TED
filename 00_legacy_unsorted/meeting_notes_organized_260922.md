# 2026-09-22 미팅 메모 정리 — eTPD(GD/TED) & B cell TCE Autoimmune/I&I

> 원본: 2026-09-22 15:14 자료 공유 미팅 코멘트 메모(두서없이 작성됨)
> 작성 배경: 두 개 독립 주제(① eTPD 타겟/적응증 리서치 — GD/TED 트랙, ② B cell TCE autoimmune/I&I 전략)로 분리해 코멘트/피드백/확인질문/액션아이템으로 재구성. 기존 GD_TED_plan.md, GD_TED_report.md, GD_TED_market_sizing_report.md, bcell-tce-autoimmune-strategy.md(메모리) 대비 이미 다뤄진 내용은 "기완료"로 표시하고, 신규 내용만 액션아이템으로 계층화함.
> 모호한 조각 4건은 사용자 확인 완료(하단 §0 참조), 그 결과를 반영해 작성.

---

## 0. 모호했던 메모 조각 — 확인 결과

| 조각 | 확인 결과 | 후속 처리 |
|---|---|---|
| "RA 임상/치료법 trend - therapy line 확인할 것" | RA는 계속 Tier C(배제) 유지, therapy line 데이터는 다른 Tier A 질환(MG/PV+NMOSD/pSS) 비교용 벤치마크로만 수집 | Part 2 §A에 벤치마크 자료로 편입 |
| "프로티나" | 항체 서열 engineering 벤더사(고유명사, 구체 계약/역량 범위는 별도 확인 필요) | Part 1 §E에 벤더 feasibility 확인 액션아이템으로 반영 |
| "R1b" | 확정 아님 — 사용자 추정: IGF1R이 아니라 한국 에이프릴바이오(April Bio)가 개발하다 중단한 에셋의 타겟을 지칭한 것으로 추정, cytokine 계열 가능성. 사용자 본인도 "확인 필요"로 표시 | Part 1 §C에 조사 항목으로 등록(에이프릴바이오 discontinued asset 타겟 확인) |
| "shedding 되는 비율이 높지 않아서 IC" | TSHR은 (shedding 정도와 무관하게) 다른 자가면역질환처럼 면역복합체(IC) 침착에 의한 염증 기전과는 다르게 작동할 것이라는 취지. TSHR ectodomain shedding 정도 자체는 미확인 상태 | Part 1 §E에 두 갈래로 반영: (1) TSHR 병인기전은 IC 침착형이 아니라는 전제를 eTPD 설계 근거에 명시, (2) shedding rate 자체는 별도 확인 필요 항목으로 유지 |

---

# Part 1. eTPD — GD/TED 트랙

## 1-A. 경쟁 약물 지형: Line/Class별 정리 (신규)

**원문 코멘트**
> "group - 질환을 놓고, 약물 class가 어떤 것들이 있고, 어떤 기전이 있고, 가장 유의한 것이고, 어떤 순서로 쓰고 있는지 - 임상 환자들이 address 가능한 환자군" / "경쟁 약물을 정리하고 - 처리하고 있는 현재 약물 순서(line별 정리) / class 별로 정리 / class의 단점이 있는지" / "TSHR - 시장의 unmet needs만 있으면 할 만 함"

**현황 대비 평가**: GD_TED_report.md Section C4에 MoA class × 개발단계(Phase) 매트릭스는 이미 존재하나, **"현재 임상 현장에서 어떤 순서(line)로 약물을 쓰는지"**와 **"class별 한계/단점을 정리한 비교표"**는 아직 없음 — 이 부분이 이번 메모의 핵심 신규 요청으로 판단됨.

**피드백/시사점**
- Section C6(Unmet Needs)에 이미 일부 class 한계가 흩어져 있음(teprotumumab 고비용/청각AE, ATD 재발, RAI의 TED 악화 위험 등) — 이를 line-of-therapy 축으로 재편집하면 됨
- "TSHR - 시장의 unmet needs만 있으면 할 만함" 코멘트는 기존 Section E4 결론(GD를 1차 적응증으로 — 명확한 PD biomarker + unmet need)과 방향이 일치 — 재검증 성격의 코멘트로 판단, 별도 조사보다는 기존 결론 확인/브리핑에 가까움

**Action items**
1. GD 치료 line 표 작성: 1차(ATD) → 2차(RAI/수술) → 재발시 옵션 — 각 단계에서 놓치는 환자군(재발, 임신, ATD 불응 등) 명시
2. TED 치료 line 표 작성: 1차(IVMP/selenium) → 승인 표적치료(teprotumumab/veligrotug 등) → 재발/무반응시 옵션(off-label rituximab/tocilizumab 등)
3. Class별 한계 비교표(1장) 작성 — ATD/RAI/수술/IVMP/IGF-1R mAb/FcRn 억제제/TSHR 직접길항/TSAb-IgG sweeping, 각 class의 핵심 한계 1-2줄
4. 위 3개 산출물을 "address 가능한 환자군" 관점으로 교차 — 어느 class 조합에도 걸리지 않는 잔여 환자군(예: TRAb 음성 TED, inactive TED, ATD 장기불응 GD) 재확인 — Section C6과 통합

---

## 1-B. TED 임상 경쟁 구도 및 FcRn 항체 진입 전략 (부분 신규)

**원문 코멘트**
> "TED 임상 경쟁 - placebo 약물" / "FcRn antibody 가 어떻게 임상을 들어간 이유/전략"

**현황 대비 평가**: Section D(핵심 임상시험)와 Section E2(efgartigimod VitaliThy/UplighTED CT.gov 원문 대조)가 관련 사실을 이미 확보 — UplighTED가 placebo 대비 효능 futility로 종료된 사실도 이미 반영됨. 다만 **"FcRn 항체들이 GD/TED에 진입한 전략적 이유"**(예: 기승인 적응증 gMG/CIDP에서 GD/TED로 label expansion하는 규제/상업 전략, 왜 GD를 먼저 택했는지 등)는 기전적 관찰(E2)만 있을 뿐 전략적 해석은 부족.

**Address해야 할 질문**
- efgartigimod/imeroprubart가 GD를 첫 확장 적응증으로 택한 것이 순수 mechanistic 판단(E2 결론과 일치)인지, 아니면 상업적 판단(기존 gMG/CIDP 처방 기반 활용, 규제 경로 익숙함 등)이 더 컸는지 — 공개된 문헌/IR 자료로는 구분이 어려울 수 있음, 확인 가능한 범위 내에서 조사

**Action items**
1. argenx/Immunovant의 GD/TED 적응증 확장 관련 investor call, press release, 학회 발표 자료 조사 — "왜 GD 먼저인지" 명시적 언급 여부 확인
2. Placebo-controlled 경쟁 구도 요약표: 어느 자산이 placebo 대비 성공(teprotumumab OPTIC)/실패(UplighTED)했는지 정리 — 기존 Section D/E2 데이터 재편집으로 작성 가능(신규 조사 최소)

---

## 1-C. Mechanism 딥다이브 — TSHR/IGF-1R crosstalk, autoantigen-autoantibody, 병인세포

**원문 코멘트**
> "Igf1r - linsitinib - class-effect side effect? profile" / "IGF-1r autoantigen - autoantibody" / "TSHR - IGF1R(complex) - cross로 영향/signaling 측면을 더 들여다봐야겠음" / "adipocyte / myofibroblast - IGF-1R function / OF - evidence / MoA // 병인세포가 - IGF-1R이 어디까지 연구가 되었는지" / "R1b"(§0 참조)

**현황 대비 평가**
| 항목 | 상태 |
|---|---|
| TSHR-IGF1R complex crosstalk 가설 3종 | **기완료** — Section B4에 경쟁 가설 3개 병기, "proposed" 명시 |
| IGF-1R directly-stimulating antibody 가설 | **부분 기완료** — B4에 NIH 반박 논문 인용, 별도 "IGF-1R autoantigen" 섹션은 없음 |
| Thy-1+/- fibroblast → myofibroblast/adipocyte 분화 운명 | **기완료** — Section B4, 원저(Koumas & Smith 2003) 확인 |
| adipocyte/myofibroblast에서 IGF-1R 자체의 기능적 evidence(OF=orbital fibroblast 추정) 성숙도 | **신규** — 현재는 "IGF-1R이 분화를 매개한다"는 상류 결론만 있고, "IGF-1R 연구가 각 세포유형에서 어디까지 진척되었는지"에 대한 메타적 정리는 없음 |
| Linsitinib의 IGF-1R 억제 class-effect 부작용 프로파일 | **신규** — teprotumumab AE는 깊게 다뤘으나(청각 AE 등), linsitinib을 포함한 IGF-1R class 전체의 공통 부작용(고혈당 등) 비교는 없음 |
| "R1b" (에이프릴바이오 discontinued asset 타겟 추정) | **신규/불확실** — §0 참조, 조사 필요 |

**Action items**
1. IGF-1R class-effect 부작용 비교표 작성 — teprotumumab/linsitinib/veligrotug/elegrobart/MHB-018A/IBI311 등 Section C4 파이프라인 자산 전체 대상, 공통 AE(고혈당, 청각 관련, 근경련 등) vs 개별 자산 특이 AE 구분
2. "IGF-1R autoantigen-autoantibody" 별도 섹션 신설 검토 — B4의 반박 논거(NIH)를 포함해, IGF-1R 자체를 겨냥한 자가항체 존재 여부에 대한 최신 문헌(2024-2026) 재검색
3. Orbital fibroblast(OF) 내 IGF-1R 발현/기능 연구의 성숙도 정리 — adipocyte 분화 경로 vs myofibroblast 분화 경로 각각에서 IGF-1R의 직접적 역할이 in vitro/in vivo 수준에서 얼마나 입증되었는지 evidence grade 부여
4. "R1b" 확인 — 에이프릴바이오(April Bio) discontinued/중단 에셋 목록 조사(예: OX40L, IL-4R, IL-18BP 계열 등 공개 파이프라인 기반 추정 후 확정), GD/TED 연관성 여부 판단

---

## 1-D. TAM/SAM 및 약가

**원문 코멘트**
> "TAM - SAM 산정해봐야 함" / "약가 - teprotumumb / veligrotub 모두 다 적용인지?"

**현황 대비 평가**: TAM/SAM 산정 자체는 GD_TED_market_sizing_report.md에서 **기완료**(GD/TED 각각 FLOOR/PREMIUM range, TSAb-IgG coverage 분석까지 포함). 다만 **teprotumumab과 veligrotug의 약가가 동일 적용되는지**(같은 가격대/보험수가 구조인지, 아니면 veligrotug가 차별화된 가격 전략을 쓰는지)는 시장성 리포트에 반영되지 않은 신규 항목.

**Action items**
1. Teprotumumab(Amgen) vs veligrotug(Viridian) 공식 약가(WAC/list price) 및 보험수가(코드) 비교 조사 — 미국 기준 우선, 가능하면 여타 승인국가(한국 등)도 병기
2. 위 결과를 GD_TED_market_sizing_report.md §2.3(실매출 Anchor) 섹션에 후속 업데이트로 반영 — veligrotug 매출이 축적되는 대로 anchor를 teprotumumab 단독에서 다중 자산으로 확장하는 기존 §5 한계 5번과 연결

---

## 1-E. eTPD 분자설계 전략

**원문 코멘트**
> "antigen = autoantibody - Fc(mutation) - FcRn; FcgRIIb / binding affinity" / "shedding 되는 비율이 높지 않아서 IC"(§0) / "프로티나 feasibility가 working한다면, 알려진 mutation-variation 기반으로 test 기회 존재한다고 봄" / "clone은 우리가 하고, Fc는 프로티나 or 특허 만료된 걸로 시도 / clone 자체가 경쟁력이 있어야 함 - binding하는 거에 있어서 어떤 idea가 있으면 더 좋을지(앞에 leading pipeline이 죽어도 살아남을 수 있도록)" / "경쟁사 pipeline > biological data <-> 공통적인 패턴을 추출해서, 그 기반으로 추천"

**현황 대비 평가**: GD_TED_report.md Section E는 TSAb-selective eTPD 접근의 개념적 적합성(E1)과 FcRn 억제제 대비 차별화(E3)까지는 다뤘으나, **구체적 분자설계**(Fc mutation 조합, FcRn/FcγRIIb affinity engineering, clone 소싱 전략)는 범위 밖이었음 — 이번 메모는 그 다음 단계(실제 분자를 어떻게 만들 것인가)에 대한 코멘트로, 전체가 신규.

**피드백/시사점**
- "TSHR 병인기전이 IC 침착형이 아니다"(§0)라는 전제는 eTPD 분자가 "병원성 IgG(TSAb) 자체를 제거"하는 것으로 충분하다는 기존 E1 논리와 부합 — 즉 IC-mediated 염증 경로를 별도로 고려할 필요가 낮다는 뜻으로, 분자설계를 단순화하는 방향의 근거로 활용 가능(단, shedding rate 자체는 미확인 — 별도 확인 필요)
- clone/Fc 소싱 분리 전략("clone은 우리가, Fc는 외부") 및 "leading pipeline이 죽어도 살아남는 binding idea" 요청은 target_review_status_260824.md/deck_architecture_and_scoring_framework.md에서 이미 정립된 **Gate G4(Engineerability & FTO)/differentiation 논리**와 정확히 같은 축 — 별도 프레임을 새로 만들기보다 기존 Major-3 타겟 검토에 쓴 G4 기준(pH/Ca 의존 결합 설계, 기존 항체/특허 지형, developability)을 GD/TED TSAb-selective 분자에도 동일 적용 권장

**Action items**
1. eTPD 분자 스펙 초안 작성: antigen-binding domain(TSAb 특이적) + Fc(FcRn 결합 engineering, 필요시 FcγRIIb 결합 부가) 조합 — 기존 deck_architecture 문서의 Gate 프레임(G1 accessibility ~ G6 measurability)을 TSAb-selective 분자에 적용해 재점검
2. "프로티나" 항체서열엔지니어링 벤더 feasibility 확인 — 어떤 mutation/variation 라이브러리를 보유하는지, TSAb epitope 대상 적용 가능성 문의(선행 조건: 벤더 컨택/NDA 여부 확인 필요 — 사용자 확인 요망)
3. TSHR ectodomain shedding rate 문헌 확인(§0에서 이월된 미해결 항목) — free antigen 접근성 판단에 직접 영향
4. 경쟁사 pipeline(Section C4의 51개 active 자산) × biological data 교차분석 — "공통 패턴" 추출 프레임 설계: 예) 성공 자산들의 공통 epitope 영역, 실패/중단 자산들의 공통 원인(UplighTED futility 등) — 이를 근거로 한 추천 로직을 별도 1페이지로 synthesis
5. Clone competitiveness 기준 정의 — "leading pipeline 실패해도 생존 가능한 binding idea"의 구체적 평가축(예: epitope 독립성, 기존 특허 미충돌 영역) 문서화 — deck_architecture의 G4/differentiation 논리 재사용

---

## 1-F. Deck 제작 노트

**원문 코멘트**
> "슬라이드에서 key point; '그림' 활용하도록 - 구조 / 조직 / 세포 / signaling"

**현황 대비 평가**: 순수 제작 지침 — GD_TED_deck_outline_260914.md(기존 프로젝트 문서)에 반영 대상. 리서치 액션아이템이 아니므로 덱 작업 단계에서 처리.

**Action items**
1. GD_TED_deck_outline_260914.md 검토 시, 구조(안와 해부) / 조직(orbital fibroblast 등) / 세포(Thy-1+/- 분화) / signaling(TSHR-IGF1R crosstalk 3가설) 각 레벨에 대응하는 다이어그램 슬롯이 있는지 확인, 없으면 추가

---

# Part 2. B cell TCE — Autoimmune/I&I 전략

## 2-A. 질환별 표준 평가축 체크리스트 (Tier A 적용)

**원문 코멘트**
> "병원성 B세포 구획 / CD19 CAR-T 임상 반응성 / a-CD20/Sco 반응성·재발시 escape·sparing / 표적 조직 내 T세포 접근성 및 배경 면역억제제 영향 / 표준치료법(SoC) / 현재 TCE 영향" / "RA 임상/치료법 trend - therapy line 확인할 것"(§0 — 벤치마크 전용으로 확정)

**현황 대비 평가**: bcell-tce-autoimmune-strategy.md(메모리)는 Tier A 심층 대상(MG, PV+NMOSD, pSS)과 작업 인프라(Linear/GitHub)만 기록되어 있고, 질환별 실제 리서치 콘텐츠는 메모리에 요약되어 있지 않음(별도 세션/저장소에서 진행 중인 것으로 추정) — 이번 메모의 체크리스트 자체가 신규 정리로 판단.

**Address해야 할 질문**
- 이 체크리스트가 이미 GitHub 저장소(bioJain/b-cell-targeting) 또는 Linear(JHa_Res)에서 진행 중인 작업과 중복되는지 확인 필요 — 중복이면 이번 정리는 "합의된 체크리스트 재확인" 성격, 신규면 "누락 항목 보완"

**Action items (Tier A 3개 질환: MG / PV+NMOSD / pSS 각각에 적용)**
1. 병원성 B세포 구획(plasmablast/long-lived plasma cell/memory B cell 등) 질환별 정리
2. CD19 CAR-T 임상 반응성 데이터 수집(있는 경우) — MG/pSS는 최근 데이터 존재 가능성 높음, PV/NMOSD는 제한적일 수 있음
3. Anti-CD20(rituximab 등) 반응성 + 재발시 escape 패턴(CD20-low/negative clone 등) + sparing 전략(plasma cell sparing 여부) 정리
4. 표적 조직 내 T세포 접근성(BBB 등 조직장벽) 및 배경 면역억제제(기존 병용약물)의 TCE 효능/안전성 영향 검토
5. 질환별 SoC 정리(1차/2차/재발시)
6. 현재 진행 중인 TCE 자산의 질환별 임상현황 정리
7. RA는 위 1-6 항목을 벤치마크 데이터로만 수집, Tier 배정 변경 없음 — 결과표에 "Tier C(배제) - 벤치마크 전용" 명시하여 혼동 방지

---

## 2-B. 신규 타겟 축 — pDC-Plasma Cell Axis 및 경쟁자산

**원문 코멘트**
> "pDC - Plasma cell (PDCA) <- 중국 쪽 approach??? 찾아볼 것!" / "LBL-047(DNTH212) Leads Biolabs / Dianthus Therapeutics, Bispecific Fusion Protein(Anti-BDCA2 × TACI ectodomain), SLE, Sjogren's disease"

**현황 대비 평가**: 완전 신규 — 기존 bcell-tce-autoimmune-strategy.md에는 B cell TCE(CD3 기반)만 언급, pDC(plasmacytoid dendritic cell)-plasma cell 축이나 BDCA2/TACI 이중표적 접근은 없음. LBL-047은 pSS(Tier A 질환)와 직접 겹치는 경쟁자산으로 **우선순위 높은 조사 대상**.

**Action items**
1. LBL-047(DNTH212) 임상 현황 전수 조사 — ClinicalTrials.gov, Leads Biolabs/Dianthus 공식 자료, MoA(anti-BDCA2로 pDC 억제 + TACI ectodomain으로 BAFF/APRIL sequestration 이중 기전) 상세화
2. "PDCA"(pDC-Plasma cell axis) 개념 정리 — pDC가 type I IFN을 통해 B세포/형질세포 성숙을 촉진하는 경로가 SLE/Sjögren's 등에서 어떻게 조명되는지 문헌 확인
3. 중국발 pDC-plasma cell axis 관련 자산/논문 조사("중국 쪽 approach" — 구체 자산명 미상, 광범위 검색 필요: BDCA2, ILT7, plasmacytoid DC 표적 + 중국 개발사 필터)
4. pSS Tier A 딥다이브에 LBL-047을 경쟁 벤치마크로 명시적으로 편입(2-A 체크리스트의 "현재 TCE/경쟁 자산 영향" 항목과 연결)

---

## 2-C. TCE 안전성 — Local vs Systemic Cytokine Release

**원문 코멘트**
> "TCE를 I&I나 autoimmune으로 끌어올 때 우려되는 사항: local cytokine이 문제일까? 혈액에서의 문제일까? local에서의 문제일지? monocyte: cytokine release issue 등 / 건질 수 있는 것과 유의할 것의 factors를 정리해야함" / "세포가 죽을 때 나오는 것(cytokine cascade → propagation: IL-1b, TNF-a, IFN-r; t cell, b cell, which?)" / "추가 arm: 국소적으로 잡는 것"

**현황 대비 평가**: 완전 신규 — 항암 TCE의 CRS(cytokine release syndrome) 경험을 자가면역/I&I 맥락으로 번역하는 안전성 프레임워크가 아직 없음.

**Action items**
1. TCE 유발 cytokine cascade 기전 정리 — 표적세포(B cell) 사멸시 방출물 vs T세포 활성화에 따른 분비물 구분, IL-1β/TNF-α/IFN-γ 각각의 기원(T cell/B cell/bystander monocyte) 명시
2. Local(조직 국소) vs systemic(혈중) cytokine release 리스크 구분 프레임 작성 — 항암 TCE 문헌(예: blinatumomab CRS 기전) 대비 자가면역 적응증에서 표적세포 총량이 적다는 점이 리스크를 낮추는 요인인지 정리
3. "건질 수 있는 것 vs 유의할 것" factor 표 작성 — 예: 유리한 요인(낮은 표적세포 burden, 국소 조직 한정 가능성) vs 불리한 요인(만성 장기투여 필요, 배경 염증성 조직 환경)
4. "국소적으로 잡는" 추가 arm 옵션 조사 — 국소 투여(intra-articular, subcutaneous depot 등) 또는 조직특이적 targeting(2nd 표적 활용 국소화) 방식의 선례 조사

---

## 2-D. 질환-병인세포 매트릭스 (질환 단계별)

**원문 코멘트**
> "질환과 병인 세포를 정리 - 질환 1차/remission/relapse (다른 lineage의 병인 세포들도 포함해서 정리)" / "effector function 대비 어떤 질환들이 들어가볼 수 있을까?"

**현황 대비 평가**: 신규 — Tier A 3개 질환에 적용할 구조화 프레임. 2-A 체크리스트의 "병원성 B세포 구획" 항목과 밀접히 연결되나, 이 항목은 **질환 단계(1차 발병/관해/재발)별 동태**와 **B세포 계열 외 lineage**까지 포괄하는 더 넓은 매트릭스.

**Action items**
1. Tier A 3개 질환 각각에 대해 질환단계(1차진단 - remission - relapse) × 병인세포(B cell lineage + 필요시 T cell/myeloid 등 타 lineage) 매트릭스 작성
2. Effector function(예: ADCC 유발 여부, cytotoxic T cell engagement 강도 등) 대비 적합 적응증 매핑 — 어떤 질환이 강한 effector function을 필요로 하는지(급성/파괴적 병리) vs 약한/조절적 effector function이 더 적합한지(만성/관해 유지) 구분

---

## 2-E. 전략적 프레이밍 — 두 개의 큰 질문 및 항체 접근 병행 고려

**원문 코멘트**
> "항체 autoimmune / I&I - open해놓고 고려" / "큰 주제 두 가지: Q1. TCE로 autoimmune/I&I 접근 가능할까? Q2. B cell 외의 다른 immune cell을 targeting하면 할 수 있나?(TCE 아니고, bispecific으로 들어간다고 할때)" / "희귀질환 중 약가를 높게 받을 가능성이 있음(앞서 나가는 에셋이 있을 경우는 어려울 수 있음)" / "autoantigen/autoantibody가 발견된 질환"

**현황 대비 평가**: bcell-tce-autoimmune-strategy.md가 이미 "TCE 플랫폼 미확정, CD3 clone pool 다양화 예정"이라 기록하고 있어 Q1(TCE feasibility)은 이미 진행 중인 질문 — 재확인 성격. Q2(non-B-cell bispecific)는 완전 신규 — 현재 전략 문서는 B cell TCE에 집중되어 있고 "B cell 외 면역세포 대상 bispecific(TCE 아님)" 옵션은 기록된 바 없음.

**Action items**
1. **Q1 답변 자료 보강**: TCE의 autoimmune/I&I 적용 가능성에 대한 최신 임상 신호(2025-2026 발표된 TCE 기반 자가면역 자산의 초기 데이터) 조사 — 기존 전략 문서의 "TCE 플랫폼 미확정" 상태에 대한 근거자료로 축적
2. **Q2 신규 스코핑 착수**: bispecific(비-TCE) 방식으로 B세포 외 면역세포(예: pDC — 2-B의 LBL-047과 연결, monocyte/macrophage, NK 등) 표적화하는 접근 후보 리스트업 — 기존 전략 문서에 새 섹션으로 추가할지 여부 사용자 판단 필요
3. Autoantigen/autoantibody가 명확히 확인된 질환 리스트 재점검 — 이는 기존 Tier A 선정(MG/PV+NMOSD/pSS)의 근거 축 중 하나로 이미 반영되었을 가능성 높음, 선정 근거 문서에 이 기준이 명시적으로 남아있는지 확인(메모리 파일에는 선정 결과만 있고 근거 상세는 없음)
4. 희귀질환 프리미엄 가격 전략 — "선도 에셋 존재시 어려움" 조건을 Tier A 3개 질환 각각에 적용해 현재 경쟁 강도 평가(2-B의 LBL-047 같은 선도 경쟁자산 유무가 직접적 판단 근거)

---

# Part 3. 통합 액션아이템 우선순위 제안 (초안 — 확정은 사용자 판단)

| 우선순위 | 트랙 | 항목 | 근거 |
|---|---|---|---|
| 높음 | eTPD | 1-A. Line/class별 경쟁약물 정리표 | 메모에서 가장 구체적/반복적으로 요청됨, 기존 자료 재편집만으로 완성 가능(신규 조사 최소) |
| 높음 | eTPD | 1-E-3. TSHR shedding rate 확인 | eTPD 분자설계 방향을 좌우하는 선행 조건 |
| 높음 | B-TCE | 2-B. LBL-047(DNTH212) 조사 | pSS Tier A 딥다이브와 직결되는 경쟁자산, 조사 범위 명확 |
| 중간 | eTPD | 1-C-1. IGF-1R class-effect AE 비교표 | 범위 명확, 기존 데이터 확장 성격 |
| 중간 | eTPD | 1-D. Teprotumumab/veligrotug 약가 비교 | 범위 명확하나 신규 조사 필요 |
| 중간 | B-TCE | 2-A. Tier A 3개 질환 체크리스트 적용 | 범위는 크나 기존 작업 인프라(Linear/GitHub) 활용 가능 — 중복 여부 먼저 확인 필요 |
| 중간 | B-TCE | 2-C. Cytokine release 안전성 프레임 | 신규 프레임워크 설계 필요, 시간 소요 예상 |
| 낮음(선행조건 필요) | eTPD | 1-E-2. "프로티나" feasibility 확인 | 사용자의 벤더 컨택 여부에 의존 |
| 낮음(스코프 판단 필요) | B-TCE | 2-E-2. Q2 non-B-cell bispecific 스코핑 | 기존 전략 범위 확장 여부를 먼저 사용자가 결정해야 함 |
| 조사 난이도 높음 | eTPD | 1-C-4. "R1b"(에이프릴바이오 자산) 확인 | 근거 단서가 약함 |
| 조사 난이도 높음 | B-TCE | 2-B-3. 중국 pDC-plasma cell axis 자산 | 구체 자산명 없이 광범위 검색 필요 |

---

# Part 4. 사용자 판단이 필요한 열린 질문 (요약)

1. **1-E-2**: "프로티나"와의 feasibility 논의가 이미 진행 중인지, 아니면 이번이 첫 컨택 검토인지?
2. **2-A**: Tier A 체크리스트가 GitHub/Linear 진행 작업과 중복되는지 — 중복이면 이번 정리는 재확인용으로 축소 가능
3. **2-E-2**: Q2(non-B-cell bispecific, non-TCE)를 기존 bcell-tce-autoimmune-strategy.md 범위에 편입할지, 별도 신규 트랙으로 분리할지
4. **1-C-4 / 2-B-3**: "R1b"(에이프릴바이오 자산)와 "중국 pDC-plasma cell axis" 조사에 투입 가능한 시간/우선순위 — 단서가 약해 광범위 검색이 필요함을 감안
