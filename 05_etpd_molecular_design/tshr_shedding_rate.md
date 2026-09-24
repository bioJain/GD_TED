---
linear_issue: JHA-83
created: 2026-09-24
source: claude-code
milestone: cluster-5-etpd-molecular-design
status: done
search_cutoff: 2026-09-24
pubmed_live_search: completed
inputs:
  - 00_legacy_unsorted/GD_TED_report.md
  - 00_legacy_unsorted/meeting_notes_organized_260922.md
  - 00_baseline_biomni/landscape_v2/report_graves_ted_landscape_v2.md
---

# TSHR ectodomain shedding rate 및 circulating soluble TSHR 조사

## 결론

- **TSHR ectodomain(A/alpha-subunit)이 세포 표면에서 실제로 shed된다는 정성적 근거는 있다.** 사람 갑상선세포 및 TSHR 발현 세포에서 관찰되었고, cleavage 뒤 세포표면 체류 및 proteolysis/disulfide-linked processing의 영향을 받는다.
- 그러나 검색 범위에서 **사람 in vivo의 단위시간당 shedding rate, surface TSHR 중 shed되는 분율, 또는 shed A-subunit의 반감기를 수치화한 자료는 확인되지 않았다.** 따라서 현재 근거로 `x%/h`, `molecules/cell/day` 또는 systemic production rate를 설정할 수 없다.
- 사람 혈중 soluble TSHR를 직접 다룬 문헌은 1992년 연구 한 건(PMID **1497642**)이 핵심이다. 약 60 kDa TSHR-related peptide-like immunoreactivity와 Graves' disease군의 증가를 보고했지만, PubMed 색인 초록에는 군별 절대농도와 분석단위가 없다. **검증 가능한 circulating concentration 수치는 확보되지 않았다.** 이 신호가 이후 확립된 shed A-subunit과 완전히 동일하다는 것도 직접 입증되지 않았다.
- 따라서 eTPD 설계에서 circulating soluble TSHR에 의한 target-mediated drug disposition 또는 peripheral antigen sink를 **존재 가능성은 있으나 정량 불가한 risk**로 취급한다. 현 단계에서 "shedding이 낮다" 또는 "혈중 농도가 낮다"고 단정할 근거는 없다.

## PubMed live search

2026-09-24에 NCBI PubMed E-utilities(`esearch`, `esummary`, `efetch`)로 live search를 실행했다. 검색은 제목/초록 필드를 우선 사용했고, 후보의 PMID, 저자, 제목, 저널, 연도, 권(호), 페이지 및 DOI를 PubMed XML에서 다시 대조했다.

| # | PubMed query | 결과 수 | 판정 |
|---|---|---:|---|
| 1 | `(TSH receptor[Title/Abstract] OR thyrotropin receptor[Title/Abstract]) AND (shedding[Title/Abstract] OR shed[Title/Abstract] OR soluble[Title/Abstract] OR cleavage[Title/Abstract])` | 208 | 기전 및 후보 문헌 포괄 검색 |
| 2 | `(soluble TSH receptor[Title/Abstract] OR soluble thyrotropin receptor[Title/Abstract]) AND (serum OR plasma OR circulating OR concentration)` | 33 | 혈중 soluble TSHR 검색. soluble cytokine receptor 등 다수의 비관련 결과는 제외 |
| 3 | `(TSHR[Title/Abstract]) AND (ectodomain shedding OR A subunit shedding)` | 22 | shed A-subunit 핵심 문헌 확인 |

본 조사에서 `shedding rate`는 (a) 일정 시간 동안 방출되는 A-subunit 양, (b) 합성 또는 표면발현 receptor 중 방출되는 분율, 또는 (c) circulating A-subunit 농도와 반감기로부터 계산되는 flux로 정의했다. 단순 cleavage 유무, band intensity, detergent-soluble fraction 및 recombinant construct 분비는 사람 in vivo rate로 간주하지 않았다.

검색 URL: [query 1](https://pubmed.ncbi.nlm.nih.gov/?term=%28TSH+receptor%5BTitle%2FAbstract%5D+OR+thyrotropin+receptor%5BTitle%2FAbstract%5D%29+AND+%28shedding%5BTitle%2FAbstract%5D+OR+shed%5BTitle%2FAbstract%5D+OR+soluble%5BTitle%2FAbstract%5D+OR+cleavage%5BTitle%2FAbstract%5D%29), [query 2](https://pubmed.ncbi.nlm.nih.gov/?term=%28soluble+TSH+receptor%5BTitle%2FAbstract%5D+OR+soluble+thyrotropin+receptor%5BTitle%2FAbstract%5D%29+AND+%28serum+OR+plasma+OR+circulating+OR+concentration%29), [query 3](https://pubmed.ncbi.nlm.nih.gov/?term=%28TSHR%5BTitle%2FAbstract%5D%29+AND+%28ectodomain+shedding+OR+A+subunit+shedding%29).

## 후보 PMID 및 서지사항 직접 검증

아래 서지사항은 검색결과 문자열을 재사용하지 않고 PubMed `efetch` XML의 각 레코드에서 직접 확인했다.

| PMID | PubMed에서 확인한 서지사항 | 이 질문에 대한 직접성 | 확인 결과 |
|---:|---|---|---|
| [8626810](https://pubmed.ncbi.nlm.nih.gov/8626810/) | Couet J, Sar S, Jolivet A, Hai MT, Milgrom E, Misrahi M. *Shedding of human thyrotropin receptor ectodomain. Involvement of a matrix metalloprotease.* **J Biol Chem.** 1996;271(8):4545-4552. doi:10.1074/jbc.271.8.4545. | 직접 실험 | 사람 thyrocyte와 transfected L/CHO cell에서 shedding 확인. endocytosis/recycling/lysosomal degradation 억제 시 증가, TSH 및 phorbol ester로 소폭 증가, serum 감소 시 증가, BB-2116으로 억제. 초록에는 절대 rate 또는 분율 없음 |
| [10411305](https://pubmed.ncbi.nlm.nih.gov/10411305/) | Tanaka K, Chazenbalk GD, McLachlan SM, Rapoport B. *The shed thyrotropin receptor is primarily a carboxyl terminal truncated form of the A subunit, not the entire A subunit.* **Mol Cell Endocrinol.** 1999;150(1-2):113-119. doi:10.1016/S0303-7207(99)00018-0. | 직접 실험 | shed species의 주성분이 C-terminal truncated A-subunit임을 제시. 표준 serum 조건에서는 normal-sized A-subunit도 더 적은 양으로 검출. rate 및 혈중농도 없음 |
| [10567361](https://pubmed.ncbi.nlm.nih.gov/10567361/) | Tanaka K, Chazenbalk GD, McLachlan SM, Rapoport B. *Subunit structure of thyrotropin receptors expressed on the cell surface.* **J Biol Chem.** 1999;274(48):33979-33984. doi:10.1074/jbc.274.48.33979. | 직접 실험 | 낮은 A/B subunit ratio를 partial shedding의 근거로 제시하지만, 일반화 가능한 시간당 rate는 제시하지 않음 |
| [12919313](https://pubmed.ncbi.nlm.nih.gov/12919313/) | Quellari M, Desroches A, Beau I, Beaudeux E, Misrahi M. *Role of cleavage and shedding in human thyrotropin receptor function and trafficking.* **Eur J Biochem.** 2003;270(17):3486-3497. doi:10.1046/j.1432-1033.2003.03718.x. | 직접 실험 | cleavage/shedding 후 free beta-subunit의 activation 및 internalization을 연구. 생체 shedding rate/혈중농도 자료 아님 |
| [15319351](https://pubmed.ncbi.nlm.nih.gov/15319351/) | Latif R, Ando T, Davies TF. *Monomerization as a prerequisite for intramolecular cleavage and shedding of the thyrotropin receptor.* **Endocrinology.** 2004;145(12):5580-5588. doi:10.1210/en.2004-0797. | 직접 실험 | CHO 모델에서 TSH가 cleavage 및 shedding을 시간·농도 의존적으로 증가시킴. cell-based cleavage assay는 있으나 사람 in vivo shedding rate로 전환할 수 없음 |
| [17911409](https://pubmed.ncbi.nlm.nih.gov/17911409/) | Ando T, Latif R, Davies TF. *Antibody-induced modulation of TSH receptor post-translational processing.* **J Endocrinol.** 2007;195(1):179-186. doi:10.1677/JOE-07-0058. | 직접 실험 | 일부 TSHR antibody가 cleavage를 억제하고 receptor expression을 높이는 epitope-dependent 효과를 보고. 일정한 고유 shedding rate 가정이 부적절함을 뒷받침 |
| [26799472](https://pubmed.ncbi.nlm.nih.gov/26799472/) | Rapoport B, McLachlan SM. *TSH Receptor Cleavage Into Subunits and Shedding of the A-Subunit; A Molecular and Clinical Perspective.* **Endocr Rev.** 2016;37(2):114-134. doi:10.1210/er.2015-1098. | 종설 | A-subunit shedding의 기전 및 Graves' disease 면역원성 가설을 종합. 정량적 사람 in vivo rate 또는 circulating concentration의 기준값은 PubMed 초록에 없음 |
| [1497642](https://pubmed.ncbi.nlm.nih.gov/1497642/) | Murakami M, Miyashita K, Yamada M, Iriuchijima T, Mori M. *Characterization of human thyrotropin receptor-related peptide-like immunoreactivity in peripheral blood of Graves' disease.* **Biochem Biophys Res Commun.** 1992;186(2):1074-1080. doi:10.1016/0006-291X(92)90856-G. | 사람 혈장 직접 측정 | RIA dilution parallelism, 약 60 kDa 신호, Graves' disease군에서 normal 및 Hashimoto hypothyroidism군보다 유의하게 높은 immunoreactivity를 보고. 색인 초록에는 절대농도/단위 미기재 |
| [6244931](https://pubmed.ncbi.nlm.nih.gov/6244931/) | Hashizume K, DeGroot LJ. *Release of thyrotropin receptor from thyroid plasma membranes: effect of hydrocortisone, propranolol, and adenosine 3',5'-monophosphate.* **Endocrinology.** 1980;106(5):1463-1468. doi:10.1210/endo-106-5-1463. | 간접, 비생리적 in vitro | bovine membrane/hypotonic buffer에서 receptor release를 관찰. 저자도 비생리적 조건임을 명시하므로 사람 shedding rate 또는 circulating concentration 근거로 사용하지 않음 |
| [9685994](https://pubmed.ncbi.nlm.nih.gov/9685994/) | Misrahi M, Couet J, Milgrom E. *[Mechanisms of shedding of a soluble form of the TSH receptor].* **Ann Endocrinol (Paris).** 1997;58(5):365-369. DOI 미등재. | 종설/기전 요약 | PMID와 프랑스어 제목의 레코드 실재를 확인. PMID 8626810의 기전과 부합하지만 독립적인 rate 또는 농도값은 없음 |

### 기존 merge본 후보와의 대조

이전 merge본에 적힌 후보 식별자는 live PubMed record와 재대조했다. 이 과정에서 세 건의 PMID 오기재를 확인했으므로 그대로 병합하지 않았다.

| 기존 기재 | live PubMed 대조 | 처리 |
|---:|---|---|
| `8626801` | HIV-1 protease 논문 | TSHR shedding 논문의 올바른 PMID `8626810`으로 교정 |
| `9202231` | connexin 43 및 hypoglycemia 논문 | two-cleavage-site 논문의 올바른 PMID `9202233`으로 교정. 본 표의 핵심 rate/concentration 근거에는 포함하지 않음 |
| `11397853` | preterm birth risk-factor 논문 | TSHR 문헌 식별자로 사용할 수 없어 제외 |
| `16075037` | *Thyrotropin receptor-associated diseases: from adenomata to Graves disease*와 일치 | 유효한 종설 후보이나 직접 rate/concentration 자료가 아니므로 핵심 표에서는 제외 |

## Shedding rate 평가

### 확인된 사실

1. TSHR은 single-chain receptor에서 A- 및 B-subunit으로 cleavage되고, 일부 extracellular A-subunit이 세포표면에서 유리된다.
2. 측정치는 실험계에 민감하다. cell-surface residency, serum 농도, TSH, phorbol ester, receptor monomerization 및 결합 항체가 processing/shedding을 바꾼다.
3. 따라서 배양세포의 band intensity나 A/B ratio를 사람 조직의 정상상태 flux로 치환할 수 없다.

### 찾지 못한 정량치

- 사람 thyrocyte에서 `fraction shed / unit time`
- 사람에서 soluble TSHR A-subunit의 production/clearance rate
- shed A-subunit의 혈중 반감기
- 정상인, Graves' disease 또는 TED에서 재현된 절대 circulating concentration reference range

**판정:** biological phenomenon은 확인되지만, JHA-83에서 요구한 의미의 정량적 shedding rate는 현재 PubMed 문헌으로 **미확립(not established)** 이다. 이는 "0" 또는 "낮음"을 뜻하지 않는다.

## Circulating soluble TSHR concentration 평가

PMID 1497642가 사람 peripheral blood에서 가장 직접적인 후보이나, 해당 assay는 TSHR amino acids 32-56 합성 peptide에 대한 antiserum으로 측정한 `TSHRP-1-like immunoreactivity`이다. 약 60 kDa라는 분자량 및 질환군 차이는 soluble extracellular-domain 가설과 일치하지만 다음 이유로 현대적인 intact/shed TSHR 농도 기준값으로 바로 사용할 수 없다.

- epitope-specific immunoreactivity이며 molecular identity를 완전히 확정하지 않음
- PubMed 초록에 절대 수치 및 단위가 없음
- 후속 독립 cohort 또는 표준화된 assay reference range를 이번 live search에서 확인하지 못함

그러므로 molar concentration으로의 변환, tissue-to-plasma partition 또는 decoy occupancy 계산은 보류한다. 원문 전문을 합법적으로 확보하면 우선 확인할 항목은 각 군의 `mean/median`, 분산, 표본수, 표준물질, 회수율, 검출한계 및 dilution linearity이다.

## eTPD 분자설계에 대한 결정

| 설계 질문 | 현재 답 | 후속 조치 |
|---|---|---|
| soluble antigen sink를 수치로 PK 모델에 넣을 수 있는가? | 아니오. 검증된 농도와 turnover가 없음 | 초기 모델은 0이 아닌 wide sensitivity range를 사용하고 가정으로 명시 |
| shedding이 낮다고 전제해도 되는가? | 아니오 | membrane-bound 및 soluble A-subunit 양쪽에 대한 binding/clearance assay 설계 |
| 후보 clone 비교에서 무엇을 측정해야 하는가? | soluble A-subunit interference와 membrane TSHR 결합을 분리 | recombinant A-subunit spike-in 농도구배, cell-surface binding, internalization 및 ternary-complex/clearance readout 포함 |
| 어떤 임상 검체가 필요한가? | GD/TED 및 대조군 plasma/serum | orthogonal immunoassay와 immunoprecipitation-MS로 analyte identity 및 절대농도 확인 |

## Repo 근거와 JHA-88 전달사항

- `00_legacy_unsorted/meeting_notes_organized_260922.md` §0 및 §1-E의 질문처럼 IC 침착 기전과 shedding rate는 분리해 해석한다.
- `00_legacy_unsorted/GD_TED_report.md` Section E1의 기본 cargo는 circulating TSAb이며, 정량되지 않은 free soluble TSHR를 primary clearance cargo로 재해석하지 않는다.
- `00_baseline_biomni/landscape_v2/report_graves_ted_landscape_v2.md` §5.1-5.2의 LCA-0321/MER511 주장은 soluble TSHR 농도 또는 turnover의 임상 검증을 대신하지 않는다.
- JHA-88의 현 molecule spec에는 shedding을 숫자로 채우지 않고 `unknown; empirical gate`로 전달한다.

## 최종 판정과 완료 조건

PubMed live search는 정상 응답했고, 핵심 후보 PMID와 서지사항을 PubMed 원문 레코드에서 직접 검증했으며, shedding rate 및 circulating soluble TSHR concentration의 정량 근거 유무까지 평가했다. **검색은 성공했으므로 문서 상태를 `done`으로 변경한다.** `done`은 수치가 존재함을 뜻하는 것이 아니라, 현재 공개·색인 문헌에서 수치가 확립되지 않았다는 negative finding까지 포함해 JHA-83의 검색 작업을 완료했다는 뜻이다.
