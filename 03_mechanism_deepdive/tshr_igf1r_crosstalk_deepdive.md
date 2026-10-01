---
linear_issue: JHA-79
created: 2026-09-28
source: manual
milestone: cluster-3-mechanism-deepdive
status: done
inputs:
  - 00_legacy_unsorted/GD_TED_report.md
  - _shared/GD_TED_reference.md
  - _shared/GD_TED_qa_checklist.md
  - 03_mechanism_deepdive/igf1r_autoantigen_review.md
  - 03_mechanism_deepdive/orbital_fibroblast_igf1r_maturity.md
---

# TSHR-IGF-1R complex crosstalk: 경쟁가설 3종 signaling deep-dive

## Executive conclusion

**TSHR-IGF-1R crosstalk는 생물학적으로 지지되지만, 분자배치는 아직 `proposed`임.** 가장 재현성 높은 기능적 관찰은 (1) TSH/IGF-1 동시 자극의 ERK 및 hyaluronan(HA) 상승, (2) TSHR-selective agonist/TSAb 반응 중 일부가 IGF-1R 또는 arrestin-β-1(ARRB1) 억제로 소실됨, (3) 두 수용체의 proximity/co-immunoprecipitation임[1-6]. 그러나 이 결과만으로 **ARRB1 scaffold 모델**과 **ectodomain 직접결합 모델** 중 하나를 배타적으로 확정할 수 없음. 직접결합은 engineered cell/modeling 중심이고, ARRB1은 환자 유래 orbital fibroblast(OF)의 기능적 perturbation 근거가 더 강함[5,7]. 두 기전은 동시에 존재할 수도 있음.

세 번째 축인 **IGF-1R directly-stimulating autoantibody 가설**은 현재 근거가 가장 약함. M22는 IGF-1R에 결합하거나 IGF-1R autophosphorylation을 유발하지 않으면서도 IGF-1R-dependent HA 반응을 만들며, TSHR 차단은 그 반응을 제거함[2,4,8]. 따라서 현재의 보수적 모델은 **TSAb가 TSHR을 직접 자극하고, IGF-1R은 receptor complex/crosstalk를 통해 신호를 증폭**한다는 것임. 2025년 혈청 anti-IGF-1R 연구는 항체의 존재 가능성을 지지하지만, 병인성 agonist가 아니라 억제/보호 방향을 제안하므로 이 결론을 뒤집지 않음[9,10].

조직별 출력은 다름. OF에서는 HA가 crosstalk perturbation으로 직접 측정된 대표 출력이고, proliferation은 IGF-1 ligand-dependent 반응에서 측정된 별도 출력이며(crosstalk perturbation만으로 측정된 것 아님), adipogenic remodeling은 별도의 제한적 근거로 분리해야 함(crosstalk perturbation 연구들은 adipocyte fate를 직접 측정하지 않음)[1,11,12]. thyrocyte에서는 NIS, TPO, thyroglobulin 및 thyroid hormone synthesis가 주 출력임[1,11,12]. 따라서 동일한 receptor crosstalk를 TED와 thyroid hormone biology에서 동일한 downstream program으로 도식화하면 안 됨.

## 1. 용어와 판정 원칙

- **Established observation:** 실험에서 직접 관찰된 receptor proximity, perturbation-response 또는 downstream readout.
- **Supported model:** 복수 perturbation이 일관되지만 정확한 분자배치가 확정되지 않은 해석.
- **Proposed:** 직접결합 interface, ARRB1의 구조적 위치, 환자 내 agonistic anti-IGF-1R Ab처럼 대안 설명이 남은 기전.
- `Complex`는 고정된 단일 stoichiometry를 뜻하지 않음. proximity, co-immunoprecipitation, functional coupling을 포괄하는 작업 용어임.
- IGF-1R inhibitor의 효과는 IGF-1R이 신호에 필요함을 지지하지만, IGF-1R이 자가항체의 직접 항원임을 증명하지 않음. 특히 linsitinib은 IGF-1R/IR dual kinase inhibitor이므로 receptor attribution에 한계가 있음[12].

## 2. 공통 signaling backbone

### 2.1 관찰된 입력과 proximal event

1. **TSHR 입력:** TSH 또는 TSAb(M22, KSAb1, 환자 IgG)가 TSHR을 활성화. TSHR은 GPCR로서 canonical Gs/cAMP 신호와 Gi/Go-linked ERK 신호를 낼 수 있음[3,6].
2. **IGF-1R 입력:** IGF-1이 receptor tyrosine kinase인 IGF-1R을 활성화하여 PI3K/Akt 및 Ras/Raf/MEK/ERK로 전달[11,12].
3. **Crosstalk:** 동시 TSH/IGF-1 자극은 OF, primary human thyrocyte, HEK-TSHR에서 ERK1/2를 빠르게 synergistic하게 활성화함. Pertussis toxin 또는 Gi/Go knockdown이 이를 부분 억제하여 crosstalk가 적어도 일부 TSHR-Gi/Go를 사용함을 지지[3].
4. **TSAb 단독 crosstalk:** M22의 HA dose-response는 high-potency IGF-1R-dependent phase와 lower-potency IGF-1R-independent phase로 분리됨. IGF-1R antagonist는 전자만, TSHR antagonist는 양쪽을 억제함[2,4]. 즉 IGF-1R은 모든 TSHR output의 필수 구성요소가 아니라 **일부 출력을 증폭하는 branch**로 해석하는 것이 적절함.

### 2.2 공통 downstream과 세포별 출력

| signaling node | 근거가 지지하는 연결 | OF consequence | thyrocyte consequence | 근거 수준 |
|---|---|---|---|---|
| TSHR → Gi/Go → ERK1/2 | pertussis toxin 및 Gi/Go knockdown으로 synergy 부분 감소[3] | HA 프로그램의 proximal signal, 세포 활성화 | NIS 등 thyroid-specific gene regulation에 기여 | supported, 세포실험 |
| IGF-1R → PI3K/Akt | IGF-1 유도 pIGF-1R/pAkt와 OF proliferation/HA가 linsitinib으로 감소[12] | proliferation, HA; FOXO1 nuclear exclusion과 remodeling 연결[13] | NIS 자극에 Akt 필요, TSH/IGF-1 cooperativity | supported, 단 linsitinib의 IR confounding |
| 양 receptor → MEK/ERK | 동시 자극에서 빠른 synergistic pERK[3] | HA 및 fibroblast activation | NIS, TPO/TG 관련 기능 출력 | supported |
| Akt → FOXO1 cytoplasmic localization | M22 또는 IGF-1이 nuclear FOXO1을 낮추고 Akt inhibition이 역전[13] | adipogenic/HA-permissive remodeling과 연관 | 본 연구에서 미평가 | supported association, fate 인과는 미확립 |
| receptor activation → recycling/expression | TSH/M22가 TSHR/IGF-1R surface expression을 함께 높이며 endocytosis inhibition으로 감소[14] | 반복 자극에 대한 feed-forward sensitization 가능 | 직접 확인 범위 아님 | proposed amplification loop |

**주의:** HA는 두 receptor의 crosstalk를 측정하는 가장 일관된 OF readout이나, HA 상승만으로 adipogenesis, myofibroblast differentiation 또는 임상 proptosis를 각각 확정할 수 없음. IGF-1R의 direct adipogenesis 근거는 별도 문서에서 B, lower confidence, myofibroblast fate는 C로 판정되어 있음.

## 3. 가설 1: ARRB1 scaffold-mediated crosstalk

### 3.1 도식화 가능한 신호사슬

```text
TSH/TSAb
  ↓ direct binding
TSHR activation ── Gs → cAMP/PKA → IGF-1R-independent TSHR output
  │
  ├─ Gi/Go ─────────────────────────────┐
  │                                     ↓
  └─ GRK-associated receptor state → ARRB1 scaffold ← IGF-1R
                                        ↓
                                   MEK → ERK1/2
                                        ↓
                         OF: HA secretion/activation
                         thyrocyte: NIS and differentiated function
```

이 모델에서 ARRB1은 두 receptor를 가까이 유지하고 ERK signalosome을 조립하는 **proposed scaffold**임. ARRB1 knockdown은 M22 high-potency phase, KSAb1 potency/efficacy, 환자 IgG 유도 HA 및 ERK phosphorylation을 억제했고 TSHR/IGF-1R proximity도 낮춤. ARRB2 knockdown에는 같은 효과가 없었음[5]. 같은 ARRB1-dependent proximity가 human thyrocyte와 osteoblast-like cell에서도 관찰되어 OF 특이 현상만은 아님[5].

### 3.2 downstream consequence

- **OF:** high-potency TSAb response의 IGF-1R-dependent HA secretion, ERK phosphorylation. HA의 높은 수분결합력은 orbital tissue expansion/edema에 기여할 수 있으나, 이 세포실험이 임상 endpoint를 직접 측정한 것은 아님[2,4,5].
- **Thyrocyte:** receptor crosstalk는 NIS upregulation과 TSH-dependent differentiated function을 조절. cAMP/PKA level에서는 cooperativity가 관찰되지 않고 ERK/Akt inhibition이 NIS synergy를 거의 제거하여, crosstalk가 canonical cAMP만으로 설명되지 않음을 지지[11].
- **치료적 예측:** IGF-1R blockade 또는 ARRB1 disruption은 crosstalk branch를 낮추지만 high-dose TSAb의 IGF-1R-independent TSHR branch는 남을 수 있음. 실제로 IGF-1R antagonists는 높은 M22 농도에서 효능을 잃은 반면 TSHR antagonist는 양 branch를 억제함[4].

### 3.3 근거와 한계

- **강점:** patient-derived GO OF에서 genetic knockdown, functional HA, pERK, proximity를 한 실험계에서 연결한 직접 perturbation 근거[5].
- **한계:** knockdown은 ARRB1이 proximity/crosstalk에 필요함을 보이지만, ARRB1이 두 receptor 사이의 유일한 물리적 bridge임을 증명하지 않음. receptor trafficking 또는 signalosome stability 저하가 proximity를 간접적으로 낮췄을 가능성 존재.
- **판정:** **supported functional model, exact architecture는 proposed.**

## 4. 가설 2: TSHR ectodomain-IGF-1R direct association

### 4.1 도식화 가능한 신호사슬

```text
             direct ectodomain interface, proposed
TSHR ECD  ═══════════════════════════════  IGF-1R ectodomain
   │                                           │
TSH/TSAb                                     basal/IGF-1 input
   ↓                                           ↓
TSHR conformational change ── allosteric coupling ── IGF-1R-dependent branch
   ├─ Gs/cAMP                              ├─ PI3K/Akt
   └─ Gi/Go                                └─ MEK/ERK
                    convergent ERK/Akt
                           ↓
              cell-type-specific effector program
```

2025년 연구는 TSHR leucine-rich ectodomain과 active-state IGF-1R dimer의 docking 및 molecular dynamics stability를 제시하고, full-length TSHR 또는 β-arrestin 결합이 불가능한 TSHR-ECD-only cell 모두에서 약 360 kDa co-immunoprecipitated complex와 colocalization을 관찰함[7]. 이는 **ARRB1 없이도 두 receptor가 결합할 수 있음**을 지지하나, endogenous patient OF에서 해당 interface와 stoichiometry를 확정한 것은 아님.

### 4.2 기존 물리적 근거와 의미

- 2008년 TAO/control OF, thyrocyte 및 thyroid tissue에서 reciprocal pull-down과 colocalization이 보고됨. TAO OF의 IGF-1R surface level은 control OF보다 높고, TSHR은 thyrocyte가 OF보다 높았음[1].
- Proximity ligation assay는 endogenous protein proximity를 40 nm 이내에서 검출하지만 직접 접촉 자체를 증명하지는 않음[6]. Co-immunoprecipitation 역시 같은 macromolecular assembly를 지지하지만 중간단백질 없는 direct contact의 단독 증거는 아님.
- ECD-only construct 결과는 direct contact 가설을 강화하지만 overexpression, detergent extraction, engineered construct 및 in silico force-field 의존성이 남음[7].

### 4.3 downstream consequence와 가설 특이 예측

직접결합 모델도 최종적으로 ERK/Akt, HA, NIS 등의 공통 readout에 수렴하므로 downstream만으로 ARRB1 모델과 구분하기 어려움. 구분 가능한 예측은 다음과 같음.

1. TSHR-ECD/IGF-1R interface-disrupting mutation 또는 경쟁 peptide가 receptor surface expression을 보존하면서 proximity와 crosstalk만 선택적으로 제거해야 함.
2. ARRB1-null 조건에서도 endogenous receptor의 direct-contact FRET/crosslinking signal이 유지되어야 함.
3. 반대로 interface mutant에서도 ARRB1 recruitment는 유지되나 crosstalk가 소실된다면 direct interface의 독립적 필요성을 지지함.

- **판정:** **direct association은 supported in engineered systems, patient-cell causal architecture는 proposed.** ARRB1 모델과 배타적이지 않으며 direct contact가 basal complex를 만들고 ARRB1이 activation/trafficking/ERK signalosome을 안정화할 가능성도 있음.

## 5. 가설 3: pathogenic directly-stimulating anti-IGF-1R antibody

### 5.1 가설과 현재 더 잘 지지되는 대안

```text
가설 3, 근거 약함:
patient IgG → direct IGF-1R binding/agonism → pIGF-1R → PI3K/Akt + ERK → OF activation

현재 더 잘 지지되는 대안:
TSAb → direct TSHR activation → TSHR/IGF-1R crosstalk → ERK/Akt → HA
                              └→ TSHR-only branch도 병존
```

직접 agonist 가설이 성립하려면 affinity-purified anti-IGF-1R Ab가 TSHR-null 세포에서도 IGF-1R kinase/autophosphorylation 및 downstream response를 재현하고, antigen depletion 또는 IGF-1R-selective blockade가 이를 제거해야 함. 현재 핵심 결과는 반대 방향임.

- M22는 IGF-1R autophosphorylation을 일으키지 않으면서 IGF-1R-dependent HA를 유도했고 TSHR antagonist가 전체 반응을 차단함[2].
- M22가 TSHR에는 결합하지만 IGF-1R에는 결합하지 않는 조건에서 teprotumumab biosimilar가 crosstalk-dependent phase만 억제함[8]. 이는 IGF-1R blockade의 효과가 anti-IGF-1R agonist의 존재를 요구하지 않음을 보여줌.
- 2020년 비판적 검토는 TSHR이 stimulating autoantibody의 직접 표적이고 기존 IGF-1R 관찰은 crosstalk로 설명 가능하다고 결론[15].
- 2025년 두 코호트는 circulating anti-IGF-1R Ab를 측정했으나 higher level이 GO 부재/낮은 중증도와 연관되어 억제/보호 방향을 제안함[9,10]. 한 연구의 OF proliferation 실험은 anti-IGF-1R affinity-purified fraction이 아닌 total IgG를 사용하여 항원 특이 기능을 확정하지 못함[9].

### 5.2 downstream 및 임상 해석

- IGF-1R blockade로 HA/proliferation이 감소하거나 teprotumumab이 임상 효능을 보이는 것은 **IGF-1R pathway relevance**를 지지함[4,8].
- 같은 결과를 **pathogenic agonistic anti-IGF-1R Ab의 존재**로 역추론할 수 없음. receptor crosstalk, ligand-dependent basal signaling, receptor internalization/downregulation이 모두 대안 설명임.
- 검출된 anti-IGF-1R Ab는 binding Ab, inhibitory Ab, neutral Ab가 혼합될 수 있으므로 `anti-IGF-1R Ab positive`와 `IGF-1R-stimulating Ab positive`를 동일시하지 않아야 함.
- **판정:** **pathogenic directly-stimulating antibody model은 unsupported/proposed.** 항체 존재 자체는 suggested이나 agonistic pathogenicity는 입증되지 않음.

## 6. 조직/세포 유형별 차이

| 구분 | receptor context | crosstalk output | 병리/생리 consequence | 해석상 주의 |
|---|---|---|---|---|
| **TED patient OF/preadipocyte** | TSHR은 낮지만 기능성 있음. TAO OF에서 IGF-1R surface abundance 증가 보고[1] | rapid ERK, Akt/FOXO1, HA, proliferation; adipogenesis는 별도 제한적 근거[2-5,12,13] | hydrophilic matrix expansion, edema, orbital fat remodeling에 기여 가능 | HA를 adipogenesis/fibrosis의 대리변수로 사용하지 말 것 |
| **CD34+ fibrocyte-derived OF** | TSHR 및 thyroid autoantigen expression이 상대적으로 두드러지는 병인 세포군으로 제안 | TSHR/IGF-1R complex가 disease IgG response를 매개한다는 모델(`proposed`, CD34+ 세포 특이 crosstalk 1차 데이터 없이 review[16]에 기반) | cytokine/chemokine 및 matrix-producing OF pool에 기여 가능 | CD34- resident OF와 혼합배양 결과를 lineage-specific 결과로 해석하지 말 것[16] |
| **CD34- resident OF** | CD34+ OF와 paracrine interaction, Slit2에 의한 phenotype modulation 보고 | HA 및 inflammatory output에 관여 가능 | orbital remodeling 조절 | crosstalk 연구 상당수가 unsorted culture이므로 subset attribution 미확정[16] |
| **Thyrocyte** | TSHR abundance가 OF보다 높고 IGF-1R과 association[1] | ERK/Akt-dependent NIS; TPO/TG protein 및 fT4 regulation[11,17] | iodide uptake와 thyroid hormone synthesis | OF의 HA/adipogenesis 결론을 thyrocyte에 외삽 금지 |
| **3T3-L1/HEK-TSHR** | engineered receptor expression 또는 adipocyte model | receptor proximity, expression/recycling, rapid pERK[3,14] | mechanism dissection | stoichiometry 및 expression이 primary human cell과 다름 |
| **osteoblast-like cell** | ARRB1-dependent proximity 관찰[5] | crosstalk 가능성 | TED 직접 consequence 아님 | generalizability 보조근거일 뿐 disease-cell 근거 아님 |

### 핵심 대비: OF vs thyrocyte

- **입력은 공유:** TSH/TSAb가 TSHR을 자극하고 IGF-1R-dependent branch가 ERK/Akt를 증폭할 수 있음.
- **수용체 비율은 다름:** TSHR은 thyrocyte에서 OF보다 높고, IGF-1R은 TAO OF에서 control OF보다 높다는 관찰[1]. 이 차이는 동일 ligand에도 threshold와 branch 비중이 달라질 가능성을 제시함.
- **출력은 다름:** OF는 HA/proliferation/remodeling, thyrocyte는 NIS/TPO/TG/fT4. 따라서 `TSHR → IGF-1R → HA`를 전 조직의 보편 경로로 표현하지 말 것.
- **질환 연결도 다름:** thyrocyte crosstalk는 thyroid differentiated function의 조절이고, OF crosstalk는 TED effector-cell activation의 proposed amplifier임.

## 7. 가설별 evidence matrix

| 질문 | ARRB1 scaffold | direct receptor association | directly-stimulating IGF-1R Ab |
|---|---|---|---|
| 핵심 직접 관찰 | ARRB1 knockdown으로 proximity, pERK, HA 감소[5] | modeling, ECD-only/full-length co-IP, colocalization[7] | pathogenic agonism을 충족한 직접 관찰 없음[15] |
| patient-derived OF 기능 근거 | **있음**[5] | 기존 co-IP/colocalization 있음[1], 2025 direct-interface 검증은 engineered cell 중심[7] | 환자 IgG 반응은 있으나 TSHR/crosstalk로 설명 가능[2,8] |
| thyrocyte 근거 | ARRB1-dependent proximity[5] | tissue/thyrocyte association[1] | 없음 |
| downstream | ERK, HA | 공통 ERK/Akt로 추정, interface-specific output 미분리 | 가설상 pIGF-1R/Akt/ERK이나 미입증 |
| 경쟁 설명 | receptor trafficking 변화 | scaffold/중간단백질, overexpression artifact | TSAb → TSHR-IGF-1R crosstalk |
| 현재 판정 | **supported functional model; architecture proposed** | **supported association; endogenous causal interface proposed** | **unsupported/proposed pathogenic model** |

## 8. JHA-86 deck용 3-panel specification

### Panel A: ARRB1 scaffold

- Nodes: `TSAb/TSH`, `TSHR`, `ARRB1`, `IGF-1R`, `Gi/Go`, `ERK`, `HA`.
- Solid edges: `TSAb → TSHR`, `TSHR → Gi/Go`, `ERK → HA`.
- Dashed proposed edges: `TSHR — ARRB1 — IGF-1R`.
- Inhibitor callouts: `ARRB1 knockdown`, `IGF-1R blockade`, `TSHR blockade`.
- Footer: `Patient-derived OF functional perturbation; exact physical architecture proposed.`

### Panel B: direct ectodomain association

- Nodes: `TSHR-ECD`, `IGF-1R ectodomain`, `Akt`, `ERK`, `cell-specific output`.
- Double dashed contact: `TSHR-ECD ═ IGF-1R` with label `MD + co-IP/ECD-only cells`.
- Split outputs: `OF: HA/remodeling`; `thyrocyte: NIS/TPO/TG`.
- Footer: `Direct association supported in engineered systems; patient-cell interface not yet causal.`

### Panel C: antibody hypothesis challenged

- Red crossed dashed arrow: `anti-IGF-1R Ab ⇢ direct IGF-1R agonism`.
- Preferred solid path: `TSAb → TSHR → crosstalk → IGF-1R-dependent ERK/Akt`.
- Parallel branch: `TSHR → IGF-1R-independent output`.
- Footer: `IGF-1R pathway relevance ≠ pathogenic stimulating anti-IGF-1R antibody.`

### 공통 legend

- Solid arrow: 직접 perturbation으로 지지.
- Dashed arrow/contact: proposed molecular step.
- Red cross: 현재 직접 근거 부족 또는 반박 근거 우세.
- 색상 권고: TSHR blue, IGF-1R orange, ARRB1 gray, downstream green. 색상만으로 의미를 전달하지 않고 선 형태와 label을 병기.

## 9. 통합 working model과 의사결정 시사점

가장 절약적인 working model은 다음과 같음.

1. TSAb가 TSHR을 직접 자극.
2. TSHR은 IGF-1R-independent branch와 IGF-1R-dependent high-sensitivity branch를 함께 가동.
3. 두 receptor는 basal direct association을 형성할 수 있고, ARRB1은 proximity, trafficking 또는 ERK signalosome을 안정화할 수 있음. 이 병존모델은 **proposed**이며 직접 검증 필요.
4. OF에서는 HA/proliferation 및 일부 adipogenic program, thyrocyte에서는 thyroid-specific differentiated function으로 출력이 분기.
5. 따라서 IGF-1R blockade는 TED effector output을 낮출 수 있으나, 이것이 IGF-1R을 primary autoantigen으로 만들지는 않으며 TSHR-only signaling 잔존 가능성을 예측.

**Therapeutic interpretation:** IGF-1R 표적 임상효능은 crosstalk network의 druggability를 지지하지만 어느 molecular architecture를 증명하지 않음. TSHR 단독, IGF-1R 단독, dual blockade를 비교할 때 ligand/TSAb 농도, disease-cell subset, active/inactive phase 및 HA/adipogenesis/fibrosis endpoint를 분리해야 함.

## 10. 결정적 후속실험

1. **Endogenous interface test:** patient-derived sorted OF에서 CRISPR knock-in으로 predicted TSHR-ECD interface residue만 변이. surface expression, ligand binding, canonical cAMP를 보존한 상태에서 FRET/crosslinking, pERK, HA 측정.
2. **ARRB1 vs direct-contact epistasis:** ARRB1 knockout, interface mutant, double perturbation을 비교. additive/non-additive 결과로 scaffold와 direct contact의 직렬/병렬 관계 판별.
3. **Spatial/temporal mapping:** live-cell single-molecule imaging으로 ligand 전후 complex formation, ARRB1 recruitment, internalization/recycling의 순서를 추적.
4. **Cell-subset resolution:** CD34+/CD34- 및 Thy-1+/Thy-1- human OF에서 receptor abundance와 동일 perturbation-response를 비교.
5. **Antibody falsification test:** anti-IGF-1R affinity purification/depletion 후 TSHR-null, IGF-1R wild-type/kinase-dead cell에서 binding, receptor autophosphorylation, Akt/ERK 및 HA-compatible reporter 평가.
6. **Tissue translation:** paired patient thyrocyte/OF 또는 organoid에서 동일 TSAb 농도와 selective TSHR/IGF-1R perturbation을 적용하여 tissue-specific branch contribution 정량.

## 11. 검색 방법과 한계

- 검색일: **2026-09-28**.
- Database: PubMed. 검색어: `TSHR IGF-1R beta arrestin crosstalk`, `TSH IGF-1 receptor crosstalk orbital fibroblast`, `thyrocyte TSHR IGF1R crosstalk`, `TSHR IGF1R direct interaction` 및 관련 논문의 cited/citing chain.
- 2024-2026 신규 문헌은 primary mechanistic study를 우선했고 review는 field context와 상반된 해석 확인에 사용.
- 주요 한계는 human in vitro 중심, donor/OF subset 이질성, overexpression system, pharmacologic selectivity, HA 중심 endpoint임. Teprotumumab 임상반응은 pathway relevance를 지지하지만 세 경쟁가설을 판별하는 근거로 사용하지 않음.
- 본 문서는 3가설을 설명하기 위한 mechanistic synthesis이며 systematic review/meta-analysis가 아님.

## 12. 참고문헌

1. Tsui S, Naik V, Hoa N, et al. Evidence for an association between thyroid-stimulating hormone and insulin-like growth factor 1 receptors: a tale of two antigens implicated in Graves' disease. *J Immunol.* 2008;181:4397-4405. PMID: [18768899](https://pubmed.ncbi.nlm.nih.gov/18768899/). doi: [10.4049/jimmunol.181.6.4397](https://doi.org/10.4049/jimmunol.181.6.4397).
2. Krieger CC, Neumann S, Place RF, Marcus-Samuels B, Gershengorn MC. Bidirectional TSH and IGF-1 receptor cross talk mediates stimulation of hyaluronan secretion by Graves' disease immunoglobins. *J Clin Endocrinol Metab.* 2015;100:1071-1077. PMID: [25485727](https://pubmed.ncbi.nlm.nih.gov/25485727/). doi: [10.1210/jc.2014-3566](https://doi.org/10.1210/jc.2014-3566).
3. Krieger CC, Perry JD, Morgan SJ, et al. TSH/IGF-1 receptor cross-talk rapidly activates extracellular signal-regulated kinases in multiple cell types. *Endocrinology.* 2017;158:3676-3683. PMID: [28938449](https://pubmed.ncbi.nlm.nih.gov/28938449/). doi: [10.1210/en.2017-00528](https://doi.org/10.1210/en.2017-00528).
4. Neumann S, Krieger CC, Gershengorn MC. Inhibiting thyrotropin/insulin-like growth factor 1 receptor crosstalk to treat Graves' ophthalmopathy: studies in orbital fibroblasts in vitro. *Br J Pharmacol.* 2017;174:328-340. PMID: [27987211](https://pubmed.ncbi.nlm.nih.gov/27987211/). doi: [10.1111/bph.13693](https://doi.org/10.1111/bph.13693).
5. Krieger CC, Place RF, Bevilacqua C, et al. Arrestin-β-1 physically scaffolds TSH and IGF1 receptors to enable crosstalk. *Endocrinology.* 2019;160:1468-1479. PMID: [31127272](https://pubmed.ncbi.nlm.nih.gov/31127272/). doi: [10.1210/en.2019-00055](https://doi.org/10.1210/en.2019-00055).
6. Krieger CC, Neumann S. Proximity ligation assay to study TSH receptor homodimerization and crosstalk with IGF-1 receptors in human thyroid cells. *Front Endocrinol (Lausanne).* 2022;13:989626. PMID: [36246873](https://pubmed.ncbi.nlm.nih.gov/36246873/). doi: [10.3389/fendo.2022.989626](https://doi.org/10.3389/fendo.2022.989626).
7. Latif R, Mezei M, Davies TF. Mechanisms in thyroid eye disease: the TSH receptor interacts directly with the IGF-1 receptor. *Endocrinology.* 2025;166:bqaf009. PMID: [39821041](https://pubmed.ncbi.nlm.nih.gov/39821041/). doi: [10.1210/endocr/bqaf009](https://doi.org/10.1210/endocr/bqaf009).
8. Krieger CC, Neumann S, Marcus-Samuels B, Gershengorn MC. Inhibition of TSH/IGF-1 receptor crosstalk by teprotumumab as a treatment modality of thyroid eye disease. *J Clin Endocrinol Metab.* 2022;107:e1653-e1660. PMID: [34788857](https://pubmed.ncbi.nlm.nih.gov/34788857/). doi: [10.1210/clinem/dgab824](https://doi.org/10.1210/clinem/dgab824).
9. Lanzolla G, Rotondo Dottore G, Comi S, et al. In vivo and in vitro evidence for a protective role of autoantibodies against the insulin-like growth factor-1 receptor in Graves' orbitopathy. *Endocrine.* 2025;89:137-142. PMID: [40156685](https://pubmed.ncbi.nlm.nih.gov/40156685/). doi: [10.1007/s12020-025-04219-6](https://doi.org/10.1007/s12020-025-04219-6).
10. Nowak M, Wielkoszyński T, Londzin-Olesik M, et al. Antibodies against the receptor for insulin-like growth factor 1, IGF-1, and IGFBP-3 in Graves' and Basedow's disease with and without orbitopathy. *Endokrynol Pol.* 2025;76:40-51. PMID: [40071798](https://pubmed.ncbi.nlm.nih.gov/40071798/). doi: [10.5603/ep.102336](https://doi.org/10.5603/ep.102336).
11. Morgan SJ, Neumann S, Marcus-Samuels B, Gershengorn MC. Thyrotropin and insulin-like growth factor 1 receptor crosstalk upregulates sodium-iodide symporter expression in primary cultures of human thyrocytes. *Thyroid.* 2017;27:1083-1094. PMID: [27638195](https://pubmed.ncbi.nlm.nih.gov/27638195/). doi: [10.1089/thy.2016.0323](https://doi.org/10.1089/thy.2016.0323).
12. Chen MH, et al. Linsitinib inhibits IGF-1-induced cell proliferation and hyaluronic acid secretion by suppressing PI3K/Akt and ERK pathway in orbital fibroblasts from patients with thyroid-associated ophthalmopathy. *PLoS One.* 2024;19:e0311093. PMID: [39693285](https://pubmed.ncbi.nlm.nih.gov/39693285/). doi: [10.1371/journal.pone.0311093](https://doi.org/10.1371/journal.pone.0311093).
13. Kumar S, Coenen MJ, Scherer PE, Bahn RS. Forkhead transcription factor FOXO1 is regulated by both a stimulatory thyrotropin receptor antibody and insulin-like growth factor-1 in orbital fibroblasts from patients with Graves' ophthalmopathy. *Thyroid.* 2015;25:1145-1155. PMID: [26213859](https://pubmed.ncbi.nlm.nih.gov/26213859/). doi: [10.1089/thy.2015.0254](https://doi.org/10.1089/thy.2015.0254).
14. Xiang P, Mezei M, Latif R, Davies TF. Stimulating thyrotropin receptor antibodies enhance the expression of both thyrotropin receptors and insulin-like growth factor 1 receptors in fibroblasts. *Thyroid.* 2026;36:903-911. PMID: [42374926](https://pubmed.ncbi.nlm.nih.gov/42374926/). doi: [10.1177/10507256261463222](https://doi.org/10.1177/10507256261463222).
15. Krieger CC, Neumann S, Gershengorn MC. Is there evidence for IGF1R-stimulating Abs in Graves' orbitopathy pathogenesis? *Int J Mol Sci.* 2020;21:6561. PMID: [32911689](https://pubmed.ncbi.nlm.nih.gov/32911689/). doi: [10.3390/ijms21186561](https://doi.org/10.3390/ijms21186561).
16. Smith TJ. TSHR-IGF-IR complex drives orbital fibroblast misbehavior in thyroid eye disease. *Curr Opin Endocrinol Diabetes Obes.* 2024;31:177-183. PMID: [39082947](https://pubmed.ncbi.nlm.nih.gov/39082947/). doi: [10.1097/MED.0000000000000878](https://doi.org/10.1097/MED.0000000000000878).
17. Neumann S, et al. Linsitinib decreases thyrotropin-induced thyroid hormone synthesis by inhibiting crosstalk between thyroid-stimulating hormone and insulin-like growth factor 1 receptors in human thyrocytes in vitro and in vivo in mice. *Thyroid.* 2025;35:204-216. PMID: [39718934](https://pubmed.ncbi.nlm.nih.gov/39718934/). doi: [10.1089/thy.2024.0393](https://doi.org/10.1089/thy.2024.0393).

## 13. 검증 로그

| claim | tier | 검증 방법 | 결과 | 일자 |
|---|---|---|---|---|
| ARRB1 knockdown이 receptor proximity, pERK, HA를 억제 | 하, 정성 기전 | PubMed 원저 abstract 및 PMID 대조[5] | 일치 | 2026-09-28 |
| ECD-only TSHR가 IGF-1R과 약 360 kDa complex를 형성 | 중, 정량 포함 기전 | PubMed 원저 abstract에서 construct/size 직접 대조[7] | 일치, engineered-cell 한계 명기 | 2026-09-28 |
| M22 response에 IGF-1R-dependent/independent branch 병존 | 하, 정성 기전 | 두 독립 원저 abstract 대조[2,4] | 일치 | 2026-09-28 |
| thyrocyte crosstalk가 NIS/TPO/TG/fT4에 관여 | 중, 기능 기전 | human primary-cell 원저 및 mouse 포함 원저 abstract 대조[11,17] | 일치, 세포/동물 범위 분리 | 2026-09-28 |
| circulating anti-IGF-1R Ab가 보호/억제 방향일 가능성 | 중, 임상 연관 | 2025년 독립 코호트 2건 대조[9,10] | 방향 일치, cross-sectional/assay 한계 명기 | 2026-09-28 |
| ref [7] 서지 정보(Latif et al.)의 article locator/DOI | 하, 서지 무결성 | Crossref DOI lookup(`10.1210/endocr/bqaf008` vs `bqaf009`) 및 PubMed PMID 39821041 대조 | PR #17이 DOI를 `bqaf008`으로 수정했으나 이는 다른 논문(Thakore et al., miR-433-3p/osteoblast). 올바른 값은 `bqaf009`이며 본 문서에서 정정 | 2026-10-01 |
| executive conclusion의 adipogenic remodeling 서술 | 하, 정성 기전 | crosstalk 근거 문헌[1,11,12]의 측정 endpoint 대조 및 repo 내 maturity review 판정 대조 | crosstalk perturbation 연구는 adipocyte fate를 직접 측정하지 않음. adipogenesis를 별도/제한적 근거로 분리하도록 수정 (PR #14 Codex P2 반영) | 2026-10-01 |
| executive conclusion의 proliferation 서술 | 하, 정성 기전 | [1,11,12] 측정 endpoint 대조 (PR #33 Codex P2) | proliferation은 IGF-1 ligand-dependent 반응 측정[12]이지 crosstalk perturbation 출력이 아님. HA와 분리하도록 수정 | 2026-10-01 |
| §5.2 teprotumumab/IGF-1R blockade 서술의 인용 | 하, 정성 기전 | 섹션 단위 claim-인용 대조 (PR #33 Codex P2) | 무인용 factual claim이었으나 [4,8] 추가로 수정 | 2026-10-01 |
| CD34+ fibrocyte-derived OF의 IgG response 매개 모델 | 하, 정성 기전 | [16] 원문 범위 대조(review이며 CD34+ 세포 특이 crosstalk 1차 데이터 아님) | `proposed` 명시 태깅으로 근거 수준 정합 (PR #14 review 반영) | 2026-10-01 |

### 독립 QA 결과 (별도 세션, 2026-10-01)

`_shared/GD_TED_qa_checklist.md` 중 본 문서에 적용 가능한 항목:

| 항목 | 판정 | 비고 |
|---|---|---|
| D2 (complex 가설 proposed 명기) | PASS | 분자배치/architecture 전반에 `proposed` 라벨 유지 |
| F1 (본문 in-line citation 존재) | PASS (수정 후) | 섹션 단위 claim-인용 대조 수행. 무인용 factual claim 1건(teprotumumab 임상 효능, §5.2)을 [4,8] 추가로 수정. 참고문헌 번호 [1]-[17] 전수 본문 사용 일치 |
| F2 (번호-참고문헌 일치) | PASS | 불일치 0건 |
| F3 (중복 항목) | PASS | 중복 0건 |
| F4 (PMID 실존 검증) | PASS | 17/17 PMID NCBI E-utilities 대조 일치 (제목/저널/연도) |
| F5 (마케팅 언어) | PASS | 해당 없음 |
| F6 (근거 수준 표현) | PASS | proposed/supported/unsupported/suggested 사용 |
| H1 (영문 용어 유지) | PASS | TSHR, IGF-1R, TSAb 등 영문 유지 |
| H2 (가운뎃점 미사용) | PASS | U+00B7 0건 |
| H3 (개조식 문체) | PASS | 명사 종결형 유지 |
| A/B/C/E 항목 | 범위 밖 | 역학/staging/치료제 수치는 본 문서가 다루지 않음 |

**QA D2 판정:** PASS. 문서 전반에서 complex의 존재와 세부 molecular architecture를 구분하고, 세 가설의 미확립 부분을 `proposed`, `supported`, `unsupported`로 명시함. 작성 세션(2026-09-28)과 분리된 독립 QA를 2026-10-01 수행하였고 상기 표와 같이 전 항목 PASS이므로 status를 `done`으로 갱신함.
