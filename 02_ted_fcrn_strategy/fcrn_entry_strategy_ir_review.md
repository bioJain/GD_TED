---
linear_issue: JHA-74
created: 2026-09-28
source: manual
milestone: cluster-2-ted-fcrn-strategy
status: done
inputs:
  - 00_legacy_unsorted/GD_TED_report.md
  - 00_baseline_biomni/landscape_v2/pipeline_assets_v2.csv
  - 00_baseline_biomni/landscape_v2/asset_trial_crosswalk_v2.csv
  - 00_baseline_biomni/landscape_v2/clinical_trials_v2.csv
---

# FcRn 항체 개발사의 GD/TED 진입 전략: 공개 IR 및 임상설계 검토

**조사 기준일:** 2026-09-28  
**독립 QA 확인일:** 2026-09-30 (`fcrn_entry_strategy_ir_review_qa.md`)

**v2 기준일:** repo의 Biomni v2 수치/상태는 2026-09-10 data cut이며, 그 이후 공개된 내용은 아래에 별도로 날짜를 표시했다.  
**범위:** argenx의 efgartigimod, Immunovant의 batoclimab/imeroprubart, 비교군인 rozanolixizumab 및 nipocalimab의 GD/TED 개발.

## 1. 결론

1. **Immunovant는 GD 선정 이유를 가장 명시적으로 설명했다(근거 수준: 높음, 회사 공시).** GD는 TSHR-stimulating IgG(TRAb)가 질환의 직접 병인이고 기존 ATD는 이를 제거하지 않으며, ATD 재발/불충분 반응 후 ablation을 원하지 않는 환자가 상당하다는 기전적/미충족수요/시장 논리를 동시에 제시한다. 회사는 GD를 FcRn의 `first-in-class` 기회로 분류하고, MG/CIDP는 이미 형성된 FcRn 시장에서 `best-in-class`를 노리는 별도 전략으로 구분했다.[S1] 따라서 **GD 진입을 기존 gMG/CIDP 처방 기반 재사용만으로 해석하는 것은 공시와 맞지 않는다.** 더 직접적인 동인은 (i) pathogenic IgG를 제거하는 기전 적합성, (ii) 70년 이상 제한된 약물 혁신, (iii) ATD 이후 비파괴적 치료 공백, (iv) 큰 잠재 환자군이다.[S1]
2. **argenx는 TED와 이후 GD의 선택 근거를 서로 다르게 공개했다(근거 수준: 중간).** TED 진입 당시 회사는 TSHR autoantibody의 병인성, autoantibody 제거의 임상 근거, IgG 감소가 TED와 동반 hyperthyroidism을 함께 다룰 가능성, steroid/teprotumumab의 내약성 한계를 제시했다.[S2] 그러나 2025년 UplighTED futility 중단 뒤 2026년 시작한 GD Phase 3에 대해서는 공개 공시에서 `thyroid-driven autoimmunity` 확장과 시험 개시만 확인되며, **왜 GD를 다시/우선 선택했는지에 대한 독립적인 상업 논리는 찾지 못했다.**[S3,S4] 그러므로 argenx GD 전략은 **기전적 타당성이 명시적이고, 상업적 의도는 임상설계/기존 franchise에서의 추론**으로만 표시해야 한다.
3. **TED 실패는 FcRn 전체 또는 GD 실패와 동일하지 않다(근거 수준: 높음/중간).** efgartigimod UplighTED 두 건은 proptosis responder를 24주 primary endpoint로 둔 active moderate-to-severe TED 시험이었고 futility로 종료됐다.[S5,S6] 반면 GD 시험은 euthyroid/off-ATD와 TRAb seronegativity를 측정한다.[S7,S8] 즉 TED의 안와 구조/염증 endpoint 실패를 thyroid hormone 및 circulating TRAb 중심의 GD 가설에 자동 외삽할 수 없다. 이 해석은 `GD_TED_report.md` Section E2의 “GD가 TED보다 FcRn에 더 직접적인 mechanistic fit일 수 있다”는 결론과 **방향상 일치하지만 아직 임상 입증 전**이다.
4. **다른 FcRn 자산은 GD/TED 진입 양상이 확인되지 않았다(근거 수준: 중간, registry 부재 확인).** rozanolixizumab과 nipocalimab에 대해 ClinicalTrials.gov를 자산명/동의어와 GD/TED 조건으로 검색했으나 2026-09-28 현재 중재시험을 찾지 못했다.[S13,S14] 이는 “개발하지 않는다”는 회사 의사결정의 증거가 아니라 **공개 등록시험 부재**의 증거다. 따라서 FcRn class의 GD/TED 전략은 현재 argenx/Immunovant 사례로만 일반화하면 안 된다.

## 2. 자산명/코드 정리

| 회사 | 자산 | 정확한 대응 | GD/TED 상태(as-of 2026-09-28) | 근거 |
|---|---|---|---|---|
| Immunovant | batoclimab | **IMVT-1401**, 과거 RVT-1401 | GD Phase 2 POC 완료; TED Phase 3 두 건 primary endpoint 미달 후 전 적응증 개발 중단 | [S1,S9,S10] |
| Immunovant | imeroprubart | **IMVT-1402**, batoclimab과 별개인 차세대 FcRn mAb | GD potentially registrational Phase 2 프로그램 진행; TED 등록시험 없음 | [S1,S11,S12,S15] |
| argenx | efgartigimod alfa/efgartigimod PH20 SC | Fc fragment; SC는 rHuPH20 병용 제형 | TED UplighTED 중단; GD Phase 3 두 건 시작 | [S2,S5-S8] |

> **명칭 정정:** 이슈 본문의 “imeroprubart(舊 batoclimab RVT-1401 계열)”는 부정확하다. 같은 HanAll-origin FcRn 계열이지만, 공시상 batoclimab은 former IMVT-1401이고 imeroprubart는 IMVT-1402의 INN이다.[S1]

## 3. 회사별 전략 판독

### 3.1 Immunovant: 명시적 기전 + 명시적 시장 선택

**회사가 직접 말한 것.** 2026 Form 10-K는 GD를 TSHR에 결합하는 IgG autoantibody가 유발하는 질환으로 정의하고, ATD가 underlying pathology인 stimulating TRAb를 다루지 않는다고 설명한다. 또한 미국 GD 약 88만 명, ATD 재발 후 ablation을 선택하지 않은 약 33만 명이라는 회사/제3자 분석과, 재발/불충분 반응/불내약 환자가 25-30%라는 자체 시장 분석을 제시한다.[S1] 이 수치는 회사 공시의 market-sizing 추정치이므로 독립 역학치로 취급하지 않는다.

**포트폴리오 문구가 전략을 분리한다.** 회사는 GD 등을 “first- and best-in-class” 미충족수요 영역으로, MG/CIDP는 이미 anti-FcRn commercial presence가 있는 시장에서 differentiated best-in-class를 노리는 영역으로 별도 기술했다.[S1] 따라서 GD 선택은 gMG/CIDP 영업 기반 활용보다 **새 endocrine franchise/first-in-class 시장 창출**에 더 가깝다는 해석이 타당하다(추론, 근거 수준: 중간).

**batoclimab에서 imeroprubart로의 전환.** batoclimab GD 단일군 POC(NCT05907668)는 24주에 ATD 증량 없이 FT3/FT4 정상화 **또는** FT3/FT4가 정상 하한(LLN) 미만인 composite 68.8%, baseline ATD의 50% 이하에서 순수 정상화 53.1%, off-ATD 상태에서 같은 정상화-또는-LLN-미만 composite 31.3%를 보고했다.[S9] 68.8%/31.3%는 정상화만이 아니라 갑상선호르몬이 정상범위 미만으로 떨어진 경우도 반응자로 포함하는 composite endpoint이므로, 순수 정상화율(53.1%)과 구분 없이 인용하면 POC 효능을 과대평가할 위험이 있다. 회사는 이 POC와 깊은 IgG 감소-임상반응 관계를 IMVT-1402 성공확률의 근거로 제시한다.[S1] 동시에 batoclimab은 albumin 감소/LDL 상승이라는 off-target profile이 있었고, 2026년 TED Phase 3 두 건 실패 후 전체 개발을 중단했다.[S1] 즉 imeroprubart 진입은 “batoclimab의 이름 변경”이 아니라 **GD human POC와 운영 자산은 승계하되 분자 profile을 바꾸는 후속 전략**이다(추론, 근거 수준: 높음/중간).

### 3.2 argenx: TED의 명시적 mechanistic thesis, GD의 제한된 공개 설명

**TED 진입 논리.** 2024 Form 20-F는 (i) TSHR autoantibody가 TED 병리에 관여한다는 nonclinical/clinical evidence, (ii) autoantibody 제거의 임상 근거, (iii) efgartigimod가 pathogenic IgG를 줄여 증상 및 hyperthyroidism까지 완화할 가능성, (iv) steroid/teprotumumab의 제한을 제시했다.[S2] 이는 기전/미충족수요 논리이며, 기존 gMG/CIDP 처방 기반을 TED 선정 사유로 명시하지 않았다.

**결과와 pivot.** UplighTED 2건(NCT06307613/NCT06307626)은 active moderate-to-severe TED에서 efgartigimod PH20 SC와 placebo를 비교하고 24주 proptosis responder를 primary endpoint로 설정했으나, 사전 interim futility 분석 후 2025년에 종료됐다.[S5,S6] 2026 공시는 이후 GD registrational study를 `expanding development into thyroid-driven autoimmunity`라고 소개했으나, TED 실패와 GD 시작 사이의 의사결정 기준, 예상 시장, gMG/CIDP commercial infrastructure synergy는 공개하지 않았다.[S3,S4]

**판정.** argenx가 GD를 택한 이유에 대해 공개자료가 지지하는 강한 결론은 “circulating pathogenic IgG/TRAb를 겨냥하는 기전 가설”까지다. 기존 VYVGART 제조/SC 제형/안전성/규제 경험이 실행위험을 낮춘다는 것은 합리적이나 **회사 발언으로 확인되지 않은 포트폴리오 추론(근거 수준: 낮음)**이다.

## 4. 임상디자인에서 읽히는 의도

| 프로그램 | population/therapy line | 대조군/구성 | 핵심 endpoint | 전략적 의도 역추론 |
|---|---|---|---|---|
| Batoclimab GD POC, NCT05907668 | ATD 치료 중인 GD 성인, 단일군 24주 | comparator 없음; 680 mg QW 12주 후 340 mg QW 12주 | Week 24 hormone 정상화, ATD 감량/off-ATD | 초기에는 빠른 mechanistic de-risking과 ATD-sparing signal 탐색. 단일군이라 자연경과/ATD 효과와 분리 한계.[S9] |
| Imeroprubart GD, NCT06727604 | GD 성인; 장기 치료/중단 지속성 평가 | 600 mg QW 지속, 26주 후 placebo 전환, 52주 placebo 등 | Week 26 euthyroid/off-ATD; Week 52 및 치료중단 후 6/12개월 지속, TRAb 음전 | 단순 hormone control이 아니라 **drug-free remission/durability** claim을 겨냥한 설계. placebo 전환은 maintenance requirement를 검증.[S11] |
| Imeroprubart GD, NCT07018323 | GD 성인; 두 용량 | 2 doses vs placebo, 26주 | euthyroid/off-ATD 및 TRAb seronegativity | dose selection과 confirmatory placebo contrast를 동시 확보하려는 potentially registrational 전략.[S12] |
| Efgartigimod TED UplighTED, NCT06307613/626 | active moderate-to-severe TED; baseline thyroid disease controlled | randomized, quadruple-masked, placebo-controlled, 24주 | proptosis responder; diplopia/GO-QoL | thyroid biochemical control보다 orbital disease modification을 정면 검증. 이 endpoint에서 futility였으므로 GD biochemical hypothesis와 구분 필요.[S5,S6] |
| Efgartigimod GD, NCT07570316/07596849 | GD 성인; ATD 병용 후 감량/중단을 전제로 한 것으로 endpoint에서 확인 | Part A randomized quadruple-masked placebo, 이후 추가 blinded/open-label periods | Week 24 euthyroid/off-ATD; time-to-response, low-dose ATD, TRAb 음전 | 두 병렬 Phase 3와 엄격한 placebo contrast는 exploratory 진입이 아니라 등록 목적을 시사. off-ATD/seronegativity는 symptom control보다 underlying autoimmunity와 remission을 겨냥한다.[S7,S8] |

### Therapy-line 해석의 한계

공개 registry는 endpoint와 ATD 사용/감량을 명확히 보여주지만 모든 시험에서 “2L/3L” 같은 상업적 therapy-line label을 일관되게 지정하지 않는다.[S7-S12] 따라서 이 문서에서는 **ATD 이후 또는 ATD-sparing population**이라고만 표현하며, “공식 second-line”이라고 단정하지 않는다. 특히 회사의 relapsed/uncontrolled/intolerant 시장 서술과 실제 protocol eligibility는 동일 개념이 아니므로 분리한다.[S1]

## 5. 다른 FcRn 자산

| 자산/회사 | GD/TED 공개 임상 확인 | 해석 |
|---|---|---|
| rozanolixizumab/UCB | ClinicalTrials.gov에서 `rozanolixizumab OR UCB7665`와 Graves/TED 조건을 조합 검색했으나 등록 중재시험 0건(2026-09-28).[S13] | gMG 등 다른 IgG-mediated 질환 개발이 GD/TED 자동 확장을 뜻하지 않는다. “계획 없음”이 아니라 “공개 계획/시험을 확인하지 못함”. |
| nipocalimab/J&J | ClinicalTrials.gov에서 `nipocalimab OR M281`과 Graves/TED 조건을 조합 검색했으나 등록 중재시험 0건(2026-09-28).[S14] | FcRn class mechanistic plausibility만으로 회사의 GD/TED 전략을 추정할 근거 부족. |

검색 부재는 registry 명칭, 미등록 초기계획, 국가 registry 차이 때문에 위음성일 수 있다. 이 두 자산에 대해서는 “실패”가 아니라 **no public GD/TED trial identified**로 코딩해야 한다.

## 6. 종합 판단: commercial vs mechanistic

| 질문 | 결론 | 근거 수준 |
|---|---|---|
| GD 선택은 mechanistic인가? | **예.** stimulating TRAb가 직접 병인이고 FcRn inhibition이 circulating IgG를 감소시킨다는 논리는 Immunovant가 명시했으며, argenx 설계도 TRAb 음전/off-ATD를 포함한다.[S1,S7,S8,S11,S12] | 높음(기전 명시), 중간(임상효과는 미확정) |
| 상업적 판단도 있는가? | **Immunovant는 예.** 큰 relapsed/uncontrolled/intolerant pool, 비파괴적 치료 공백, first-in-class 기회를 명시한다.[S1] **argenx는 불명확.** GD 시장 선택의 별도 market-sizing/처방기반 synergy 발언을 확인하지 못했다.[S3,S4] | Immunovant 높음; argenx 낮음/부재 |
| 기존 gMG/CIDP 기반 활용이 핵심인가? | Immunovant는 MG/CIDP를 established FcRn market 전략으로 따로 분류한다. GD 선정의 핵심 근거라고 명시하지 않았다.[S1] argenx도 운영 synergy를 직접 언급하지 않았다. | 중간 |
| Section E2와 일치하는가? | **방향상 일치.** GD 시험은 circulating TRAb/thyroid biochemistry/off-ATD를 직접 겨냥하고, TED 시험은 orbital proptosis에서 실패했다. 다만 GD Phase 3 결과 전에는 “GD 우월성”이 아니라 **mechanistic fit 가설**이다.[S5-S12] | 중간 |

## 7. 참고문헌 및 확인 로그

모든 URL은 **2026-09-28 확인**. ClinicalTrials.gov 상태/설계는 live 조회이며, repo v2의 2026-09-10 frozen cut과 구분한다.

- **[S1]** Immunovant, FY2026 Form 10-K: asset naming, business strategy, GD rationale/market estimate, batoclimab discontinuation, IMVT-1402 program. https://www.sec.gov/Archives/edgar/data/1764013/000176401326000064/imvt-20260331.htm
- **[S2]** argenx, FY2024 Form 20-F: TED rationale and UplighTED design. https://www.sec.gov/Archives/edgar/data/1697862/000169786225000024/argx-20241231.htm
- **[S3]** argenx, FY2025 results (Form 6-K exhibit): GD registrational study and `thyroid-driven autoimmunity`. https://www.sec.gov/Archives/edgar/data/1697862/000169786226000010/a09earningspressreleaseq4.htm
- **[S4]** argenx, FY2025 Form 20-F: GD pipeline entry, UplighTED discontinuation, commercial franchise context. https://www.sec.gov/Archives/edgar/data/1697862/000169786226000032/argx-20251231.htm
- **[S5]** ClinicalTrials.gov, NCT06307613, UplighTED study 1. https://clinicaltrials.gov/study/NCT06307613
- **[S6]** ClinicalTrials.gov, NCT06307626, UplighTED study 2. https://clinicaltrials.gov/study/NCT06307626
- **[S7]** ClinicalTrials.gov, NCT07570316, efgartigimod PH20 SC GD Phase 3. https://clinicaltrials.gov/study/NCT07570316
- **[S8]** ClinicalTrials.gov, NCT07596849, efgartigimod PH20 SC GD Phase 3. https://clinicaltrials.gov/study/NCT07596849
- **[S9]** ClinicalTrials.gov, NCT05907668, batoclimab GD Phase 2 results. https://clinicaltrials.gov/study/NCT05907668
- **[S10]** ClinicalTrials.gov, NCT05517421/NCT05524571, batoclimab TED Phase 3. https://clinicaltrials.gov/study/NCT05517421 ; https://clinicaltrials.gov/study/NCT05524571
- **[S11]** ClinicalTrials.gov, NCT06727604, IMVT-1402 GD long-duration study. https://clinicaltrials.gov/study/NCT06727604
- **[S12]** ClinicalTrials.gov, NCT07018323, IMVT-1402 GD dose-ranging/placebo study. https://clinicaltrials.gov/study/NCT07018323
- **[S13]** ClinicalTrials.gov API search, rozanolixizumab/UCB7665 + Graves/TED (0 applicable intervention studies identified). https://clinicaltrials.gov/api/v2/studies?query.term=%28rozanolixizumab%20OR%20UCB7665%29%20AND%20%28Graves%20OR%20%22thyroid%20eye%20disease%22%20OR%20thyrotoxicosis%29&pageSize=100
- **[S14]** ClinicalTrials.gov API search, nipocalimab/M281 + Graves/TED (0 applicable intervention studies identified). https://clinicaltrials.gov/api/v2/studies?query.term=%28nipocalimab%20OR%20M281%29%20AND%20%28Graves%20OR%20%22thyroid%20eye%20disease%22%20OR%20thyrotoxicosis%29&pageSize=100
- **[S15]** ClinicalTrials.gov API search, imeroprubart/IMVT-1402 + TED/Graves (3개 시험 모두 GD가 condition이며 TED는 exclusion criteria로만 등장; 별도 TED 중재시험 0건, 2026-09-28 확인). https://clinicaltrials.gov/api/v2/studies?query.term=%28imeroprubart%20OR%20IMVT-1402%29%20AND%20%28%22thyroid%20eye%20disease%22%20OR%20TED%20OR%20Graves%29&pageSize=100

### Claim verification log

| claim | tier | 검증 방법 | 결과 | 일자 |
|---|---|---|---|---|
| Batoclimab=IMVT-1401, imeroprubart=IMVT-1402 | 중 | SEC 10-K 원문 내 naming 문구 대조 | PASS | 2026-09-28 |
| Batoclimab TED Phase 3 실패/전체 중단 | 상 | 독립 QA에서 Immunovant 10-K와 NCT05517421/NCT05524571 원문 대조, direct quote 확인 | PASS — 두 Phase 3의 primary endpoint 미달 및 batoclimab 전 적응증 중단 확인 | 2026-09-30 |
| UplighTED futility 종료 | 상 | 독립 QA에서 argenx 20-F와 NCT06307613/NCT06307626의 `whyStopped` 원문 대조, direct quote 확인 | PASS — 두 시험 `TERMINATED`, 사전 interim analysis상 intended efficacy 입증 가능성이 낮아 중단 | 2026-09-30 |
| Batoclimab GD endpoint 수치 | 상 | 독립 QA에서 NCT05907668 posted results의 outcome title/value direct quote 대조 | PASS — 68.8%/31.3%는 정상화 또는 LLN 미만 composite, 53.1%만 정상화 endpoint임을 재확인 | 2026-09-30 |
| IMVT-1402/efgartigimod GD 설계 | 상 | 독립 QA에서 NCT06727604/NCT07018323/NCT07570316/NCT07596849의 phase, arm, outcome 원문 대조 | PASS — phase, 대조군, Week 24/26 endpoint, TRAb 관련 secondary endpoint 확인 | 2026-09-30 |
| Rozanolixizumab/nipocalimab GD/TED 등록시험 부재 | 중 | ClinicalTrials.gov API 자산명/코드/질환 조합 검색 | PASS, 단 부재 증거의 한계 명시 | 2026-09-28 |
| Imeroprubart/IMVT-1402 TED 등록시험 부재 | 중 | ClinicalTrials.gov API `imeroprubart OR IMVT-1402` + TED/Graves 조합 검색([S15]); 이전 버전은 이 claim에 nipocalimab 검색([S14])을 오인용 | PASS, 단 부재 증거의 한계 명시 | 2026-09-28 |
