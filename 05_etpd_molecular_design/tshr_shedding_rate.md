---
linear_issue: JHA-83
created: 2026-09-24
source: manual
milestone: cluster-5-etpd-molecular-design
status: in-review
inputs:
  - 00_legacy_unsorted/GD_TED_report.md
  - 00_legacy_unsorted/meeting_notes_organized_260922.md
  - 00_baseline_biomni/landscape_v2/report_graves_ted_landscape_v2.md
literature_checked: 2026-09-24
pubmed_live_search: attempted-but-unavailable
---

# TSHR ectodomain shedding rate 문헌 확인

## 결론 요약

- **사람에서의 TSHR ectodomain shedding rate는 현재 검토 범위에서 미확인(잠정)**: 확인한 문헌은 TSHR의 constitutive intramolecular cleavage와 A-subunit shedding을 정성적으로 입증하지만, 정상인/GD 환자의 thyroid에서 단위 시간당 방출량, 전체 surface TSHR 중 방출 비율, 또는 in vivo half-life를 제시하지 않음[1-4]. 따라서 추정 백분율을 분자 스펙에 입력하지 않음.
- **순환 soluble TSHR ectodomain 농도도 임상적으로 검증된 수치가 없음**: 확인 범위에서 정상인 또는 GD/TED 환자 plasma/serum의 intact soluble TSHR A-subunit을 절대농도(mass/volume 또는 molarity)로 정량한 검증된 assay/cohort를 찾지 못함. `TSHR mRNA splice variant`, recombinant TSHR, TRAb assay의 soluble receptor reagent는 환자 혈중 soluble antigen 측정치가 아니므로 제외함.
- **free TSHR antigen을 sweeping target으로 삼는 설계는 현재 근거로 지지되지 않음**: 접근 가능한 농도와 turnover가 모두 미확정이므로, soluble TSHR 자체를 주된 clearance cargo로 설정하거나 antigen-sink 용량을 계산할 수 없음. 반면 TSAb/TRAb는 혈중 접근 가능한 IgG이므로, `TSHR ectodomain bait -> 병원성 autoantibody 포획 -> clearance`가 문헌과 개발 지형에 부합하는 기본 방향임. 이 결론은 효능 입증이 아니라 **design prior**임.

## 1. PubMed 검색 상태와 검색식

**중요 정정**: 초안 작성 시 PubMed live search를 시도했으나 실행 환경의 web-search 인증 오류와 NCBI network 차단으로 검색 결과 화면/record를 직접 열지 못함. 따라서 아래 참고문헌의 PMID는 live PubMed record와 대조 완료된 것으로 간주하면 안 되며, 본 문서는 `in-review` 상태임.

시도한 검색식:

- `TSH receptor ectodomain shedding cleavage A subunit`
- `"Shedding of human thyrotropin receptor ectodomain"`
- `soluble TSH receptor serum Graves concentration`
- `thyrotropin receptor A-subunit shedding rate`

완료 조건은 PubMed에서 위 검색식 및 동의어(`thyrotropin receptor`, `TSHR`, `soluble receptor`, `cleavage`, `release`)를 직접 실행하고, 각 record의 PMID/서지사항/abstract를 대조하며, 관련 논문의 cited-by/reference chain을 검토하는 것임. 이 검증 전에는 `문헌상 미보고` 결론을 **잠정 결론**으로만 사용함.

## 2. 질문과 판정 기준

본 조사에서 `shedding rate`는 (a) 일정 시간 동안 방출되는 TSHR A-subunit의 양, (b) 합성/표면발현된 receptor 중 방출되는 분율, 또는 (c) 사람 혈중 soluble A-subunit 농도와 half-life 중 하나가 수치로 제시된 경우로 한정함. 배양세포의 band intensity, cleavage 유무, detergent-soluble fraction 또는 recombinant construct 분비는 사람의 in vivo rate로 환산하지 않음.

## 3. 알려진 기전과 알려지지 않은 수치

### 3.1 기전

TSHR은 단일-chain precursor로 합성된 뒤 ectodomain 내 두 절단 부위 사이의 약 50-amino-acid segment가 제거되어 extracellular A-subunit과 membrane-spanning B-subunit을 형성함. 두 subunit은 disulfide bond로 연결될 수 있으며, 결합이 환원되면 A-subunit이 세포 표면에서 방출될 수 있음[1-3]. 세포계 연구는 metalloprotease activity가 ectodomain release에 관여함을 지지하지만, 특정 physiological sheddase, 조직별 flux와 사람에서의 조절인자는 확정되지 않음[1,2].

### 3.2 수치 판정

| 질문 | 확인 결과 | 분자설계에 사용할 수 있는 값 |
|---|---|---|
| 전체 TSHR 중 cleavage되는 비율 | transfected-cell biochemical studies에서 cleavage/uncleaved species를 관찰했으나 사람 thyroid의 population rate 미보고[1-3] | 없음 |
| cleavage된 receptor 중 A-subunit이 shed되는 비율 | shedding 현상은 입증됐으나 standardized denominator와 사람 in vivo time course 미보고[1-3] | 없음 |
| plasma/serum soluble TSHR A-subunit 농도 | 검증된 endogenous antigen immunoassay 및 정상/GD reference range를 확인하지 못함[3,4] | 없음 |
| soluble TSHR half-life/clearance | 사람 PK 자료 미보고[3,4] | 없음 |
| alternative-splice soluble TSHR | transcript/construct 수준 근거를 proteolytic A-subunit shedding 또는 혈중 농도로 환산할 수 없음[4] | 없음 |

핵심적으로 `cleavage`, `A/B-subunit 구조`, `A-subunit release`는 서로 연결되지만 동일한 endpoint가 아님. 세포에서 cleavage가 관찰됐다는 사실만으로 혈중 soluble antigen abundance가 높거나 낮다고 판정할 수 없음.

## 4. sweeping 접근성 판단

### 4.1 판정

**Free soluble TSHR ectodomain: 현재 `No-go as a quantified primary cargo`, 단 experimental validation 대상.** 농도, molecular form, epitope integrity, residence time이 모두 미확정이므로 dose, binding capacity 또는 target-mediated drug disposition을 계산하는 표적항원으로 사용할 근거가 부족함.

**Circulating anti-TSHR autoantibody: `Proceed as the intended cargo`, 단 selectivity/functional neutralization 검증 필요.** repo의 v2 landscape에서 LCA-0321은 anti-TSHR autoantibody 선택적 binding/removal, MER511은 engineered TSHR ectodomain-Fc를 통한 neutralization/clearance를 표방함. 두 프로그램 모두 human efficacy와 target-disposition 결과가 아직 확립되지 않았고 evidence confidence가 각각 Low, Low-moderate이므로 선행 validation의 대체물이 아님.

### 4.2 설계 리스크

1. **Soluble-antigen sink 불확실성**: endogenous soluble A-subunit이 존재하면 bait와 병원성 antibody의 경쟁, 또는 construct와의 complex 형성에 영향을 줄 수 있으나 현재 용량 계산 불가.
2. **Epitope mismatch**: shed A-subunit의 processing/glycosylation/conformation이 membrane TSHR과 다르면 TSAb epitope를 완전히 재현하지 못할 가능성.
3. **TSH/TRAb 기능 혼합**: blocking/neutral TRAb와 TSAb를 구분하지 않는 affinity-only readout은 병원성 cargo selectivity를 과대평가할 가능성.
4. **Assay interference**: soluble TSHR, endogenous TSH, anti-drug antibody 및 bait-drug complex가 ligand-binding assay를 교란할 가능성.

### 4.3 JHA-88에 전달할 최소 실험 입력

- 사람 plasma/serum에서 immunocapture-LC-MS 또는 orthogonal sandwich assay로 soluble TSHR A-subunit의 LLOQ와 농도 범위를 먼저 설정.
- full-length membrane TSHR, purified shed-like A-subunit, engineered bait 사이의 TSAb clone panel binding/competition을 비교.
- GD/TED sample에서 free TSAb, total TSAb, drug-bound TSAb를 구분하고 functional cAMP bioassay를 병행.
- 예상 therapeutic concentration 대비 soluble TSHR molar ratio를 측정한 후에만 antigen-sink/target-mediated disposition model에 포함.
- 현재 molecule spec의 shedding 항목은 숫자가 아니라 `unknown; empirical gate`로 기록하고 임의의 low/high 가정을 base case로 사용하지 않음.

## 5. 근거의 한계

- 초기 핵심 문헌은 transfected mammalian cells, immunoblot, radiolabeling 중심이며 임상 biofluid 정량 연구가 아님[1-3].
- `문헌상 미보고`는 존재하지 않음을 증명한 것이 아니라, 아래 후보 mechanism literature와 repo의 direct-TSHR program evidence를 검토한 범위에서 설계에 사용할 검증 수치를 발견하지 못했다는 의미임.
- LCA-0321/MER511의 공개 설명에서 soluble TSHR concentration 또는 endogenous shedding-rate 기반 dose rationale은 repo frozen evidence package에 확인되지 않음. 사람 결과 공개 시 재평가 필요.

## 참고문헌

초안 입력일: **2026-09-24**. 아래 PMID는 live PubMed record 대조 전의 후보 식별자이며, 검증 완료 전 인용에 사용하지 않음.

1. Couet J, Sar S, Jolivet A, Hai MT, Milgrom E, Misrahi M. *Shedding of human thyrotropin receptor ectodomain. Involvement of a matrix metalloprotease.* Journal of Biological Chemistry. 1996;271:4545-4552. **PMID: 8626801**.
2. Chazenbalk GD, Tanaka K, Nagayama Y, Kakinuma A, Jaume JC, McLachlan SM, Rapoport B. *Evidence that the thyrotropin receptor ectodomain contains not one, but two, cleavage sites.* Endocrinology. 1997;138:2893-2899. **PMID: 9202231**.
3. Rapoport B, McLachlan SM. *The thyrotropin receptor's great divide: cleavage into subunits, with shedding of the A-subunit.* Journal of Clinical Endocrinology & Metabolism. 2001;86:2600-2604. **PMID: 11397853**.
4. Davies TF, Ando T, Lin RY, Tomer Y, Latif R. *Thyrotropin receptor-associated diseases: from adenomata to Graves disease.* Journal of Clinical Investigation. 2005;115:1972-1983. **PMID: 16075037**.

## Repo 근거

- `00_legacy_unsorted/meeting_notes_organized_260922.md` §0, §1-E: IC 침착 기전과 shedding rate 질문의 분리.
- `00_legacy_unsorted/GD_TED_report.md` Section E1: circulating TSAb를 extracellular sweeping cargo로 보는 기존 개념.
- `00_baseline_biomni/landscape_v2/report_graves_ted_landscape_v2.md` §5.1-5.2: LCA-0321/MER511 mechanism claim과 human-evidence boundary.
