---
linear_issue: JHA-84
created: 2026-09-27
source: codex
milestone: cluster-5-etpd-molecular-design
status: in-review
search_cutoff: 2026-10-01
inputs:
  - 00_baseline_biomni/landscape_v2/pipeline_assets_v2.csv
  - 00_baseline_biomni/landscape_v2/direct_source_documents_v2.jsonl
  - 00_baseline_biomni/landscape_v2/claim_evidence_anchors_v2.csv
  - 00_baseline_biomni/landscape_v2/source_anchors_v2.csv
  - 00_baseline_biomni/landscape_v2/report_graves_ted_landscape_v2.md
  - 00_baseline_biomni/landscape_v2/reference_v2.md
  - 00_legacy_unsorted/GD_TED_report.md
---

# 경쟁/benchmark 분자 스펙 deep-dive

## Executive summary

- 공개 근거에서 직접 비교 가능한 분자 정량치는 제한적이다. K1-70의 reported association constant는 `4 x 10^10 L/mol`이며, 단순 역수로 환산한 apparent `KD`는 약 `25 pM`이다. GenSci098은 학회 포스터에서 cell-based TSHR binding `EC50 1.11 nM`과 M22-stimulated cAMP inhibition `IC50 2.3 nM`을 공개했으나 solution-phase `KD/kon/koff`는 검색 범위에서 확인되지 않았다.
- MER511은 eTPD 설계에 가장 직접적인 construct benchmark다. WO2025030009A1은 Merida의 TSHR ectodomain/FcγRIIB platform에 대한 TSHR fragment, stabilization mutations, Fc mutation candidates 및 sequence listings를 공개한다. 다만 patent가 `MER511` code나 최종 clinical construct를 직접 특정하지 않으므로 candidate disclosure와 final drug specification을 동일시할 수 없다.
- K1-70은 receptor-blocking benchmark로 높은 affinity와 human PK/PD proof를 제공하지만, 정상 TSH signaling도 차단한다. 원숭이/쥐에서 hypothyroid pharmacology가 관찰됐고 일본 Phase 1 고용량에서도 thyroid hormone 저하와 L-thyroxine 보조가 필요했다. TSAb 제거형 eTPD의 목표 product profile은 이 on-target liability를 피해야 한다.
- Batoclimab과 efgartigimod는 antigen-selective하지 않은 FcRn benchmark다. 전자는 GD Phase 2에서 Week 24 biochemical responder `68.8% (22/32; 95% CI 50.0-83.9)`를 보였지만 open-label, single-arm 결과다. 후자는 건강인에서 multiple dosing 후 total IgG를 평균 75% 낮춘 class-level PD benchmark이나 TED Phase 3 두 건은 futility로 종료됐다.
- LCA-0321과 MER511의 human efficacy/developability 결론은 아직 낼 수 없다. 각각 v2 evidence confidence `Low`, `Low-moderate`를 유지하며, patent embodiment, sponsor claim, registry fact를 분리한다.

## 범위와 판독 규칙

Section C4 가운데 TSHR/자가항체 축 5개와 FcRn/Fc engineering 비교군 3개를 선정했다. `pipeline_assets_v2.csv`의 asset key를 유지했고 live registry/PubMed를 2026-09-27에 재확인했고, 2026-10-01 follow-up fact-check에서 전수 재검증했다(참고문헌 23은 2026-10-01 추가). 단계는 적응증별로 기록하며, 다른 적응증의 승인/후기 단계로 올려 쓰지 않았다.

- **공개 수치 확인**: 원문에서 수치와 assay context를 확인한 경우
- **정성 정보만 공개**: `high affinity`, `enhanced binding` 등 방향만 공개되고 비교 가능한 수치가 없는 경우
- **검색 범위에서 미확인**: 조사한 public source에서 확인하지 못한 경우. 비공개, 부재 또는 미측정을 뜻하지 않음
- **비공개/NR 명시**: source가 undisclosed/not reported라고 명시한 경우에만 사용
- **해당 없음**: modality에 해당 지표를 그대로 적용할 수 없는 경우
- affinity 단위와 assay format이 다른 값은 직접 순위화하지 않음
- sponsor/학회 초록의 preclinical 주장은 독립 재현으로 간주하지 않음

## Public patent landscape 및 sequence-disclosure scan

본 절은 Google Patents에서 제공하는 WO publication record와 공개 원문을 이용한 technical landscape다. Legal FTO opinion, claim construction 또는 국가별 live-claim 판단이 아니다. Patent가 clinical asset code를 직접 명시하지 않으면 sponsor, target, mechanism 및 timing의 일치만으로 최종 clinical molecule의 exact sequence라고 단정하지 않았다. 검색일은 2026-09-27이며, 2026-10-01 follow-up fact-check에서 3개 특허 family를 재검증했다.

| Asset | Candidate patent family | Priority/publication | 공개된 핵심 내용 | Asset mapping | JHA-88에서 사용 가능한 범위 |
|---|---|---|---|---|---|
| **MER511** | WO2025030009A1, *Molecules for controlling immune response* | 2023-08-01 / 2025-02-06 | Merida 출원. TSHR260/TSHR289와 SEQ ID NOs 1-8, 307-317; TSHR stabilization candidates `R112P/D143P/V169R/I253R/H63S` 및 추가 proline variants; FcγRIIB-enhancing candidates including `P238D`, `S267E/L328F`; FcγR-reducing `G236R/L328R`; full molecule/Fc sequence listings; M22/K1-18, patient-serum cAMP, FcγRIIB uptake 및 mouse studies | **Probable.** Sponsor, construct 및 MoA가 일치하지만 `MER511` 또는 final selected variant를 직접 명시하지 않음 | Candidate design space와 assay benchmark로 사용. MER511 exact sequence/mutation이라고 표기 금지 [19] |
| **LCA-0321** | WO2025207934A1, *Lysosomal targeting bifunctional molecules for degradation of TSHR autoantibodies* | 2024-03-28 / 2025-10-02 | Lycia 출원. ASGPR ligand + carrier protein + TSHR polypeptide; Fc-TSHR 및 HSA-TSHR formats; TSHR/HSA/linker sequences; stabilized TSHR candidates; patient-derived M22/K1-18 uptake/degradation; `21-L004`가 mouse에서 4시간 후 serum anti-TSHR 70.5% clearance를 보였다는 example | **높음(코드 명시).** Publication이 K1-18 clearance example(hFcRn Tg32 mouse)에서 `LCA-0321` code를 직접 명시한다. 다만 final development construct/CMC specification은 여전히 미지정 | ASGPR mechanism, carrier/valency/linker와 preclinical assay 설계에 사용. Clinical construct/CMC로 전이 금지 [20] |
| **GenSci098/YB-101/GS-098** | WO2024046384A1, *Antibody binding to TSHR and use thereof* | 2022-08-31 / 2024-03-07 | Changchun GeneScience 출원. TSHR antibody CDR/VH/VL/full-chain SEQ ID listings; humanized candidates; IgG4 `S228P/L235E/M252Y/S254T/T256E` 및 IgG1 `L234A/L235A/M252Y/S254T/T256E` candidate Fc designs; human/mouse/monkey binding, cAMP, FcRn 및 ADCC assays | **Probable patent-to-asset mapping.** 공개 보도자료/공시에 따라 세 명칭은 동일 molecule로 확인 [23]. Patent는 final selected clinical sequence를 asset code로 직접 지정하지 않음 | 공개 candidate sequence/Fc space와 assay 결과로 사용. Final clinical sequence는 별도 확인 전 미확정 [21] |

### Patent search log 및 경계

- Asset name, sponsor/assignee, target와 mechanism 조합으로 검색했다. `MER511`, `LCA-0321`, `GenSci098/YB-101/GS-098` exact-code 검색만으로는 primary patent를 안정적으로 회수하지 못했으며 assignee/mechanism 검색으로 위 family를 확인했다.
- WO2025030009A1은 `MER511` code를 명시하지 않지만, WO2025207934A1은 example에서 `LCA-0321` code를 직접 명시한다. MER511 mapping confidence는 `Probable`이며 exact clinical sequence는 **검색 범위에서 미확인**이다.
- WO2024046384A1은 다수 antibody/Fc embodiments를 포함한다. GenSci 보도자료와 공시에 따라 GenSci098/YB-101/GS-098을 동일 molecule로 확인해 취급하지만 [23], 어느 SEQ ID 조합이 final clinical molecule인지는 **검색 범위에서 미확인**이다. 참고로 이 family는 EP/AU 기록 기준 Shanghai Scizeng Medical Technology로 재매각되어 있으며, GenSci→RTW/Yarrow ex-China license 방향과 일치한다 [21,23].
- 공개 family가 존재한다는 사실은 freedom-to-operate 또는 침해/비침해 결론이 아니다. 국가별 pending/granted status, claim scope, expiry/PTA/PTE 및 license chain은 patent counsel 검토 대상이다.

## 공통 비교표

| 자산 | Construct/표적 | Binding affinity | 물성/developability | in vitro/in vivo 및 human data | 근거 수준 |
|---|---|---|---|---|---|
| **LCA-0321** | anti-TSHR AAb LYTAC degrader | Patent의 M22/K1-18 BLI kinetics는 정성 확인; final asset `KD/kon/koff`는 **검색 범위에서 미확인** | Patent candidate: ASGPR ligand, Fc 또는 HSA carrier, TSHR polypeptide와 linker. Final sequence, MW, pI, Tm, aggregation, formulation/yield는 **검색 범위에서 미확인**; Phase 1 SAD/MAD, planned `n=48` | Patent `21-L004`: mouse에서 4시간 후 serum anti-TSHR 70.5% 감소, 이후 antibody-producing B-cell 때문에 rebound. Sponsor의 human efficacy 결과는 아직 없음 | Patent + sponsor pipeline + CTIS; asset mapping 높음(코드 명시); v2 confidence **Low** [1,2,20] |
| **MER511** | monomeric TSHR ectodomain-mutant Fc fusion; anti-TSHR AAb/FcγRIIB | Patent는 candidate FcγRIIB affinity `약 1-0.001 µM`, preferred `0.1-0.01 µM` 범위를 기재하나 MER511 selected construct 값은 **검색 범위에서 미확인** | Patent candidate TSHR260/289, stabilization/Fc mutations와 sequences 공개. Final mutations/sequence, MW, pI, Tm, SEC monomer, viscosity, formulation은 **검색 범위에서 미확인**; IV/SC SAD/MAD | Patent와 sponsor 초록: M22/K1-18/patient-serum neutralization, FcγRIIB uptake, humanized FcγR/FcRn mouse depletion, total mouse IgG 보존. NEXUS human 결과는 아직 없음 | Patent + congress abstract + sponsor + registry; asset mapping Probable; v2 confidence **Low-moderate** [3-5,19] |
| **K1-70** | human IgG1 lambda TSHR-blocking monoclonal autoantibody | reported `Ka 4 x 10^10 L/mol`; 단순 역수 apparent `KD 약 25 pM`; 직접 보고 KD가 아니며 assay 간 비교 금지 | full IgG; IV/IM 연구. sequence, pI, Tm, aggregation, solubility, expression/formulation은 **검색 범위에서 미확인** | CHO에서 TSH/TSAb-induced cAMP 차단. Rat/monkey에서 T3/T4 저하, TSH 증가; monkey NOAEL `100 mg/kg/dose`, rat NOAEL 미확립. 일본 Phase 1(GD 환자) `n=12`, single IV `5/25/75/150 mg`; SAE 0, TEAE `83.3%` | Peer-reviewed in vitro, preclinical, Phase 1 [6-8] |
| **GenSci098/YB-101/GS-098** | 동일 molecule의 sponsor/licensing별 명칭; TSHR antagonistic mAb | Cell-based TSHR binding `EC50`: human `1.11 nM`, mouse `1.31 nM`, rat `5.81 nM`, cyno `1.66 nM`; M22-cAMP inhibition `IC50 2.3 nM`; solution `KD/kon/koff`는 **검색 범위에서 미확인** | Patent candidate antibody/Fc sequences 공개. Final clinical SEQ ID, pI, Tm, aggregation, formulation/bioavailability는 **검색 범위에서 미확인**. SC Phase 1 dose `15/45/90/180/270 mg` | TED orbital fibroblast active/inactive donor HA/IL-6/IL-8 IC50 공개; M22 mouse `0.5 mg/kg`에서 40.8%, `3 mg/kg`에서 99.7% T4 inhibition; half-life mouse `327 h`, monkey `462 h`; sponsor-reported tox에서 hypothyroidism 없음 | Patent + congress poster + registry; patent mapping Probable; v2 confidence **Moderate** [9-11,21,22] |
| **ATX-GD-59** | 두 TSHR peptide의 intradermal antigen-specific immunotherapy | 단일 ligand-receptor `KD`: **해당 없음**; peptide sequence/MHC affinity는 **검색 범위에서 미확인** | 10 intradermal doses/18 weeks; peptide별 함량, formulation stability, solubility, 제조수율은 **검색 범위에서 미확인** | Phase 1 open-label `n=12`; 10회 완료 `n=10`; Week 18 fT3 정상범위 `5/10`, 추가 개선 `2/10`, 악화 `3/10`; TRAb-fT3 변화 `r=0.85, p=0.002` | Peer-reviewed single-arm Phase 1; v2 confidence **Low-moderate** [12] |
| **Batoclimab/IMVT-1401** | fully human anti-FcRn mAb; broad IgG lowering | FcRn `KD/kon/koff`, pH 6.0/7.4 selectivity는 **검색 범위에서 미확인** | SC `680 mg QW` 12주 후 `340 mg QW` 12주. sequence, isotype/effector silencing, pI, Tm, aggregation, formulation은 **검색 범위에서 미확인** | GD Phase 2 open-label `n=32`: primary `22/32 (68.8%)`; ATD 50% 이상 감량 동반 `17/32 (53.1%)`; ATD-free biochemical response `10/32 (31.3%)`. Missing Week 24는 non-responder 처리 | ClinicalTrials.gov posted results, sponsor-controlled Phase 2 [13] |
| **Efgartigimod alfa** | engineered human IgG1 Fc fragment, ABDEG; FcRn antagonist | FcRn affinity가 wild-type Fc보다 acidic/neutral pH에서 증가한다는 정성 정보 공개; 본 source set의 정량 `KD`는 **검색 범위에서 미확인** | Fc-only, no Fab; IV 및 PH20 SC 제품. pI, Tm, aggregation, viscosity는 **검색 범위에서 미확인** | FIH `n=62`: single dose total IgG 최대 50%, multiple dosing 평균 75% 감소, 마지막 dose 약 8주 후 baseline 복귀. 별도 TED Phase 3 NCT06307613/626은 intended efficacy 입증 가능성이 낮아 terminated | Peer-reviewed Phase 1 + registry [14-16] |
| **Nipocalimab/M281** | fully human aglycosylated effectorless IgG1 anti-FcRn mAb | neutral/acidic pH high-affinity, unique epitope라는 정성 정보 공개; 정량 `KD`는 본 source set에서 **검색 범위에서 미확인** | IV full mAb; aglycosylated/effectorless. sequence, pI, Tm, aggregation, formulation은 **검색 범위에서 미확인** | 용량 의존적 FcRn occupancy/IgG 감소(주입 속도와 무관). Healthy volunteer Phase 1에서 `30 mg/kg`을 7.5-60분, `60 mg/kg`을 15분에 주입; active GD/TED efficacy data 없음 | Peer-reviewed molecular/nonclinical + Phase 1; 질환 직접성 낮음 [17,18] |

## 자산별 deep-dive

### 1. LCA-0321: selective degradation concept, 공개 spec은 거의 없음

Lycia는 LCA-0321을 anti-TSHR autoantibody를 결합해 lysosomal elimination하는 LYTAC로 설명한다. CTIS의 LCA-0321-01은 first-in-human SAD/MAD, planned `n=48`이다. WO2025207934A1은 ASGPR ligand, Fc/HSA carrier, TSHR polypeptide, linker와 sequence embodiments를 공개하고, `21-L004`의 M22/K1-18 uptake/degradation 및 mouse anti-TSHR clearance를 제시한다. WO2025207934A1은 K1-18 clearance example(hFcRn Tg32 mouse)에서 `LCA-0321` code를 직접 명시하지만, final selected construct와 CMC specification은 여전히 특정하지 않는다. 따라서 patent example은 platform feasibility 근거이며 clinical molecule의 exact valency, sequence, affinity 또는 CMC specification으로 인용하지 않는다. [1,2,20]

### 2. MER511: 가장 가까운 Fc-engineered mechanistic benchmark

Endocrine Society 초록은 MER511을 `monomeric TSHR-IgG Fc fusion`으로 규정한다. mutated Fc는 inhibitory/endocytic FcγRIIB affinity를 높이고 activating FcγR/C1q affinity를 없애도록 설계됐다. 이 construct는 (1) soluble decoy에 의한 AAb neutralization, (2) liver sinusoidal endothelial cell의 FcγRIIB-mediated clearance/degradation, (3) antigen-specific B-cell function 억제를 한 분자에 결합한다. [3,5]

WO2025030009A1은 TSHR260/289, 여러 stabilization variants, FcγRIIB-enhancing Fc candidates, FcγR-reducing candidates 및 full-molecule sequence listings를 공개한다. Patent example과 sponsor 설명의 mechanism은 강하게 일치하지만, patent가 final MER511 construct를 특정하지 않는다. 따라서 `P238D`, `S267E/L328F`, `G236R/L328R` 또는 특정 TSHR mutation set을 “MER511 mutation”으로 단정하지 않는다. Sponsor의 TSH non-binding/signaling preservation, antibody-like half-life 및 total-mouse-IgG sparing도 human validation 전에는 design/preclinical claim으로 유지한다. [5,19]

NEXUS는 IV single ascending dose, SC single dose, SC multiple dose로 safety, PK, PD, ADA를 측정한다. 공개 registry에서 용량과 formulation concentration은 확인되지 않았고 결과는 아직 게시되지 않았다. 이 자산을 JHA-88의 수치 anchor로 쓰지 말고, 다음 experimental gates의 qualitative benchmark로 사용한다. [4]

1. TSH non-binding 및 native TSH signaling preservation
2. patient polyclonal TSAb neutralization/depletion
3. activating FcγR/C1q silencing과 FcγRIIB uptake의 분리 검증
4. total IgG sparing 및 antigen-specific B-cell effect
5. IV/SC 양쪽을 허용하는 exposure/formulation

### 3. K1-70: affinity/PK-PD는 강하지만 정상 receptor 차단 liability 존재

K1-70은 환자 B cell에서 얻은 human IgG1 lambda blocking autoantibody다. 논문의 association constant `4 x 10^10 L/mol`은 단순 역수 환산 시 `KD 2.5 x 10^-11 M`, 즉 약 `25 pM`이다. 이 값은 assay 조건이 다른 SPR/BLI affinity와 직접 비교하면 안 된다. CHO-TSHR에서 TSH, stimulating mAb 및 환자 TSAb의 cAMP stimulation을 차단했다. [6]

반복투여 toxicology에서 rat과 cynomolgus monkey 모두 T3/T4 감소와 TSH 증가를 보였고, 저자는 이를 K1-70 pharmacology에 따른 hypothyroid state로 해석했다. Monkey NOAEL은 `100 mg/kg/dose`, rat NOAEL은 확립되지 않았다. [7] 일본 Phase 1은 Graves' disease 환자 `n=12`, single IV `5, 25, 75, 150 mg`이었다. SAE는 없었지만 TEAE는 10/12였고 고용량 thyroid hormone 저하는 L-thyroxine으로 관리됐다. Proptosis “50% of eyes improved”는 small, uncontrolled exploratory inactive-TED signal이므로 efficacy proof가 아니다. [8]

### 4. GenSci098/YB-101/GS-098: 동일 molecule, final patent sequence는 미확정

GenSci 보도자료(2025-12-15, GS-098(YB-101) ex-China licensing)에 따라 GenSci098, YB-101 및 GS-098은 licensing/보유관계 이전에 따른 동일 molecule의 명칭으로 확인된다 [23]. GenSci098 TED Phase 1은 SC `15-270 mg` SAD/MAD, GD Phase 1은 single SC dose이며 YB-101 Phase 2는 `n=232`, randomized/double-blind/placebo-controlled, 24-week dosing으로 2026-09 recruiting 상태다. [9-11]

ETA 2024 poster는 cell-based cross-species TSHR binding, M22-cAMP inhibition, TED patient orbital fibroblast HA/IL-6/IL-8 inhibition, mouse T4 inhibition과 mouse/monkey half-life를 수치로 공개한다. Active-TED donor orbital fibroblast에서 GenSci098/teprotumumab IC50은 HA `0.64/0.79 nM`, IL-6 `2.93/1.97 nM`, IL-8 `5.72/1.57 nM`이었고 inactive-TED donor에서는 각각 `0.44/0.60`, `1.98/1.23`, `3.65/0.99 nM`이었다. 이는 sponsor poster-derived in vitro comparison이며 solution-phase affinity나 임상 efficacy가 아니다. WO2024046384A1은 antibody variable/full-chain 및 Fc candidate sequences를 포함하지만 asset code별 final sequence를 지정하지 않으므로 clinical molecule sequence는 미확정으로 유지한다. [21,22]

### 5. ATX-GD-59: 분자 affinity보다 immune-tolerance PD가 핵심

ATX-GD-59는 antibody/degrader가 아니라 두 TSHR peptide의 antigen-specific immunotherapy다. 따라서 TSAb 또는 TSHR `KD` 비교는 부적절하다. Phase 1은 12명, open-label이고 10명이 전 투여를 완료했다. 7/10의 hormone 개선과 TRAb 변화 상관은 hypothesis-generating이며 spontaneous fluctuation, regression to the mean 및 무대조 설계를 배제하지 못한다. eTPD와 공유하는 benchmark는 total IgG를 보존하는 antigen specificity뿐이다. [12]

### 6. FcRn/Fc benchmark: efficacy ceiling과 broad-IgG liability

Batoclimab의 최신 posted result는 32명 single-arm study다. Week 24 primary responder는 `22/32 (68.8%; 95% CI 50.0-83.9)`, ATD 50% 이상 감량을 동반한 biochemical responder는 `17/32 (53.1%; 95% CI 34.7-70.9)`, ATD-free biochemical responder는 `10/32 (31.3%; 95% CI 16.1-50.0)`다. Registry는 missing Week 24 assessment를 non-responder로 처리했다. 25/32가 전체 study를 완료했고 serious TEAE는 3/32였으나, serious event와 treatment causality는 동일 개념이 아니다. 이 결과는 FcRn blockade의 GD activity signal이나 open-label, single-arm, background-ATD design이므로 placebo-adjusted efficacy, batoclimab 단독효과 또는 remission 증거가 아니다. [13]

Efgartigimod FIH 결과의 multiple-dose total-IgG 평균 75% 감소와 약 8주 recovery는 broad IgG lowering의 PD/회복 benchmark다. 반면 active moderate-to-severe TED에서 각각 수행된 별도의 randomized, parallel, placebo-controlled Phase 3 trials인 NCT06307613과 NCT06307626은 prespecified interim analysis에서 intended efficacy를 입증할 가능성이 낮다고 판단돼 terminated됐다. Registry상 종료 결정은 safety concern 때문이 아니다. NCT06307626은 NCT06307613의 extension study가 아니며, 공개 정보만으로 종료 원인을 target biology, dose/exposure, population 또는 endpoint 중 하나로 귀속하거나 FcRn class 전체의 TED 비효과로 일반화할 수 없다. [14-16]

Nipocalimab은 pH-independent high-affinity FcRn binding, aglycosylated/effectorless full-IgG라는 Fc engineering comparator다. 다만 GD/TED 직접 임상 데이터가 없어 disease benchmark로는 사용하지 않는다. [17,18]

## JHA-88로 전달할 관찰 근거

| 설계축 | 공개 관찰 | Source/evidence | Confidence/경계 |
|---|---|---|---|
| Cargo binding | K1-70 reported Ka와 GenSci098 cell-binding EC50/cAMP IC50 공개 | Peer-reviewed paper, sponsor poster | 서로 다른 assay이므로 직접 순위화 불가 |
| Native signaling | MER511은 TSH non-binding/signaling preservation을 주장; K1-70은 정상 signaling 차단 liability 확인 | Sponsor/patent, preclinical/Phase 1 | MER511 human validation 없음 |
| Fc routing | Merida patent는 FcγRIIB-enhancing, FcγR-reducing candidate mutations와 sequences 공개 | Patent family WO2025030009A1 | MER511 final mutation set 미확정 |
| Lysosomal routing | Lycia patent는 ASGPR ligand, Fc/HSA carrier, TSHR/linker formats 공개 | Patent family WO2025207934A1 | LCA-0321 final construct 미확정 |
| Selectivity | MER511 total-mouse-IgG sparing claim; FcRn agents는 broad total-IgG lowering | Sponsor/preclinical, Phase 1 | Cross-study 정량 비교 제한 |
| Human PD | Batoclimab Week 24 biochemical response 68.8%, ATD-free response 31.3%; K1-70 TSAb suppression과 hormone lowering | Registry posted result, Phase 1 paper | Batoclimab single-arm/background ATD; K1-70 n=12 |

## Proposed JHA-88 design/assay gates

아래는 경쟁사 공개 spec이 아니라 위 관찰에서 도출한 내부 권고이며 empirical validation이 필요하다.

| 설계축 | Proposed gate | 근거 유형 |
|---|---|---|
| Cargo binding | Patient polyclonal IgG에서 affinity/avidity/functional neutralization을 함께 측정 | Evidence-derived |
| Native signaling | TSH dose-response shift와 basal cAMP 영향 없음; TSAb inhibition/depletion과 분리 | Risk-control |
| Fc routing | FcγRIIB uptake/clearance, FcγRI/IIA/IIIA/C1q silencing, FcRn PK를 각각 정량 | Engineering recommendation |
| Selectivity | TSAb/TRAb depletion 대비 total IgG, vaccine IgG와 albumin 보존비 설정 | Evidence-derived/risk-control |
| Developability | SEC monomer/HMW, Tm, pI, viscosity, solubility, expression titer, freeze-thaw와 SC concentration 측정 | Engineering recommendation |
| Human PD | TRAb/TSI/TSAb, total IgG, FT3/FT4/TSH, ATD reduction, rebound와 off-treatment durability 분리 | Evidence-derived |
| Evidence boundary | Patent candidate를 final asset spec으로 승격하지 않고 sponsor claim과 verified result를 분리 | Governance gate |

## Data gaps 및 권장 후속 확인

1. **Patent-to-final-asset mapping:** 세 primary family가 candidate sequence/design space를 공개하지만 final MER511, LCA-0321 및 GenSci098/YB-101/GS-098 sequence selection은 확인되지 않았다. 해당 연결은 sponsor confirmation 또는 asset-code가 포함된 후속 patent/regulatory disclosure가 필요하다.
2. **Legal FTO:** 본 technical scan은 국가별 live claim, expiry/PTA/PTE, prosecution history 또는 license chain을 판정하지 않았다. Legal FTO는 patent counsel의 별도 claim chart가 필요하다.
3. **Assay-normalized affinity:** K1-70 Ka, GenSci098 cell EC50, patent FcγRIIB range는 assay가 다르다. 동일 antigen construct, temperature, pH 및 immobilization에서 SPR/BLI를 재측정하지 않으면 자산 간 순위를 정하지 않는다.
4. **CMC/developability:** 여덟 자산 모두 비교 가능한 SEC, DLS, DSF, pI, viscosity, solubility 및 expression yield package가 공개되지 않았다. “SC 임상”을 고농도 SC developability의 충분한 증거로 해석하지 않는다.
5. **Patient-sample breadth:** MER511의 polyclonal neutralization claim은 sample 수/분포가 공개되지 않았다. TSAb epitope heterogeneity를 반영한 최소 cohort와 non-stimulating TRAb/TBAb interference panel이 필요하다.
6. **Durability:** FcRn recovery benchmark는 있지만 antigen-selective depletion 뒤 TSAb rebound/human durability는 검색 범위에서 확인되지 않았다. JHA-88에서 half-life와 disease modification을 동일 개념으로 취급하지 않는다.

## 참고문헌 및 공개 source

1. Lycia Therapeutics. [Programs: LCA-0321](https://lyciatx.com/pipeline/programs/). Sponsor pipeline; accessed 2026-09-27.
2. CTIS. [LCA-0321-01, 2025-524053-14-00](https://euclinicaltrials.eu/ctis-public/view/2025-524053-14-00?lang=en). Registry; accessed 2026-09-27.
3. Merida Biosciences. [Pipeline and programs: MER511](https://meridabio.com/pipeline-programs/). Sponsor source; accessed 2026-09-27.
4. ClinicalTrials.gov. [NCT07305818 NEXUS](https://clinicaltrials.gov/study/NCT07305818). Registry; accessed 2026-09-27.
5. Merida Biosciences. [Specific and Deep Depletion of anti-TSHR Autoantibodies](https://doi.org/10.1210/jendso/bvaf149.2238). *J Endocr Soc.* 2025;9(Suppl 1), congress abstract.
6. Evans M, et al. [Monoclonal autoantibodies to the TSH receptor](https://pubmed.ncbi.nlm.nih.gov/20550534/). *Clin Endocrinol.* 2010;73:404-412. PMID 20550534.
7. Furmaniak J, et al. [Preclinical studies on the toxicology, pharmacokinetics and safety of K1-70, a human monoclonal autoantibody to the TSH receptor with TSH antagonist activity](https://pubmed.ncbi.nlm.nih.gov/32257067/). *Auto Immun Highlights.* 2019;10:11. PMID 32257067.
8. Noh JY, et al. [Safety, pharmacokinetics, and potential benefits of TSH-receptor-specific monoclonal autoantibody K1-70 in Japanese Graves' disease patients: results of a phase 1 trial](https://pubmed.ncbi.nlm.nih.gov/40301067/). *Endocr J.* 2025;72(8):897-909. PMID 40301067.
9. ClinicalTrials.gov. [NCT06569758 GenSci098 in TED](https://clinicaltrials.gov/study/NCT06569758). Registry; accessed 2026-09-27.
10. ClinicalTrials.gov. [NCT07286656 GenSci098 in GD](https://clinicaltrials.gov/study/NCT07286656). Registry; accessed 2026-09-27.
11. ClinicalTrials.gov. [NCT07682896 YB-101 Phase 2 in GD](https://clinicaltrials.gov/study/NCT07682896). Registry; accessed 2026-09-27.
12. Pearce SHS, et al. [ATX-GD-59 Phase 1](https://pubmed.ncbi.nlm.nih.gov/31194638/). *Thyroid.* 2019;29:1003-1011. PMID 31194638.
13. ClinicalTrials.gov. [NCT05907668 batoclimab in GD, posted results](https://clinicaltrials.gov/study/NCT05907668). Registry results posted 2026-08-13; accessed 2026-09-27.
14. Ulrichts P, et al. [Efgartigimod safely and sustainably reduces IgGs in humans](https://pubmed.ncbi.nlm.nih.gov/30040076/). *J Clin Invest.* 2018;128:4372-4386. PMID 30040076.
15. ClinicalTrials.gov. [NCT06307613 UplighTED](https://clinicaltrials.gov/study/NCT06307613). Registry; accessed 2026-09-27.
16. ClinicalTrials.gov. [NCT06307626, ARGX-113-2309, parallel Phase 3 study in active moderate-to-severe TED](https://clinicaltrials.gov/study/NCT06307626). Registry; accessed 2026-09-27.
17. Seth NP, et al. [Nipocalimab, an immunoselective FcRn blocker that lowers IgG and has unique molecular properties](https://pubmed.ncbi.nlm.nih.gov/39936406/). *mAbs.* 2025;17(1):2461191. PMID 39936406.
18. Leu JH, et al. [Pharmacokinetics and pharmacodynamics across infusion rates of intravenously administered nipocalimab: results of a phase 1, placebo-controlled study](https://pubmed.ncbi.nlm.nih.gov/38362023/). *Front Neurosci.* 2024;18:1302714. PMID 38362023.
19. Merida Biosciences. [WO2025030009A1, Molecules for controlling immune response](https://patents.google.com/patent/WO2025030009A1/en). Patent publication; priority 2023-08-01; published 2025-02-06; accessed 2026-09-27.
20. Lycia Therapeutics. [WO2025207934A1, Lysosomal targeting bifunctional molecules for degradation of TSHR autoantibodies](https://patents.google.com/patent/WO2025207934A1/en). Patent publication; priority 2024-03-28; published 2025-10-02; accessed 2026-09-27.
21. Changchun GeneScience Pharmaceutical. [WO2024046384A1, Antibody binding to TSHR and use thereof](https://patents.google.com/patent/WO2024046384A1/en). Patent publication; priority 2022-08-31; published 2024-03-07; accessed 2026-09-27.
22. Sun G. [GenSci098: a potent TSHR antagonistic antibody for the treatment of TED](https://www.eta2024.com/files/download/SHC-602.pdf). ETA 2024 poster SHC-602; sponsor-authored conference poster.
23. GenSci. [GenSci secures up to $1.365B in global ex-China licensing deal for GS-098 (YB-101) with RTW Investments](https://www.genscigroup.com/en/news/media/183). Press release, 2025-12-15; accessed 2026-10-01.

## QA self-check

- [x] Section C4 관련 주요 자산 8개 수합
- [x] Binding affinity, 물성/developability, in vitro/in vivo/human data를 공통 열로 비교
- [x] 공개 상태를 `공개 수치`, `정성 정보`, `검색 범위에서 미확인`, `비공개/NR 명시`, `해당 없음`으로 분리
- [x] Tier 1 public patent family/sequence-disclosure scan 및 asset-mapping confidence 기록
- [x] LCA-0321/MER511의 sponsor claim과 registry/논문 fact 분리 및 v2 confidence 유지
- [x] GenSci098/YB-101/GS-098을 확인된 동일 molecule alias로 통합하되 final patent sequence는 미확정으로 표시
- [x] KHN939/SCTT11 등 target 미상 자산에 기전 부여하지 않음
- [x] 각 정량 결과에 source type과 원문 링크 제공
- [x] JHA-88 전달용 observed evidence와 proposed internal gate 분리
- [x] 본문 가운뎃점 미사용
- [x] 2026-10-01 follow-up fact-check: 참고문헌 22건 서지·수치 검증 및 오류 수정(일본 K1-70 Phase 1 저자/대상자, Furmaniak 서지, nipocalimab 2건 저널/저자, LCA-0321 코드 명시 여부, CTIS 공식 포털 링크)
