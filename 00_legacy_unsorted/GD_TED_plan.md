---
name: GD_TED_plan
description: Graves' Disease & TED comprehensive analysis plan — 역학/병리기전/치료법 3섹션 구조, Global+7MM 역학, preclinical 포함 전체 active 파이프라인, eTPD 별도 섹션 (Section E)
sources: [chat]
aliases: [Graves TED plan, GD TED analysis plan, 6T review GD TED]
---

# Graves' Disease & Thyroid Eye Disease (TED) — Comprehensive Analysis Plan

> 작성일: 2026-09-11  
> Plan 세션 확정; 실행은 별도 Work 세션  
> 확정 파라미터: Global+7MM 역학 | Preclinical 포함 전체 active 파이프라인 (discontinued/NDR 제외) | 중립 본문 + eTPD 시사점 별도 섹션 (Section E)

---

## 1. 분석 목표 및 범위

### 1.1 대상 질환 (각각 독립 분석 + 연관성 명시)

- **Graves' Disease (GD)**: TSHR 자가항체(TSAb/TRAb) 매개 자가면역 갑상선기능항진증 — 가장 흔한 자가면역 갑상선 질환
- **Thyroid Eye Disease (TED, Graves' Ophthalmopathy/GO)**: 안와 섬유모세포/지방조직을 표적으로 하는 자가면역 안와병증 — ~90-95%가 GD 맥락에서 발생하나 독립 경과 가능

### 1.2 분석 영역 (5개 섹션)

| 섹션 | 내용 |
|---|---|
| **Section A** | Epidemiology & Clinical Characterization |
| **Section B** | Molecular & Pathobiological Mechanism |
| **Section C** | Therapeutic Landscape (SoC, approved, pipeline) |
| **Section D** | Key Clinical Trials to Follow |
| **Section E** | eTPD Implications (**중립 본문과 분리된 별도 섹션**) |

### 1.3 확정 파라미터

- **역학 지역**: Global + 7MM (US, DE, FR, UK, IT, ES, JP); 한국 데이터 가용 시 별도 기재
- **파이프라인 범위**: Preclinical 포함 전체 active — discontinued/NDR 제외 (본 작업 명시 기준; 기존 landscape 원칙과 다름)
- **eTPD 관점**: Section E에만 집약 — Section A-D 본문에 eTPD 언급 삽입 금지

---

## 2. 산출물 파일 구조

| 파일명 | 목적 | 생성 주체 |
|---|---|---|
| `GD_TED_plan.md` (본 파일) | 작업 전체 계획서 | Plan 세션 (완료) |
| `GD_TED_execution_log.md` | 도구 호출/실패-mitigation/시간별 수행 내역 — 추적/재현성 확보 | Work 세션 첫 단계에서 생성 |
| `GD_TED_reference.md` | 참고문헌 목록 — [x] 번호 부여; report와 numbering 일치 | Work 세션에서 누적 작성 |
| `GD_TED_report.md` | 본문 보고서 — in-line citation [x]; Section A-E 구조 | Work 세션 최종 통합 |
| `GD_TED_qa_checklist.md` | QA agent용 검토 목록 — 본 계획서 §6에서 도출 | Work 세션 첫 단계에서 초기화 후 QA 세션 공급 |

**저장 위치**: `/projects/019ff321-e837-70af-bff8-3eadcbf93ece/` 하위 — 모든 파일 동일 경로

---

## 3. 데이터 소스 계획

| 소스 | 활용 목적 | 우선순위 |
|---|---|---|
| **PubMed** | 역학 원문; 병리기전 review; 임상 RCT 결과 | 최우선 |
| **ClinicalTrials.gov** | Active 파이프라인 NCT 확인; trial 설계/endpoint 검증; status 교차확인 | 최우선 |
| **Consensus / Elicit** | Systematic review 탐색; high-quality epi 문헌 발굴 | 1차 보완 |
| **Web search (fast/standard)** | 최신 press release; 아직 PubMed 미색인 데이터; FDA/EMA 공식 문서 | 실시간 보완 |
| **AdisInsight** | Pipeline 검증 — preclinical 포함 회사/MoA/phase 분류 | Pipeline 1차 소스 |
| **Open Targets** | TSHR, IGF1R, FCGRT(FcRn) 연관 genetic/expression data | Mechanism 보완 |
| **ChEMBL** | Small molecule IGF-1R inhibitor (linsitinib 등) 특성 확인 | 필요 시 |
| **FDA/EMA 공식 라벨** | Teprotumumab (TEPEZZA) — 승인 기반 근거 정확성 확보 | 치료제 섹션 |

---

## 4. 연구 질문 목록 (섹션별 구조화)

### Section A — Epidemiology & Clinical Characterization

**A1. 질환 정의**
- GD: 병태생리 본질; TSHR 자가항체의 역할; 갑상선 외 manifestation과의 관계
- TED: 안와 조직 변화의 본질; GD와 관계 (temporal relationship 포함); 독립 경과 빈도

**A2. Incidence / Prevalence**
- GD: 연간 incidence (/100,000); prevalence (Global, 7MM 국가별); 성별/연령 분포
- TED: GD 환자 내 발생 비율; 임상적 유의 TED vs. sight-threatening TED 비율 구분
- 7MM 국가별 편차 요인 (요오드 섭취량, 인종, screening 수준)

**A3. 증상**
- GD: 갑상선기능항진 증상 (심계항진, 체중감소, 열불내성, 발한 등); 갑상선종; 피부/조갑 변화 (pretibial myxedema, onycholysis)
- TED: 안와 증상 (proptosis, diplopia, 결막부종, 각막노출, 시신경병증); 증상 스펙트럼 (mild lid lag → sight-threatening)
- 두 질환 증상의 시간적 관계 — 동시/순차/독립 발현 패턴

**A4. Life-threatening Potential**
- GD: Thyroid storm — 정의; 촉발 인자 (수술, 감염, 조영제); 사망률
- TED: Dysthyroid Optic Neuropathy (DON) — 비율; 영구 시력 손실 위험; Corneal ulceration/perforation 위험

**A5. 진단**
- GD: TFTs (TSH 억제, FT4/FT3 상승); TRAb/TSAb 검사 (assay 종류 및 특이도); 방사성 요오드 섭취율; 갑상선 초음파
- TED: 임상 진단 (CAS 적용); NOSPECS 분류; CT/MRI 안와 영상; 완전한 안과 검사 배터리 (visual acuity, perimetry, Hertel exophthalmometry)
- 감별진단 — TED vs. 다른 orbital pathology

**A6. Staging & Severity Classification**
- GD: 공식 staging system 부재 여부 명시; TFT 기반 severity; TRAb 수치 연속 변수로 활용; 갑상선종 크기 (WHO grading)
- TED:
  - **NOSPECS**: class 0-6 정의 및 각 임상적 의미
  - **EUGOGO**: mild / moderate-to-severe / sight-threatening — 각 기준 구체적 수치 포함
  - **CAS (Clinical Activity Score)**: 7점 (첫 방문) vs. 10점 (추적) 체계; active (CAS ≥3) 판정 기준; 치료 반응 예측 가치

**A7. Severity 상승 기준 (Progression Indicators)**
- TED: CAS 상승; proptosis ≥2mm 증가 (6개월 내); diplopia 악화; 시력 저하; corneal exposure 증가
- GD: ATD 불응/재발; TRAb 고지속; 갑상선 증가; 심방세동/골감소증 합병

---

### Section B — Molecular & Pathobiological Mechanism

**B1. 유전적 요인**
- HLA class II (DRB1*03:01, DQA1*05:01 등) 연관성 — 강도 및 인종별 편차
- Non-HLA loci: PTPN22 (R620W), CTLA4, CD40, FOXP3, FCRL3, thyroglobulin (TG), TSHR 유전자 다형성
- GD 발병 특이 vs. TED 중증도 특이 유전 요인 구분 (데이터 존재 시)
- 쌍둥이 연구: 유전성 기여도 추정값

**B2. 환경적 요인**
- 흡연: TED #1 modifiable risk factor; 용량-반응 관계; 메커니즘 (직접 oxidative stress; 간접 HLA-DR 발현 자극; 혈류 저산소)
- 요오드: 과잉 섭취 → GD 발병 위험 (Jod-Basedow effect)
- 스트레스/감염: molecular mimicry (Yersinia enterocolitica TSHR homology 포함)
- 산후 발병: postpartum thyroiditis와 true GD onset 구분
- **RAI → TED 악화 위험**: 치료 선택 시 핵심 변수 (흡연 동반 시 위험 증가)
- 셀레늄 결핍: TED 중증도 연관

**B3. GD 핵심 발병 기전**
- TSHR 중추 자가항원 — 관용(tolerance) 붕괴 기전
- B cell → plasma cell → TSAb (주로 IgG1/IgG4) 생산 경로
- TSAb의 TSHR 결합: Gs-coupled → cAMP/PKA → 갑상선호르몬 합성/분비 자극 (생리적 TSH 수용체 역할 대체)
- TRAb 스펙트럼: TSAb (stimulating) / TBAb (blocking) / neutral — 각 임상적 의미 및 assay 구분
- T cell help: Tfh (follicular helper T) 역할; Th2 → B cell 활성화; Treg dysfunction
- 림프구 침윤 패턴 — 갑상선 내 lymphoid follicle 형성

**B4. TED 발병 기전**
- TSHR 안와 섬유모세포(orbital fibroblast) 발현: low-level; cAMP 매개 hyaluronan synthase 유도
- IGF-1R 공동 수용체 역할:
  - TSHR-IGF-1R 막 내 signalosome 형성 가설 — 현재 논쟁 상태 명시 필요
  - IGF-1R 경유 PI3K/AKT; MAPK 활성화 → fibroblast 증식/분화
  - GD-IgG의 IGF-1R 교차활성화 여부 — 확립된 사실 vs. 가설 구분
- 안와 fibroblast 두 운명 (Thy-1 기준):
  - Thy-1+ (CD90+): myofibroblast 분화 → 섬유화 → 근육 비대
  - Thy-1- (CD90-): 지방세포 분화 (adipogenesis) → 안와 지방 증가
- Hyaluronan/glycosaminoglycan 과생산 → 삼투압 → 안와 조직 팽창
- Cytokine milieu 상 phase dependency:
  - Active phase (CAS ≥3): Th1 dominant (IL-1β, TNF-α, IFN-γ, IL-6) — 염증/부종
  - Inactive/fibrotic phase: Th2/TGF-β dominant (IL-4, IL-5, IL-13) — 섬유화 고착
- T cell trafficking: CD4+ Th1 초기 염증 주도; mast cell, macrophage 참여

**B5. 발병 vs. 진행 드라이버**
- 발병: 초기 TSAb titer; TSHR epitope 노출; 유전적 배경
- 진행: 흡연; RAI 치료; IGF-1R 상향조절; Th1/Th2 balance shift; 국소 ROS; TSAb 고지속
- Inactive phase 전환: fibrosis 고착; adipocyte remodeling 완료 — 이후 anti-inflammatory 치료 효과 감소

---

### Section C — Therapeutic Landscape

**C1. GD SoC (Graves' Hyperthyroidism)**
- **Anti-thyroid drugs (ATD)**: methimazole (MMI)/carbimazole (CMZ), propylthiouracil (PTU)
  - 기전: thyroid peroxidase 억제 → 갑상선호르몬 합성 차단
  - 반응률; 재발률 (~50% at 18개월 — 수치 출처 요구); 부작용 (agranulocytosis ~0.2-0.5%, hepatotoxicity PTU 특이)
  - 임신 중 선택 기준: PTU 1st trimester; MMI/CMZ 2nd/3rd trimester
  - 장기 ATD (LDAT): 재발 감소 근거 검토
- **Radioactive iodine (RAI, I-131)**: 갑상선 파괴적 치료; 가임 여성 제한; **TED 악화 위험** — prednisolone 예방 투여 기준
- **Thyroidectomy**: 즉각 euthyroid; TED에 미치는 영향 (RAI vs. surgery)

**C2. TED SoC**
- **IV methylprednisolone (IVMP)**: active TED 1차 치료 (EUGOGO guideline); 누적 용량 한계 (≤8g); 반응률 및 재발
- **Orbital decompression surgery**: sight-threatening TED (DON); cosmetic; sequence (decompression → strabismus → lid) 원칙
- **Orbital irradiation**: moderate-to-severe active TED — 보조 요법; 근거 수준
- **Selenium supplementation**: mild TED (EUGOGO 권고) — 근거 등급 명시 (RCT COSMOS study 등)

**C3. Approved Targeted Therapy**
- **Teprotumumab (TEPEZZA, Horizon Therapeutics/Amgen)**:
  - MoA: IGF-1R 단클론 항체 길항제
  - 승인: FDA 2020년 1월 (moderate-to-severe active TED)
  - 핵심 임상: Phase 2 RCT (NCT01943578) + OPTIC Phase 3 (NCT03298867); OPTIC-X extension (NCT03461783)
  - 결과: proptosis response (≥2mm 감소); CAS response; QoL (GO-QoL); 재발률; re-treatment 데이터
  - 주요 AE: 청각 관련 (hyperacusis, tinnitus, sensorineural hearing loss — 빈도 및 reversibility); 혈당 상승; 근경련; 탈모
  - 당뇨 환자 IGF-1R 차단 영향; 임신 금기 명시

**C4. Active Pipeline (Preclinical 포함 전체 active, discontinued/NDR 제외)**

MoA class별 분류:

| MoA Class | 분자 타겟 | 대표 자산 (탐색 대상) |
|---|---|---|
| IGF-1R inhibitor (small molecule) | IGF-1R TK | Linsitinib (OSI-906) |
| FcRn inhibitor | FCGRT → IgG 반감기 단축 → TSAb 감소 | Batoclimab (RVT-1401); Rozanolixizumab; Efgartigimod (argenx); Nipocalimab (J&J) |
| Anti-CD20 | B cell/plasma cell 고갈 | Rituximab; Obinutuzumab |
| IL-6 / IL-6R | Th1 cytokine 차단 | Tocilizumab |
| CD40 / CD40L | B-T cell co-stimulation 차단 | Iscalimab |
| TSHR antagonist Ab | TSHR direct blocking | K1-70 |
| IGF-1R Ab (non-teprotumumab) | IGF-1R | 추가 탐색 |
| Other/preclinical | TBD | — |

→ 각 자산별 수집 항목: 개발사; 현재 임상 단계 (indication-specific, Highest Status trap 주의); 적응증 (GD/TED 구분); 핵심 trial NCT; 반응 데이터 (가용 시 — proptosis, CAS, TRAb titer); 안전성 프로파일

**C5. 반응/내구성/안전성 비교**
- 반응률 정의 통일: proptosis 기준 vs. CAS 기준 vs. QoL (GO-QoL) 기준 — 비교 시 동일 기준 사용
- Durability: teprotumumab post-treatment relapse data; FcRn inhibitor IgG recovery kinetics (반등 시점)
- Safety comparison table (teprotumumab vs. IVMP vs. rituximab vs. FcRn inhibitors)

**C6. Unmet Needs**
- Teprotumumab 이후 미충족:
  - 고비용; 재발 (~25%); 청각 AE 빈도 및 영구 손상 위험
  - Inactive TED: approved systemic therapy 전무
  - TRAb 음성 TED (~5-10%): 진단 및 타겟 불명확
- GD 갑상선 치료 미충족:
  - ATD 재발 후 장기 관리 옵션 (수술/RAI 이외)
  - 관해 예측 biomarker 부재
  - 임신 중 안전 장기 옵션 부재
- 공통 미충족: TED 진행 예측 biomarker; active-to-inactive 전환 시점 예측

---

### Section D — Key Clinical Trials to Follow

각 시험별 수집 항목:
- NCT ID / 시험명; 개발사; Phase; 대상 (GD vs. TED; active vs. inactive); Primary endpoint; 예상 readout 시점; **팔로업 이유** (mechanistic or regulatory significance)

우선 탐색 대상:
1. **Batoclimab (RVT-1401)** — FcRn/TED Phase 2/3 (Immunovant/Roivant)
2. **Rozanolixizumab** — FcRn/TED or GD (UCB)
3. **Efgartigimod** — FcRn/TED or GD (argenx)
4. **Nipocalimab** — FcRn/TED or GD (J&J/Janssen)
5. **Iscalimab** — CD40L/TED or GD (Novartis)
6. **Linsitinib** — IGF-1R SM/TED Phase 2
7. **Teprotumumab re-treatment** — OPTIC-X final results; re-treatment protocol 확립 여부
8. **Rituximab** — anti-CD20/TED Phase 2/3 (ongoing)
9. **Tocilizumab** — IL-6R/TED (CIRTED, others) — 결과 및 guideline 반영 여부
10. **K1-70** — TSHR antagonist Ab/GD early phase

---

### Section E — eTPD Implications (중립 본문과 분리)

**E1. TSAb의 eTPD 표적 적합성 평가**
- TSAb subclass: 주로 IgG1/IgG4 → FcRn 의존적 반감기 (~21일)
- 혈중 TSAb 농도 범위 (nM): extracellular depletion 타겟으로서 접근 가능성
- 순환 중 soluble target — sweeping 전략 적합성 (cell-bound TSHR와 구분)
- TSHR 자체를 sweeping 타겟으로 삼는 경우 (free TSHR antigen 수준): 데이터 확인 필요

**E2. GD vs. TED — 어느 적응증이 eTPD에 더 적합한가**
- GD: TSAb 제거 → 갑상선 자극 직접 차단 가능; PD biomarker 명확 (TFTs, TRAb titer)
- TED: TSAb 외 IGF-1R 경로 독립적 관여 가능성 → TSAb만 제거 시 충분한지 불확실
- 환자군 크기, 질환 chronicity, TSAb titer dynamics, clinical endpoint 측정 용이성 비교

**E3. FcRn 억제제와의 차별화 포인트**
- 기존 FcRn inhibitor: 전체 IgG 감소 → 면역억제 부작용; 감염 위험; protective Ab 손실
- eTPD (TSAb-selective 접근 가능성): 병원성 IgG만 선택적 제거 → 이론적 안전성 우위
- 해결 과제: TSAb epitope 기반 선택성 구현; 분자 설계 (bispecific sweeping Ab vs. ASGPR-based degrader)
- FcRn inhibitor 임상 data 축적 속도와의 timeline 압박

**E4. 경쟁 지형 요약 (eTPD 관점)**
- FcRn inhibitor 계열: TED/GD에서 TSAb 감소 + 임상 활성 근거 확보 진행 중
- TSAb-selective 접근: 차별화 가능하나 개발 초기; epitope/설계 데이터 부재
- 결론 명시: eTPD 전략이 FcRn 억제제 대비 우위를 갖기 위한 요건

---

## 5. 실행 계획 (Work 세션 상세)

### 5.1 Phase별 도구 호출 계획

| Phase | 주요 도구 | 예상 query 수 | 목적 |
|---|---|---|---|
| **Setup** | memory_read; 파일 초기화 | 3-5 | context 확인; execution_log/reference/qa_checklist 생성 |
| **A1-A2 Epidemiology** | PubMed, Web, Consensus/Elicit | 12-15 | incidence/prevalence 원문; 7MM 수치 확보 |
| **A3-A7 Clinical** | PubMed, Web (EUGOGO guideline) | 10-12 | 증상/진단/staging/severity 원문 |
| **B1-B2 Genetics/Env** | PubMed, Open Targets | 8-10 | 유전적 loci; 환경적 요인 문헌 |
| **B3-B5 Mechanism** | PubMed, Open Targets, ChEMBL | 12-15 | GD/TED 병리기전 review 심층 검색 |
| **C1-C2 SoC** | PubMed, Web (FDA label) | 8-10 | ATD/RAI/surgery; IVMP/selenium 데이터 |
| **C3 Teprotumumab** | PubMed, Web | 6-8 | OPTIC/OPTIC-X 결과; AE 데이터 |
| **C4-C6 Pipeline** | ClinicalTrials.gov, AdisInsight, Web | 20-25 | 전체 active pipeline; 반응/안전성/unmet needs |
| **D Key Trials** | ClinicalTrials.gov, Web | 8-10 | NCT 상세; status/endpoint/readout 확인 |
| **E eTPD** | 합성 분석 (추가 도구 최소) | 3-5 | 기존 수집 데이터 기반 추론 |
| **Report 작성** | — | — | report.md Section A-E 초안; 인용 번호 부여 |
| **QA 실행** | 별도 QA 세션 | 별도 | §6 checklist 기반 검토 |

**총 예상 tool call 수**: ~90-110회  
**총 예상 소요 시간**: 5-8시간 (work 세션 내 연속 또는 phase별 분할 가능)

### 5.2 실행 순서 (Step-by-step)

```
Step 0: Setup
  0a. execution_log.md 생성 (타임스탬프 헤더 포함)
  0b. reference.md 생성 (빈 템플릿 + 번호 규칙 명시)
  0c. qa_checklist.md 생성 (§6.2 내용 그대로 복사)
  0d. 현재 project memory 파일 확인 (context 누락 방지)

Step 1: Section A — GD & TED Epidemiology (batch 1)
  1a. PubMed: "Graves disease epidemiology incidence prevalence systematic review"
  1b. PubMed: "thyroid eye disease Graves ophthalmopathy epidemiology prevalence"
  1c. Web: "Graves disease global burden 7MM 2023 2024 2025 statistics"
  1d. Web: "thyroid eye disease TED incidence EU US Japan epidemiology"
  1e. Consensus/Elicit: high-quality epi reviews for both conditions

Step 2: Section A — Symptoms, Diagnosis, Staging (batch 2)
  2a. Web: "EUGOGO 2022 guidelines thyroid eye disease classification" (최신 원문)
  2b. PubMed: "EUGOGO NOSPECS clinical activity score CAS thyroid ophthalmopathy staging"
  2c. PubMed: "Graves disease thyroid storm diagnosis management"
  2d. PubMed: "TRAb TSAb assay Graves disease diagnosis accuracy"
  2e. PubMed: "dysthyroid optic neuropathy diagnosis incidence"

Step 3: Section B — Genetics
  3a. PubMed: "Graves disease HLA PTPN22 CTLA4 genetics susceptibility review"
  3b. PubMed: "thyroid eye disease genetic risk factor severity"
  3c. Open Targets: TSHR — disease associations; genetic evidence

Step 4: Section B — Environmental Factors + GD Mechanism
  4a. PubMed: "Graves disease smoking risk factor TED mechanism"
  4b. PubMed: "RAI radioiodine thyroid eye disease worsening risk"
  4c. PubMed: "Graves disease TSHR autoantibody TSAb TBAb mechanism pathogenesis review"
  4d. PubMed: "TSAb TRAb spectrum stimulating blocking neutral clinical significance"

Step 5: Section B — TED Mechanism (deep dive)
  5a. PubMed: "thyroid eye disease orbital fibroblast TSHR IGF-1R pathogenesis review"
  5b. PubMed: "IGF-1R TSHR complex signalosome orbital fibroblast Graves ophthalmopathy"
  5c. PubMed: "TED active inactive phase cytokine Th1 Th2 shift"
  5d. PubMed: "hyaluronan glycosaminoglycan orbital fibroblast Graves ophthalmopathy"
  5e. PubMed: "Thy-1 fibroblast subpopulation orbital adipogenesis myofibroblast TED"

Step 6: Section C — GD SoC + TED SoC
  6a. PubMed: "methimazole carbimazole antithyroid drug Graves relapse remission rate"
  6b. PubMed: "long-term antithyroid drug LDAT Graves disease relapse prevention"
  6c. PubMed: "IV methylprednisolone thyroid eye disease EUGOGO treatment"
  6d. PubMed: "selenium thyroid eye disease COSMOS randomized trial"
  6e. Web: "RAI thyroid eye disease risk prophylactic steroids guideline"

Step 7: Section C — Teprotumumab (Approved)
  7a. PubMed: "teprotumumab TEPEZZA OPTIC phase 3 trial results"
  7b. PubMed: "teprotumumab OPTIC-X extension retreatment thyroid eye disease"
  7c. PubMed: "teprotumumab hearing loss hyperacusis adverse events"
  7d. Web: "TEPEZZA FDA prescribing information label" (official PI)

Step 8: Section C — Pipeline (active, preclinical 포함)
  8a. ClinicalTrials.gov: condition="thyroid eye disease" + status=recruiting/active_not_recruiting
  8b. ClinicalTrials.gov: condition="Graves disease" + status=recruiting/active + interventional
  8c. Web/AdisInsight: "batoclimab RVT-1401 thyroid eye disease phase"
  8d. Web: "rozanolixizumab efgartigimod nipocalimab thyroid eye disease 2025 2026"
  8e. PubMed: "FcRn inhibitor IgG Graves disease TED TSAb reduction"
  8f. PubMed: "rituximab thyroid eye disease randomized trial CIRTED"
  8g. PubMed: "tocilizumab thyroid eye disease randomized controlled trial"
  8h. PubMed: "linsitinib IGF-1R thyroid eye disease clinical trial"
  8i. Web: "iscalimab CD40L thyroid eye disease Graves"
  8j. Web: "K1-70 TSHR antagonist antibody Graves disease"
  8k. AdisInsight/Web: preclinical stage pipeline TED 2025 2026

Step 9: Section D — Key Trials 정리
  9a. 위 Step 8 결과에서 NCT 번호 추출 + 상세 status/endpoint/readout 일정 확인
  9b. Priority ranking + 팔로업 이유 작성

Step 10: Section E — eTPD Synthesis
  10a. 수집 데이터 기반 TSAb 적합성 평가 작성
  10b. FcRn inhibitor 경쟁 지형 vs. eTPD 차별화 포인트 작성

Step 11: Report 통합 작성
  11a. Section A-E 순서로 report.md 작성 (개조식 한국어; 영어 기술 용어 유지)
  11b. 인용 발생 시 reference.md에 즉시 추가 + [x] 번호 부여
  11c. 각 핵심 claim: 근거 등급 명시 (RCT / cohort / expert opinion / in vitro)

Step 12: QA 실행 (별도 세션 — §6 참조)
  12a. QA 세션에 system prompt + report.md + reference.md + qa_checklist.md 공급
  12b. FAIL/PARTIAL 항목 수정 후 report.md 최종 확정
```

### 5.3 Execution_log 기록 형식 (Work 세션 준수)

```
[HH:MM] TOOL: <tool_name>
  Query/Input: "<exact query or action>"
  Result: <brief summary OR "no relevant results">
  PMIDs (if PubMed): [comma-separated]
  Action: <what was extracted / filed to reference.md / skipped>
  Status: SUCCESS / PARTIAL / FAIL
  Mitigation (if FAIL/PARTIAL): <대안 query 또는 대체 소스>
```

---

## 6. QA 프레임워크

### 6.1 QA 에이전트 설정

**별도 Claude 세션 (fresh conversation)에서 QA 수행**  
report.md 완성 후, 새 세션에 다음 순서로 공급:
1. QA 에이전트 시스템 프롬프트 (아래)
2. report.md 전문
3. reference.md 전문
4. qa_checklist.md 전문 (§6.2)

**QA 에이전트 시스템 프롬프트 (Work 세션에서 복사하여 사용)**:
```
You are a scientific quality assurance agent reviewing a comprehensive disease analysis report on Graves' Disease (GD) and Thyroid Eye Disease (TED).

Your task: systematically evaluate the attached report.md against the provided qa_checklist.md.

For EACH checklist item:
- Mark: PASS / FAIL / PARTIAL
- If FAIL or PARTIAL: quote the exact problematic text; explain the specific error; suggest a concrete correction
- Do not give benefit of the doubt on factual inaccuracies

Standards:
- Scientific rigor: no unqualified claims; uncertain mechanisms labeled as "proposed" or "under investigation"
- Citation integrity: every factual claim has [x] in-line citation; [x] matches reference.md numbering
- No marketing language ("revolutionary", "breakthrough", "game-changing")
- Language: Korean body text; English technical terms preserved; no middle dots (·)
- Pipeline scope: preclinical + active only; no discontinued/NDR assets included
- eTPD content: confined to Section E only; not present in Sections A-D

Output format: table (checklist item | PASS/FAIL/PARTIAL | comment/correction)
```

### 6.2 QA Checklist (본 작업 특이적 — qa_checklist.md로 저장)

**[A] 질환 구분/개념 정확성**
- [ ] A1: GD와 TED를 별개 질환으로 구분하면서 연관성 명시 (TED ≠ GD, but ~90-95% TED is GD-associated)
- [ ] A2: TED가 GD 없이도 발생 가능함을 기술 (~5-10% TED: euthyroid or hypothyroid)
- [ ] A3: GD 환자에서 TED 발생 비율 올바르게 기술 (mild orbital changes ~50%; clinically significant TED ~20-25%)

**[B] 역학 수치 정확성**
- [ ] B1: GD incidence와 prevalence 수치가 registry/cohort study 이상 근거에서 인용됨
- [ ] B2: TED epidemiology는 GD 대비 비율 또는 독립 수치로 명확히 제시됨
- [ ] B3: 7MM 국가별 수치 — 단일 출처 의존 시 명기됨; 복수 출처 교차확인 권장
- [ ] B4: Incidence와 prevalence 혼동 없이 구분 제시

**[C] Staging/Severity 정확성**
- [ ] C1: CAS 체계 정확히 기술 — 7점 (첫 방문) vs. 10점 (추적 방문) 구분
- [ ] C2: EUGOGO 3 tier 각 기준 구체적 수치 포함하여 정확히 기술
- [ ] C3: NOSPECS 7 class 개요 정확히 기술
- [ ] C4: GD 자체에 대한 공식 staging system 부재 사실 명기

**[D] 병리기전 정확성**
- [ ] D1: TSAb (stimulating) vs. TBAb (blocking) vs. neutral TRAb 구분 정확히 기술
- [ ] D2: TSHR-IGF-1R 복합체 가설 — 확립된 사실이 아닌 "proposed" / "under investigation" 명기
- [ ] D3: Thy-1+ (myofibroblast 분화) vs. Thy-1- (adipocyte 분화) fibroblast 운명 정확히 기술
- [ ] D4: RAI가 TED 악화 위험을 가질 수 있다는 사실 기술; 흡연 동반 시 위험 증가 포함
- [ ] D5: TED active phase (Th1 dominant) vs. inactive/fibrotic phase (Th2/TGF-β dominant) cytokine milieu 차이 기술
- [ ] D6: 흡연이 TED #1 modifiable risk factor임을 명시

**[E] 치료제 정보 정확성**
- [ ] E1: Teprotumumab FDA 승인일 (2020년 1월) 및 적응증 (moderate-to-severe active TED) 정확
- [ ] E2: Teprotumumab 주요 AE — 청각 관련 (hearing loss, hyperacusis, tinnitus) 명기; reversibility 불확실성 포함
- [ ] E3: IVMP가 active TED 1차 SoC로 기술 (EUGOGO guideline 근거)
- [ ] E4: ATD 재발률 수치 출처 명시됨
- [ ] E5: RAI 후 TED 악화 예방을 위한 prednisolone 투여 권고 기술
- [ ] E6: 파이프라인 각 자산의 임상 단계가 indication-specific으로 확인됨 (Highest Status trap 적용 여부 확인)
- [ ] E7: Discontinued/NDR 자산이 포함되지 않음 (본 작업 범위 명시 기준)

**[F] 인용/참고문헌 정확성**
- [ ] F1: report.md 본문 모든 사실 claim에 [x] in-line citation 존재
- [ ] F2: [x] 번호가 reference.md 번호와 전수 일치
- [ ] F3: reference.md 중복 항목 없음
- [ ] F4: 무작위 샘플 5개 이상 PMID 실존 검증
- [ ] F5: 마케팅 언어 없음
- [ ] F6: 불확실한 mechanism/claim에 근거 수준 표현 사용 ("suggested", "proposed", "under investigation", "in vitro only" 등)

**[G] eTPD 섹션 분리 원칙**
- [ ] G1: eTPD 관련 내용이 Section A-D에 없고 Section E에만 기술됨
- [ ] G2: eTPD 시사점에서 speculative 항목에 근거 수준 명기
- [ ] G3: FcRn inhibitor vs. eTPD TSAb-selective 접근의 차별화 포인트 명확히 기술

**[H] 언어/형식**
- [ ] H1: 영어 기술 용어 (TSHR, IGF-1R, TSAb, CAS, EUGOGO, TRAb, FcRn 등) 영문 유지
- [ ] H2: 가운뎃점(·) 미사용 — 슬래쉬(/), 쉼표(,), 세미콜론(;) 적절 사용
- [ ] H3: 개조식(명사 종결형) 문체 유지

---

## 7. 위험 요소 및 Mitigation

| 위험 요소 | 가능성 | Mitigation |
|---|---|---|
| TED pipeline 최신 정보 불완전 | 중간 | ClinicalTrials.gov + 기업 press release 교차 확인; AdisInsight 보완 |
| 7MM 국가별 TED 역학 데이터 공백 | 높음 | Global 수치에서 인구비 추정; 한계 명기; 가용 데이터 출처 명시 |
| TSHR-IGF-1R mechanistic 논쟁 과대 기술 위험 | 중간 | 원문 인용 시 저자 주장 수준으로 표현; QA D2 항목 집중 검토 |
| Pipeline phase 오분류 (Highest Status trap) | 중간 | ClinicalTrials.gov indication-level status 우선; AdisInsight 보조 |
| Teprotumumab 이후 데이터 PubMed 미색인 | 중간 | Web search; ENDOCRINE/ENDO conference abstract 탐색 |
| QA 에이전트 context 길이 초과 | 낮음 | report.md를 섹션별 분할하여 QA 진행 |

---

## 8. 참고문헌 관리 규칙

### 8.1 reference.md 형식
```
[1] Author(s). Title. Journal. Year;Vol(Issue):Pages. PMID: XXXXXXXX. [확인일: YYYY-MM-DD]
[2] Organization/Author. Document title. Source/URL. [확인일: YYYY-MM-DD]  ← 웹/공식문서
```

### 8.2 인용 원칙
- PMID 확인된 peer-reviewed 문헌 최우선
- 웹 소스 (press release, FDA PI, guideline 원문): URL + 확인일 명기
- Review 논문 인용 시: 원 데이터 출처 추적 권장 (secondary citation 최소화)
- 동일 claim에 복수 출처 가능 시: [x, y] 형태로 복수 인용

---

_본 계획서 확정일: 2026-09-11 (Plan 세션). Work 세션에서 변경 필요 시 execution_log.md에 이유 기록 후 적용._
