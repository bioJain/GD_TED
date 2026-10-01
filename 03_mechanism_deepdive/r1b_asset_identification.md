---
linear_issue: JHA-80
created: 2026-09-28
source: claude-code
milestone: cluster-3-mechanism-deepdive
status: in-review
inputs:
  - 00_legacy_unsorted/meeting_notes_organized_260922.md
  - 00_baseline_biomni/landscape_v2/clinical_trials_v2.csv
---

# "R1b" 확인 — 에이프릴바이오 중단자산 타겟 추정 (+ Amgen dazodalibep c.f. 비교)

## 결론 요약

| 항목 | 결론 |
|---|---|
| 타겟 추정 | **추정 (확정 아님, 그러나 근거 강함)** — "R1b"는 특정 유전자/단백질 타겟의 약어가 아니라, 에이프릴바이오(April Bio)가 룬드벡(Lundbeck)에 기술수출한 **APB-A1(사내 코드) / Lu AG22515(룬드벡 코드)**의 갑상선안병증(TED) 적응증 **임상 1b상(Phase 1b)**을 가리킨 것으로 추정됨. 해당 자산의 타겟은 **CD40L(CD40 ligand, CD154) 저해**(CD40-CD40L costimulatory pathway 차단)이며, cytokine 자체는 아니지만 사용자가 원 메모에서 언급한 "cytokine 계열 가능성"과 궤를 같이하는 면역조절(costimulatory/TNF superfamily) 기전임 |
| 중단 여부 | **확인됨** — 2026-08-19 룬드벡이 APB-A1(Lu AG22515)의 **TED 적응증 개발을 중단**한다고 발표. 단, 회사 전체 asset 폐기나 SAFA 플랫폼 문제가 아니라 "TED 적응증에 CD40L 타겟이 최적이 아니었다"는 적응증-특이적 중단이며, 다른 적응증에서 재개 검토 중 |
| GD/TED 연관성 | **있음(직접적)** — 원 후보(OX40L/IL-4R/IL-18BP)는 모두 배제되었으나, 실제 확인된 자산(APB-A1/CD40L)은 다른 후보들보다 오히려 본 프로젝트와 직접적 관련성이 더 큼: TED 환자 대상 임상이었고, TSHR 자가항체(autoantibody) 저하라는 GD/TED 핵심 병인 경로 관련 downstream biomarker 신호를 관찰한 사례(단, 비대조 Phase 1b이므로 인과성/target engagement 확정 아님) |

---

## 1. 조사 경위

메모 원문 조각 "R1b"의 문맥은 확인 불가하나, 2026-09-23 사용자 클라리피케이션에 따라 "IGF1R이 아니라 에이프릴바이오가 개발하다 중단한 에셋의 타겟"으로 추정하고 조사를 시작함. 이슈에 제시된 후보(OX40L, IL-4R, IL-18BP)를 우선 확인한 결과:

- **IL-18BP (APB-R3)**: 에이프릴바이오의 SAFA 플랫폼 기반 자산으로 2024년 Evommune에 기술수출되어 **EVO301**으로 명명됨. **중등도-중증 아토피 피부염(AD)** 적응증 Phase 2a(무작위/이맹검/위약대조, n≈60)가 2026-02 완료되어 1차 endpoint(EASI) 충족을 보고했으며, Phase 2b 용량탐색 시험을 진행 예정임 — 중단된 자산이 아님[1][2][19][20]. IBD는 전임상/번역 근거 수준에서 언급된 적응증이며 임상 개발 적응증이 아님. → **배제**
- **OX40L (IMB-101)**: OX40L x TNF-α 이중항체 후보물질이나, 이는 2016년 HK이노엔/와이바이오로직스 공동연구에서 유래해 2020년 아이엠바이오로직스(IMBiologics)로 이관된 프로그램으로, 에이프릴바이오 자체 중단자산이라 보기 어려움[3]. → **배제**
- **IL-4R**: 공개 검색 범위 내에서 에이프릴바이오의 IL-4R 타겟 파이프라인 자체를 확인하지 못함. → **배제(근거 부재)**

후보가 모두 배제된 상태에서 "중단(discontinued)"이라는 키워드로 재검색한 결과, 2026-08-19 발표된 **APB-A1(Lu AG22515)의 TED 적응증 개발 중단** 뉴스가 확인됨. 이 자산의 임상 단계가 정확히 **"1b상"**이었다는 점에서(스폰서 룬드벡의 시험 개시 보도자료가 명시적으로 "proof-of-concept phase Ib trial"로 표기함[18]), 원 메모 조각 "R1b"가 (a) 타겟 약어가 아니라 (b) **"임상 1b상"을 가리키는 표기가 와전/오기된 것**일 가능성이 높다고 판단함. 이 경우 사용자의 원 추정("타겟을 지칭")과 실제 사실("임상 phase를 지칭") 사이에 해석 차이가 있으나, 지칭 대상 자산(에이프릴바이오 중단자산) 자체는 동일하게 식별됨.

## 2. 확인된 사실 — APB-A1 / Lu AG22515

| 항목 | 내용 | 출처 |
|---|---|---|
| 자산명 | APB-A1(에이프릴바이오 코드) = Lu AG22515(룬드벡 코드) | [4][5] |
| 플랫폼 | SAFA(albumin-binding Fab fusion, 반감기 연장) | [1] |
| 타겟/기전 | CD40-CD40L(CD154) costimulatory pathway 차단(CD40L 저해) | [4][6] |
| 기술이전 | 2021년 에이프릴바이오 → 룬드벡(Lundbeck) 아웃라이선스 | [5] |
| 적응증 | 갑상선안병증(TED), moderate-to-severe active TED 환자 대상 | [7] |
| 임상 경과 | Phase 1a 완료(2023-08) → Phase 1b 개시(2024-09, 중등도-중증 활동성 TED 환자 대상, 단일군/비맹검/non-randomized 설계, NCT06557850). **환자 수 19 vs 20 (2026-10-01 QA에서 해소)**: 룬드벡 1차 보도자료(2024-09 시험 개시)는 계획 등록 수를 "19 patients are planned to be enrolled"로 명시하고, ClinicalTrials.gov NCT06557850은 실제 등록(enrollment, ACTUAL) **20명**으로 기록함 — 19=계획, 20=실제 등록으로 상호 모순되지 않음. 저장소 canonical registry extract(`00_baseline_biomni/landscape_v2/clinical_trials_v2.csv`, NCT06557850 행, data cut 2026-09-10)의 n_enrolled=20은 실제 등록 수와 일치. 참고로 레지스트리 phase 필드는 PHASE1이나, 스폰서 보도자료가 "proof-of-concept phase Ib trial"로 명시하므로 1b 표기는 스폰서 1차 출처에 근거함 | [7][17][18] |
| 중간 분석 신호(2025-11) | 안구돌출(proptosis) 약 2.06mm 감소, TSHR 자가항체(TRAb) 저하 신호 관찰. **주의**: 이 시험은 위약대조가 없는 단일군(uncontrolled/single-group) Phase 1b이므로 (a) 이 변화가 치료로 인한 것인지 단독으로 확정할 수 없고, (b) TRAb 감소는 CD40L에 대한 직접적 target engagement/occupancy의 증거가 아니라 distal한 downstream pharmacodynamic biomarker 신호로만 해석해야 함 | [7][6] |
| 중단 발표 | 2026-08-19, 룬드벡이 2026년 상반기 사업자료(Q2 실적 발표)에서 TED 적응증에서의 후속 개발 중단(방향 전환) 발표. **주의**: 임상시험 등록부(NCT06557850)는 data cut 2026-09-10 기준 여전히 ACTIVE_NOT_RECRUITING이며 terminated/withdrawn/suspended로 보고되지 않음 — "중단 발표"가 레지스트리 상태 갱신과 동일하지 않음 | [6][8][17] |
| 중단 사유 | "CD40-CD40L 생물학적 활성(자가항체 감소)은 확인되었으나, 기대 수준의 임상적 효과로 이어지지 않음" — SAFA 플랫폼이 아닌 "TED 적응증에 CD40L 타겟이 적합하지 않다"는 타겟-적응증 매칭 문제로 설명됨 | [8][9] |
| 향후 계획 | 개발 완전 중단이 아니며, CD40-CD40L 경로가 더 직접적으로 관여하는 적응증으로 개발 방향 전환. 룬드벡은 신경면역 분야(다발성경화증 MS, 시신경척수염 NMOSD, 중증근무력증 MG 등)를 후보 적응증으로 제시했고, 파이프라인 페이지에서 Lu AG22515를 Neurology 항목으로 재배치함. 이미 확보된 Phase 1 안전성/내약성 데이터로 Phase 2 재개 시 큰 지연은 없을 것이라는 입장 | [9][21][22] |

확인일: 2026-09-28 (초판, 공개 뉴스/IR 자료 기준) / 2026-10-01 (독립 QA follow-up: 룬드벡 시험 개시 보도자료 및 ClinicalTrials.gov NCT06557850 등록 페이지 direct-quote 대조 수행 — 상세는 검증 로그 참조)

## 3. GD/TED 연관성 판단

**연관성 있음(직접적).** 원래 후보로 제시되었던 OX40L/IL-4R/IL-18BP는 GD/TED와 직접적 연관 근거가 약하거나(OX40L은 자가면역 전반 겨냥, 회사 고유 자산도 아님) 확인 불가했던 반면, 실제로 식별된 자산(APB-A1/CD40L)은:

1. **TED 환자를 직접 대상으로 한 임상 자산**이었음(본 프로젝트의 핵심 적응증과 동일)
2. **TSHR 자가항체(TRAb) 저하**라는, GD/TED 병인의 핵심 축(TSAb-TSHR 자가면역 경로)과 관련된 downstream biomarker 변화가 관찰된 사례로, 기존 `GD_TED_report.md`의 TSHR/TSAb 병인 논의(Section B/D)와 mechanism 수준에서 연결됨(단, CD40L에 대한 직접 target engagement가 입증된 것은 아님 — 위 §2 주의사항 참조)
3. **"downstream biomarker(TRAb) 변화 + 임상적 효과 부족"**이라는 패턴은 eTPD 자산 설계 시 참고할 만한 사례임 — TSHR 자가항체 수치가 낮아지는 신호가 있더라도 임상적 개선(proptosis, CAS 등)으로 충분히 이어지지 않을 수 있다는 시사점을 제공하며, 이는 03_mechanism_deepdive 트랙의 다른 산출물(`orbital_fibroblast_igf1r_maturity.md`)이 다루는 "biomarker 변화 ≠ 임상 효과" 논점과도 맥락이 닿음. 다만 이 시험이 비대조 Phase 1b라는 점에서 "target engagement는 성공했다"는 식의 강한 인과적 결론으로 확장해서는 안 됨

다만 CD40L 자체가 GD/TED eTPD 설계의 직접적 경쟁/대안 타겟으로 재검토할 만한지(예: Section C4 파이프라인 매트릭스에 추가할지)는 본 이슈의 범위를 넘어서므로 별도 판단 이슈로 남김.

## 4. c.f. — Amgen dazodalibep(CD40L) 임상 성공 사례와의 비교 (2026-09-28 추가조사)

같은 CD40L 타겟을 겨냥한 자산 중, Amgen의 **dazodalibep(VIB4920/HZN-4920, 옛 MedImmune/Viela Bio → Horizon Therapeutics → 2023년 Amgen의 Horizon 인수로 편입)**가 2026-09-22 전신 Sjögren's disease Phase 3(OASIZ 301) topline 성공을 발표함[10][11][14]. **에이프릴바이오/룬드벡의 APB-A1과는 별개의 회사/분자로, 자산 자체의 연관성(라이선스, 파생 등)은 없음.** 동일 타겟이 왜 한쪽에서는 실패(TED)하고 다른 쪽에서는 성공(Sjögren's)했는지 비교하면 다음과 같이 **타겟팅 방식/모달리티/적응증/임상디자인이 모두 다름**이 확인됨.

| 비교축 | 에이프릴바이오 APB-A1(Lu AG22515) | Amgen dazodalibep(VIB4920/HZN-4920) |
|---|---|---|
| 개발 주체 | 에이프릴바이오 개발 → 2021 룬드벡 아웃라이선스[5] | MedImmune 개발 → Viela Bio → Horizon Therapeutics → 2023 Amgen이 Horizon 인수(약 278억 달러)로 확보[12][13] |
| 타겟 | CD40L(동일 타겟) | CD40L(동일 타겟) |
| 타겟팅 방식(결합 포맷) | **항체 유래 scFv** — anti-CD40L monoclonal 항체의 CDR 기반 결합 도메인을 사용[4] | **비항체 engineered scaffold(Tn3)** — human tenascin-C 유래 FN3 domain 기반 combinatorial library에서 선별한 binder로, CD40L homotrimer 표면 epitope을 인식. 항체 유래 결합 도메인이 아님[13] |
| 모달리티(구조) | anti-CD40L scFv + anti-albumin Fab(SAFA, "SL335" clone) 융합단백질. **Fc 완전 결여**, 반감기는 혈청알부민 결합을 통한 간접 연장[4] | Tn3 scaffold 2분자 + human serum albumin(HSA) 직접 융합(HSA-Tn3-Tn3 유사 구조). **Fc 완전 결여**, 반감기는 HSA 직접 융합으로 연장[13] |
| Fc/모달리티 설계 배경(공통 맥락) | 1990-2000년대 1세대 anti-CD40L mAb인 ruplizumab(BG9588)/toralizumab(IDEC-131)이 Fc-FcγRIIa(CD32a) 매개 혈소판 응집으로 혈전색전증(뇌졸중, 심근경색, 폐색전 등, 사망 1례 포함)을 일으켜 개발 중단된 역사적 사건이 있음[15][16]. 이후 2세대 anti-CD40L 계열은 Fc를 완전히 제거하거나(Fab/scFv 기반) 변형 Fc(FcγRIIA 결합 제거)를 사용하는 방향으로 진화함[16] | 위와 동일한 역사적 실패(ruplizumab/toralizumab 혈전색전증)를 원천적으로 피하기 위해, **애초에 항체가 아닌 non-Ig scaffold(Tn3)로 설계**하여 Fc 자체를 배제[13] |
| → 두 자산 모두 "1세대 anti-CD40L mAb의 Fc-매개 혈전색전증 문제 회피"라는 동일한 설계 동기를 공유하지만, **APB-A1은 항체 유래 결합부위를 유지한 Fab/scFv 포맷**, **dazodalibep은 항체 자체를 벗어난 non-Ig scaffold 포맷**이라는 점에서 모달리티 진화 경로가 다름 | | |
| 적응증 | **갑상선안병증(TED, Graves' orbitopathy) 단일 적응증**에서 Phase 1b 진행[7] | **전신 Sjögren's disease**를 1차 등록 적응증으로 Phase 3 pivotal 성공, 병행하여 **류마티스관절염(RA)** Phase 2 탐색도 수행[10][11][14] |
| 임상 디자인 | Phase 1b, 중등도-중증 활동성 TED 환자 대상(계획 19명/실제 등록 20명 — 위 §2 표 참조), 위약대조 없는 단일군/비맹검 설계, 1차 목표는 proptosis 개선, 상대적으로 짧은 관찰기간, 초기 개발 단계 규모의 탐색적 시험[7][17][18] | Phase 3 OASIZ 301(pivotal), 1차 endpoint ESSDAI(EULAR Sjögren's Syndrome Disease Activity Index), 48주 관찰, 4주차부터 개선 신호 확인 후 48주까지 지속. 후속 Phase 3(OASIZ 303)도 2026년 4분기 완료 예정[10][11] |
| 결과 | downstream biomarker 신호(TSHR 자가항체/TRAb 감소) 관찰 + 중간분석 proptosis 개선 신호(약 2.06mm)까지 있었으나, 최종적으로 "TED 적응증에 CD40L 타겟이 최적이 아니다"라는 판단으로 **2026-08-19 TED 적응증 개발 중단**[6][8][9] | 1차 endpoint 충족, 통계적으로 유의하고 임상적으로 의미있는 개선을 확인해 **2026-09-22 Phase 3 topline positive 발표**. 애널리스트(Jefferies)는 최대 매출 전망을 10억 달러에서 45억 달러로 상향[11][14] |

**해석 — 무엇이 차이를 만들었는가(중요한 방법론적 유의):**

두 시험은 서로 다른 분자, 질환, 용량/노출, 환자군, 평가변수, 임상디자인(비대조 탐색적 Phase 1b vs pivotal Phase 3)이 동시에 다른 **완전히 confound된 비교**이며, 공개 정보만으로는 어느 한 변수(적응증, 통계적 검정력, 모달리티)를 성패의 "핵심 변수"로 특정하거나 서로 순위를 매길 근거가 없음. 아래는 우열을 가리지 않은 **개별 가설(unranked hypotheses)**로만 제시함:

1. **가설 A — 적응증/병인 차이**: Sjögren's disease/RA는 전신적/확산적 T-B세포 costimulation 이상이 병인의 중심인 반면, TED는 이미 형성된 안와조직 리모델링(fibrosis/adipogenesis)이 만성 활동성 표현형의 상당 부분을 차지함. CD40-CD40L 차단 같은 상류 면역활성화 억제 접근이 국소 조직 리모델링이 진행된 TED에서는 구조적 임상지표(proptosis/CAS) 개선으로 이어지기 더 어려울 수 있다는 가설 — 본 문서 §3-3 및 `orbital_fibroblast_igf1r_maturity.md`의 "biomarker 변화 ≠ 임상 효과" 논점과 방향은 일치하나, 이 비교 자체가 그 가설을 입증하지는 못함
2. **가설 B — 임상디자인/통계적 검정력 차이**: APB-A1의 TED 시험은 비대조 초기 탐색적 Phase 1b(n=19~20)였던 반면, dazodalibep은 pivotal 규모의 Phase 3였음. 룬드벡이 "생물학적 활성은 확인되었으나 임상효과가 기대에 못 미쳤다"고 설명한 점은 참고할 만하나, 이 발언 자체가 검정력 문제를 배제하는 직접 증거는 아님
3. **가설 C — 모달리티/타겟팅 방식 차이**: 결합 포맷(항체 유래 scFv vs non-Ig scaffold) 차이가 효능에 기여했을 가능성을 배제할 근거도, 지지할 근거도 현재 확보되지 않음. 두 분자 모두 1세대 mAb의 Fc-매개 혈전색전증 문제는 해결한 상태라는 점만 확인됨
4. **자산 자체는 무관계(사실로 확인됨)**: 두 자산은 계열이나 라이선스 관계가 없는 완전히 별개의 화합물이며, 우연히 같은 타겟(CD40L)을 서로 다른 시기/기업/적응증에서 겨냥한 사례임

**GD/TED 프로젝트에의 시사점**: 위 confounding 때문에 이 비교만으로 CD40L의 GD/TED eTPD 타겟 적합성을 강화하거나 약화하는 결론을 내릴 수는 없음. 다만 가설 A(적응증/병인 차이) 방향은 다른 03_mechanism_deepdive 산출물의 "biomarker 변화 ≠ 임상 효과" 논점과 궤를 같이하므로, 향후 통제된 근거(예: 동일 적응증 내 모달리티 비교, 또는 동일 모달리티의 적응증 간 비교)가 추가로 필요함. Sjögren's disease Phase 3 성공 사례 자체는 GD_TED_report.md의 line-of-therapy 벤치마크 자산(Tier A 질환 비교군)으로 별도 참고할 가치가 있음(본 이슈 범위 밖, 별도 판단 필요).

## 5. 한계 및 잔여 불확실성

- 원 메모 조각 "R1b"의 정확한 문맥(작성 당시 화자의 의도)은 확인할 수 없음 — 본 결론은 "타겟 후보 배제 + 유일하게 부합하는 중단 사례 발견"이라는 정황 추론이며, 원문 대조가 불가능하므로 **완전한 확정(100%)은 아님**
- "R1b = Phase 1b" 해석이 "R1b = 특정 타겟 약어"라는 사용자의 원 추정과 결이 다르다는 점은 명시해 둠. 다만 사용자가 지칭하려던 실체(에이프릴바이오 중단자산)는 동일하게 특정됨
- 본 조사는 공개 뉴스/IR 자료에 한정되었으며, 상업 DB(Cortellis 등)는 수행하지 않음. 2026-10-01 독립 QA에서 룬드벡 시험 개시 보도자료와 ClinicalTrials.gov 등록 페이지 direct-quote 대조를 수행했으나, 룬드벡 Q2 실적 원문(PDF/IR) 자체의 직접 대조는 보도자료/언론 경유로 대체함

## 참고문헌

[1] SAFA (anti-Serum Albumin Fab Associated) platform technology, Medicines Patent Pool LAPAL. https://lapal.medicinespatentpool.org/technology/safa-anti-serum-albumin-fab-associated-platform-technology/print (확인일 2026-09-28)

[2] bqura, "AprilBio's IL-18 Inhibitor 'APB-R3' Begins Phase 2 Trial". https://bqura.com/posts/300 (확인일 2026-09-28)

[3] 데일리팜, "면역질환 경쟁력 '쑥'...K-바이오, 잇단 기술수출 성과" (IMB-101/OX40L 연혁 관련). https://m.dailypharm.com/user/news/15784 (확인일 2026-09-28)

[4] 메디파나뉴스, "에이프릴바이오, CD40L 기반 신약 임상/적응증 확대 본격화". https://www.medipana.com/news/articleView.html?idxno=342346 (확인일 2026-09-28)

[5] 이투데이, "에이프릴바이오 '룬드벡, APB-A1 갑상선안병증 환자대상 임상개시'". https://www.etoday.co.kr/news/view/2406436 (확인일 2026-09-28)

[6] 한국경제, "에이프릴바이오 '룬드벡, APB-A1 개발 중단 아니다'". https://www.hankyung.com/article/202608190405i (확인일 2026-09-28)

[7] 더바이오, "에이프릴바이오 기술수출 'APB-A1', TED 1b상서 안구돌출 2.06㎜↓". https://www.thebionews.net/news/articleView.html?idxno=25523 (확인일 2026-09-28)

[8] 머니투데이, "에이프릴바이오, 'APB-A1' 개발 방향 전환…'지연 길지 않을 것'". https://www.mt.co.kr/thebio/2026/08/20/2026082013224473307 (확인일 2026-09-28)

[9] 더바이오, "에이프릴바이오 '룬드벡, APB-A1 개발 중단 아니다'" 관련 후속 보도. https://www.thebionews.net/news/articleView.html?idxno=27397 (확인일 2026-09-28)

[10] Amgen, "Amgen Announces Positive Topline Phase 3 Results for Dazodalibep in Moderate-to-Severe Systemic Sjögren's Disease" (2026-09-22). https://www.amgen.com/newsroom/press-releases/2026/09/amgen-announces-positive-topline-phase-3-results-for-dazodalibep-in-moderatetosevere-systemic-sjgrens-disease (확인일 2026-09-28)

[11] MedCity News, "Amgen Drug Meets Goals of Key Test in Common Autoimmune Disease With No Approved Meds". https://medcitynews.com/2026/09/amgen-sjogren-autoimmune-chronic-disease-dazodalibep-cd40l-amgn/ (확인일 2026-09-28)

[12] BioSpace, "Amgen asset from $27.8B Horizon buy scores in Phase 3 Sjögren's study". https://www.biospace.com/drug-development/amgen-asset-from-27-8b-horizon-buy-scores-in-phase-3-sjogrens-study (확인일 2026-09-28)

[13] USPTO Patent, "CD40L-specific TN3-derived scaffolds and methods of use thereof" (dazodalibep 구조 관련 특허). https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/10000553 (확인일 2026-09-28); 및 Synapse PatSnap, "Delving into the Latest Updates on CD40 ligand(Amgen, Inc.)". https://synapse.patsnap.com/drug/bb9802f7663341088f30ff538bd0bd0b (확인일 2026-09-28)

[14] Parameter, "Amgen (AMGN) Shares Surge 4% After Breakthrough Sjögren's Disease Trial Success". https://parameter.io/amgen-amgn-shares-surge-4-after-breakthrough-sjogrens-disease-trial-success/ (확인일 2026-09-28)

[15] ResearchGate, "Anti-CD40L Immune Complexes Potently Activate Platelets In Vitro and Cause Thrombosis in FCGR2A Transgenic Mice". https://www.researchgate.net/publication/44806726 (확인일 2026-09-28)

[16] Frontiers in Immunology, "Clinical applications and challenges of CD40/CD40L signaling regulation in autoimmune diseases" (2026). https://www.frontiersin.org/journals/immunology/articles/10.3389/fimmu.2026.1830312/full (확인일 2026-09-28)

[17] 저장소 내부 canonical registry extract, `00_baseline_biomni/landscape_v2/clinical_trials_v2.csv` (NCT06557850 행, ClinicalTrials.gov 원 출처, data cut 2026-09-10)

[18] H. Lundbeck A/S, "Lundbeck initiates clinical trial in immunology for Lu AG22515 in Thyroid Eye Disease" (시험 개시 보도자료, 2024-09; "proof-of-concept phase Ib trial", "19 patients are planned to be enrolled" 인용). https://news.cision.com/h--lundbeck-a-s/r/lundbeck-initiates-clinical-trial-in-immunology-for-lu-ag22515-in-thyroid-eye-disease,c4044547 (확인일 2026-10-01)

[19] Evommune, Inc., "Evommune Secures Exclusive Rights to Develop and Commercialize a Phase 2-ready IL-18 targeted fusion protein from AprilBio" (2024-06-24, APB-R3 → EVO301). https://ir.evommune.com/news-events/press-releases/detail/96/evommune-secures-exclusive-rights-to-develop-and-commercialize-a-phase-2-ready-il-18-targeted-fusion-protein-from-aprilbio (확인일 2026-10-01)

[20] Evommune, Inc., "Evommune Initiates Phase 2 Trial of IL-18 Targeted Fusion Protein, EVO301, in Adult Patients with Atopic Dermatitis" (2025-03-17). https://ir.evommune.com/news-events/press-releases/detail/91/evommune-initiates-phase-2-trial-of-il-18-targeted-fusion-protein-evo301-in-adult-patients-with-atopic-dermatitis ; 및 Evommune IL-18BP Fusion Protein 파이프라인 페이지(Phase 2a 2026-02 완료, 1차 endpoint 충족, Phase 2b 예정). https://www.evommune.com/il-18bp-fusion-protein/ (확인일 2026-10-01)

[21] 더바이오, "TED 접고 신경질환으로…룬드벡, 에이프릴바이오 'Lu AG22515' 개발전략 전환" (2026-08-19, MS/NMOSD/MG 후보 적응증 제시 관련). https://www.thebionews.net/news/articleView.html?idxno=27328 (확인일 2026-10-01)

[22] H. Lundbeck A/S, Pipeline (Lu AG22515, CD40L blocker, Neurology 항목 재배치 확인). https://www.lundbeck.com/global/our-science/pipeline (확인일 2026-10-01)

## 검증 로그

| Claim | Tier | 검증 방법 | 결과 | 일자 |
|---|---|---|---|---|
| APB-A1(Lu AG22515) 타겟이 CD40L이며 TED 적응증 개발이 2026-08-19 중단(방향 전환) 발표됨 | 상(중단 사실/적응증) | 1차 출처 direct-quote 대조(룬드벡 시험 개시 보도자료: "proof-of-concept phase Ib trial", "19 patients are planned to be enrolled", CD40L blocker/SAFA 명시[18]; ClinicalTrials.gov NCT06557850: PHASE1, SINGLE_GROUP, masking NONE, enrollment 20 ACTUAL[17]) + 복수 독립 언론사(한국경제, 머니투데이, 메디파나뉴스, 더바이오) 교차확인 + 작성 세션과 분리된 독립 QA 세션 재확인 | **PASS(2026-10-01 갱신)** — conventions 상 tier 요건(분리된 QA 세션 + 1차 출처 direct-quote 대조) 충족. 단, 룬드벡 Q2 실적 원문(PDF/IR) 직접 대조는 보도자료/언론 경유로 대체 | 2026-09-28 / 2026-10-01 갱신 |
| Phase 1b 중간 분석 proptosis 2.06mm 감소, TRAb 저하 신호 | 중(정량 수치, mechanism) | 단일 매체(더바이오) 기사 기반. 2026-10-01 QA에서 ENDO 2026 룬드벡 포스터 초록("Interim analyses demonstrated clinically meaningful reduction in proptosis and pharmacodynamic response")이 정성적 교차뒷받침으로 확인됨 | PARTIAL 유지(정량치 2.06mm 자체는 여전히 단일 출처, 포스터 정량 원문 대조 권장) | 2026-09-28 / 2026-10-01 갱신 |
| OX40L(IMB-101)/IL-4R/IL-18BP(APB-R3) 후보 배제 근거 | 하(정성적 배제 판단) | 공개 뉴스/DB 검색 | PASS | 2026-09-28 |
| dazodalibep(VIB4920/HZN-4920) Phase 3(OASIZ 301) topline positive, ESSDAI 1차 endpoint 충족(2026-09-22) | 상(임상 phase/결과) | 복수 독립 출처(Amgen 공식 press release, MedCity News, Parameter/투자매체) 교차확인 | PASS(1차 출처인 Amgen 보도자료 확인, SEC 8-K 원문 직접 대조는 미수행) | 2026-09-28 |
| APB-A1은 항체 유래 scFv+SAFA(Fab) 포맷, dazodalibep은 non-Ig Tn3 scaffold+HSA 융합 포맷이며 둘 다 Fc 결여 | 중(모달리티 구조 서술) | 특허문헌(USPTO) 및 PatSnap 요약 기반, 1차 논문(structure paper) 직접 대조는 미수행 | PARTIAL(특허 청구항 수준 확인, peer-reviewed 구조논문 교차확인 권장) | 2026-09-28 |
| 1세대 anti-CD40L mAb(ruplizumab/toralizumab)의 Fc-FcγRIIa 매개 혈전색전증 역사 | 중(기전/역사적 사실) | 학술 리뷰(Frontiers in Immunology 2026) 및 1차 연구(ResearchGate/FCGR2A transgenic mice 논문) 교차확인 | PASS | 2026-09-28 |
