# Graves' Disease & Thyroid Eye Disease 경쟁환경 조사 계획

## 요약
Graves' Disease(GD)와 Thyroid Eye Disease(TED)에 대해 (1) 글로벌 주요국 역학(incidence/prevalence + 환자 풀 추정), (2) 진단 방법, (3) 병기/중증도 기준, (4) 병기별 SoC, (5) 개발 중 신약 파이프라인을 문헌 조사하여 한국어 보고서(Markdown) + 구조화 엑셀로 정리한다.

## 확정된 범위 (사용자 결정사항)
- 용도: 경쟁환경/시장 조사 관점
- 역학 지역: 글로벌 주요국 (미국, EU5, 한국, 일본, 중국)
- TED 병기 체계: EUGOGO 중증도 분류 + CAS 활성도 중심 (보조로 VISA/NOSPECS 간략 언급)
- 환자 풀 추정: 포함 (문헌 rate × 주요국 인구)
- 신약 파이프라인: 포함
- 대상: 성인 중심 (소아는 제외)
- 언어: 한국어 (의학용어 영어 병기)
- 산출물: Markdown 보고서 + Excel

## 실행 방법
1. **문헌 조사** (LiteratureSearch + WebSearch/WebFetch)
   - 역학: 인구기반 코호트/메타분석 (예: 미국 Olmsted County, 덴마크, 영국 CPRD, 한국 NHIS 기반 연구 등)
   - 가이드라인: ATA/AACE GD 가이드라인, EUGOGO 2021 TED 관리 합의안(Eur J Endocrinol), ETA/ETA-EUGOGO 자료
   - 진단: TSH/FT4/FT3, TRAb(TSI), TSHR-Ab, 갑상선 초음파/섭취율, TED의 안과 평가(CT/MRI, Hertel exophthalmometry 등)
   - 병기/중증도: CAS 점수 체계, EUGOGO mild/moderate-severe/sight-threatening 기준
   - SoC: GD — 항갑상선약제(MMI/PTU), 방사성요오드, 수술, β-blocker; TED — 경과 관찰, Selenium, IV methylprednisolone, 안와 방사선/수술, teprotumumab 등
   - 파이프라인: IGF-1R 표적(teprotumumab 이후), 항-TSHR, 면역 조절제 등 개발 중 치료제
2. **환자 풀 추정**: 문헌 prevalence/incidence × 주요국 성인 인구(최신 공인 인구통계) → 질환별 환자수 표 (가정 명시)
3. **구조화**: 아래 엑셀 시트 구성에 맞춰 표 작성

## 산출물
- `/mnt/results/report_graves_ted_landscape.md` — 섹션: ① GD 역학 ② TED 역학 ③ 환자 풀 추정 ④ GD 진단/병기/SoC ⑤ TED 진단/병기(CAS·EUGOGO)/SoC ⑥ 파이프라인 ⑦ 참고문헌
- `/mnt/results/Graves_TED_landscape.xlsx` — 시트: GD_역학, TED_역학, 환자풀_추정, GD_진단, GD_SoC, TED_진단, TED_병기_CAS_EUGOGO, TED_SoC, 파이프라인
- (xlsx는 /workspace에서 작성 후 /mnt/results로 복사)

## 가정
- 역학 수치는 문헌 보고값을 그대로 인용하고, 환자 풀 추정은 별도 계산임을 표기
- TED 역학은 GD 환자 기준 발생 비율과 인구 기반 수치를 병기
- SoC는 최신 가이드라인(2021 EUGOGO, ATA 2016 및 이후 업데이트) 기준

## 검증 기준
- 모든 수치에 출처(논문/가이드라인) 명시
- 계산된 환자 풀은 입력 가정(rate, 인구, 연도)을 표에 명시하여 재현 가능
- 그림 불필요 (표 중심); 필요 시 역학 비교 표만
