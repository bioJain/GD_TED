---
linear_issue: JHA-84
created: 2026-09-27
source: claude-code
milestone: cluster-5-etpd-molecular-design
status: in-review
search_cutoff: 2026-09-27
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

- 공개 근거에서 직접 비교 가능한 분자 정량치는 매우 제한적이다. 여덟 자산 중 anti-TSHR 결합상수가 공개된 것은 K1-70뿐이며, 공개 association constant `4 x 10^10 L/mol`을 역수로 환산하면 `KD 약 25 pM`이다. LCA-0321, MER511, GenSci098/YB-101, batoclimab의 `KD`, `kon`, `koff` 및 developability panel은 **비공개**다.
- MER511은 eTPD 설계에 가장 직접적인 construct benchmark다. 공개 초록상 monomeric TSHR ectodomain-mutant Fc fusion이고, Fc는 FcγRIIB affinity를 높이는 한편 activating FcγR/C1q affinity를 제거하도록 설계됐다. 그러나 mutation sequence, 각 receptor affinity, purity/aggregation, thermal stability 및 human PK는 **비공개**다. 따라서 공개 정보만으로 Fc engineering 조합을 복제하거나 우열을 정할 수 없다.
- K1-70은 receptor-blocking benchmark로 높은 affinity와 human PK/PD proof를 제공하지만, 정상 TSH signaling도 차단한다. 원숭이/쥐에서 hypothyroid pharmacology가 관찰됐고 일본 Phase 1 고용량에서도 thyroid hormone 저하와 L-thyroxine 보조가 필요했다. TSAb 제거형 eTPD의 목표 product profile은 이 on-target liability를 피해야 한다.
- Batoclimab과 efgartigimod는 antigen-selective하지 않은 FcRn benchmark다. 전자는 GD Phase 2에서 Week 24 biochemical responder `68.8% (22/32; 95% CI 50.0-83.9)`를 보였지만 open-label, single-arm 결과다. 후자는 건강인에서 multiple dosing 후 total IgG를 평균 75% 낮춘 class-level PD benchmark이나 TED Phase 3 두 건은 futility로 종료됐다.
- LCA-0321과 MER511의 human efficacy/developability 결론은 아직 낼 수 없다. 각각 v2 evidence confidence `Low`, `Low-moderate`를 유지하며, sponsor claim과 registry fact를 분리한다.

## 범위와 판독 규칙

Section C4 가운데 TSHR/자가항체 축 5개와 FcRn/Fc engineering 비교군 3개를 선정했다. `pipeline_assets_v2.csv`의 asset key를 유지했고 live registry/PubMed를 2026-09-27에 재확인했다. 단계는 적응증별로 기록하며, 다른 적응증의 승인/후기 단계로 올려 쓰지 않았다.

- **공개**: 논문, 학회 초록, registry 또는 sponsor가 값/특성을 명시한 경우
- **비공개**: 확인한 공개 source set에 값이 없는 경우. 0 또는 측정하지 않았다는 뜻이 아님
- **해당 없음**: 해당 modality에 그 지표를 그대로 적용할 수 없는 경우
- affinity 단위와 assay format이 다른 값은 직접 순위화하지 않음
- sponsor/학회 초록의 preclinical 주장은 독립 재현으로 간주하지 않음

## 공통 비교표

| 자산 | Construct/표적 | Binding affinity | 물성/developability | in vitro/in vivo 및 human data | 근거 수준 |
|---|---|---|---|---|---|
| **LCA-0321** | anti-TSHR AAb LYTAC degrader | anti-TSHR AAb `KD/kon/koff`: **비공개**; lysosomal receptor affinity: **비공개** | sequence, MW, valency, Fc isotype/mutations, pI, Tm, aggregation, solubility, formulation, yield: **비공개**; Phase 1 SAD/MAD, planned `n=48` | Sponsor는 선택적 결합/신속 제거와 general immunosuppression 회피를 주장. 정량 preclinical result와 human result는 **비공개** | Sponsor pipeline + CTIS; v2 confidence **Low** [1,2] |
| **MER511** | monomeric TSHR ectodomain-mutant Fc fusion; anti-TSHR AAb/FcγRIIB | patient AAb, FcγRIIB, activating FcγR, FcRn, C1q의 정량 affinity: **비공개** | FcγRIIB affinity 증가, activating FcγR/C1q 결합 제거 설계; exact mutations/sequence, MW, pI, Tm, SEC monomer, viscosity, expression, formulation: **비공개**; IV/SC SAD/MAD | Patient-derived stimulating mAb 및 polyclonal GD/TED sample neutralization, humanized FcγR/FcRn mouse에서 transferred M22 선택적 depletion, total mouse IgG 보존을 sponsor 초록이 보고. NEXUS Phase 1 human 결과 **비공개** | Congress abstract + sponsor + registry; v2 confidence **Low-moderate** [3-5] |
| **K1-70** | human IgG1 lambda TSHR-blocking monoclonal autoantibody | association constant `4 x 10^10 L/mol`, 환산 `KD 약 25 pM`; assay 간 비교 주의 | full IgG; IV/IM 연구. sequence, pI, Tm, aggregation, solubility, expression/formulation: **비공개** | CHO에서 TSH/TSAb-induced cAMP 차단. Rat/monkey 반복투여에서 T3/T4 저하, TSH 증가; monkey NOAEL `100 mg/kg/dose`, rat NOAEL 미확립. 일본 Phase 1 `n=12`, single IV `5/25/75/150 mg`; SAE 0, TEAE `83.3%`, 고용량 thyroid hormone 저하/L-thyroxine 관리, TSAb 저하 | Peer-reviewed in vitro, GLP-like preclinical, Phase 1 [6-8] |
| **GenSci098/YB-101** | v2상 TSHR-blocking monoclonal antibody; GenSci098에서 YB-101로 개발명 전환 | TSHR `KD/kon/koff`, epitope, TSH/TSAb competition potency: **비공개** | SC; Phase 1에서 `15/45/90/180/270 mg` dose levels 공개. sequence, isotype/Fc, pI, Tm, aggregation, formulation/concentration, bioavailability: **비공개** | TED Phase 1 SAD/MAD `n=76` recruiting; GD Phase 1 SAD `n=24` recruiting; GD Phase 2 randomized placebo-controlled `n=232`, 24-week dosing recruiting. 결과 **비공개** | Registry + v2 mapping; v2 confidence **Moderate** [9-11] |
| **ATX-GD-59** | 두 TSHR peptide의 intradermal antigen-specific immunotherapy; TSHR-reactive T cell tolerance | 단일 ligand-receptor `KD`: **해당 없음**; peptide sequence/MHC affinity: **비공개** | 10 intradermal doses/18 weeks; peptide별 함량, formulation stability, solubility, 제조수율: **비공개** | Phase 1 open-label `n=12`; 10회 완료 `n=10`; Week 18 fT3 정상범위 `5/10`, 추가 개선 `2/10`, 악화 `3/10`; TRAb-fT3 변화 상관 `r=0.85, p=0.002`; 주 AE는 경증 injection-site swelling/pain. 대조군이 없어 remission proof 아님 | Peer-reviewed single-arm Phase 1; v2 confidence **Low-moderate** [12] |
| **Batoclimab/IMVT-1401** | fully human anti-FcRn mAb; broad IgG lowering | FcRn `KD/kon/koff`, pH 6.0/7.4 selectivity: **비공개** | SC `680 mg QW` 12주 후 `340 mg QW` 12주. sequence, isotype/effector silencing, pI, Tm, aggregation, formulation: **비공개** | GD Phase 2 open-label `n=32`: Week 24 FT3/FT4 정상/LLN, ATD 증량 없음 `68.8%`; ATD 50% 이상 감량 동반 `53.1%`; ATD-free biochemical response `31.3%`. 25/32 study completion, serious TEAE 3/32. 단일군이므로 약물 효과 크기 확정 불가 | ClinicalTrials.gov posted results, sponsor-controlled Phase 2 [13] |
| **Efgartigimod alfa** | engineered human IgG1 Fc fragment, ABDEG; FcRn antagonist | FcRn affinity가 wild-type Fc보다 acidic/neutral pH에서 증가했다는 공개 논문 근거; 본 조사에서 검증한 source의 정량 `KD`: **비공개** | Fc-only, no Fab; IV 및 PH20 SC 제품. exact mutation set은 peer-reviewed paper에 공개됐으나 본 deliverable에서 sequence/FTO 검증은 미수행; pI, Tm, aggregation, viscosity는 **비공개** | FIH healthy volunteer `n=62`: single dose total IgG 최대 50% 감소, multiple dosing 평균 75% 감소, 마지막 dose 약 8주 후 baseline 복귀; albumin/비-IgG Ig 영향 없음. 별도의 randomized, parallel, placebo-controlled TED Phase 3 trials인 NCT06307613과 NCT06307626은 interim futility assessment 후 terminated | Peer-reviewed Phase 1 + registry [14-16] |
| **Nipocalimab/M281** | fully human aglycosylated effectorless IgG1 anti-FcRn mAb | neutral/acidic pH 모두 high-affinity, unique IgG-binding-site epitope; 정량 `KD`는 본 source set에서 **비공개** | IV full mAb; aglycosylated/effectorless. sequence, pI, Tm, aggregation, formulation: **비공개** | Cell/in vivo에서 dose/time-dependent FcRn occupancy 및 IgG 감소. Healthy Phase 1에서 `30 mg/kg`을 7.5-60분, `60 mg/kg`을 15분 투여 가능; active GD/TED efficacy data **비공개** | Peer-reviewed molecular/nonclinical + Phase 1; 질환 직접성 낮음 [17,18] |

## 자산별 deep-dive

### 1. LCA-0321: selective degradation concept, 공개 spec은 거의 없음

Lycia는 LCA-0321을 anti-TSHR autoantibody를 결합해 lysosomal elimination하는 LYTAC로 설명한다. CTIS의 LCA-0321-01은 first-in-human SAD/MAD, planned `n=48`이다. 그러나 공개 pipeline/registry에는 TSHR antigen domain, valency, lysosome-shuttling receptor, linker, Fc architecture, binding constants 또는 preclinical depletion curve가 없다. 따라서 “rapidly eliminate”는 sponsor design intent이지 검증된 human kinetic claim이 아니다. eTPD 설계 input으로 사용할 수 있는 값은 현재 **없음**이며, comparator assay에 동일 patient IgG panel을 포함시키는 수준으로만 활용한다. [1,2]

### 2. MER511: 가장 가까운 Fc-engineered mechanistic benchmark

Endocrine Society 초록은 MER511을 `monomeric TSHR-IgG Fc fusion`으로 규정한다. mutated Fc는 inhibitory/endocytic FcγRIIB affinity를 높이고 activating FcγR/C1q affinity를 없애도록 설계됐다. 이 construct는 (1) soluble decoy에 의한 AAb neutralization, (2) liver sinusoidal endothelial cell의 FcγRIIB-mediated clearance/degradation, (3) antigen-specific B-cell function 억제를 한 분자에 결합한다. Sponsor는 TSH non-binding/TSH signaling preservation, antibody-like half-life, total mouse IgG sparing을 보고했지만 정량 표, comparator dose, sample 수, 통계와 exact Fc mutation은 공개 초록에 없다. [3,5]

NEXUS는 IV single ascending dose, SC single dose, SC multiple dose로 safety, PK, PD, ADA를 측정한다. 공개 registry에서 용량, formulation concentration 및 결과는 비공개다. 이 자산을 JHA-88의 수치 anchor로 쓰지 말고, 다음 experimental gates의 qualitative benchmark로 사용한다. [4]

1. TSH non-binding 및 native TSH signaling preservation
2. patient polyclonal TSAb neutralization/depletion
3. activating FcγR/C1q silencing과 FcγRIIB uptake의 분리 검증
4. total IgG sparing 및 antigen-specific B-cell effect
5. IV/SC 양쪽을 허용하는 exposure/formulation

### 3. K1-70: affinity/PK-PD는 강하지만 정상 receptor 차단 liability 존재

K1-70은 환자 B cell에서 얻은 human IgG1 lambda blocking autoantibody다. 논문의 association constant `4 x 10^10 L/mol`은 단순 역수 환산 시 `KD 2.5 x 10^-11 M`, 즉 약 `25 pM`이다. 이 값은 assay 조건이 다른 SPR/BLI affinity와 직접 비교하면 안 된다. CHO-TSHR에서 TSH, stimulating mAb 및 환자 TSAb의 cAMP stimulation을 차단했다. [6]

반복투여 toxicology에서 rat과 cynomolgus monkey 모두 T3/T4 감소와 TSH 증가를 보였고, 저자는 이를 K1-70 pharmacology에 따른 hypothyroid state로 해석했다. Monkey NOAEL은 `100 mg/kg/dose`, rat NOAEL은 확립되지 않았다. [7] 일본 Phase 1은 `n=12`, single IV `5, 25, 75, 150 mg`이었다. SAE는 없었지만 TEAE는 10/12였고 고용량 thyroid hormone 저하는 L-thyroxine으로 관리됐다. Proptosis “50% of eyes improved”는 small, uncontrolled exploratory inactive-TED signal이므로 efficacy proof가 아니다. [8]

### 4. GenSci098/YB-101: 임상 개발은 진전, 분자 identity/spec은 비공개

Registry상 GenSci098 TED Phase 1은 SC `15-270 mg` SAD/MAD, GD Phase 1은 single SC dose다. YB-101 Phase 2는 `n=232`, randomized/double-blind/placebo-controlled, 24-week dosing으로 2026-09 recruiting 상태다. 공개 registry는 GenSci098와 YB-101의 동일 분자성, TSHR epitope, blocking mechanism, affinity, sequence 또는 Fc design을 증명하지 않는다. 동일 asset mapping은 v2 curation을 따르되 public molecular proof가 없다는 제한을 유지한다. [9-11]

### 5. ATX-GD-59: 분자 affinity보다 immune-tolerance PD가 핵심

ATX-GD-59는 antibody/degrader가 아니라 두 TSHR peptide의 antigen-specific immunotherapy다. 따라서 TSAb 또는 TSHR `KD` 비교는 부적절하다. Phase 1은 12명, open-label이고 10명이 전 투여를 완료했다. 7/10의 hormone 개선과 TRAb 변화 상관은 hypothesis-generating이며 spontaneous fluctuation, regression to the mean 및 무대조 설계를 배제하지 못한다. eTPD와 공유하는 benchmark는 total IgG를 보존하는 antigen specificity뿐이다. [12]

### 6. FcRn/Fc benchmark: efficacy ceiling과 broad-IgG liability

Batoclimab의 최신 posted result는 32명 single-arm study다. Week 24 primary responder는 `22/32`이고 ATD-free biochemical responder는 `10/32`다. 7명이 전체 study를 완료하지 않았으며 serious TEAE가 3명에게 보고됐다. 이 결과는 FcRn blockade가 GD biochemical control을 만들 수 있다는 clinical benchmark이나, placebo-adjusted efficacy, remission 또는 TSAb-selective mechanism의 증거는 아니다. [13]

Efgartigimod FIH 결과의 multiple-dose total-IgG 평균 75% 감소와 약 8주 recovery는 broad IgG lowering의 PD/회복 benchmark다. 반면 active moderate-to-severe TED에서 각각 수행된 별도의 randomized, parallel, placebo-controlled Phase 3 trials인 NCT06307613과 NCT06307626은 interim analysis 뒤 efficacy 달성 가능성이 낮아 terminated됐다. NCT06307626은 NCT06307613의 extension study가 아니다. 따라서 systemic IgG lowering의 크기만으로 TED clinical efficacy를 예측하면 안 된다. [14-16]

Nipocalimab은 pH-independent high-affinity FcRn binding, aglycosylated/effectorless full-IgG라는 Fc engineering comparator다. 다만 GD/TED 직접 임상 데이터가 없어 disease benchmark로는 사용하지 않는다. [17,18]

## JHA-88로 전달할 설계 입력

| 설계축 | 공개 benchmark | JHA-88 적용 |
|---|---|---|
| Cargo affinity | K1-70 약 25 pM만 정량 공개. Degrader/fusion은 비공개 | 단일 경쟁값을 target으로 복제하지 않음. Patient polyclonal IgG에서 affinity/avidity/functional neutralization을 함께 gate |
| Native signaling 보존 | MER511은 TSH non-binding/signaling preservation을 주장. K1-70은 정상 signaling 차단 liability 확인 | TSH dose-response shift 없음, basal cAMP 영향 없음, TSAb inhibition/depletion과 분리한 필수 gate |
| Fc routing | MER511은 FcγRIIB 증가, activating FcγR/C1q 제거라는 방향 공개 | FcγRIIB uptake/clearance, FcγRI/IIA/IIIA 및 C1q silencing, FcRn PK를 각각 정량. Exact mutation은 별도 patent/FTO 검토 전 미정 |
| Selectivity | MER511 mouse total IgG sparing claim; FcRn agents는 total IgG 50-75% lowering benchmark | TSAb/TRAb depletion 대비 total IgG, vaccine IgG, albumin 보존비를 명시 |
| Developability | MER511 IV/SC, LCA SAD/MAD, YB-101 SC 가능성만 공개. CMC 값 비공개 | SEC monomer, HMW, Tm, pI, viscosity, solubility, expression titer, freeze-thaw, SC concentration을 자체 측정 gate로 설정 |
| Human PD | Batoclimab Week 24 biochemical response 68.8%, ATD-free 31.3%; K1-70 TSAb suppression과 hormone lowering | TRAb/TSI/TSAb, total IgG, FT3/FT4/TSH, ATD reduction, rebound 및 off-treatment durability를 분리 |
| Evidence boundary | LCA/MER human 결과 없음; YB-101 결과 없음; ATX와 batoclimab은 single-arm | Sponsor claim을 target product claim으로 승격하지 않음. 공개되지 않은 값은 `비공개` 유지 |

## Data gaps 및 권장 후속 확인

1. **특허 family/sequence/FTO:** MER511 Fc mutations, LCA-0321 architecture 및 GenSci098/YB-101 sequence는 공개 web/registry/논문 근거로 해소되지 않았다. Patent landscaping과 sequence listing 전문 검토를 별도 수행한다.
2. **Assay-normalized affinity:** K1-70 값도 association constant 기반이다. 동일 antigen construct, temperature, pH 및 immobilization에서 SPR/BLI를 재측정하지 않으면 자산 간 순위를 정하지 않는다.
3. **CMC/developability:** 여덟 자산 모두 비교 가능한 SEC, DLS, DSF, pI, viscosity, solubility 및 expression yield package가 공개되지 않았다. “SC 임상”을 고농도 SC developability의 충분한 증거로 해석하지 않는다.
4. **Patient-sample breadth:** MER511의 polyclonal neutralization claim은 sample 수/분포가 공개되지 않았다. TSAb epitope heterogeneity를 반영한 최소 cohort와 non-stimulating TRAb/TBAb interference panel이 필요하다.
5. **Durability:** FcRn recovery benchmark는 있지만 antigen-selective depletion 뒤 TSAb rebound/human durability는 비공개다. JHA-88에서 half-life와 disease modification을 동일 개념으로 취급하지 않는다.

## 참고문헌 및 공개 source

1. Lycia Therapeutics. [Programs: LCA-0321](https://lyciatx.com/pipeline/programs/). Sponsor pipeline; accessed 2026-09-27.
2. CTIS. [LCA-0321-01, 2025-524053-14-00](https://ctis.eu/trial/2025-524053-14-00). Registry; accessed 2026-09-27.
3. Merida Biosciences. [Pipeline and programs: MER511](https://meridabio.com/pipeline-programs/). Sponsor source; accessed 2026-09-27.
4. ClinicalTrials.gov. [NCT07305818 NEXUS](https://clinicaltrials.gov/study/NCT07305818). Registry; accessed 2026-09-27.
5. Merida Biosciences. [Specific and Deep Depletion of anti-TSHR Autoantibodies](https://doi.org/10.1210/jendso/bvaf149.2238). *J Endocr Soc.* 2025;9(Suppl 1), congress abstract.
6. Evans M, et al. [Monoclonal autoantibodies to the TSH receptor](https://pubmed.ncbi.nlm.nih.gov/20550534/). *Clin Endocrinol.* 2010;73:404-412. PMID 20550534.
7. Furmaniak J, et al. [Preclinical toxicology, PK and safety of K1-70](https://pubmed.ncbi.nlm.nih.gov/32257067/). *Auto Immun Highlights.* 2020;11:9. PMID 32257067.
8. Ohye H, et al. [Japanese K1-70 Phase 1](https://pubmed.ncbi.nlm.nih.gov/40301067/). *Endocr J.* 2025. PMID 40301067.
9. ClinicalTrials.gov. [NCT06569758 GenSci098 in TED](https://clinicaltrials.gov/study/NCT06569758). Registry; accessed 2026-09-27.
10. ClinicalTrials.gov. [NCT07286656 GenSci098 in GD](https://clinicaltrials.gov/study/NCT07286656). Registry; accessed 2026-09-27.
11. ClinicalTrials.gov. [NCT07682896 YB-101 Phase 2 in GD](https://clinicaltrials.gov/study/NCT07682896). Registry; accessed 2026-09-27.
12. Pearce SHS, et al. [ATX-GD-59 Phase 1](https://pubmed.ncbi.nlm.nih.gov/31194638/). *Thyroid.* 2019;29:1003-1011. PMID 31194638.
13. ClinicalTrials.gov. [NCT05907668 batoclimab in GD, posted results](https://clinicaltrials.gov/study/NCT05907668?format=json). Registry results posted 2026-08-13; accessed 2026-09-27.
14. Ulrichts P, et al. [Efgartigimod safely and sustainably reduces IgGs in humans](https://pubmed.ncbi.nlm.nih.gov/30040076/). *J Clin Invest.* 2018;128:4372-4386. PMID 30040076.
15. ClinicalTrials.gov. [NCT06307613 UplighTED](https://clinicaltrials.gov/study/NCT06307613). Registry; accessed 2026-09-27.
16. ClinicalTrials.gov. [NCT06307626, ARGX-113-2309, parallel Phase 3 study in active moderate-to-severe TED](https://clinicaltrials.gov/study/NCT06307626). Registry; accessed 2026-09-27.
17. Ling LE, et al. [Nipocalimab molecular properties](https://pubmed.ncbi.nlm.nih.gov/39936406/). *mAbs.* 2025;17:2456156. PMID 39936406.
18. Ling LE, et al. [Nipocalimab PK/PD across infusion rates](https://pubmed.ncbi.nlm.nih.gov/38362023/). *Clin Transl Sci.* 2024;17:e13751. PMID 38362023.

## QA self-check

- [x] Section C4 관련 주요 자산 8개 수합
- [x] Binding affinity, 물성/developability, in vitro/in vivo/human data를 공통 열로 비교
- [x] 공개되지 않은 수치는 추정하지 않고 `비공개`로 표시
- [x] LCA-0321/MER511의 sponsor claim과 registry/논문 fact 분리 및 v2 confidence 유지
- [x] KHN939/SCTT11 등 target 미상 자산에 기전 부여하지 않음
- [x] 각 정량 결과에 source type과 원문 링크 제공
- [x] JHA-88 전달용 설계 입력과 evidence boundary 명시
- [x] 본문 가운뎃점 미사용
