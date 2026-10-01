---
linear_issue: JHA-78
created: 2026-09-27
source: manual
milestone: cluster-3-mechanism-deepdive
status: done
inputs:
  - 00_legacy_unsorted/GD_TED_report.md
  - _shared/GD_TED_reference.md
  - _shared/GD_TED_qa_checklist.md
---

# Orbital fibroblast 분화경로별 IGF-1R 연구 성숙도

## 결론 요약

| 분화경로 | 종합 grade | 직접 human in vitro | 직접 in vivo | 판정 |
|---|---:|---|---|---|
| adipocyte | **B, lower confidence** | **있음, target-specific 연구 1건.** 환자 유래 orbital adipose-derived stromal cell(이하 OADSC)에서 IGF-1 자극, IGF-1R antibody 차단 및 downstream PI3K 차단으로 lipid accumulation과 adipogenic marker 변화를 확인[2]. 별도 linsitinib 연구[8]는 IGF-1R/IR dual inhibition이므로 direct replication이 아니라 supportive evidence로만 분류 | **제한적/비선택적.** TED mouse에서 linsitinib이 orbital brown adipose tissue 형성을 낮췄으나 IGF-1R/IR dual inhibitor이고 면역/갑상선 효과가 병존[5]. dual TSHR/IGF1R CRISPR도 mouse 및 organoid의 adipogenesis를 억제했으나 IGF1R 단독 인과효과와는 구분 불가[10] | 단일 human in vitro 연구가 IGF-1R-specific 인과성을 직접 지지하고 여러 비선택적 연구의 방향이 일치함. 다만 target-specific 독립 재현 및 OF lineage 한정 in vivo 검증은 미완료 |
| myofibroblast | **C** | **직접 근거 부족.** TGF-β 유도 fibrosis assay와 IGF-1R 감소가 함께 관찰된 RBM47 knockdown 연구는 있으나, IGF1R 자체를 조작하여 α-SMA/collagen/contraction을 rescue한 실험은 아님[9] | **직접 근거 없음.** linsitinib mouse 연구는 inflammation, muscle edema, adipose tissue 개선을 보였지만 IGF-1R 의존적 myofibroblast fate 억제를 입증하지 않음[5]. dual CRISPR 연구의 fibrosis 개선도 두 receptor 동시 편집 결과[10] | IGF-1R이 OF의 myofibroblast commitment를 직접 구동한다는 주장은 현재 가설/간접근거 수준. TGF-β 중심 fibrosis biology와 IGF-1R pathway를 동일시하면 안 됨 |

**핵심 해석:** IGF-1R의 기능 근거는 두 OF fate에 대칭적이지 않음. **adipocyte 경로는 target-specific human in vitro evidence 1건과 복수의 supportive evidence가 있으나 독립적 target-specific 재현 및 in vivo attribution이 제한된 B, lower confidence**, **myofibroblast 경로는 lineage-specific direct evidence가 부족한 C**로 판정함. Teprotumumab의 임상 효능은 IGF-1R pathway의 TED relevance를 강하게 지지하지만, proptosis/CAS/diplopia 같은 임상 endpoint만으로 adipogenesis와 fibrosis 중 어느 fate가 얼마나 매개되었는지는 분리할 수 없으므로 이 grading의 직접 근거로 승격하지 않음[11,12].

## 1. Evidence grade 정의

본 평가는 논문 수가 아니라 **“IGF-1R 자체의 조작이 해당 OF 분화 fate를 바꾸는가”**에 대한 인과성 및 translation 수준을 평가함.

| Grade | 사전 정의 | 이 문서에서 요구하는 최소 근거 |
|---|---|---|
| **A, established** | target-specific in vivo 인과성과 human relevance가 모두 확인됨 | IGF1R 선택적 genetic/pharmacologic perturbation이 적절한 TED in vivo model에서 해당 lineage endpoint를 변화시키고, human OF 또는 조직에서 방향이 일치. 가능하면 독립 재현 또는 임상 tissue/biomarker 연결 포함 |
| **B, supported** | 직접 in vitro 인과성이 확인되었으나 재현성 또는 in vivo attribution에 중요한 제한 존재 | 환자 유래 OF에서 target-specific ligand/receptor perturbation과 fate-specific endpoint가 확인되고, 별도의 human tissue/비선택적 perturbation/in vivo 근거 중 하나 이상이 같은 방향을 지지. target-specific 독립 재현이 없으면 **lower confidence**를 병기 |
| **C, preliminary/indirect** | 연관 또는 간접 perturbation 중심 | expression/correlation, upstream regulator 조작, 혼합 endpoint, 단일 탐색 연구. IGF1R 자체 조작과 lineage-specific endpoint 사이의 직접 인과 사슬이 불완전 |

Grade는 **2026-09-27 PubMed 검색 기준**이며, A가 “임상 승인”, B가 “동물”, C가 “세포”라는 단순 단계표가 아님. 약물의 target selectivity, 세포 정체성, fate-specific endpoint, rescue 실험 유무를 함께 고려함.

## 2. 범위와 판정 규칙

- **세포 범위:** primary human orbital fibroblast/preadipocyte/OADSC 및 disease-relevant orbital model. 일반 fibroblast 또는 fibrocyte 결과는 mechanistic context로만 사용.
- **adipocyte endpoint:** Oil Red O/lipid accumulation, adiponectin, leptin, AP2/FABP4, FAS, PPARγ, adipose tissue volume/formation 등.
- **myofibroblast endpoint:** α-SMA/ACTA2, collagen/fibronectin, contractility, TGF-β 유도 myofibroblast differentiation 또는 orbital fibrosis histology 등.
- **제외 원칙:** HA secretion, cytokine, proliferation만 측정한 연구는 중요한 OF activation 근거이나 어느 분화 fate의 직접 근거로도 계산하지 않음[3,4,6,7].
- **수용체 attribution:** linsitinib은 IGF-1R와 insulin receptor(IR)를 함께 억제함. TSHR/IGF1R dual editing은 두 target을 함께 바꿈. 따라서 두 접근은 in vivo efficacy를 보여도 IGF1R 단독의 필요성 또는 충분성을 확정하지 못함[5,10].

## 3. Adipocyte 경로: Grade B

### 3.1 직접 근거

1. **환자 유래 세포의 ligand-to-receptor 인과 사슬:** TAO 환자 유래 OADSC에서 IGF-1은 proliferation, lipid accumulation, adiponectin/leptin/AP2/FAS 및 PPARγ를 증가시킴. IGF-1R-blocking antibody 또는 PI3K inhibitor가 이 반응과 Akt phosphorylation을 낮춰 **IGF-1 → IGF-1R → PI3K/Akt → PPARγ → adipogenic differentiation** 축을 직접 지지함[2]. 단, donor 수/질환상태의 일반화 및 in vivo fate tracing은 제한됨.
2. **독립적 supportive pharmacology, direct replication 아님:** TED orbital fat single-nucleus RNA-seq 연구에서 adipogenic transition 증가와 IGF-1R pathway 이상이 함께 관찰되었고, 별도 primary OF 실험에서 linsitinib이 adipogenesis를 억제함[8]. 이는 human tissue association과 functional inhibition의 방향 일치를 제공하지만, linsitinib이 IR도 억제하므로 IGF-1R-specific 인과실험의 독립 재현으로 계산하지 않음.
3. **supportive pathway evidence:** TSH/IGF-1R cross-talk 연구들은 IGF-1R blockade가 OF signaling/HA를 줄임을 반복 확인했지만 adipocyte fate 자체를 읽지 않은 경우가 많음[3,4,6,7]. 따라서 pathway plausibility는 강화하되 direct adipogenesis evidence와 구분함.

### 3.2 in vivo 수준

- TSHR A-subunit immunization mouse에서 유래한 OF는 IGF-1R expression 및 adipogenic propensity가 증가했고, IGF-1 자극에 HA를 분비함[4]. 이는 disease model의 ex vivo phenotype이지, 살아 있는 동물에서 IGF1R을 조작해 adipocyte fate를 바꾼 실험은 아님.
- 같은 계열 mouse model에서 oral linsitinib은 early/late treatment 모두 orbital brown adipose tissue 형성과 MRI tissue remodeling을 낮춤[5]. **in vivo supportive**로 분류하나, IGF-1R/IR dual inhibition, systemic thyroid/immune effects, brown adipose endpoint 때문에 OF-autonomous IGF1R 인과성을 확정할 수 없음.
- 2026년 dual TSHR/IGF1R CRISPR 연구는 primary OF, 3D human orbital organoid 및 TED mouse orbital tissue에서 두 유전자 편집과 adipogenesis 감소를 보고함[10]. dual 편집이 각 single-gene arm보다 우수했다는 설계이므로 translational support는 강하지만, 공개 abstract만으로 IGF1R single arm의 fate-specific effect size와 통계량을 검증하기 어렵고 dual result를 IGF1R 단독 증명으로 간주하지 않음.

### 3.3 왜 A가 아닌가

- human OF in vitro에서는 receptor-blocking antibody를 포함한 target-specific 직접 근거 1건과 방향이 일치하는 별도 human tissue/pharmacology 근거가 있으므로 C보다 높음. 다만 target-specific 독립 재현이 없어 **B, lower confidence**로 제한함.
- 그러나 **OF-selective Igf1r loss-of-function 단독군 + lineage tracing 또는 fate-specific histology**를 갖춘 TED animal evidence가 확인되지 않음.
- Teprotumumab RCT의 proptosis 개선은 임상적으로 매우 중요한 pathway validation이나, 감소한 orbital volume이 기존 adipocyte의 크기/생존, 신규 adipogenesis, HA/edema 또는 inflammation 중 무엇에서 비롯됐는지를 분해하지 않음[11,12]. 따라서 fate-specific A 기준을 충족하지 않음.

## 4. Myofibroblast 경로: Grade C

### 4.1 확인된 근거

1. Legacy report의 출발점인 Koumas 등은 human OF에서 **Thy-1+ subset만** TGF-β/platelet concentrate에 반응해 α-SMA-positive myofibroblast로, **Thy-1- subset만** PPARγ agonist에 반응해 lipofibroblast로 분화함을 보였음[1]. 이 연구는 fate competence를 정의하지만 IGF-1/IGF-1R을 조작하지 않았으므로 IGF-1R 기능 근거가 아님.
2. RBM47 knockdown은 TAO OF에서 TGF-β-induced fibrosis readout과 adipogenesis를 낮추면서 IGF-1R expression도 낮춤[9]. 저자들은 adipogenesis에 대해서는 IGF-1R/ERK 연결을 제시했으나, fibrosis arm에서 **IGF1R knockdown/선택적 blockade 또는 IGF1R rescue가 TGF-β-induced α-SMA/collagen/contraction을 매개함**을 보인 것은 아님. 따라서 IGF-1R과 myofibroblast fate 사이에는 간접성 존재.
3. Linsitinib mouse에서 orbital inflammation, muscle edema 및 adipose tissue가 개선되었지만 abstract에 IGF-1R-dependent myofibroblast differentiation endpoint가 보고되지 않음[5]. Sirius red를 방법에 포함했다는 사실만으로 fibrosis 결과 또는 lineage mechanism을 추론하지 않음.
4. Dual TSHR/IGF1R CRISPR는 mouse와 organoid에서 fibrosis 감소를 보고했으나 두 receptor를 동시에 편집했으며, single IGF1R arm의 fibrosis 결과가 공개 abstract에서 정량 제시되지 않음[10]. 그러므로 **in vivo direct = 없음**, **in vivo indirect/supportive = 있음**으로 구분함.

### 4.2 해석 한계

- “IGF-1R inhibitor가 TED를 개선함”과 “IGF-1R이 Thy-1+ OF의 myofibroblast commitment를 직접 구동함”은 서로 다른 claim임.
- IGF-1R blockade가 inflammation/HA/edema를 줄여 이차적으로 fibrosis를 완화할 가능성과, myofibroblast 내부의 직접 신호를 차단할 가능성이 현재 실험으로 분리되지 않음.
- 따라서 myofibroblast 경로는 **C**가 적절함. “효과 없음”의 결론이 아니라 **직접 검증이 아직 부족함**의 의미임.

## 5. Evidence matrix

| 연구 | system/perturbation | adipocyte endpoint | myofibroblast endpoint | in vitro/in vivo | 판정 기여 |
|---|---|---|---|---|---|
| Koumas 2003[1] | primary human orbital/myometrial fibroblast, Thy-1 sorting; TGF-β 또는 PPARγ agonist | Thy-1- lipid droplet | Thy-1+ α-SMA | in vitro | 두 fate의 baseline biology. IGF-1R 근거 아님 |
| Zhao 2013[2] | TAO OADSC, IGF-1; IGF-1R antibody/PI3K inhibitor | lipid 및 다수 marker 증가/차단 | 미측정 | in vitro | adipocyte의 핵심 direct evidence |
| Krieger 2015[3] | GO OF, TSH/IGF-1/M22; IGF-1R antagonist | 미측정, HA만 | 미측정 | in vitro | receptor cross-talk 보조 근거 |
| Görtz 2016[4] | TSHR-immunized mouse 유래 OF | ex vivo adipogenic propensity 증가 | 미측정 | ex vivo | disease-model consistency, direct in vivo 아님 |
| Gulbins 2023[5] | TED mouse, linsitinib(IGF-1R/IR) | orbital brown adipose tissue 감소 | direct fate 미보고 | in vivo | adipocyte supportive, attribution 제한 |
| Lee 2024[6] | TAO OF, linsitinib | 미측정, proliferation/HA/signaling | 미측정 | in vitro | IGF-1R pathway target engagement |
| Tsui 2008[7] | TAO/control OF/tissue, receptor association/blocking | 미측정 | 미측정 | in vitro/ex vivo tissue | receptor complex plausibility |
| Transcriptomic study 2024[8] | TED orbital fat snRNA-seq + OF linsitinib | adipogenic transition/억제 | 미측정 | human ex vivo/in vitro | adipocyte 독립 재현, IR confounding |
| Zhu 2025[9] | TAO OF, RBM47 siRNA | 감소, IGF-1R/ERK 연결 | TGF-β fibrosis 감소 | in vitro | fibrosis에는 간접 근거만 제공 |
| G4F7-CRISPR 2026[10] | dual TSHR/IGF1R editing, OF/organoid/TED mouse | 감소 | 감소 | in vitro/organoid/in vivo | 양 경로 supportive, dual-target attribution 제한 |
| Teprotumumab RCT[11,12] | active moderate-to-severe TED 환자, IGF-1R mAb | fate-specific 미측정 | fate-specific 미측정 | human in vivo | pathway clinical validation, fate grading에는 간접 |

## 6. 남은 결정적 실험

### Adipocyte를 B에서 A로 올릴 조건

- inducible, OF-restricted **Igf1r single knockout** TED model과 적절한 TSHR/IR control.
- lineage tracing을 통한 신규 orbital adipocyte 생성량, depot volume, PPARγ/FABP4/adiponectin의 일관된 감소.
- genetic rescue 또는 IGF1R-selective agent로 on-target 재현.
- 치료 전후 human orbital imaging/tissue biomarker로 adipogenesis 변화와 임상 반응 연결.

### Myofibroblast를 C에서 B/A로 올릴 조건

- sorted Thy-1+ human OF에서 IGF1/IGF1R gain/loss-of-function 후 α-SMA, collagen, fibronectin 및 gel contraction 측정.
- TGF-β stimulation 상태에서 IGF1R perturbation과 constitutively active downstream rescue로 직접 경로 확인.
- OF-restricted Igf1r single knockout TED model에서 lineage-resolved fibrosis와 extraocular muscle function 평가.
- dual TSHR/IGF1R 결과를 IGF1R-only, TSHR-only, dual군으로 분해한 effect size 및 통계 공개.

## 7. 문헌검색 및 한계

- 검색일: **2026-09-27**.
- database: PubMed. 주요 검색어: `orbital fibroblast IGF-1 receptor adipogenesis`, `orbital fibroblast IGF-1R myofibroblast fibrosis`, `IGF-1R TGF beta orbital fibroblast`, `linsitinib murine model Graves orbitopathy`, `teprotumumab fibroblast`.
- title/abstract screening 후 primary mechanistic study를 우선함. Review는 탐색에 사용했으나 grade의 핵심 근거로 사용하지 않음.
- negative publication bias와 용어 이질성(`Graves' orbitopathy`, `thyroid-associated ophthalmopathy`, `thyroid eye disease`; OF/OADSC/fibrocyte) 때문에 “연구 없음”을 절대적 부재로 해석하지 않음.
- 2026년 CRISPR 논문[10]은 검색일 현재 PubMed abstract에서 확인되는 최신 근거임. 상세 single-arm 수치가 본 문서에서 독립 검증되지 않았으므로 보수적으로 평가함.

## 참고문헌

1. Koumas L, Smith TJ, Feldon S, Blumberg N, Phipps RP. Thy-1 expression in human fibroblast subsets defines myofibroblastic or lipofibroblastic phenotypes. *Am J Pathol.* 2003;163(4):1291-1300. PMID: [14507638](https://pubmed.ncbi.nlm.nih.gov/14507638/). doi: [10.1016/S0002-9440(10)63488-8](https://doi.org/10.1016/S0002-9440(10)63488-8).
2. Zhao P, Deng Y, Gu P, et al. Insulin-like growth factor 1 promotes the proliferation and adipogenesis of orbital adipose-derived stromal cells in thyroid-associated ophthalmopathy. *Exp Eye Res.* 2013;107:65-73. PMID: [23219871](https://pubmed.ncbi.nlm.nih.gov/23219871/). doi: [10.1016/j.exer.2012.11.014](https://doi.org/10.1016/j.exer.2012.11.014).
3. Krieger CC, Neumann S, Place RF, Marcus-Samuels B, Gershengorn MC. Bidirectional TSH and IGF-1 receptor cross talk mediates stimulation of hyaluronan secretion by Graves' disease immunoglobins. *J Clin Endocrinol Metab.* 2015;100(3):1071-1077. PMID: [25485727](https://pubmed.ncbi.nlm.nih.gov/25485727/). doi: [10.1210/jc.2014-3566](https://doi.org/10.1210/jc.2014-3566).
4. Görtz GE, Moshkelgosha S, Jesenek C, et al. Pathogenic phenotype of adipogenesis and hyaluronan in orbital fibroblasts from female Graves' orbitopathy mouse model. *Endocrinology.* 2016;157(10):3771-3778. PMID: [27552248](https://pubmed.ncbi.nlm.nih.gov/27552248/). doi: [10.1210/en.2016-1304](https://doi.org/10.1210/en.2016-1304).
5. Gulbins A, Horstmann M, Daser A, et al. Linsitinib, an IGF-1R inhibitor, attenuates disease development and progression in a model of thyroid eye disease. *Front Endocrinol (Lausanne).* 2023;14:1211473. PMID: [37435490](https://pubmed.ncbi.nlm.nih.gov/37435490/). doi: [10.3389/fendo.2023.1211473](https://doi.org/10.3389/fendo.2023.1211473).
6. Lee JY, Lee SB, Yang SW, et al. Linsitinib inhibits IGF-1-induced cell proliferation and hyaluronic acid secretion by suppressing PI3K/Akt and ERK pathway in orbital fibroblasts from patients with thyroid-associated ophthalmopathy. *PLoS One.* 2024;19(12):e0311093. PMID: [39693285](https://pubmed.ncbi.nlm.nih.gov/39693285/). doi: [10.1371/journal.pone.0311093](https://doi.org/10.1371/journal.pone.0311093).
7. Tsui S, Naik V, Hoa N, et al. Evidence for an association between thyroid-stimulating hormone and insulin-like growth factor 1 receptors: a tale of two antigens implicated in Graves' disease. *J Immunol.* 2008;181(6):4397-4405. PMID: [18768899](https://pubmed.ncbi.nlm.nih.gov/18768899/). doi: [10.4049/jimmunol.181.6.4397](https://doi.org/10.4049/jimmunol.181.6.4397).
8. Kim DW, Kim S, Han J, et al. Transcriptomic profiling of thyroid eye disease orbital fat demonstrates differences in adipogenicity and IGF-1R pathway. *JCI Insight.* 2024;9(24):e182352. PMID: [39704170](https://pubmed.ncbi.nlm.nih.gov/39704170/). doi: [10.1172/jci.insight.182352](https://doi.org/10.1172/jci.insight.182352).
9. Zhu R, Chen F, Wang BW, et al. RBM47 as a potential therapeutic target for thyroid-associated ophthalmopathy. *Int Immunopharmacol.* 2025;147:113955. PMID: [39746275](https://pubmed.ncbi.nlm.nih.gov/39746275/). doi: [10.1016/j.intimp.2024.113955](https://doi.org/10.1016/j.intimp.2024.113955).
10. Shi M, Yu P, Liu L, et al. Fluoropolymer-mediated delivery of a dual TSHR/IGF1R-targeting CRISPR-Cas9 system for localized therapy in thyroid-associated ophthalmopathy. *Adv Mater.* 2026;38(11):e11078. PMID: [41486850](https://pubmed.ncbi.nlm.nih.gov/41486850/). doi: [10.1002/adma.202511078](https://doi.org/10.1002/adma.202511078).
11. Smith TJ, Kahaly GJ, Ezra DG, et al. Teprotumumab for thyroid-associated ophthalmopathy. *N Engl J Med.* 2017;376:1748-1761. PMID: [28467880](https://pubmed.ncbi.nlm.nih.gov/28467880/). doi: [10.1056/NEJMoa1614949](https://doi.org/10.1056/NEJMoa1614949).
12. Douglas RS, Kahaly GJ, Patel A, et al. Teprotumumab for the treatment of active thyroid eye disease. *N Engl J Med.* 2020;382:341-352. PMID: [31971679](https://pubmed.ncbi.nlm.nih.gov/31971679/). doi: [10.1056/NEJMoa1910434](https://doi.org/10.1056/NEJMoa1910434).

## 검증 로그 (독립 QA, 2026-10-01)

PR #9 follow-up으로 수행된 독립 세션 QA 결과. 검증 방법은 PubMed E-utilities(esummary/efetch) 원문 대조 기준이다.

| claim | tier | 검증 방법 | 결과 | 일자 |
|---|---|---|---|---|
| 참고문헌 [1]-[12]의 PMID 실존 및 서지(저자, 저널, 연도, 권호) | 하 | PubMed esummary API 전수 대조(12건) | 8건 일치. 4건에서 저자/권호 오류 확인 및 본문 정정: [2] Wang Y, Zhang S, Zhang Y -> Zhao P, Deng Y, Gu P (Wang Y는 교신저자가 아닌 제4저자), [4] Moshkelgosha S, So PW, Deasy N, Diaz-Cano S, Banga JP -> Görtz GE, Moshkelgosha S, Jesenek C, et al. (기존 저자 목록은 해당 논문의 저자와 불일치), [6] Chen MH -> Lee JY, Lee SB, Yang SW, [9] Choi CJ -> Zhu R, Chen F, Wang BW 및 145권 -> 147권. [8][10]은 저자 누락이라 신규 보기, [10]은 권호 누락 보강 | 2026-10-01 |
| [2] IGF-1이 TAO 유래 OADSC의 proliferation/lipid accumulation을 증가시키고 adiponectin/leptin/AP2/FAS mRNA와 PPARγ protein을 올림. IGF-1R antibody 또는 PI3K inhibitor(LY294002)가 이 반응과 p-Akt 상승을 차단 | 중 | abstract direct quote 대조 | 일치. "IGF-1 enhances the adipogenesis of TAO OADSCs by up-regulation of PPARγ via the activation of the IGF-1R and PI3K pathways" 원문 확인 | 2026-10-01 |
| [1] Thy-1+ subset만 TGF-β/platelet concentrate에 반응해 α-SMA+ myofibroblast로, Thy-1- subset만 PPARγ agonist에 반응해 lipofibroblast로 분화 | 중 | abstract direct quote 대조 | 일치. 원문의 PPARγ agonist는 15-deoxy-Delta(12,14)-PGJ(2)와 ciglitazone | 2026-10-01 |
| [5] 경구 linsitinib(early/late 투여)이 brown adipose tissue를 감소/정상화하고 MRI상 inflammation 감소와 muscle edema 감소를 보임. abstract에 myofibroblast fate endpoint 없음, Sirius red는 methods에만 기재 | 중 | abstract direct quote 대조 | 일치. "normalized the amount of brown adipose tissue in both the early and late group", "significant reduction of existing muscle edema and formation of brown adipose tissue" 원문 확인 | 2026-10-01 |
| [8] TED orbital fat snRNA-seq에서 fibroblast의 adipogenesis 전이 증가와 IGF-1R pathway 이상이 관찰되고, linsitinib이 TED orbital fibroblast in vitro에서 adipogenesis를 억제 | 중 | abstract direct quote 대조 | 일치. "linsitinib, a small-molecule inhibitor of IGF-1R, effectively reduced adipogenesis in TED orbital fibroblasts in vitro" 원문 확인 | 2026-10-01 |
| [9] RBM47 knockdown이 adipogenesis와 TGF-β 유도 fibrosis를 낮추고 IGF-1R을 downregulate하며, adipocyte differentiation은 IGF-1R/ERK 경유로 억제됨. fibrosis arm에 IGF1R 조작 또는 rescue는 없음 | 중 | abstract direct quote 대조 | 일치. fibrosis 평가는 scratch assay/RT-PCR/WB이고 IGF1R rescue 서술 없음 | 2026-10-01 |
| [10] G4F7-CRISPR dual TSHR/IGF1R 편집이 primary OF/3D orbital organoid/TAO mouse에서 adipogenesis/inflammation/fibrosis를 억제하며 single-gene arm보다 우수. single-arm 정량치는 abstract에 미제시 | 중 | abstract direct quote 대조 | 일치. "demonstrating superior therapeutic efficacy over either single-gene approaches" 원문 확인, single-arm 세부 수치 미제시 | 2026-10-01 |
| [3] IGF-1R antagonist가 M22 자극 high-potency phase의 HA 분비를 억제 | 하 | abstract direct quote 대조 | 일치 | 2026-10-01 |
| [7] IGF-1Rbeta와 TSHR의 pull-down association, colocalization, IGF-1R-blocking mAb에 의한 TSH 유발 ERK phosphorylation 차단 | 하 | abstract direct quote 대조 | 일치 | 2026-10-01 |
| [11][12] teprotumumab RCT 서지(NEJM 2017;376:1748-1761 / NEJM 2020;382:341-352) 및 본문에서 fate-specific endpoint로 승격하지 않는 서술 | 중 | PubMed esummary 대조 | 일치 | 2026-10-01 |
| 가운뎃점 미사용, 인용 앵커 [1]-[12]와 참고문헌 목록 1:1 대응, frontmatter 필수 키 유지 | 하 | 문서 전체 grep 및 스크립트 검사 | 가운뎃점 0건, dangling/unused 앵커 0건, 필수 키 6종 확인 | 2026-10-01 |
