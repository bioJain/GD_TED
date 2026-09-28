---
linear_issue: JHA-80
created: 2026-09-28
source: claude-code
milestone: cluster-3-mechanism-deepdive
status: done
inputs:
  - 00_legacy_unsorted/meeting_notes_organized_260922.md
---

# "R1b" 확인 — 에이프릴바이오 중단자산 타겟 추정

## 결론 요약

| 항목 | 결론 |
|---|---|
| 타겟 추정 | **추정 (확정 아님, 그러나 근거 강함)** — "R1b"는 특정 유전자/단백질 타겟의 약어가 아니라, 에이프릴바이오(April Bio)가 룬드벡(Lundbeck)에 기술수출한 **APB-A1(사내 코드) / Lu AG22515(룬드벡 코드)**의 갑상선안병증(TED) 적응증 **임상 1b상(Phase 1b)**을 가리킨 것으로 추정됨. 해당 자산의 타겟은 **CD40L(CD40 ligand, CD154) 저해**(CD40-CD40L costimulatory pathway 차단)이며, cytokine 자체는 아니지만 사용자가 원 메모에서 언급한 "cytokine 계열 가능성"과 궤를 같이하는 면역조절(costimulatory/TNF superfamily) 기전임 |
| 중단 여부 | **확인됨** — 2026-08-19 룬드벡이 APB-A1(Lu AG22515)의 **TED 적응증 개발을 중단**한다고 발표. 단, 회사 전체 asset 폐기나 SAFA 플랫폼 문제가 아니라 "TED 적응증에 CD40L 타겟이 최적이 아니었다"는 적응증-특이적 중단이며, 다른 적응증에서 재개 검토 중 |
| GD/TED 연관성 | **있음(직접적)** — 원 후보(OX40L/IL-4R/IL-18BP)는 모두 배제되었으나, 실제 확인된 자산(APB-A1/CD40L)은 다른 후보들보다 오히려 본 프로젝트와 직접적 관련성이 더 큼: TED 환자 대상 임상이었고, TSHR 자가항체(autoantibody) 저해라는 GD/TED 핵심 병인 경로에 작용을 시도한 사례 |

---

## 1. 조사 경위

메모 원문 조각 "R1b"의 문맥은 확인 불가하나, 2026-09-23 사용자 클라리피케이션에 따라 "IGF1R이 아니라 에이프릴바이오가 개발하다 중단한 에셋의 타겟"으로 추정하고 조사를 시작함. 이슈에 제시된 후보(OX40L, IL-4R, IL-18BP)를 우선 확인한 결과:

- **IL-18BP (APB-R3)**: 에이프릴바이오의 SAFA 플랫폼 기반 자산으로 Evommune에 기술수출됨. IBD/류마티스 관절염 적응증으로 **Phase 2a 진행 중**이며 중단된 자산이 아님[1][2]. → **배제**
- **OX40L (IMB-101)**: OX40L x TNF-α 이중항체 후보물질이나, 이는 2016년 HK이노엔/와이바이오로직스 공동연구에서 유래해 2020년 아이엠바이오로직스(IMBiologics)로 이관된 프로그램으로, 에이프릴바이오 자체 중단자산이라 보기 어려움[3]. → **배제**
- **IL-4R**: 공개 검색 범위 내에서 에이프릴바이오의 IL-4R 타겟 파이프라인 자체를 확인하지 못함. → **배제(근거 부재)**

후보가 모두 배제된 상태에서 "중단(discontinued)"이라는 키워드로 재검색한 결과, 2026-08-19 발표된 **APB-A1(Lu AG22515)의 TED 적응증 개발 중단** 뉴스가 확인됨. 이 자산의 임상 단계가 정확히 **"1b상"**이었다는 점에서, 원 메모 조각 "R1b"가 (a) 타겟 약어가 아니라 (b) **"임상 1b상"을 가리키는 표기가 와전/오기된 것**일 가능성이 높다고 판단함. 이 경우 사용자의 원 추정("타겟을 지칭")과 실제 사실("임상 phase를 지칭") 사이에 해석 차이가 있으나, 지칭 대상 자산(에이프릴바이오 중단자산) 자체는 동일하게 식별됨.

## 2. 확인된 사실 — APB-A1 / Lu AG22515

| 항목 | 내용 | 출처 |
|---|---|---|
| 자산명 | APB-A1(에이프릴바이오 코드) = Lu AG22515(룬드벡 코드) | [4][5] |
| 플랫폼 | SAFA(albumin-binding Fab fusion, 반감기 연장) | [1] |
| 타겟/기전 | CD40-CD40L(CD154) costimulatory pathway 차단(CD40L 저해) | [4][6] |
| 기술이전 | 2021년 에이프릴바이오 → 룬드벡(Lundbeck) 아웃라이선스 | [5] |
| 적응증 | 갑상선안병증(TED), moderate-to-severe active TED 환자 대상 | [7] |
| 임상 경과 | Phase 1a 완료(2023-08) → Phase 1b 개시(2024-09, 중등도-중증 활동성 TED 환자 19명) | [7] |
| 중간 분석 신호(2025-11) | 안구돌출(proptosis) 약 2.06mm 감소, TSHR 자가항체(TRAb) 저하 등 기전 관여(target engagement) 확인 | [7][6] |
| 중단 발표 | 2026-08-19, 룬드벡이 TED 적응증 개발 중단 발표 | [6][8] |
| 중단 사유 | "CD40-CD40L 생물학적 활성(자가항체 감소)은 확인되었으나, 기대 수준의 임상적 효과로 이어지지 않음" — SAFA 플랫폼이 아닌 "TED 적응증에 CD40L 타겟이 적합하지 않다"는 타겟-적응증 매칭 문제로 설명됨 | [8][9] |
| 향후 계획 | 개발 완전 중단이 아니며, CD40-CD40L 경로가 더 직접적으로 관여하는 다른 적응증에서 재개 검토 중. 이미 확보된 Phase 1 안전성/내약성 데이터로 큰 지연은 없을 것이라는 입장 | [9] |

확인일: 2026-09-28 (모든 항목 공개 뉴스/IR 자료 기준, 공시 원문 또는 임상시험 등록 페이지 직접 대조는 미수행)

## 3. GD/TED 연관성 판단

**연관성 있음(직접적).** 원래 후보로 제시되었던 OX40L/IL-4R/IL-18BP는 GD/TED와 직접적 연관 근거가 약하거나(OX40L은 자가면역 전반 겨냥, 회사 고유 자산도 아님) 확인 불가했던 반면, 실제로 식별된 자산(APB-A1/CD40L)은:

1. **TED 환자를 직접 대상으로 한 임상 자산**이었음(본 프로젝트의 핵심 적응증과 동일)
2. **TSHR 자가항체(TRAb) 저해**라는, GD/TED 병인의 핵심 축(TSAb-TSHR 자가면역 경로)에 직접 작용을 시도한 사례로, 기존 `GD_TED_report.md`의 TSHR/TSAb 병인 논의(Section B/D)와 mechanism 수준에서 연결됨
3. **"target engagement 성공 + 임상적 효과 부족"**이라는 실패 패턴은 eTPD 자산 설계 시 중요한 선례로 참고 가능 — TSHR 자가항체 수치를 낮추는 것 자체가 임상적 개선(proptosis, CAS 등)으로 충분히 이어지지 않을 수 있다는 시사점을 제공하며, 이는 03_mechanism_deepdive 트랙의 다른 산출물(`orbital_fibroblast_igf1r_maturity.md`)이 다루는 "biomarker 변화 ≠ 임상 효과" 논점과도 맥락이 닿음

다만 CD40L 자체가 GD/TED eTPD 설계의 직접적 경쟁/대안 타겟으로 재검토할 만한지(예: Section C4 파이프라인 매트릭스에 추가할지)는 본 이슈의 범위를 넘어서므로 별도 판단 이슈로 남김.

## 4. 한계 및 잔여 불확실성

- 원 메모 조각 "R1b"의 정확한 문맥(작성 당시 화자의 의도)은 확인할 수 없음 — 본 결론은 "타겟 후보 배제 + 유일하게 부합하는 중단 사례 발견"이라는 정황 추론이며, 원문 대조가 불가능하므로 **완전한 확정(100%)은 아님**
- "R1b = Phase 1b" 해석이 "R1b = 특정 타겟 약어"라는 사용자의 원 추정과 결이 다르다는 점은 명시해 둠. 다만 사용자가 지칭하려던 실체(에이프릴바이오 중단자산)는 동일하게 특정됨
- 본 조사는 공개 뉴스/IR 자료에 한정되었으며, 상업 DB(Cortellis 등) 또는 룬드벡/에이프릴바이오 공시 원문 직접 대조는 수행하지 않음

## 참고문헌

[1] SAFA (anti-Serum Albumin Fab Associated) platform technology, Medicines Patent Pool LAPAL. https://lapal.medicinespatentpool.org/technology/safa-anti-serum-albumin-fab-associated-platform-technology/print (확인일 2026-09-28)

[2] bqura, "AprilBio's IL-18 Inhibitor 'APB-R3' Begins Phase 2 Trial". https://bqura.com/posts/300 (확인일 2026-09-28)

[3] 데일리팜, "면역질환 경쟁력 '쑥'...K-바이오, 잇단 기술수출 성과" (IMB-101/OX40L 연혁 관련). https://m.dailypharm.com/user/news/15784 (확인일 2026-09-28)

[4] 메디파나뉴스, "에이프릴바이오, CD40L 기반 신약 임상·적응증 확대 본격화". https://www.medipana.com/news/articleView.html?idxno=342346 (확인일 2026-09-28)

[5] 이투데이, "에이프릴바이오 '룬드벡, APB-A1 갑상선안병증 환자대상 임상개시'". https://www.etoday.co.kr/news/view/2406436 (확인일 2026-09-28)

[6] 한국경제, "에이프릴바이오 '룬드벡, APB-A1 개발 중단 아니다'". https://www.hankyung.com/article/202608190405i (확인일 2026-09-28)

[7] 더바이오, "에이프릴바이오 기술수출 'APB-A1', TED 1b상서 안구돌출 2.06㎜↓". https://www.thebionews.net/news/articleView.html?idxno=25523 (확인일 2026-09-28)

[8] 머니투데이, "에이프릴바이오, 'APB-A1' 개발 방향 전환…'지연 길지 않을 것'". https://www.mt.co.kr/thebio/2026/08/20/2026082013224473307 (확인일 2026-09-28)

[9] 더바이오, "에이프릴바이오 '룬드벡, APB-A1 개발 중단 아니다'" 관련 후속 보도. https://www.thebionews.net/news/articleView.html?idxno=27397 (확인일 2026-09-28)

## 검증 로그

| Claim | Tier | 검증 방법 | 결과 | 일자 |
|---|---|---|---|---|
| APB-A1(Lu AG22515) 타겟이 CD40L이며 TED 적응증 개발이 2026-08-19 중단됨 | 상(중단 사실/적응증) | 복수 독립 언론사(한국경제, 머니투데이, 메디파나뉴스, 더바이오) 교차확인 | PASS(교차확인 완료, 1차 공시/IR 원문 직접 대조는 미수행 — cross-model 검증 별도 세션 권고) | 2026-09-28 |
| Phase 1b 중간 분석 proptosis 2.06mm 감소, TRAb 저하 신호 | 중(정량 수치, mechanism) | 단일 매체(더바이오) 기사 기반, 추가 출처 미확보 | PARTIAL(단일 출처, 복수 출처 교차확인 권장) | 2026-09-28 |
| OX40L(IMB-101)/IL-4R/IL-18BP(APB-R3) 후보 배제 근거 | 하(정성적 배제 판단) | 공개 뉴스/DB 검색 | PASS | 2026-09-28 |
