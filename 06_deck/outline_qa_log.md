---
linear_issue: JHA-86
created: 2026-10-01
source: claude-code
milestone: cluster-6-deck
status: draft
---

# GD/TED report deck outline — QA 및 수치 조정 로그

본 문서는 `GD_TED_report_deck_outline.md` 작성 과정의 (1) 입력 간 수치 충돌 조정, (2) 인용 무결성 검증, (3) outline 단계 QA 체크리스트, (4) 잔여 gap을 기록한다. 신규 사실 수집은 수행하지 않았고 repo 자료 내부 정합성 확인과 인용 존재 검증만 수행했다.

## 1. 조정 규칙

1. **as-of 우선순위**: Biomni v2 frozen cut(2026-09-10)과 cluster 재검증본(2026-09-24~10-01)이 다르면 재검증본을 채택하고 두 날짜를 슬라이드 source line에 병기한다.
2. **legacy 우선순위**: `00_legacy_unsorted/`는 동결 문서이므로, 동일 항목을 다룬 cluster 산출물이 있으면 cluster를 채택한다.
3. **합산 금지**: 서로 다른 endpoint, 모집단, 추적기간의 수치를 하나의 비율이나 금액으로 합치지 않는다.
4. **해소 불가**: 어느 쪽도 우위를 판정할 수 없으면 양쪽을 분모와 함께 병기한다.

## 2. 수치 충돌과 조정 결과

| # | 항목 | 입력 A | 입력 B | 조정 | 슬라이드 |
|---|---|---|---|---|---|
| C1 | 파이프라인 자산 수 | legacy C4: 72개 프로그램, active 51 / discontinued 21 | v2: 48 asset rows | **어느 쪽도 `active 자산 수`로 쓰지 않음.** 정규화 단위가 다르고(commercial pipeline vs registry intervention inventory) legacy 원표는 비공개이므로 역산 불가. 덱은 자산 수 대신 `자산 x 적응증 최고 active 단계` 매트릭스만 제시 | 27 |
| C2 | ATD 재발률 | legacy C1: 단일기관 코호트, MMI 중단 1년 이내 35%. 계획서 원안 `~50% @18개월`은 미확인 | JHA-70: Azizi RCT, 84개월 relapse 통상군 56% / 장기군 17% | **JHA-70 채택.** 단일 RCT 결과임과 protocol 외 일반화 제한을 commentary에 명시. legacy 35%와 원안 50%는 덱에서 사용하지 않음 | 18, 19 |
| C3 | Teprotumumab 재발/지속성 | legacy: 모집단 재발률 `~25%` 원안 수치 미확인. OPTIC-X 48주 유지 90.6% | JHA-71: pooled Week 72 proptosis response 38/56, 최종 dose 후 99주 내 추가 치료 19/106(17.9%); 독립 real-world n=21 중 initial responder 17명 중 8명(47%) reactivation | **해소 불가, 병기.** 시험 추적 집단과 독립 real-world series는 분모/정의/추적기간이 달라 하나로 합치지 않음. 원안 `~25%`는 사용하지 않음 | 24 |
| C4 | TED PREMIUM TAM | legacy market sizing: `$8.09B로 보수적 채택` | JHA-82: 기계적 median은 $7.50B이며 $8.09B는 협의 scope 이상치($0.3051B) 제외 후 3건 median | **JHA-82 채택.** `보수적 채택`이라는 표현을 `scope-adjusted 대표값`으로 교체 | 41 |
| C5 | Batoclimab GD POC 반응률 | 68.8% 단독 인용 가능성 | JHA-74/JHA-84: 68.8%는 정상화 **또는** LLN 미만 composite, 순수 정상화 53.1%, off-ATD 31.3%(n=32 단일군) | **세 수치 병기 필수.** 68.8% 단독 인용은 과대평가로 명시 | 36 |
| C6 | efgartigimod GD Phase 3 명칭 | legacy: `VitaliThy` | JHA-74: NCT07570316/07596849를 명칭 없이 기재 | **2026-10-01 ClinicalTrials.gov 직접 조회로 해소.** NCT07570316의 공식 acronym이 `VitaliThy`임을 확인. 덱에서 병기 | 37 |
| C7 | MER511 class 분류 | 입력 CSV 계열: TSHR receptor 길항 | JHA-73 2026-09-29 cross-confirm: anti-TSHR autoantibody 제거/항원특이 면역조절 | **JHA-73 채택.** 정상 TSH signaling 보존을 회사가 명시하므로 receptor 길항제로 분류하지 않음 | 28, 38 |
| C8 | Rilzabrutinib 적응증 | `pipeline_assets_v2.csv`: Active TED | JHA-73: frozen registry condition/title/FT4 endpoint 기준 GD P2 | **JHA-73 채택** | 27, 28 |
| C9 | KHN939 / SCTT11 표적 | 입력에서 IGF-1R 계열로 묶일 여지 | JHA-73: 공개 registry와 CSV 모두 target 미확인 | **`표적 미공개`로 분리.** 기전을 부여하지 않음 | 27, 28 |
| C10 | Chronic/inactive TED의 systemic option 유무 | legacy C6: `inactive TED 승인 치료 전무` | JHA-87: 미국에서 teprotumumab/veligrotug가 activity/duration 무관 승인, 중국 IBI311 승인, teprotumumab chronic trial 근거 존재 | **JHA-87 채택.** `전무`가 아니라 지역 access, 부적합/무반응, 고정 deficit 잔존으로 재정의 | 23, 45 |
| C11 | TRAb 음성 TED 비율 | legacy 계획서: 5-10% | JHA-87: 원저로 직접 확인되지 않음. assay 병용 불일치 9.4%는 별도 수치 | **`5-10% x TED pool` 계산 금지.** 비율 대신 operational subgroup으로 서술 | 10, 45 |
| C12 | Orbital irradiation 위치 | legacy slide 14: Mayo RCT 6개월 시점 유의한 효과 없음 | JHA-71: stage 3 후속 옵션에 orbital RT+GC 포함 | **병존.** 덱은 JHA-71의 line 위치를 쓰고 RT 단독 근거의 한계는 각주로 유지 | 22 |
| C13 | IGF-1R 청각 AE | legacy C3: 등록임상 7-12% vs 실사용 38.6-81.5% | JHA-76: 청각은 단일 preferred term이 아니며 PT별로 hypoacusis 9.8%, tinnitus 12.0%, ear discomfort 12.0% 등 | **JHA-76 채택.** PT 합산 금지, `미보고`≠0 범례 필수. legacy의 실사용 코호트 수치는 덱 본문에서 사용하지 않음 | 34 |
| C14 | Lu AG22515 Phase 1b 등록 수 | 룬드벡 보도자료: 19명 계획 | NCT06557850: 실제 등록 20명 | **모순 아님.** 19=계획, 20=실제. 덱은 실제 등록 20명 사용 | 39 |

## 3. 인용 무결성 검증

### 3.1 PubMed PMID (2026-10-01, `get_article_metadata` 전수 조회)

| PMID | 확인 결과 |
|---|---|
| 31127272 | Arrestin-β-1 Physically Scaffolds TSH and IGF1 Receptors to Enable Crosstalk. Endocrinology. 일치 |
| 39821041 | Mechanisms in Thyroid Eye Disease: The TSH Receptor Interacts Directly With the IGF-1 Receptor. Endocrinology. 일치 |
| 32911689 | Is There Evidence for IGF1R-Stimulating Abs in Graves' Orbitopathy Pathogenesis? Int J Mol Sci. 일치 |
| 40156685 | In vivo and in vitro evidence for a protective role of autoantibodies against IGF-1R in Graves' orbitopathy. Endocrine. 일치 |
| 40071798 | Antibodies against IGF-1R, IGF-1, and IGFBP-3 in the serum of patients with Graves' and Basedow's disease. Endokrynol Pol. 일치 |
| 38824618 | Long-Term Efficacy of Teprotumumab in Thyroid Eye Disease. Thyroid. 일치 |
| 38142982 | Reactivation After Teprotumumab Treatment for Active Thyroid Eye Disease. Am J Ophthalmol. 일치 |
| 21591944 | Selenium and the course of mild Graves' orbitopathy. N Engl J Med. 일치 |
| 30081019 | Efficacy of Tocilizumab in Corticosteroid-Resistant Graves Orbitopathy. Am J Ophthalmol. 일치 |
| 25343233 | Randomized controlled trial of rituximab in patients with Graves' orbitopathy. J Clin Endocrinol Metab. 일치 |
| 38165576 | Risk of recurrence at withdrawal of short- or long-term methimazole therapy. Endocrine. 일치 |
| 33914484 | Outcomes of Graves' Disease Patients Following ATD, RAI, or Thyroidectomy as First-line. Ann Surg. 일치 |
| 40301067 | Safety, PK, and potential benefits of K1-70 in Japanese Graves' disease patients, phase 1. Endocr J. 일치 |
| 41389254 | Factors predicting cure at one year after RAI in Graves' disease. Hell J Nucl Med. 일치 |
| 42374926 | Stimulating TSHR Antibodies Enhance Expression of Both TSHR and IGF-1R in Fibroblasts. Thyroid. 일치 |

**결과: 15/15 PASS.**

### 3.2 ClinicalTrials.gov NCT

| NCT | 본 세션 직접 확인 | 결과 |
|---|---|---|
| NCT07570316 | 수행(2026-10-01) | PHASE3, RECRUITING, acronym **VitaliThy**, sponsor argenx, conditions Graves' Disease, enrollment 230, primary = Week 24 euthyroid off-ATD, secondary에 TRAb seronegativity. repo 기술과 일치하며 명칭 충돌(C6) 해소 |
| NCT05176639 | 수행(2026-10-01) | PHASE3, COMPLETED, acronym **THRIVE**, sponsor Viridian, enrollment 113, primary = Week 15 PRR, has_results=true. repo 기술과 일치 |
| NCT03298867, NCT04583735, NCT06021054, NCT05276063, NCT05987423, NCT06106828, NCT03938545, NCT06307613, NCT06307626, NCT07305818, NCT07682896, NCT06569758, NCT06727604, NCT07018323, NCT06557850 | 미수행 | repo 내 독립 QA 세션이 2026-09-29~10-01에 phase/status/condition을 registry 원문 direct quote로 대조한 기록이 있음(`moa_phase_matrix_extended_qa.md` 3절, `fcrn_entry_strategy_ir_review_qa.md` 3절, `r1b_asset_identification.md` 검증 로그). 본 세션은 그 기록을 승계하며 **독립 재검증은 수행하지 않았음**을 명시 |

## 4. outline 단계 QA 체크리스트

| 항목 | 판정 | 비고 |
|---|---|---|
| Cover, Key Takeaways 3장, Contents 순서 | PASS | slide 1-5 |
| Key Takeaways의 `→ slide N` pointer 유효성 | PASS | 인용된 17, 18, 22, 24, 12, 14, 41, 42, 29, 30, 44, 45, 46 모두 실재 |
| Contents의 6개 섹션과 divider 1:1 대응 | PASS | slide 6, 11, 17, 26, 40, 44 |
| 모든 content 슬라이드에 archetype 1개 지정 | PASS | T4-T13 배정 완료 |
| 모든 content 슬라이드에 evidence grade 지정 | PASS | 최저 등급 기준 |
| 모든 content 슬라이드에 exhibit banner(대상/범위/as-of) 지정 | PASS | 표/차트 보유 슬라이드 전수 |
| 제목이 결론 문장(assertion)이며 topic label 미사용 | PASS | `개요`, `현황` 등 미사용. 단, 한국어 45자 초과 후보 5건은 렌더링 시 재단 필요(6절) |
| 적색 점선 영역 슬라이드당 1개 이하 | PASS | slide 19, 45 각 1개 |
| 색/scale이 의미를 담는 슬라이드에 범례 지정 | PASS | slide 23, 25, 27, 29, 32, 34, 47 |
| 추정치에 E 접미 | PASS | slide 41, 42, 51 |
| 의견을 Our view/Considerations 박스로 격리 | PASS | slide 15, 19(주석), 35, 36, 37, 39, 46, 49 |
| cross-trial 비교 금지 표시 | PASS | slide 29, 34 각주 |
| 마케팅 언어 | PASS | 미사용 |
| 가운뎃점 미사용 | PASS | 슬래시/쉼표/세미콜론 사용 |
| 영어 기술 용어 유지 | PASS | TSHR, IGF-1R, TSAb, CAS, FcRn, PRR 등 |
| Appendix와 Sources 존재 | PASS | slide 53-55 |
| 그림 슬롯 4레벨(구조/조직/세포/signaling) 배치 | PASS | slide 7, 12, 13, 14 |
| Reader test(제목만으로 Key Takeaways 논증 재현) | PARTIAL | S4가 11장으로 길어 slide 33-34(IGF-1R 자산/AE)와 slide 38(TSHR 축)의 제목이 같은 층위에서 반복될 여지. 렌더링 시 재검토 |
| 렌더링 QA(이미지 확인, overflow) | 미수행 | outline 단계 범위 밖. 승인 후 수행 |

## 5. 잔여 gap

덱 slide 52에 그대로 노출할 항목이다.

| # | gap | 상태 | 해소 경로 |
|---|---|---|---|
| G1 | 7MM 개별국가(DE/FR/UK/IT/ES) GD/TED 역학 수치 | 미확보 | 상업 report 원문 scope 확보 또는 국가별 claims DB |
| G2 | TED active-to-inactive Th1/Th2 cytokine milieu 전환 문헌 | 미확보 | 추가 PubMed 라운드(본 작업 범위 밖) |
| G3 | TSHR ectodomain shedding 정량치 | 미확인 | PMID 1497642 전문 확보 후 군별 농도/단위/assay 성능 검토 |
| G4 | TED 직접 TSAb-positive population estimate | 미확보 | cohort 자료 확보 전까지 TED mechanism SAM은 NR 유지 |
| G5 | Lumvoa 공식 unit WAC, HCPCS, CMS payment limit | 미확인 | HCPCS quarterly update 및 CMS ASP file 모니터 |
| G6 | 2026년 Tepezza unit WAC | 미확인 | 2020년 출시 WAC와 2026년 signal의 직접 비교 금지 유지 |
| G7 | MER511, LCA-0321, GenSci098의 final clinical construct | 미확정 | sponsor confirmation 또는 asset-code 포함 후속 공시 |
| G8 | Clone competitiveness 평가기준 | 미착수 | JHA-85 |
| G9 | eTPD 분자 스펙 초안 | 미착수 | JHA-88 |

## 6. 렌더링 전 처리 필요 항목

1. 한국어 제목 45자 초과 후보: slide 19, 24, 29, 39, 43. 의미 손실 없이 재단하거나 bold prefix 사용.
2. `_shared/deck_style.md`를 report-deck-style v0.4로 갱신(archetype 코드, outline 포맷, 렌더 경로).
3. Biomni v2 figure 6종은 assertion 구조와 불일치하므로 기본 미사용. figure 3만 slide 27 보조로 재사용 검토.
4. 본 세션은 읽기 전용 clone이므로 repo push는 별도 수행.
