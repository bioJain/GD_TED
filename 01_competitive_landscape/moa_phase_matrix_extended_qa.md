---
linear_issue: JHA-73
created: 2026-09-29
source: biomni-qa
milestone: cluster-1-competitive-landscape
status: in-review
inputs:
  - 01_competitive_landscape/moa_phase_matrix_extended.md
  - _shared/GD_TED_qa_checklist.md
  - docs/repo_conventions.md
---

# moa_phase_matrix_extended.md 독립 QA 보고서

**QA 실행일:** 2026-09-29
**QA 대상:** `01_competitive_landscape/moa_phase_matrix_extended.md` (SHA 0c2c8a5)
**적용 체크리스트:** `_shared/GD_TED_qa_checklist.md`
**QA 성격:** 작성 세션과 분리된 독립 세션. 작성 과정의 프롬프트, 추론, 중간 draft는 제공되지 않았으며, 문서 자체와 1차 출처만 근거로 삼았다. 세션 분리와 독립성 전제(작성 과정 미제공)는 `repo_conventions.md` §QA 독립성 요건을 충족한다. 작성 세션의 모델/provider 정보는 제공되지 않았으므로, cross-model 검증 요건의 충족 여부는 작성 세션 기록 확인 전까지는 추정으로 기재한다.

## 1. 검증 방법

- 임상 phase/상태/적응증 판정은 ClinicalTrials.gov API v2 원문(`https://clinicaltrials.gov/api/v2/studies/{nctId}`)으로 직접 조회했으며, `designModule.phases`, `statusModule.overallStatus`, `conditionsModule.conditions`, `leadSponsor`, 개입명을 문자 그대로 인용했다. 조회 시점은 2026-09-29이다.
- 대상 문서의 frozen data cut은 2026-09-10이다. 본 QA의 live 조회와 cut 시점의 상태 차이는 불일치로 판정하지 않고, 상태가 한 방향으로만 진행했는지(진행 중 단계 상승, 종료 등)로 판정했다.
- 승인/규제 심사 상태는 FDA 원문(approval letter, 라벨), sponsor 공시(HKEX 공시, 보도자료)로 대조했다.
- 자산별 registry 전수 검색(`query.intr`)으로 문서에 인용되지 않은 추가 시험 존재 여부를 확인했다.
- 언어/형식 항목(H1-H3)은 문서 전문 대상 grep 및 수동 검토로 판정했다.

## 2. 체크리스트 항목별 판정

| 항목 | 판정 | 근거/코멘트 |
|---|---|---|
| A1 GD/TED 별개 구분 + 연관성 명시 | PARTIAL | GD와 TED를 별개 적응증으로 분리 판정하는 것은 본 문서의 핵심 방법이며 전체에서 일관된다("v2의 48개 자산은 trial_ids를 clinical_trials_v2.csv와 연결해 GD와 TED를 각각 판정"). 그러나 TED-GD 연관성 수치(~90-95%)에 대한 서술은 없다. 매트릭스 문서의 목적상 필수는 아니므로 report.md 계열 문서에서 확인할 사항으로 남긴다 |
| A2 TED 단독 발생 가능성 | N/A | 본 문서에 질환 개념 서술이 없다 |
| A3 GD 환자 중 TED 발생 비율 | N/A | 본 문서에 역학 서술이 없다 |
| B1 GD incidence/prevalence 근거 수준 | N/A | 역학 수치 미포함 |
| B2 TED epidemiology 표기 | N/A | 역학 수치 미포함 |
| B3 7MM 국가별 수치 출처 | N/A | 역학 수치 미포함 |
| B4 incidence/prevalence 구분 | N/A | 역학 수치 미포함 |
| C1 CAS 7점/10점 구분 | N/A | staging 서술 미포함 |
| C2 EUGOGO 3 tier | N/A | staging 서술 미포함 |
| C3 NOSPECS | N/A | staging 서술 미포함 |
| C4 GD 공식 staging 부재 명기 | N/A | staging 서술 미포함 |
| D1 TSAb/TBAb/neutral TRAb | N/A | 병리기전 서술 미포함. 다만 MER511을 "TSHR receptor 길항제가 아님"으로 정확히 구분한 것은 이 정신과 부합한다 |
| D2 TSHR-IGF-1R 복합체 가설 표현 | N/A | 병리기전 서술 미포함 |
| D3 fibroblast 운명 (Thy-1) | N/A | 병리기전 서술 미포함 |
| D4 RAI TED 악화 위험 | N/A | 치료 시술 서술 미포함 |
| D5 active/inactive cytokine milieu | N/A | 병리기전 서술 미포함. 다만 시험 분류에서 active/inactive TED를 구분한 것(MHB018A, KHN939, IBI311)은 이 구분과 정합적이다 |
| D6 흡연 = TED #1 modifiable risk factor | N/A | 위험요인 서술 미포함 |
| E1 Teprotumumab 승인일/적응증 | PASS | 본 문서는 "Teprotumumab (TED A)"로 표기. FDA approval letter(2020-01-21) 원문 "Tepezza is indicated for treatment of thyroid eye disease", 라벨 "Initial U.S. Approval: 2020"와 일치. 승인일 자체는 본 문서에 기재되지 않아 오류 소지 없음 |
| E2 Teprotumumab 청각 AE | N/A | AE 서술 미포함 |
| E3 IVMP 1차 SoC | N/A | SoC 서술 미포함 |
| E4 ATD 재발률 출처 | N/A | 해당 수치 미포함 |
| E5 RAI 후 prednisolone 권고 | N/A | 해당 서술 미포함 |
| E6 indication-specific 임상 단계 판정 | PASS | 지정 4개 상 tier claim(MER511, GenSci098/YB-101, KHN939, SCTT11)과 확장 검증한 승인/심사 자산(Teprotumumab, IBI311, Veligrotug, Satralizumab, Efgartigimod) 전부가 registry/규제 원문과 일치했다. 상세는 3절. §7의 PROVISIONAL을 해제할 수 있다 |
| E7 discontinued/NDR 자산 제외 | PASS | §5.1에 stopped/failed/suspended 10개, §5.2에 NDR/범위외 및 관찰 10개를 명시 보존. TED-terminated efgartigimod는 TED에서만 제외하고 GD P3는 본표 유지한 것이 registry 원문과 일치(NCT06307613/26 TERMINATED, NCT07570316/7596849 RECRUITING) |
| F1 모든 사실 claim에 [x] 인용 | PARTIAL | [x] 번호 인용은 없다. 대신 §6.1에 direct source 목록을 두고 본표에 trial ID를 병기했으며, 이는 repo_conventions.md 인용 규칙("신규 산출물은 본문에서 출처 파일명을 명시하고, 새 문헌은 문서 말미에 자체 참고문헌 목록을 둔다")과는 부합한다. checklist F1의 문언(번호 인용)과는 불일치이므로 PARTIAL로 기재하며, 번호 체계 통합은 conventions이 별도 작업으로 규정한 사항이다 |
| F2 [x] 번호와 reference.md 일치 | N/A | 번호 인용 체계를 사용하지 않는다 |
| F3 reference.md 중복 항목 | N/A | 본 문서는 reference.md를 인용 대상으로 하지 않는다 |
| F4 PMID 5개 이상 실존 검증 | PARTIAL | PMID 인용이 없어 검증 대상이 없다. 대신 §6.1의 source URL 5건 전부를 본 QA에서 live 재확인했으며 모두 실존하고 내용이 문서 서술과 일치했다(3절 인용 참조) |
| F5 마케팅 언어 | PASS | "revolutionary", "breakthrough", "game-changing", "혁신적", "획기적" 등의 표현이 전문에서 검출되지 않았다 |
| F6 근거 수준 표현 | PASS | 불확실한 판정에 "관찰 목록"(K1-70, ZB001, LASN01, Aflibercept, Lonigutamab), "PENDING"(§6.2), "PROVISIONAL"(§7) 등 근거 수준을 명시했다 |
| G1 eTPD Section E 한정 | N/A | 본 문서에 eTPD 서술이 없다. 분리 원칙 위반 없음 |
| G2 eTPD speculative 항목 근거 수준 | N/A | eTPD 서술 없음 |
| G3 FcRn vs eTPD 차별화 | N/A | eTPD 서술 없음. 다만 FcRn 억제(Efgartigimod, IMVT-1402)와 anti-TSHR AAb 제거(MER511), pan-IgG 제거(BHV-1300)를 별개 MoA class로 분리한 것은 차별화 관점과 정합적이다 |
| H1 영문 기술 용어 유지 | PASS | TSHR, IGF-1R, FcRn, BTK, JAK, mTOR, CAR-T, LYTAC, MoDE, CD40L, BCMA 등이 영문으로 유지되었다 |
| H2 가운뎃점 미사용 | PASS | 전문 grep 결과 가운뎃점이 검출되지 않았다 |
| H3 개조식(명사 종결형) 문체 | PARTIAL | 표와 단계 표기는 개조식이나, 서술부(§1 판정 방법, 판정 메모)가 "~사용했다", "~분리했다" 식의 평서형 종결이다. checklist 문언(명사 종결형)과 문자적으로는 불일치하나, 표 중심 문서에서 가독성 문제는 없다. 심각도 낮음 |

**판정 요약:** PASS 8, PARTIAL 4 (A1, F1, F4, H3), FAIL 0, N/A 18. FAIL 없음. PARTIAL 4건은 모두 본 문서의 문서 유형(매트릭스)이 checklist 원래 대상(report.md)과 다른 데서 오는 것으로, 데이터 정확성 결함이 아니다.

## 3. Tier-상 claim별 cross-confirm 결과

### 3.1 지정 4개 claim

**Claim 1. MER511: GD Phase 1, TED 임상 단계 없음 — 기존 판정과 일치 (CONFIRMED)**

- Source: https://clinicaltrials.gov/study/NCT07305818
- Registry direct quote (officialTitle): "A Phase 1, First-in-Human, Placebo-Controlled, Single and Multiple Ascending Dose Study to Evaluate Safety, Tolerability, Pharmacokinetics, Pharmacodynamics, and Immunogenicity of Intravenous and Subcutaneous Administration of MER511 in Adults With Graves' Disease"
- Registry direct quote (phases): `PHASE1` / (overallStatus): `RECRUITING` / (conditions): `["Graves Disease"]` / (leadSponsor): `Merida Biosciences`
- TED 임상 단계 없음 근거: `query.intr=MER511` 전수 검색에서 MER511 시험은 NCT07305818 1건뿐이다. condition에 TED가 없다.
- Sponsor 원문 (https://meridabio.com/pipeline-programs/): "Merida is developing MER511, a precision biologic designed to selectively eliminate pathogenic autoantibodies and their B-cell sources while preserving normal immune function." / "MER511 is being evaluated in the NEXUS Phase 1 Study for the treatment of Graves' disease." / pipeline heading "Graves' disease and thyroid eye disease (TED)" — 문서의 "회사 pipeline은 GD/TED를 함께 명시, 임상은 GD만" 판정과 정확히 일치한다.
- MoA class (anti-TSHR AAb 제거)도 sponsor 문언과 일치하며, receptor 길항제가 아닌 판정은 타당하다.

**Claim 2. GenSci098/YB-101: GD Phase 2, TED Phase 1 — 기존 판정과 일치 (CONFIRMED)**

- GD Source: https://clinicaltrials.gov/study/NCT07682896
- Registry direct quote (briefTitle): "Evaluation of YB-101 for Safety, Tolerability, Pharmacokinetics, and Efficacy in Graves' Disease" / (phases): `PHASE2` / (overallStatus): `RECRUITING` / (conditions): `["Graves' Disease"]` / (leadSponsor): `Yarrow Bioscience, Inc.`
- TED Source: https://clinicaltrials.gov/study/NCT06569758
- Registry direct quote (officialTitle): "A Phase 1 Clinical Study to Evaluate the Safety, Tolerability, Pharmacokinetics, and Pharmacodynamics of Single and Multiple Ascending Subcutaneous Doses of GenSci098 in TED Patients" / (phases): `PHASE1` / (overallStatus): `RECRUITING` / (conditions): `["Safety", "Tolerability", "GenSci098", "Thyroid Eye Disease (TED)"]` / (leadSponsor): `Changchun GeneScience Pharmaceutical Co., Ltd.`
- 적응증별 최고 active 단계 분리(GD P2 / TED P1)는 두 원문과 일치한다.
- 보완 사항(판정 불변): `query.intr=GenSci098` 검색에서 문서에 인용되지 않은 추가 시험 NCT07286656 "A Study of GensSci098 in Subjects With Graves' Disease"(`PHASE1`, `RECRUITING`, Changchun GeneScience)이 확인되었다. GD 최고 active 단계는 P2이므로 매트릭스 판정은 변하지 않으나, 핵심 trial ID 열에 NCT07286656을 병기하는 것을 권고한다.

**Claim 3. KHN939: TED Phase 3 — 기존 판정과 일치 (CONFIRMED)**

- Source: https://clinicaltrials.gov/study/NCT07720635 , https://clinicaltrials.gov/study/NCT07720648
- Registry direct quote (NCT07720635 briefTitle): "A Phase III Study of KHN939 in Chinese Patients With Moderate-to-Severe Active Thyroid Eye Disease" / (phases): `PHASE3` / (overallStatus): `NOT_YET_RECRUITING` / (conditions): `["Thyroid Eye Disease"]`
- Registry direct quote (NCT07720648 briefTitle): "A Phase III Study of KHN939 in Chinese Patients With Moderate-to-Severe Inactive Thyroid Eye Disease" / (phases): `PHASE3` / (overallStatus): `NOT_YET_RECRUITING` / (conditions): `["Thyroid Eye Disease"]`
- (leadSponsor, 양쪽 공통): `Chengdu Kanghong Pharmaceutical Group Co., Ltd.`
- TED P3 판정은 원문과 일치한다. intervention은 "KHN939", "Placebo"뿐이므로 표적 미공개 유지 판정도 타당하다.
- 교정 제안: 개발사 열의 "registry sponsor"는 실제 leadSponsor인 "Chengdu Kanghong Pharmaceutical Group Co., Ltd."로 명시할 것을 권고한다.

**Claim 4. SCTT11: TED Phase 1/2 — 기존 판정과 일치 (CONFIRMED)**

- Source: https://clinicaltrials.gov/study/NCT06769984
- Registry direct quote (officialTitle): "A Multicentre, Randomized, Double-blinded, Placebo-controlled Phase I/II Clinical Study to Evaluate the Safety, Tolerability, Pharmacokinetics, Pharmacodynamics, and Efficacy of SCTT11 in Healthy Participants and Participants with Moderate-to-severe Thyroid Eye Disease" / (phases): `["PHASE1", "PHASE2"]` / (overallStatus): `NOT_YET_RECRUITING` / (conditions): `["TED"]` / (leadSponsor): `Sinocelltech Ltd.`
- TED P1/2 판정은 원문과 일치한다. 표적 미공개 유지도 타당하다(intervention은 "SCTT11", "Placebo"뿐).
- 교정 제안: 개발사 열의 "registry sponsor"는 "Sinocelltech Ltd."로 명시할 것을 권고한다.

### 3.2 확장 검증: 승인/규제 심사 자산

**Claim 5. Teprotumumab: TED Approved — 기존 판정과 일치 (CONFIRMED)**

- Source: https://www.accessdata.fda.gov/drugsatfda_docs/appletter/2020/761143Orig1s000ltr.pdf , https://www.accessdata.fda.gov/drugsatfda_docs/label/2020/761143s000lbl.pdf
- FDA approval letter direct quote (2020-01-21): "We have approved your BLA for Tepezza (teprotumumab-trbw) effective on the date of this letter ... Tepezza is indicated for treatment of thyroid eye disease."
- Label direct quote: "TEPEZZA (teprotumumab-trbw) for injection, for intravenous use Initial U.S. Approval: 2020" / "TEPEZZA is an insulin-like growth factor-1 receptor inhibitor indicated for the treatment of Thyroid Eye Disease"
- Registry 보조: NCT03298867 (pivotal, `PHASE3`, `COMPLETED`, conditions `["Thyroid Eye Disease", "Graves' Orbitopathy"]`), NCT06248619 (SC 후속, `PHASE3`, `ACTIVE_NOT_RECRUITING`). 문서가 승인 후 Phase 3/SC 연구를 Approved 셀에 중복 계수하지 않은 판정도 정합적이다.

**Claim 6. IBI311: TED Approved (중국) — 기존 판정과 일치 (CONFIRMED)**

- Source: https://www.hkexnews.hk/listedco/listconews/sehk/2025/0314/2025031400313.pdf (Innovent HKEX 공시, 2025-03-14)
- Direct quote: "the new drug application ('NDA') of SYCUME (teprotumumab N01 injection), a recombinant anti-insulin-like growth factor 1 receptor ('IGF-1R') monoclonal antibody), received approval by the National Medical Products Administration of China ('NMPA') for the treatment of thyroid eye disease ('TED')."
- IBI311 = SYCUME (teprotumumab N01) 동일성: Antibody Society DB(https://db.antibodysociety.org/db0/763/)가 "INN: Teprotumumab N01 / Drug code(s): IBI311 / Brand name: SYCUME / Company: Innovent Biologics (Suzhou) Co. Ltd."로 확인. 승인 근거 시험은 RESTORE-1(CTR20223393)로 IBI311 Phase 3와 일치한다.
- Registry 보조: NCT05795621 (active TED, `PHASE2`+`PHASE3`, `COMPLETED`), NCT07113262 (inactive TED, `PHASE3`, `RECRUITING`). 문서의 "active/inactive TED 시험 모두 존재" 서술과 일치한다.

**Claim 7. Veligrotug/Lumvoa: TED Approved (미국) — 기존 판정과 일치 (CONFIRMED)**

- Source: https://investors.viridiantherapeutics.com/news/news-details/2026/Viridian-Therapeutics-Announces-U-S--FDA-Approval-and-Launch-of-Lumvoa-veligrotug-vvze-for-the-Treatment-of-Thyroid-Eye-Disease/default.aspx (2026-06-26)
- Direct quote: "Viridian Therapeutics ... today announced that the U.S. Food and Drug Administration (FDA) has approved Lumvoa (veligrotug-vvze) for the treatment of thyroid eye disease (TED)."
- 보조: FDA BLA 문서(https://www.accessdata.fda.gov/drugsatfda_docs/nda/2026/761530Orig1s000OtherR.pdf) "Veligrotug (VRDN-001) ... under BLA 761530 ... full antagonist of IGF-1R".
- Registry 보조: NCT05176639 (active TED, `PHASE3`, `COMPLETED`), NCT06021054 (chronic TED, `PHASE3`, `COMPLETED`). v2 cut(2026-09-10)은 승인(2026-06-26) 이후이므로 "v2 cutoff 승인 상태 사용" 서술도 시점상 타당하다.

**Claim 8. Satralizumab: TED Regulatory review — 기존 판정과 일치 (CONFIRMED)**

- Source: https://www.gene.com/media/press-releases/15118/2026-06-29/fda-grants-priority-review-to-genentechs , https://www.roche.com/media/releases/med-cor-2026-06-30
- Direct quote: "the U.S. Food and Drug Administration (FDA) has accepted and granted priority review to a supplemental Biologics License Application (sBLA) for Enspryng (satralizumab) for the treatment of thyroid eye disease (TED). ... The FDA is expected to make a decision on approval by October 15, 2026."
- 2026-09-29 기준 승인되지 않았으므로 "TED RR(Regulatory review)", "v2 cutoff에 TED 승인 아님" 표기는 정확하다.
- Registry 보조: NCT05987423, NCT06106828 (SatraGO-1/2, 모두 `PHASE3`, `COMPLETED`, conditions `["Thyroid Eye Disease"]`).

**Claim 9. Efgartigimod PH20 SC: GD P3 active / TED P3 terminated 분리 — 기존 판정과 일치 (CONFIRMED)**

- GD Source: https://clinicaltrials.gov/study/NCT07570316 , https://clinicaltrials.gov/study/NCT07596849
- Registry direct quote (officialTitle): "A Phase 3, Randomized, Double-Masked, Placebo-Controlled, Multicenter Study Evaluating the Efficacy and Safety of Efgartigimod PH20 SC PFS in Adult Participants With Graves' Disease Inadequately Controlled With Antithyroid Drugs" / (phases): `PHASE3` / (overallStatus): `RECRUITING` / (conditions): `["Graves' Disease", "Graves Disease"]` (NCT07570316), `["Graves Disease"]` (NCT07596849)
- TED Source: https://clinicaltrials.gov/study/NCT06307613 , https://clinicaltrials.gov/study/NCT06307626
- Registry direct quote (officialTitle): "A Phase 3, Randomized, Double-Masked, Placebo-Controlled, Multicenter Study to Evaluate the Efficacy, Safety, Tolerability, Pharmacokinetics, Pharmacodynamics, and Immunogenicity of Efgartigimod PH20 SC Administered by Prefilled Syringe in Adult Participants With Thyroid Eye Disease" / (phases): `PHASE3` / (overallStatus): `TERMINATED` / (conditions): `["Thyroid Eye Disease"]`
- Highest Status trap 처리(GD는 본표, TED는 부표)는 원문과 일치한다.

**Claim 10. BHV-1300: pan-IgG 제거 class, GD P3 — 기존 판정과 일치 (CONFIRMED)**

- Source: https://www.biohaven.com/pipeline/
- Direct quote: "BHV-1300 ... INDICATION: Common Disease (Graves', RA) ... PHASE 3 ... Therapeutic pan-IgG depletion using Biohaven's proprietary MoDE platform technology ..."
- anti-TSHR 선택적 자산이 아니라는 class 분리 판정은 sponsor 문언과 일치한다.

**Claim 11. BHV-1440: TSHR AAb Degrader, GD/TED, preclinical — 기존 판정과 일치 (CONFIRMED)**

- Source: https://www.biohaven.com/pipeline/
- Direct quote: "TSHR AAb Degrader ... Graves' Disease and TED ... BHV-1440" (phase 축에서 preclinical 위치)
- registry ID 없음 표기와 PC 판정은 정합적이다.

## 4. 기존 판정과의 일치 여부 요약

| claim | 문서 기존 판정 | 독립 QA 결과 | 일치 여부 |
|---|---|---|---|
| MER511 GD P1, TED 임상 단계 없음 | §3.1, §6 | GD P1 recruiting, MER511 시험 1건(GD) 전수 확인 | 일치 |
| MER511 MoA/class | §6 anti-TSHR AAb 제거 | sponsor 문언과 일치 | 일치 |
| GenSci098/YB-101 GD P2 / TED P1 | §3.1, §6 | 두 registry 원문과 일치 | 일치 (trial ID 보완 권고) |
| KHN939 TED P3, 표적 미공개 | §3.2, §6 | 두 registry 원문과 일치 | 일치 (개발사 명시 권고) |
| SCTT11 TED P1/2, 표적 미공개 | §3.2, §6 | registry 원문과 일치 | 일치 (개발사 명시 권고) |
| Teprotumumab TED Approved | §3.2 | FDA 원문과 일치 | 일치 |
| IBI311 TED Approved (중국) | §3.2 | NMPA 승인 공시와 일치 | 일치 |
| Veligrotug/Lumvoa TED Approved (미국) | §3.2 | FDA 승인 보도자료와 일치 | 일치 |
| Satralizumab TED RR | §3.2 | FDA priority review 원문과 일치 | 일치 |
| Efgartigimod GD P3 / TED terminated 분리 | §3.1, §5.1 | 4개 registry 원문과 일치 | 일치 |
| BHV-1300 pan-IgG / BHV-1440 TSHR AAb degrader | §3.1, §6 | sponsor pipeline과 일치 | 일치 |
| §7 E6 PROVISIONAL | §7 | 본 QA 범위의 주요 상 tier phase claim 확인 | 대조 범위 PASS. 작성 모델/provider 미확인으로 cross-model 충족은 별도 확인 필요 |
| §7 E7 PASS | §7 | 부표 보존 확인 | 일치 |

## 5. 최초 QA 교정안 (필수 사항 없음, 권고 3건)

1. **GenSci098/YB-101 행 핵심 trial ID 보완:** NCT07286656(GenSci098 GD P1, recruiting)을 병기 권고. GD 최고 active 단계 판정(P2)은 불변이다.
2. **KHN939, SCTT11 개발사 명시:** "registry sponsor"를 각각 "Chengdu Kanghong Pharmaceutical Group Co., Ltd.", "Sinocelltech Ltd."로 교체 권고. registry leadSponsor 필드 근거이다.
3. **(선택) H3 문체:** 서술부를 명사 종결형으로 통일. 심각도 낮음.

최초 QA 시점에는 매트릭스 본표의 단계/상태 데이터에 대한 교정 필요 사항이 없었다. 위 권고는 데이터 판정을 바꾸지 않는 완전성/가독성 개선이며, 2026-09-30 후속 review 반영 결과는 7절에 기록한다.

## 6. 검증 일자 및 한계

- **검증 일자:** 2026-09-29 (ClinicalTrials.gov API v2 live 조회, FDA/sponsor 원문 확인)
- 본 QA는 live registry 조회이므로 문서의 frozen cut(2026-09-10) 이후 상태 변화를 포함한다. 모든 차이가 확인되었고 단계 판정을 뒤집는 변화는 없었다.
- Cortellis 기반 legacy-only preclinical 자산(CRN-12755, ETHY-001, REGN-24493, SP-1351, VBS-102, BHV-1440 등)의 원표는 공개 출처로 재전재할 수 없어, 이 중 BHV-1440만 sponsor pipeline으로 검증했다. 나머지는 본 QA의 registry 검증 범위 밖이다.
- CTIS 기반 LCA-0321(CTIS 2025-524053-14-00)은 본 QA에서 CTIS 원문 재확인을 하지 못했다. 문서 표기는 입력 자료와 일치했으나 1차 원문 대조는 미수행이다.
- 승인 상태는 규제 당국 원문 또는 회사 공시를 기준으로 하며, 중국 NMPA의 경우 공시문 원문으로 대신했다.


## 7. 2026-09-30 후속 review 반영

- GenSci098/YB-101 행에 NCT07286656을 추가하고, KHN939/SCTT11의 registry lead sponsor를 명시해 5절의 권고 1, 2를 반영했다.
- `COMPLETED`만 있고 후속 active 개발이 확인되지 않은 K1-70과 ZB001을 active 한 장 매트릭스/상세표에서 5.2절 관찰 목록으로 이동했다. 이는 1절의 completed-only 처리 원칙과 본표를 일치시킨 교정이다.
- 작성 세션의 모델/provider가 확인되지 않았으므로 독립 세션 실행 사실과 cross-model 요건 충족을 구분했다. 또한 6절의 한계대로 legacy-only 자산과 LCA-0321의 1차 원문 직접 대조는 미완료 상태로 유지한다. 따라서 JHA-73 QA gate는 이 두 항목이 해소될 때까지 열어 둔다.
