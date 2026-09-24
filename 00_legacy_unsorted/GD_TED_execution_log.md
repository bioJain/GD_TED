---
title: GD_TED_execution_log
목적: 도구 호출 / 실패-mitigation / 시간별 수행 내역 기록 (추적성/재현성 확보)
작업 시작: 2026-09-11
---

# GD/TED Work 세션 실행 로그

기록 형식:
```
[HH:MM] TOOL: <tool_name>
  Query/Input: "<exact query or action>"
  Result: <brief summary OR "no relevant results">
  PMIDs (if PubMed): [comma-separated]
  Action: <what was extracted / filed to reference.md / skipped>
  Status: SUCCESS / PARTIAL / FAIL
  Mitigation (if FAIL/PARTIAL): <대안 query 또는 대체 소스>
```

## Setup (Step 0)
[00:00] Plan 세션 확정 사항 확인 (GD_TED_plan.md, memory)
  Result: 5개 섹션 구조, Global+7MM 역학, preclinical 포함 active pipeline, eTPD 별도 Section E 확정
  Status: SUCCESS

[00:01] 사용자 확인 사항 3건 처리
  - AdisInsight 커넥터 미연결 → Cortellis/AdisInsight export 별도 제공받기로 결정 (Section C4 진행 시 요청)
  - 산출물 저장 위치 → claude.ai '6T_review_26_H2' 프로젝트 문서(claude/ 하위)로 저장
  - 진행 방식 → 섹션별 체크포인트 (A→B→C→D→E, 각 섹션 완료 시 중간 결과 공유)
  Status: SUCCESS

---

## Section A — Epidemiology & Clinical Characterization

[00:05] TOOL: PubMed search_articles (x2) — "Graves disease epidemiology incidence prevalence systematic review", "thyroid eye disease Graves ophthalmopathy epidemiology prevalence incidence"
  Result: 66건/475건 매치 중 상위 10건씩 확보. 국가별 세부 수치 문헌은 미발견, 중국 전국 메타분석(GD prevalence 450/100,000) 확보
  Status: PARTIAL — 7MM 국가별 수치 gap 확인

[00:06] TOOL: PubMed search_articles — EUGOGO/NOSPECS/CAS staging (0건), thyroid storm Burch-Wartofsky (34건), TRAb/TSAb/TBAb assay (1건), DON incidence (14건)
  Action: 상위 PMID 추출 후 get_article_metadata로 abstract 확보
  Status: SUCCESS (EUGOGO는 쿼리 재구성 후 별도 검색으로 확보)

[00:07] TOOL: WebSearch — EUGOGO 2021/2022 guideline, Graves disease 7MM 국가 통계
  Result: EUGOGO 원문 PMID 확인(34297684), 7MM은 DelveInsight 등 상업 forecast만 검색됨 — 학술 근거로 부적합, reference.md에 한계 명시
  Status: PARTIAL

[00:08] TOOL: PubMed get_article_metadata — 핵심 review/원저 20편 이상 abstract 확보 (Lancet Diabetes Endocrinol 2025 TED review, Bartley Olmsted County 4편 시리즈, EUGOGO 2021 원문, teprotumumab OPTIC/OPTIC-X, TSHR genetics, TSHR-IGF1R crosstalk 등)
  Action: reference.md [1]-[18] 확정 기재, Section B/C 선행 자료 [19]-[28] 별도 기재
  Status: SUCCESS

[00:09] TOOL: PubMed search_articles — Graves disease 7MM 국가별 population-based cohort (Denmark/Sweden/UK), HLA/CTLA4/PTPN22 genetics, Thy-1/CD90 fibroblast (일부 0건 — 쿼리 과다 AND 조건으로 재구성 필요 확인)
  Status: PARTIAL — 일부 쿼리 재시도로 결과 확보(genetics, IGF1R-TSHR), 국가별 코호트/Thy-1 특이 쿼리는 최종 0건 → Section B 진행 시 쿼리 재설계 필요

Section A 초안 작성 완료 — report.md에 A1-A7 반영, 미해결 gap 3건(7MM 국가별 수치, 한국 데이터, CAS 세부 배점표) 명시하여 사용자 체크포인트 요청
사용자 결정: gap 미해결 상태로 두고 Section B로 즉시 진행

## Section B — Molecular & Pathobiological Mechanism

[00:15] TOOL: PubMed search_articles — smoking/RAI/selenium 환경요인 (일부 과다 AND 쿼리 0건 → 재구성), Tfh/Treg pathogenesis, Thy-1 fibroblast fate, twin study
  Result: RAI-TED 위험/prednisone 예방 review 확보(39787151), selenium 근거수준 review 확보(28639965, 30124533), 산화스트레스 review 확보(34944687), Tfh/Treg tissue infiltration 연구 확보(32328068) — 흥미로운 역상관 관찰(TLS/GC signature 없는 GD 40%군에서 오히려 ophthalmopathy 유병률 高)
  Status: PARTIAL — 일부 쿼리 0건, 재검색으로 대부분 확보

[00:16] TOOL: PubMed search_articles — "Smith Koumas Thy-1 orbital fibroblast subset differentiation"
  Result: Koumas/Smith 2003 Am J Pathol 원저 확인 — Thy-1+ → myofibroblast, Thy-1- → lipofibroblast 분화 직접 실험 근거(QA D3 대응)
  Status: SUCCESS

[00:17] TOOL: PubMed search_articles — "Graves disease twin study heritability concordance"
  Result: California twin study(Ringold 2002) — MZ concordance 17%, DZ 1.9%
  Status: SUCCESS

[00:18] TOOL: PubMed get_article_metadata — Section B 관련 10편 이상 abstract 확보, reference.md [30]-[38] 확정
  Status: SUCCESS

Section B 초안 작성 완료 — report.md에 B1-B5 반영. QA 셀프체크 결과 D5(active/inactive cytokine milieu 전환) 항목 FAIL로 확인 — 이번 라운드 미발견, 최종 통합 전 필수 재검색 항목으로 기록. D4(RAI+흡연 병용 위험 정량화)도 PARTIAL로 남음.

## Section C — Therapeutic Landscape (C1/C2/C3/C5 부분/C6, C4 제외)

[00:25] TOOL: PubMed search_articles — methimazole/carbimazole relapse(다수 과다-AND 쿼리 0건), selenium COSMOS/Marcocci, teprotumumab hearing loss/audiometry, tocilizumab RCT, rituximab RCT
  Result: EUGOGO selenium RCT(Marcocci 2011 NEJM, 21591944) 확보, tocilizumab RCT(Perez-Moreiras 2018) + 메타분석 2편 확보, rituximab 상반된 2-RCT 서술 review(Wiersinga 2016) 확보, teprotumumab 청각 AE 4편 확보(등록임상 7-12% vs 실사용 38.6-81.5% 간 뚜렷한 괴리 확인 — 주요 발견)
  Status: PARTIAL — ATD 재발률(원안 ~50%@18개월), teprotumumab 모집단 재발률(원안 ~25%), orbital irradiation 원저는 미확보

[00:26] TOOL: PubMed get_article_metadata — Section C 관련 9편 abstract 확보, reference.md [39]-[47] 확정
  Status: SUCCESS

Section C(C4 제외) 초안 작성 완료 — report.md에 C1/C2/C3/C5(부분)/C6 반영. 핵심 발견: teprotumumab 청각 AE 실사용 빈도가 등록임상 보고치 대비 현저히 높음(비가역 사례 존재) — QA E2 대응 강화. C4는 Cortellis/AdisInsight export 대기로 보류.

사용자 결정: "여기서 중단, export 업로드 후 C4부터 재개" — 세션 일시 중지 후 Cortellis export 수신 대기

## Section C4 — Active Pipeline (재개, 2026-09-14)

[14:20] 사용자 파일 업로드 수신 — GD_TED_Pipeline_Landscape_20260914_v2.xlsx ("코텔리스 GD 및 TED 파이프라인 - 1차 정제 파일 제공함")
  Action: openpyxl(data_only=True)로 로드, 시트 3종 확인 (GD_TED_Pipeline: 72행 원자료, MoA_Matrix_GD/MoA_Matrix_TED: Jain 사전 구축 매트릭스)
  Status: SUCCESS

[14:22] TOOL: Bash — openpyxl 파싱, "개발 단계" 컬럼 기준 중단(discontinued/NDR) 자산 필터링 (plan 원안 task-specific override: C4는 preclinical+active 전체 포함, discontinued/NDR 제외)
  Result: 전체 72건 중 active 51건 / discontinued 21건 확인. 적응증 구분(GD_TED_Pipeline 시트 "적응증 구분" 컬럼) 기준 재그룹핑 — GD+TED 겸용 17건, TED only 25건, GD only 9건
  Action: MoA_Matrix_GD/MoA_Matrix_TED 시트 원자료 그대로 report.md 표로 반영 (Jain 사전 구축분, 재계산 없이 인용) — indication-specific staging 이미 적용되어 있음을 원자료에서 직접 확인(예: efgartigimod alfa GD-active/TED-discontinued, batoclimab 양쪽 모두 discontinued로 각기 별도 행 기재)
  Status: SUCCESS

[14:23] 분석 중 주요 관찰 3건 — (1) IGF-1R 억제제 계열이 TED에서 가장 밀집(15개 이상 자산, Approved 3건 포함), GD에서는 상대적으로 희소 (2) FcRn 억제제는 GD에서 TED보다 활성 자산 많음 — efgartigimod alfa가 대표적으로 GD active/TED discontinued로 갈림 (3) TSHR-direct/TSAb-degrader 기전은 대부분 preclinical~Phase 1 단계, Phase 3는 BHV-1300 1건뿐 — Section E eTPD 비교 시 가장 관련성 높은 관찰로 플래그
  Status: SUCCESS

[14:24] 중요 발견 — iscalimab(원안 Section D 우선 추적 후보 10건 중 1건)이 본 파일에서 discontinued(Phase 2)로 확인됨. plan 원안 Section D 우선순위 리스트 재조정 필요 사항으로 기록 (Section D 착수 시 반영)
  Status: SUCCESS — Action item 기록, Section D 작업 시 처리 예정

Section C4 초안 작성 완료 — report.md에 데이터 출처 노트/GD, TED MoA×단계 매트릭스 2종/자산 상세표(GD+TED 겸용 17건, TED only 25건, GD only 9건)/종합 관찰 5건 반영. reference.md [48] 추가(Cortellis 파생 자료, 상업 DB 신뢰도 등급 별도 명시). QA E6(indication-specific staging)/E7(discontinued 제외) 대응 완료.

사용자 결정(AskUserQuestion): "Section D 진행 (권장)" — C4 완료 체크포인트 이후 Section D(주요 임상시험)로 진행

## Section D — Key Clinical Trials to Follow

[14:35] TOOL: ClinicalTrials.gov search_trials — BHV-1300/linsitinib/elegrobart/K1-70/felzartamab/rilzabrutinib/imeroprubart/efgartigimod(GD)/teprotumumab(TED)/rituximab(TED)/tocilizumab(TED) 11건 병렬 조회
  Result: BHV-1300 2건(Phase 1 biomarker + Phase 3 pivotal 신규 확인), linsitinib intervention명 검색은 전량 종양학 시험(OSI-906 코드명 중복) — 결과 미유효, elegrobart 0건(코드명 상이 추정), K1-70은 2016년 완료 Phase 1 1건만, felzartamab/rilzabrutinib 각 신규 Phase 2 1건씩 확인, imeroprubart는 IMVT-1402 코드명으로 8건(GD 관련 3건), efgartigimod GD Phase 3 신규 2건 + TED Phase 3 2건 모두 TERMINATED 확인(C4 데이터와 일치), teprotumumab 9건(SC 제형/biosimilar 다수), rituximab/tocilizumab은 신규 대형 RCT 없음(과거 완료작 위주)
  Status: PARTIAL — linsitinib/elegrobart는 재검색 필요 확인

[14:37] TOOL: ClinicalTrials.gov search_by_sponsor — Sling Therapeutics(linsitinib 개발사), Viridian Therapeutics(elegrobart 개발사) + search_trials MHB-018A/IGF-1R(TED) 병렬 조회
  Result: Sling Therapeutics 3건 확인(linsitinib 코드명 대신 성분명으로 재검색 성공) — Phase 2/3 완료작(NCT05276063) + 연장연구(NCT06112340) + 신규 Phase 3 "ORBIT"(NCT07753603, 2026-08 개시); Viridian 8건 확인 — REVEAL-1/REVEAL-2(VRDN-003=elegrobart) 2건 active_not_recruiting(PCD 2026-02/03 임박) + veligrotug 완료작 다수; MHB-018A(Minghui, 중국) 6건 확인, 그 중 3건이 활성 Phase 3; IBI311(Innovent) inactive TED 대상 Phase 3(NCT07113262) 별도 확인 — C6 unmet need("inactive TED 승인 치료 부재")에 직접 대응하는 시험 설계로 주목
  Status: SUCCESS

[14:40] TOOL: ClinicalTrials.gov get_trial_details ×6 — NCT07661056(BHV-1300 Ph3)/NCT06625411(REVEAL-1)/NCT07753603(linsitinib ORBIT)/NCT07570316(efgartigimod GD "VitaliThy")/NCT06727604(imeroprubart GD)/NCT07113262(IBI311 inactive TED) primary/secondary endpoint 및 eligibility 상세 확보
  Action: reference.md에 [49]-[62] NCT 인용 14건 추가(2차 참고 대상 NCT 포함), report.md에 Section D 신설 — D1(GD 5건)/D2(TED 5건)/D3(활성 대형 확증시험 부재로 하향, K1-70/rituximab/tocilizumab) 표 형태로 반영
  Status: SUCCESS

[14:41] 원안 계획서 우선순위 목록 재조정 — iscalimab(discontinued 확인, C4) 제외, batoclimab/rozanolixizumab/nipocalimab(FcRn 3종)은 GD/TED 적응증 등록시험 CT.gov 미확인으로 제외(batoclimab은 C4에서 GD+TED 모두 discontinued로 별도 확인, rozanolixizumab/nipocalimab은 근거 불충분 — 한계로 명기). 대신 C4 active 자산 기반으로 GD 5건(BHV-1300/efgartigimod/imeroprubart/felzartamab/rilzabrutinib) + TED 5건(linsitinib ORBIT/elegrobart REVEAL/MHB-018A/IBI311 inactive/teprotumumab SC) 재구성
  Status: SUCCESS

Section D 작성 완료 — report.md에 D1/D2/D3 표 및 재조정 근거 반영. 근접 readout 3건(REVEAL-1/2 PCD 2026-02/03, MHB-018A PCD 2026-07, teprotumumab SC PCD 2025-12) 플래그 — 다음 체크포인트 시 재확인 권고 사항으로 "다음 단계 제안"에 추가.

사용자 결정(AskUserQuestion): "Section E 진행 (권장)" — Section D 완료 체크포인트 이후 Section E(eTPD 시사점 종합)로 진행

## Section E — eTPD Implications

[14:50] TOOL: PubMed search_articles ×3 — "TSH receptor antibody serum concentration IgG subclass Graves disease"(0건, 과다 AND), "lysosome targeting chimera LYTAC extracellular protein degradation antibody"(21건), "FcRn antagonist mechanism IgG reduction infection risk safety"(1건)
  Status: PARTIAL — 첫 쿼리 재구성 필요

[14:51] TOOL: PubMed search_articles ×2 재시도 — "TSAb IgG1 IgG4 subclass thyroid stimulating antibody"(4건, 1980-90년대 고전 연구), "FcRn inhibitor efgartigimod infection risk immunoglobulin reduction"(1건)
  Result: TSAb subclass 관련 상충 문헌 확보(Weetman 1990: IgG1 단독 vs Kjaerulff 1984: IgG1/2/4 이질적 분포) — TSAb subclass 구성 미확립 상태로 결론, LYTAC review(Zhou 2026) 및 efgartigimod/nipocalimab IgG 비선택성/안전성 데이터 확보
  Status: SUCCESS

[14:52] TOOL: PubMed get_article_metadata ×2 (합계 7편) — Weetman 1990(PMID 2168443), Kjaerulff 1984(PMID 6233835), LYTAC review(PMID 42298978) 외 LYTAC 관련 2편, efgartigimod gMG IgG 변화 코호트(PMID 41699526), nipocalimab 안전성 review(PMID 41395452)
  Action: reference.md에 [63]-[67] 추가
  Status: SUCCESS

[14:54] Section E 작성(E1-E4) — TSAb eTPD 적합성(subclass 상충 명시)/GD vs TED 적합성(efgartigimod GD active-TED terminated 교차검증 신호 활용)/FcRn 억제제 차별화(비선택성 실증 + 실측 안전성 양호라는 이중 구조로 과장 방지)/경쟁지형 종합. Section A-D 재확인하여 eTPD 언급 없음 확인(QA G1)
  Status: SUCCESS

Section E 작성 완료 — report.md에 E1-E4 및 QA 셀프체크(G1-G3, F5-F6) 반영. Gap 2건 확인: TSAb subclass 문헌 상충 미해소, TSAb 혈중 농도/반감기 직접 정량 문헌 미확보 — 최종 통합 전 보완 필요 항목으로 "다음 단계 제안"에 통합 기록.

사용자 결정(AskUserQuestion): "미해결 gap 8건 보완 (권장)" — Section E 완료 체크포인트 이후 누적된 미해결 gap 보완 라운드 진행

## 미해결 gap 보완 (4차 수집분, 2026-09-14)

[15:05] TOOL: PubMed search_articles ×9 병렬 — 7MM(Denmark/Sweden/Korea) 역학, RAI+흡연 병용 위험, Th1/Th2 cytokine shift, ATD 재발률 메타분석, teprotumumab 실사용 재발률, orbital radiotherapy RCT, TSAb 농도 정량 9건 동시 조회
  Result: Denmark 검색 12건 매치했으나 상위 결과는 암/치매 등 무관 주제(cancer risk, dementia risk in hyperthyroidism) — GD/TED incidence 직접 수치 없음; Sweden 6건도 무관(COVID/대장암 등 오검색); Korea/RAI+흡연/Th1-Th2/teprotumumab 재발률/TSAb 농도는 모두 0건(과다 AND 쿼리)
  Status: PARTIAL — 대부분 재구성 필요 확인

[15:08] TOOL: PubMed search_articles ×5 재시도(쿼리 단순화) — Korea 역학(72건 매치), RAI+스테로이드 예방(6건), Th1/Th2 재시도(0건 재확인), ATD 관련 재발/치료비교(9건+7건), orbital irradiation RCT 재검색(37건 매치)
  Result: 한국 NHIS 기반 GD incidence 데이터 확보(4.6/10,000 person-years, 40세 이상 코호트 — 항생제 연구의 배경 데이터)[68], 한국 소아 코호트 배경 데이터[74], RAI 후 스테로이드 예방투여 GD 이환기간별 세분화 RCT 확보[70], ATD/RAI/thyroidectomy 비교 메타분석 2건 확보[71,72], **orbital irradiation Mayo Clinic 위약대조 RCT 확보 — 6개월 시점 유의한 효과 없음(주요 발견)**[69]
  Status: SUCCESS(일부) — Th1/Th2 milieu, TSAb 농도, teprotumumab 실사용 재발률, DE/FR/UK/IT/ES 개별 수치는 이번 라운드에서도 미확보(재쿼리 2회 시도 후에도 0건)

[15:12] TOOL: WebSearch ×2 — TEPEZZA FDA 승인 날짜 확인
  Result: BusinessWire 공식 press release(2020-01-21, URL 내 날짜코드 20200121006017로 교차확인) — FDA 승인일 2020-01-21 확정
  Action: reference.md [73] 추가, report.md C3/QA E1 PASS로 갱신
  Status: SUCCESS

[15:15] TOOL: PubMed get_article_metadata ×3 배치(총 20편 검토, 인용 가치 있는 7편 채택) — reference.md [68]-[74] 추가
  Action: report.md Section A2(한국 데이터)/C1(RAI 이환기간별 세분화, RAI+ATD 메타분석, thyroidectomy 메타분석)/C3(FDA 승인일)/QA 테이블(B1-4, E1, E4) 갱신, "다음 단계 제안"에 3건 해결/7건 잔여 gap 명시
  Status: SUCCESS

미해결 gap 보완 라운드 완료 — 9건 중 3건 해결(한국 역학, FDA 승인일, orbital irradiation 원저 — 특히 후자는 "효능 근거 예상보다 약함"이라는 반증적 발견). 잔여 7건(7MM 5개국 개별수치/EUGOGO CAS 배점표/RAI+흡연 정량/Th1-Th2 milieu/ATD, teprotumumab 재발률 원안수치/TSAb 농도)은 최종 통합 단계 재시도 대상으로 이월.

## QA 체크리스트 리뷰 및 수정 (2026-09-14)

[15:20] ACTION: 사용자 결정("잔여 gap은 남겨두고 QA 체크리스트로 이동") 반영 — Agent 도구(subagent_type: general-purpose)로 독립 QA 에이전트 스폰. 프롬프트: report.md/reference.md/qa_checklist.md 3개 파일 전체 읽기 → qa_checklist.md에 내장된 QA 시스템 프롬프트 verbatim 준수 → PMID 5개 이상 PubMed 실존 검증(F4) → [n] 인용-reference.md 번호 전수 대조 및 미인용 항목 플래그(F2) → Section A-D 본문 eTPD 용어 누출 여부 직접 grep 확인(G1) → 이미 공개된 gap은 새 발견으로 재플래그하지 않고 unhedged 허위확신 claim만 플래그 → 가운뎃점/영문 용어 형식 준수(H1/H2) 확인 지시
  Result: 대부분 PASS, PARTIAL 5건(A3/B3/C3/D4/E4 — 기존에 이미 공개된 gap, 중복 감점 아님 확인), **FAIL 5건**:
    - C1: EUGOGO CAS "추적 방문 시 2개 항목 추가, 최대 10점"이 괄호 안 3개 항목과 불일치(7+2=9≠10) — 산술 오류
    - D5: Th1(active)/Th2·TGF-β(inactive) cytokine milieu 전환 문헌 여전히 본문에 없음(기존 공개 gap이나 체크리스트 항목 자체는 FAIL 유지)
    - F2: raw PMID 인용 3건([39286340] A2 — reference.md에 해당 항목 자체가 없음; [34688699] A7 — 원래 [25]와 동일 문헌; [34789694] C3 2개소 — 원래 [47]과 동일 문헌) + reference.md 미인용 항목 7건([7],[11],[12],[26],[43],[47],[50])
    - G1: Section C4 관찰3("eTPD가 표적으로 삼는...")/C6 소제목("eTPD 관점은 Section E로 분리"— 자기모순적)/D1 표 3개 행(BHV-1300, efgartigimod GD, felzartamab)에 "eTPD" 용어 누출 확인 — Section E 자체 QA 셀프체크의 G1 PASS 기재가 부정확했음도 함께 지적
    - H2: 가운뎃점 5건("TSAb·IgG" ×4, "Th2·TGF-β" ×1)
  Status: FAIL 5건 확인, 수정 착수

[15:25] ACTION: 위 5개 FAIL 항목 전체 수정 적용
  - C1: "2개 항목" → "3개 항목(7+3=10)"으로 정정(A6)
  - F2: raw PMID 3건을 reference.md 번호로 교체([39286340]→[75] 신규 등재/PMID 39286340 확정, [34688699]→[25], [34789694]→[47] 2개소); 미인용 항목 6건에 실질적으로 부합하는 본문 위치 확인 후 in-line 인용 추가 — [7]→A1(TED 선행 시점 관련 Bartley chronology 원저), [11]→A6 EUGOGO tier(2021/2022 가이드라인 비교 논문), [12]→A2 한국 임상 프레임워크 문단, [26]→C3 OPTIC-X 조기반응 무관 재확인, [43]→B2 산화스트레스/셀레늄 기전 근거, [50]→D1 BHV-1300 행(biomarker 연구 NCT06980649); [47]은 raw-PMID 수정으로 자동 해소
  - G1: C4 관찰3/C6 소제목/D1 표 3개 행에서 "eTPD" 제거 및 중립적 표현으로 재기술, Section E QA 셀프체크 G1 항목을 "PASS(수정 후)"로 정정하고 리뷰 경위 명기
  - H2: "TSAb·IgG"(C4 매트릭스 2곳, C4 관찰3, E1) → "TSAb/IgG", "Th2·TGF-β"(다음 단계 제안 11) → "Th2/TGF-β" 전량 교체
  - D5: 기존 공개 gap 유지, "다음 단계 제안" 항목 4/9/11에 이미 반영되어 있어 추가 조치 없음(FAIL 상태로 남김, 최종 통합 전 필수 보완 사항으로 재확인)
  - report.md "다음 단계 제안" 항목 12로 QA 리뷰/수정 내역 요약 추가, reference.md에 "QA 리뷰 반영" 섹션 및 [75] 신규 항목 추가
  Status: SUCCESS — F2/G1/H2/C1 4개 항목 완전 해소, D5는 기존 정책대로 공개 gap으로 유지

[15:27] ACTION: 수정 적용 중 QA 에이전트 리포트에 없던 raw PMID 1건 자체 발견 — C3 MoA 설명 "[1, 31971679]"(31971679는 이미 reference.md [24](Douglas OPTIC Phase 3)와 동일 문헌) → "[1, 24]"로 정정. 전체 파일 재검색으로 추가 raw PMID/가운뎃점 잔존 여부 확인 완료(0건)
  Status: SUCCESS

## 내부 공유용 Deck 개요/슬라이드 제작 (2026-09-14)

[16:00] ACTION: 사용자 요청 — GD/TED 종합 리서치(기전/병리생태, 증상/진단/병기/역학, SoC, 임상-전임상 파이프라인) 내부 공유용 deck 개요 작성(20장 내외). eTPD(Section E) 시사점은 범위 외로 명시적 제외
  Action: report.md Section A-D + reference.md 기반으로 20슬라이드 + Appendix 구조 설계, GD_TED_deck_outline_260914.md 작성/프로젝트 저장
  Status: SUCCESS

[16:05] ACTION: 사용자가 개요 전체(Appendix 포함) 승인 + 슬라이드 제작 지시, 레이아웃 참고자료로 DW_eTPD_Target_DeepDive_하자인_백설련_260827_ing_v8.pptx(87슬라이드, eTPD 3개 타겟 리뷰 덱) 지정
  - project_read로 v8.pptx 전체 텍스트 추출(87슬라이드) 확인 — 단, project_read는 텍스트 추출만 반환하고 원본 바이너리(테마/폰트/색상/마스터 레이아웃)에는 접근 불가함을 확인(local_path 미제공)
  - 구조적 패턴만 추출해 참고: "[주제] – [하위주제]" 제목 컨벤션, 구분/내용/시사점 3열 표, 섹션 구분용 divider 슬라이드(타겟명 + "-"), 인용 footer, 색상 강조박스(경고/gap 박스)
  - 시각 테마(색상/폰트)는 원본 접근 불가로 자체 설계 — 갑상선/안구 질환 주제에 맞춘 네이비-틸-코럴 팔레트 신규 채택(참고 덱과 무관), 한글 폰트는 맑은 고딕 지정
  Status: PARTIAL(레이아웃 텍스트 구조는 반영, 원본 시각 테마 자체는 재현 불가 — 사용자에게 고지 필요)

[16:10] ACTION: pptx skill(SKILL.md) 확인 후 pptxgenjs로 실제 슬라이드 빌드 시작. 29슬라이드 구성: 표지(1) + Executive Summary(1) + Section 1~4 각 divider+본문(6+4+4+3=17, divider 4장 포함 21) + Close(1) + Appendix divider(1) + Appendix 본문(4) = 29
  - GD_TED_deck_outline_260914.md의 가운뎃점(·) 5건 발견 및 수정(슬래시로 대체) — 사용자 표준 선호 반영
  - 모든 슬라이드에 [n] 인용 번호를 reference.md와 1:1 대응 유지, QA 체크리스트 PARTIAL/미확보 항목을 Slide 4/13/20/Appendix에 투명하게 노출(은폐하지 않음)
  - validate.py 전체 PASS, markitdown 콘텐츠 QA(placeholder/lorem/TODO 등) 0건, LibreOffice 렌더링 기반 시각 QA로 전 슬라이드 육안 확인 — overflow/overlap 발견분(Executive Summary 5번 항목, TED 역학 표 겹침) 수정 후 재검증 완료
  Result: GD_TED_deck_260914.pptx 생성 완료(29슬라이드), SendUserFile로 전달 및 프로젝트에 claude/GD_TED_deck_260914.pptx로 저장
  Status: SUCCESS

## 별도 트랙 — Market Sizing & TSAb-IgG Coverage 분석 (2026-09-14, 신규 세션)

> 본 트랙은 GD_TED_plan.md(Section A-E, 질적 disease landscape)와 별개로, 사용자 요청("GD/TED 각각의 시장성 range + TSAb-IgG targeting coverage")에 따라 market-sizing-multitrack 스킬을 경량 적용한 작업. 별도 계획서 `GD_TED_market_sizing_plan.md`(사용자 메모리에 저장, 승인 완료: range 우선 경량 방식/Global+7MM/TSAb 광의 정의/본 프로젝트 귀속)에 따라 진행.

[17:00] ACTION: market-sizing-multitrack 스킬 SKILL.md 검토 — 2x2 트랙 프레임(top-down/bottom-up × current/premium) 및 Step 0 causality gate(Driver/Co-driver/Epiphenomenon)가 이번 coverage 질문에 적합, Step 7 기본 산출물(Excel 풀모델)은 과설계로 판단 → 경량화 적용 계획 수립, 사용자 승인 완료(AskUserQuestion 4문항: 작업 깊이/지역/TSAb 프레이밍/귀속)
  Status: SUCCESS

[17:05] TOOL: WebSearch ×3 — GD 시장규모, TED 시장규모, TEPEZZA 매출 검색
  TOOL: WebFetch ×9 — IMARC/Precedence/MarketResearchFuture(GD)/SkyQuest(GD 4건), GlobeNewswire/Mordor/DelveInsight/MarketResearchFuture(TED)/ReportsAndData(TED 5건), Amgen FY2025 실적발표(anchor)
  Result: GD 4건(base $2.26B-$4.56B, forecast $3.69B-$6.78B), TED 5건(base $0.17B-$5.36B — 1건 이상치, forecast $0.31B-$11.81B), teprotumumab FY2025 실매출 $1.90B 확보
  Status: SUCCESS — TED 5건 중 1건(MarketResearchFuture #27903, $165.4M)이 다른 4건 대비 20-30배 작아 이상치로 플래그(스코프 상이 추정)

[17:15] TOOL: PubMed search_articles/get_article_metadata — TSAb-IgG coverage 분석용 GD 혈청양성률/TED 혈청음성 비율 검색
  Result: GD — TSI/TRAb assay sensitivity 메타분석 확보(TSI 93.3%, TRAb 88.9%, Jiang 2025)[PMID 40789418], 단일기관 비교연구(van Balkum 2023, 병용 시 95.6% 확진력)[PMID 38107298] — GD coverage 약 90-95%로 추정 가능. TED — 인구기반 혈청음성 비율 직접 문헌은 미확인(검색된 것은 Hashimoto's 동반 TRAb-음성 안와병증 희귀 증례보고 수준)[PMID 33246456, 30621642] → GD_TED_report.md Section A1의 GD 비동반 비율(~10%)을 대리 추정치로 채택, 직접 정량 문헌 부재는 gap으로 명시
  Status: PARTIAL — TED 혈청음성 비율의 직접 인구기반 문헌 미확보(최종 리포트에 gap으로 명시, 임의 숫자 창작하지 않음)

[17:25] ACTION: Reconciliation 수행 — GD/TED 각각 median(FLOOR)/median(PREMIUM)/spread 계산, teprotumumab 실매출과 top-down 추정치 간 괴리(약 2.4배) 분석 및 해석 제시, GD-TED population overlap으로 인한 비합산 원칙 명시(스킬 Step 5.6 준용)
  Status: SUCCESS

[17:30] ACTION: `claude/GD_TED_market_sizing_report.md` 작성/저장(present_to_user: true) — Executive Summary/스코프/Track A·B raw data(GD 4건+TED 5건+anchor)/Reconciliation(FLOOR·PREMIUM·spread·anchor 괴리·overlap)/TSAb-IgG Coverage 분석(GD vs TED 비교표)/한계 및 후속 권고/출처 전체 반영
  Status: SUCCESS

Market Sizing 트랙 1차 완료 — 후속 권고 6건(Track C/D 확장, TED 리포트 스코프 재확인, DelveInsight 원문 확보, **TED 혈청음성 비율 정량 문헌 확보(최우선 gap)**, 실매출 anchor 확대, GD 신약 승인 시나리오 재평가) report.md §5에 기록.
