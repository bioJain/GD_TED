---
linear_issue: JHA-77
created: 2026-09-28
source: claude-code
milestone: cluster-3-mechanism-deepdive
status: done
inputs:
  - 00_legacy_unsorted/GD_TED_report.md
  - _shared/GD_TED_reference.md
  - _shared/GD_TED_qa_checklist.md
---

# IGF-1R Autoantigen/Autoantibody: 2024-2026 재검색 및 독립 섹션 신설 검토

## 결론 요약

**판정: 독립 섹션 신설 불필요 — 기존 B4 서술 보강으로 충분.**

- 2024-2026 재검색 결과, "IGF-1R이 TSAb와 무관하게 그 자체로 자가항체의 직접 표적(자가항원)인가"라는 질문에 대한 근거는 **강화되지 않고 오히려 기존 NIH 반박 입장(B4 세 번째 가설[23])과 같은 방향으로 재확인/정교화**되었다.
- 다만 2025년 두 개의 독립적 임상 코호트 연구(Pisa 그룹[N2], Katowice 그룹[N3])가 처음으로 **혈청 anti-IGF-1R 자가항체를 정량 ELISA로 측정**했고, 공통적으로 **IGF-1R 자가항체가 GO 발생/중증도와 역상관(보호적/억제성 방향)**을 보고했다 — 이는 "IGF-1R directly-stimulating antibody 근거 부족"이라는 2020년 NIH 결론[23]을 뒤집는 것이 아니라, 오히려 그 결론이 예측한 범위 밖에서 **새로운 하위 발견(자가항체는 존재하되 기능은 자극성이 아닌 억제성)**을 추가한 것이다.
- 동물모델 근거(TSHR 유전자면역은 TED 모델을 재현하나 IGF-1R 면역화는 재현하지 않음)는 2025년 review에서도 그대로 재확인되어[N7], TSHR이 유일한 확립된 primary autoantigen이라는 입장은 변하지 않았다[N7, N9].
- TSHR-IGF-1R 물리적 상호작용(receptor crosstalk) 쪽 근거는 계속 축적되고 있으나(직접 결합[21], TSHR Ab에 의한 IGF-1R 발현 동시 상향조절[N1]), 이는 "IGF-1R 자체가 자가항원"이라는 명제와는 별개 질문이며 crosstalk 기전 자체는 JHA-79(별도 이슈)의 범위다.
- 따라서 신규 근거는 (1) 독립 섹션을 정당화할 만큼 disease-defining한 새 기전을 확립하지 못했고, (2) 방향성상 오히려 "IGF-1R 자가항체 = 병인성" 가설에 불리한 쪽으로 축적되고 있어, B4의 기존 세 번째 가설 서술에 **"자가항체는 실재하나 방향은 억제/보호적일 가능성"**이라는 문장을 추가하는 것으로 충분하다고 판단한다. 아래 5절에 B4 반영용 문안을 제시한다.

## 1. Section B4 반박논거 재확인

`00_legacy_unsorted/GD_TED_report.md` Section B4의 세 번째 경쟁 가설(원문 인용 유지):

> **IGF-1R directly-stimulating antibody 가설에 대한 반박**: NIH 연구팀은 GO 병인에서 IGF-1R을 직접 자극하는 항체(IGF1R stimulating Ab)의 근거가 부족하며, 관찰된 현상들이 TSHR-IGF1R crosstalk로 설명 가능하다고 결론 — TSHR을 자극 자가항체의 유일한 직접 표적으로 유지하는 입장[23]

- 인용 [23] = Krieger CC, Neumann S, Gershengorn MC. *Is There Evidence for IGF1R-Stimulating Abs in Graves' Orbitopathy Pathogenesis?* Int J Mol Sci. 2020;21(18):6561. PMID: [32911689](https://pubmed.ncbi.nlm.nih.gov/32911689/).
- 이 논문의 핵심 주장은 "**IGF-1R을 직접 자극(stimulating)하는 항체**"에 대한 근거 부족이며, "IGF-1R에 결합하는 항체 자체가 존재하지 않는다"는 주장이 아니다. 즉 반박 대상은 **자극성(agonistic) IGF-1R Ab** 가설이지, IGF-1R에 대한 항체 결합 가능성 전체가 아니다. 이 구분이 2024-2026 신규 근거를 해석하는 데 중요하다(2절 참조).
- B4는 이를 TSHR-IGF-1R crosstalk(β-arrestin 매개 vs 직접 물리적 결합) 두 가설과 병렬로 제시하고 있으며, 세 가설 모두 "확립된 사실 아님"으로 명시하고 있다(QA D2 대응). 이번 재검색은 이 병렬 구조 자체를 바꿀 근거를 찾지 못했다.

## 2. 2024-2026 재검색 결과

### 검색 개요

- 검색일: **2026-09-28**. Database: PubMed.
- 검색어: `IGF-1R autoantibody Graves orbitopathy`, `IGF-1 receptor autoantigen thyroid eye disease`, `TSHR IGF-1R crosstalk Graves orbitopathy`, `anti-IGF-1 receptor antibody inhibitory Graves orbitopathy protective` (날짜 필터 2024-01-01 ~ 2026-12-31, 마지막 쿼리는 무필터로도 결과 없음 확인).
- 중복 제거 후 12건의 관련 논문을 스크리닝. 이하 핵심 근거만 발췌.

### 2.1 신규: 혈청 anti-IGF-1R 자가항체의 정량 측정 — 두 독립 코호트

1. **Lanzolla G, et al. In vivo and in vitro evidence for a protective role of autoantibodies against the insulin-like growth factor-1 receptor (IGF-1R) in Graves' orbitopathy.** Endocrine. 2025;89(1):137-142. PMID: [40156685](https://pubmed.ncbi.nlm.nih.gov/40156685/). doi: [10.1007/s12020-025-04219-6](https://doi.org/10.1007/s12020-025-04219-6). — Pisa 대학병원, GD 환자 147명(GO 92명 vs non-GO 55명) 횡단연구. 혈청 IGF-1R-Ab(ELISA)가 **non-GO군에서 유의하게 더 높음**(29.3 ng/mL vs 19.8 ng/mL, P=0.005); GO 환자 내에서는 IGF-1R-Ab가 diplopia 중증도와 **역상관**(더 중증일수록 낮음, P=0.035); IGF-1R-Ab 고역가(>55 ng/mL) 혈청에서 정제한 IgG를 GO 환자 유래 orbital fibroblast에 처리하자 **세포증식이 용량의존적으로 감소**(P<0.0001). 저자 결론: IGF-1R 자가항체는 GD 환자 일부에서 존재하며 GO 발생/중증도에 대해 **보호적(protective)** 역할을 시사.
2. **Nowak M, et al. Antibodies against the receptor for insulin-like growth factor 1 (IGF-1RAb) ... in the serum of patients with Graves' and Basedow's disease with and without orbitopathy.** Endokrynol Pol. 2025;76(1):40-51. PMID: [40071798](https://pubmed.ncbi.nlm.nih.gov/40071798/). doi: [10.5603/ep.102336](https://doi.org/10.5603/ep.102336). — Katowice 그룹, GBD 47명(활동성 TO 31명, 이 중 sight-threatening 10명) + 대조 20명. In-house ELISA로 IGF-1RAb 측정. **Sight-threatening 중증 TO군에서 IGF-1RAb가 non-TO GBD군보다 유의하게 낮음**(P=0.004); moderate-to-severe vs sight-threatening 사이에도 유의한 차이(P=0.014). 저자 결론: "고농도 IGF-1RAb는 TO 발생/중증 경과에 대해 보호적일 수 있으며, 항-IGF-1R 항체는 **억제성(inhibitory)** 항체로 추정됨."

- **해석**: 두 그룹이 독립적으로, 서로 다른 코호트/assay(ELISA 자체 구축)를 사용해 **"IGF-1R 자가항체 = 존재하나 방향은 억제/보호"** 라는 동일한 방향의 결론에 도달했다는 점에서 우연적 발견 이상의 신호로 볼 수 있다. 그러나 두 연구 모두 (a) 단일기관 횡단설계, (b) in-house ELISA로 cut-off 값의 외부 검증 부재, (c) 기전 규명은 Lanzolla 연구의 IgG-purification 실험 1건에 국한된다는 한계가 있어 "확립된 사실"로 승격하기는 이르다(QA F6 대응 — "suggested"/"under investigation" 수준 유지 필요).
- **B4 반박논거[23]와의 관계**: 이 결과는 [23]의 "IGF-1R 직접 자극 항체 근거 부족"이라는 결론과 **모순되지 않고 오히려 보강**한다 — 자극성(agonistic) 항체 대신, 존재가 확인된 IGF-1R 항체는 방향상 억제성(antagonistic-like)으로 보고되고 있기 때문이다. 즉 "IGF-1R을 표적으로 하는 자가항체가 병인을 유발한다"는 독립 자가항원 가설은 이번 재검색에서도 지지되지 않았다.

### 2.2 TSHR을 primary autoantigen으로 유지하는 근거 재확인

3. **Wiersinga WM, Eckstein AK, Žarković M. Thyroid eye disease (Graves' orbitopathy): clinical presentation, epidemiology, pathogenesis, and management.** Lancet Diabetes Endocrinol. 2025;13(7):600-614. PMID: [40324443](https://pubmed.ncbi.nlm.nih.gov/40324443/). doi: [10.1016/S2213-8587(25)00066-X](https://doi.org/10.1016/S2213-8587(25)00066-X). — "Genetic immunisation of mice with TSHR, but not with IGF-1R, provides a reliable animal model of TED, demonstrating that TSHR is the primary autoantigen in the disease. Crosstalk between TSHR and IGF-1R occurs via a β-arrestin scaffold." B4 원문의 동물모델 논거([1])와 동일한 결론을 2025년 시점에서도 재확인.
4. **Smith TJ. Controversies Surrounding IGF-I Receptor Involvement in Thyroid-Associated Ophthalmopathy.** Thyroid. 2025;35(3):232-244. PMID: [39909461](https://pubmed.ncbi.nlm.nih.gov/39909461/). doi: [10.1089/thy.2024.0606](https://doi.org/10.1089/thy.2024.0606). — 제목 자체가 "논쟁 중"임을 명시. TSHR/IGF-1R 신호복합체가 GD-OF와 CD34+ fibrocyte에서 병리적 IgG에 반응한다는 입장을 유지하되, IGF-1R을 독립 자가항원으로 확정하는 근거는 제시하지 않음 — "복합체를 통한 매개(mediation)"와 "IGF-1R 자체가 자가항원"을 구분해서 읽어야 함을 시사.
5. **Smith TJ. TSHR-IGF-IR complex drives orbital fibroblast misbehavior in thyroid eye disease.** Curr Opin Endocrinol Diabetes Obes. 2024;31(5):177-183. PMID: [39082947](https://pubmed.ncbi.nlm.nih.gov/39082947/). doi: [10.1097/MED.0000000000000878](https://doi.org/10.1097/MED.0000000000000878). — CD34+ fibrocyte가 TSHR/thyroglobulin/thyroperoxidase 등 **기존에 알려진 갑상선 자가항원**을 발현한다는 내용은 있으나, IGF-1R을 새로운 자가항원으로 규정하지 않음.
6. **Lanzolla G, Marinò M, Menconi F. Graves disease: latest understanding of pathogenesis and treatment options.** Nat Rev Endocrinol. 2024;20(11):647-660. PMID: [39039206](https://pubmed.ncbi.nlm.nih.gov/39039206/). doi: [10.1038/s41574-024-01016-5](https://doi.org/10.1038/s41574-024-01016-5). — "main autoantigen"은 TSHR으로 서술, IGF-1R은 치료 표적(target-based therapy) 맥락에서만 언급.

### 2.3 TSHR-IGF-1R crosstalk/복합체 형성 근거 축적 (참고 — 상세 분석은 JHA-79 범위)

7. **Xiang P, Mezei M, Latif R, Davies TF. Stimulating Thyrotropin Receptor Antibodies Enhance the Expression of Both Thyrotropin Receptors and Insulin-Like Growth Factor 1 Receptors in Fibroblasts.** Thyroid. 2026;36(8):903-911. PMID: [42374926](https://pubmed.ncbi.nlm.nih.gov/42374926/). doi: [10.1177/10507256261463222](https://doi.org/10.1177/10507256261463222). — TSH/자극성 TSHR Ab(M22)가 fibroblast에서 **TSHR과 IGF-1R 발현을 함께 상향조절**(endocytosis-recycling 매개)함을 확인 — "TSHR 자가항체가 IGF-1R 발현까지 증폭시켜 상류에서 하류 crosstalk를 강화한다"는 기존 모델[21,22]과 부합. 이는 IGF-1R을 별도 자가항원으로 만드는 근거가 아니라, **TSHR 자가항체 단일 표적으로도 두 수용체 신호를 함께 증폭시킬 수 있다는 기전**으로, 오히려 "TSHR 단일 표적으로 충분히 설명 가능"이라는 B4 결론([23])과 같은 방향이다.
8. **Latif R, Mezei M, Davies TF.** (기존 인용 [21], PMID 39821041) — TSHR ectodomain과 IGF-1R의 β-arrestin 비의존적 직접 결합을 분자동역학/co-IP로 재확인. 2025년 발표로 B4 서술 시점 이후 추가 검증 완료.

### 2.4 그 외 — 분자모방(molecular mimicry) 가설 (참고, 낮은 우선순위)

9. **Garg I, Meyer BI, Gallo RA, Wester ST, Pelaez D. Human Papillomavirus and Thyroid Eye Disease.** JAMA Ophthalmol. 2025;143(6):524-528. PMC: [PMC12022865](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC12022865/). PMID: [40272832](https://pubmed.ncbi.nlm.nih.gov/40272832/). doi: [10.1001/jamaophthalmol.2025.0847](https://doi.org/10.1001/jamaophthalmol.2025.0847). — TSHR/IGF-1R과 HPV18 L1 capsid 단백질 간 아미노산 서열 상동성(molecular mimicry) 발견, TED 안와지방 조직에서 HPV18 L1 IgG 역가 차이(대조 대비, P<.001~.03). n=22의 소규모 case-control, exploratory 수준. IGF-1R이 "왜 자가면역 표적이 될 수 있는가"에 대한 새로운 upstream 가설을 제공하나, 이번 이슈의 핵심 질문(자가항체 존재/기능)과는 결이 달라 별도 심층 검토가 필요하면 추후 이슈로 분리 권고.

## 3. 지지논거 vs 반박논거 균형 정리 (완료조건 대응)

| 구분 | 근거 | 방향 |
|---|---|---|
| **지지** (IGF-1R이 자가면역 표적/신호에 관여) | 혈청 anti-IGF-1R 자가항체가 ELISA로 실제 측정됨(2개 독립 코호트)[N2, N3] | 존재는 지지하나 **기능은 억제/보호**로 병인성 자가항원 가설에는 불리 |
| **지지** | TSHR-IGF-1R 물리적 복합체/crosstalk 근거 지속 축적[21, N1] | IGF-1R이 신호전달에 관여함을 지지하나 **자가항원 지위는 아님** |
| **지지(약함)** | HPV와 TSHR/IGF-1R 간 분자모방 가능성[N8] | exploratory, n=22, 검증 초기 단계 |
| **반박** | TSHR 유전자면역만이 TED 동물모델을 재현, IGF-1R 면역화는 재현 안 됨[N7] | TSHR이 유일한 established primary autoantigen이라는 입장 변화 없음 |
| **반박** | IGF-1R 자가항체 고역가가 오히려 GO 비발생/경증과 연관[N2, N3] | "IGF-1R 자가항체 → 병인 촉발"이라는 방향과 반대 |
| **반박** | 2025-2026 review 다수가 "IGF-1R은 신호복합체 구성요소/치료표적"으로만 서술, 독립 자가항원으로 격상하지 않음[N4, N5, N6, N9] | 학계 컨센서스가 B4 서술과 일치 |

## 4. 독립 섹션 신설 여부 판단 근거

- **신설 반대 근거**: (1) 신규 근거의 방향이 "IGF-1R 자가항체가 병인성"이라는 가설을 강화하지 않고 오히려 억제적 역할 쪽으로 쌓이고 있어, 독립 섹션이 다룰 만한 새로운 "확립되어 가는 기전"이 없음. (2) TSHR-IGF-1R crosstalk의 물리적/신호전달 측면은 이미 JHA-79로 별도 이슈가 배정되어 있어, 여기서 중복 서술하면 섹션 경계가 흐려짐(QA G1 유사 원칙 — 섹션 간 내용 분리). (3) 두 핵심 신규 연구[N2, N3] 모두 단일기관 cross-sectional, in-house assay 한계가 있어 field 전체가 "논쟁적(controversies)"이라고 스스로 규정하는 단계([N4] 제목 참조)이며 독립 섹션급 안정성에 도달하지 않음.
- **보강으로 충분한 근거**: B4는 이미 "세 가설 모두 활발히 연구 중이며 합의된 단일 기전은 없음"이라고 명시하고 있어, 새로운 하위 발견(자가항체는 존재하되 억제성)을 **세 번째 가설 항목에 한 문장 추가**하는 것만으로 최신성과 균형성 요건을 모두 충족할 수 있음.

## 5. B4 반영 제안 문안 (편집자 참고용, 최종본 반영 시 QA D2/F6 재확인 필요)

> 기존 B4 세 번째 bullet 뒤에 아래 문장 추가 권고:
>
> "— 이후 2025년 두 개의 독립 코호트 연구(Pisa, n=147[N2]; Katowice, n=67[N3])는 ELISA로 혈청 anti-IGF-1R 자가항체를 정량 측정한 결과, 이 항체가 GD 환자 일부에서 실제로 검출되나 **GO 발생 및 중증도와 역상관**하며 orbital fibroblast 증식을 억제하는 방향으로 작용함을 보고 — 이는 IGF-1R을 표적으로 하는 자가항체가 존재할 수 있음을 시사하는 동시에, 그 방향이 '자극성(stimulating)/병인성'이 아닌 **억제성/보호적**일 가능성을 제기하여 NIH 연구팀의 기존 결론[23]과 상충하지 않고 오히려 보완함. 단일기관 cross-sectional 설계로 'proposed' 수준의 근거이며 독립 재현이 필요함(QA D2/F6 대응)."

## 6. 남은 gap 및 후속 권고

- Lanzolla[N2]/Nowak[N3] 두 연구의 IGF-1RAb ELISA는 각 기관 in-house 구축으로 cut-off/표준화가 상이함 — 메타분석 또는 독립 재현 전까지 정량 수치를 report.md 본문에 절대치로 인용하지 않고 방향성(역상관)만 인용 권고.
- HPV 분자모방 가설[N8]은 n=22 exploratory 연구로, 필요 시 별도 Linear 이슈로 분리해 후속 검색 권고(현재 이슈 범위 외).
- JHA-79(TSHR-IGF1R crosstalk 딥다이브)에서 [21], [N1](Xiang 2026)을 상세 다룰 예정이므로 본 문서는 자가항원/자가항체 존재 여부에 초점을 유지함.

## 7. 참고문헌 (신규, 자체 번호 — 레거시 [21][22][23]과 별개)

- N1. Xiang P, Mezei M, Latif R, Davies TF. Stimulating Thyrotropin Receptor Antibodies Enhance the Expression of Both Thyrotropin Receptors and Insulin-Like Growth Factor 1 Receptors in Fibroblasts. *Thyroid.* 2026;36(8):903-911. PMID: [42374926](https://pubmed.ncbi.nlm.nih.gov/42374926/). doi: [10.1177/10507256261463222](https://doi.org/10.1177/10507256261463222).
- N2. Lanzolla G, Rotondo Dottore G, Comi S, et al. In vivo and in vitro evidence for a protective role of autoantibodies against the insulin-like growth factor-1 receptor (IGF-1R) in Graves' orbitopathy. *Endocrine.* 2025;89(1):137-142. PMID: [40156685](https://pubmed.ncbi.nlm.nih.gov/40156685/). doi: [10.1007/s12020-025-04219-6](https://doi.org/10.1007/s12020-025-04219-6).
- N3. Nowak M, Wielkoszyński T, Londzin-Olesik M, et al. Antibodies against the receptor for insulin-like growth factor 1 (IGF-1RAb), insulin-like growth factor 1 (IGF-1), and insulin-like growth factor binding protein 3 (IGFBP-3) in the serum of patients with Graves' and Basedow's disease with and without orbitopathy. *Endokrynol Pol.* 2025;76(1):40-51. PMID: [40071798](https://pubmed.ncbi.nlm.nih.gov/40071798/). doi: [10.5603/ep.102336](https://doi.org/10.5603/ep.102336).
- N4. Smith TJ. Controversies Surrounding IGF-I Receptor Involvement in Thyroid-Associated Ophthalmopathy. *Thyroid.* 2025;35(3):232-244. PMID: [39909461](https://pubmed.ncbi.nlm.nih.gov/39909461/). doi: [10.1089/thy.2024.0606](https://doi.org/10.1089/thy.2024.0606).
- N5. Smith TJ. TSHR-IGF-IR complex drives orbital fibroblast misbehavior in thyroid eye disease. *Curr Opin Endocrinol Diabetes Obes.* 2024;31(5):177-183. PMID: [39082947](https://pubmed.ncbi.nlm.nih.gov/39082947/). doi: [10.1097/MED.0000000000000878](https://doi.org/10.1097/MED.0000000000000878).
- N6. Lanzolla G, Marinò M, Menconi F. Graves disease: latest understanding of pathogenesis and treatment options. *Nat Rev Endocrinol.* 2024;20(11):647-660. PMID: [39039206](https://pubmed.ncbi.nlm.nih.gov/39039206/). doi: [10.1038/s41574-024-01016-5](https://doi.org/10.1038/s41574-024-01016-5).
- N7/N9. Wiersinga WM, Eckstein AK, Žarković M. Thyroid eye disease (Graves' orbitopathy): clinical presentation, epidemiology, pathogenesis, and management. *Lancet Diabetes Endocrinol.* 2025;13(7):600-614. PMID: [40324443](https://pubmed.ncbi.nlm.nih.gov/40324443/). doi: [10.1016/S2213-8587(25)00066-X](https://doi.org/10.1016/S2213-8587(25)00066-X).
- N8. Garg I, Meyer BI, Gallo RA, Wester ST, Pelaez D. Human Papillomavirus and Thyroid Eye Disease. *JAMA Ophthalmol.* 2025;143(6):524-528. PMC: [PMC12022865](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC12022865/). PMID: [40272832](https://pubmed.ncbi.nlm.nih.gov/40272832/). doi: [10.1001/jamaophthalmol.2025.0847](https://doi.org/10.1001/jamaophthalmol.2025.0847).
- 레거시 인용(재확인용, 번호는 `_shared/GD_TED_reference.md` 그대로): [21] Latif R, Mezei M, Davies TF. Mechanisms in Thyroid Eye Disease: The TSH Receptor Interacts Directly With the IGF-1 Receptor. *Endocrinology.* 2025;166(2). PMID: [39821041](https://pubmed.ncbi.nlm.nih.gov/39821041/). [22] Cui X, Wang F, Liu C. A review of TSHR- and IGF-1R-related pathogenesis and treatment of Graves' orbitopathy. *Front Immunol.* 2023;14:1062045. PMID: [36742308](https://pubmed.ncbi.nlm.nih.gov/36742308/). [23] Krieger CC, Neumann S, Gershengorn MC. Is There Evidence for IGF1R-Stimulating Abs in Graves' Orbitopathy Pathogenesis? *Int J Mol Sci.* 2020;21(18):6561. PMID: [32911689](https://pubmed.ncbi.nlm.nih.gov/32911689/).
