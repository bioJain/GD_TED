---
linear_issue: JHA-73
created: 2026-09-24
source: manual
milestone: cluster-1-competitive-landscape
status: in-review
inputs:
  - 00_legacy_unsorted/GD_TED_report.md
  - 00_baseline_biomni/landscape_v2/pipeline_assets_v2.csv
  - 00_baseline_biomni/landscape_v2/asset_trial_crosswalk_v2.csv
  - 00_baseline_biomni/landscape_v2/clinical_trials_v2.csv
  - 00_baseline_biomni/landscape_v2/frozen_trial_registry_documents_v2.jsonl
  - 00_baseline_biomni/landscape_v2/figures_v2/figure_2_mechanism_counts_v2.svg
  - 00_baseline_biomni/landscape_v2/figures_v2/figure_3_mechanism_phase_heatmap_v2.svg
---

# GD/TED MoA class x indication-specific 개발단계 통합 매트릭스

**확인일:** 2026-09-24  
**registry data cut:** 2026-09-10  
**범위:** GD 또는 TED에서 개발 중이거나 승인된 disease-directed 자산. 중단, 철회, suspended, NDR/상태 불명 프로그램은 본 매트릭스에서 제외하고 별도 부표에 보존했다.

## 1. 판정 방법

1. legacy C4의 Cortellis 파생 목록은 자산 원표를 재전재하지 않고 집계와 이름 대조에만 사용했다. legacy 기준은 72개 프로그램 중 active 51개, discontinued 21개이다.
2. v2의 48개 자산은 `trial_ids`를 `clinical_trials_v2.csv`와 연결해 **GD와 TED를 각각** 판정하고, label과 endpoint가 충돌한 경우 frozen registry 원문을 확인했다. 자산 전체의 `highest_stage`를 그대로 복사하지 않았다. 예를 들어 efgartigimod는 GD Phase 3 active이나 TED Phase 3 terminated이므로 GD만 본표에 남겼다.
3. 동일 자산의 같은 적응증에 여러 시험이 있으면 active 상태(`RECRUITING`, `NOT_YET_RECRUITING`, `ACTIVE_NOT_RECRUITING`, `ENROLLING_BY_INVITATION`) 중 최고 단계를 사용했다. 승인 자산은 `Approved`를 Phase 3/4보다 우선 표기했다.
4. `COMPLETED`만 있는 자산은 sponsor 자료에서 개발 지속 또는 규제 심사가 명시된 경우에만 본표에 유지했다. `TERMINATED`, `WITHDRAWN`, `SUSPENDED`만 있는 프로그램과 `UNKNOWN`만 있는 프로그램은 제외했다. 완료 연구만 있고 후속 개발을 확인하지 못한 자산은 `관찰/검증 필요`로 분리했다.
5. 단계는 frozen v2 snapshot을 기준으로 하며, 2026-09-10 이후 live registry 변화와 혼합하지 않았다. 따라서 “현재”는 이 data cut 현재를 뜻한다.

### 단계 표기

- `A`: Approved, `RR`: Regulatory review, `P3/P2/P1`: indication-specific phase, `PC`: preclinical/discovery
- `—`: 해당 적응증에서 active 개발을 확인하지 못함
- 한 셀의 `GD P2 / TED P1`처럼 적응증별 단계가 다르면 반드시 병기했다.
- `source`: `both`는 이름/프로그램이 legacy와 v2 양쪽에 있음, `legacy`와 `v2`는 각각 한 입력에만 있음을 뜻한다. 이는 근거 우열이 아니다.

## 2. 통합 한 장 매트릭스

| MoA class | Approved / regulatory review | Phase 3 | Phase 2 | Phase 1 / early Phase 1 | Preclinical / discovery |
|---|---|---|---|---|---|
| TSHR 직접 차단/길항 | — | — | GenSci098/YB-101 (GD P2) | GenSci098/YB-101 (TED P1); K1-70 (GD P1); MER511 (GD P1) | CRN-12755; ETHY-001; REGN-24493; SP-1351 |
| anti-TSHR autoantibody 제거/항원특이 면역관용 | — | BHV-1300 (GD P3) | — | LCA-0321 (GD/TED P1) | BHV-1440 |
| FcRn 억제 | — | Efgartigimod PH20 SC (GD P3) | IMVT-1402/imeroprubart (GD P2) | — | — |
| IGF-1R 억제 | Teprotumumab (TED A); IBI311 (TED A, 중국); Veligrotug/Lumvoa (TED A) | Linsitinib; MHB018A; KHN939; VRDN-003/elegrobart (모두 TED P3) | AMG 732; NTB003/BCG009; SCTT11 (모두 TED P2) | ZB001 (TED P1) | IGF-1-methotrexate |
| IGF-1R/TSHR 이중표적 | — | — | — | IBI3031 (TED P1) | VBS-102 |
| IL-6/IL-6R | Satralizumab (TED RR) | — | TOUR006/pacibekitug (TED P2) | — | — |
| IL-11R | — | — | LASN01 (TED P2, completed; 지속 확인 필요) | — | — |
| CD40L | — | — | — | Lu AG22515/velaprumig (TED P1/2) | — |
| Plasma/B-cell 표적 | — | — | Felzartamab (GD P2) | Allogeneic CD19/BCMA CAR-T; HN2301 in-vivo CAR-T (GD early P1) | — |
| BTK 억제 | — | — | Rilzabrutinib (GD P2) | — | — |
| JAK/mTOR/기타 면역조절 | — | — | Tofacitinib (TED P2); Sirolimus (TED P2) | — | — |
| 보조 치료 | — | — | — | — | — |

> **읽기 주의:** 위 표는 자산 수가 아니라 “자산 x 적응증의 최고 active 단계”를 압축한 것이다. Teprotumumab/IBI311의 Phase 4 연구와 승인 후 제형 연구는 Approved 셀에 중복 계수하지 않았다. Hydroxychloroquine Phase 4와 tocilizumab Phase 4는 disease-modifying pipeline과 구분되는 보조/off-label 연구이므로 아래 상세표에만 표시했다.

## 3. Active 자산 상세

### 3.1 GD 포함 자산

| 자산 | 개발사/owner at cut | MoA | GD 단계 | TED 단계 | 핵심 trial ID | source | 판정 메모 |
|---|---|---|---|---|---|---|---|
| BHV-1300 | Biohaven | IgG-directed extracellular degradation | P3 | — | NCT07661056; NCT06980649 | both | 두 GD 시험 모두 recruiting |
| Efgartigimod PH20 SC | argenx | FcRn inhibition | P3 | 제외, P3 terminated | NCT07570316; NCT07596849 / NCT06307613; NCT06307626 | both | Highest Status trap 대표 사례 |
| GenSci098/YB-101 (legacy GS-098) | GenSci | TSHR antagonism | P2 | P1 | NCT07682896 / NCT06569758 | both | 적응증별 최고 active 단계 분리 |
| IMVT-1402/imeroprubart | Immunovant | FcRn inhibition | P2 | — | NCT06727604; NCT07018323; NCT07286006 | both | recruiting/invitation |
| Felzartamab | Biogen | CD38 plasma-cell depletion | P2 | — | NCT07722546 | both | recruiting |
| Rilzabrutinib | Sanofi | BTK inhibition | P2 | GD 동반 GO subset 허용, TED 독립단계 아님 | NCT06984627 | both | frozen registry 원문의 condition/title/FT4 endpoint로 GD 판정. CSV의 `Active TED` label을 교정 |
| MER511 | Merida Biosciences | anti-TSHR AAb neutralization/clearance | P1 | 잠재 적응증, 임상 단계 미확인 | NCT07305818 | both | TED는 v2에 `potential TED`일 뿐 TED trial 없음 |
| K1-70 | AV7/academic collaborators | TSHR blockade | P1 completed, 후속 확인 필요 | legacy P2, v2 TED trial 미확인 | NCT02904330 | both | 본 매트릭스에는 검증 가능한 GD P1만 반영 |
| LCA-0321 | Lycia Therapeutics | anti-TSHR autoantibody LYTAC | P1 | P1 | CTIS 2025-524053-14-00; LCA-0321-01 | both | CT.gov 외 CTIS 근거, GD/TED 병기 |
| Allogeneic CD19/BCMA CAR-T | Shanghai Zhongshan Hospital | CD19/BCMA CAR-T | early P1 | — | NCT07129642; NCT07261345 | v2 | recruiting |
| HN2301 in-vivo CAR-T | Shanghai Zhongshan Hospital | in-vivo CD19/BCMA CAR-T | early P1 | — | NCT07333677 | v2 | recruiting |
| BHV-1440 | Biohaven | anti-TSHR AAb degrader | PC | PC | registry ID 없음 | legacy | v2 48개 목록에는 없음 |
| CRN-12755 | Crinetics/Vertex | TSHR | PC | PC | registry ID 없음 | legacy | legacy active preclinical |
| ETHY-001 | Ethyreal Bio | TSHR | PC | PC | registry ID 없음 | legacy | legacy active preclinical |
| REGN-24493 | Regeneron | TSHR | PC | PC | registry ID 없음 | legacy | legacy active preclinical |
| SP-1351 | Septerna | TSHR | PC | PC | registry ID 없음 | legacy | legacy active preclinical |
| VBS-102 | VelaVigo/Ollin | IGF-1R/TSHR dual | PC | PC | registry ID 없음 | legacy | legacy active preclinical |

### 3.2 TED 전용/주도 자산

| 자산 | 개발사/owner at cut | MoA | TED 단계 | 핵심 trial ID | source | 판정 메모 |
|---|---|---|---|---|---|---|
| Teprotumumab | Amgen | IGF-1R inhibition | Approved | NCT03298867; NCT06248619 | both | 승인 후 SC/Phase 4 연구는 단계 상향에 미사용 |
| IBI311 | Innovent | IGF-1R inhibition | Approved (중국) | NCT05795621; NCT07113262 | both | active/inactive TED 시험 모두 존재 |
| Veligrotug/Lumvoa | Viridian | IGF-1R antagonism | Approved (미국) | NCT05176639; NCT06021054 | both | v2 cutoff 승인 상태 사용 |
| Satralizumab | Roche/Chugai | IL-6R blockade | Regulatory review | NCT05987423; NCT06106828 | both | v2 cutoff에 TED 승인 아님 |
| Linsitinib | Slingshot Therapeutics | IGF-1R/IR kinase inhibition | P3 | NCT07753603; NCT06112340 | both | recruiting |
| MHB018A | Minghui Pharmaceutical | IGF-1R inhibition | P3 | NCT06989918; NCT07257185 | both | active 및 chronic/inactive TED |
| KHN939 | registry sponsor | target 미공개 | P3 | NCT07720635; NCT07720648 | both | pipeline row의 `Clinical` 대신 trial phase 사용 |
| VRDN-003/elegrobart | Viridian | IGF-1R inhibition | P3 | NCT06625411; NCT06625398 | both | active-not-recruiting |
| AMG 732 | Amgen | IGF-1R inhibition | P2 | NCT06401044; NCT07438405 | both | recruiting/active-not-recruiting |
| NTB003/BCG009 | Nanjing Chia-tai Tianqing/Biocytogen | IGF-1R inhibition | P2 | NCT07462130 | both | not-yet-recruiting |
| SCTT11 | registry sponsor | target 미공개 | P2 | NCT06769984 | both | P1/2, not-yet-recruiting |
| TOUR006/pacibekitug | Tourmaline Bio/Novartis | IL-6 pathway blockade | P2 | NCT06088979 | both | active-not-recruiting |
| LASN01 | Laekna | IL-11R blockade | P2 completed, 지속 확인 필요 | NCT06226545 | both | terminated 아님. active 후속은 snapshot에서 미확인 |
| Tofacitinib | First Affiliated Hospital of Xiamen University | JAK inhibition | P2 | NCT07547930 | v2 | recruiting investigator-led trial |
| Sirolimus | academic sponsors | mTOR inhibition | P2 | NCT04936854 | v2 | recruiting trial만 단계 근거로 사용 |
| Lu AG22515/velaprumig | Lundbeck | CD40L blockade | P1/2 | NCT06557850 | both | active-not-recruiting |
| IBI3031 | Innovent | IGF-1R/TSHR dual blockade | P1 | NCT07622368 | both | recruiting |
| ZB001 | Zenas | IGF-1R inhibition | P1 completed, 지속 확인 필요 | NCT05776121 | v2 | 후속 active trial 미확인 |
| Hydroxychloroquine | National Taiwan University Hospital | pleiotropic immunomodulation | P4, adjunct | NCT05126147 | v2 | recruiting, pipeline matrix에서는 보조 치료로 분리 |
| Tocilizumab | academic sponsors | IL-6R blockade | P4, off-label study | NCT06927375 | v2 | recruiting trial만 사용, withdrawn trial은 무시 |
| IGF-1-methotrexate | Lirum | targeted conjugate | PC | registry ID 없음 | legacy | legacy active preclinical |

## 4. legacy와 v2 자산 집합 대조

대조 단위는 **정규화한 자산명**이다. 제형, alias, 적응증별 행은 하나로 합쳤다(예: `GS-098`=`GenSci098/YB-101`, `elegrobart`=`VRDN-003`, `pacibekitug`=`TOUR006`). 따라서 legacy의 “51 active”와 v2의 “48 rows”는 아래 정규화 목록의 행 수와 직접 같지 않다.

| 구분 | 정규화 자산 | 차이 사유 |
|---|---|---|
| 양쪽 | LCA-0321; MER511; GenSci098/YB-101; K1-70; IBI3031; Veligrotug; Teprotumumab; Linsitinib; Satralizumab; Batoclimab; LASN01; Kamuvudine-9; Lu AG22515; AMG 732; Cizutamig; KHN939; SCTT11; BHV-1300; Efgartigimod; Felzartamab; IBI311; IMVT-1402; Lonigutamab; MHB018A; NTB003; Rilzabrutinib; TOUR006; VRDN-003 | alias/회사명/단계 표기가 달라도 동일 자산으로 수동 정규화. 이 중 stopped 자산은 본표가 아닌 부표로 이동 |
| legacy만 | BHV-1440; CRN-12755; ETHY-001; REGN-24493; SP-1351; VBS-102; Atheron unnamed small molecule; Regeneron unnamed ophthalmology asset; IGF-1-methotrexate; Nanocort; belimumab; vunakizumab; XM-003; MYJ-1633; KSP-0914; ANT-4; CC-001; unnamed mRNA trispecific antibody | Cortellis는 early/preclinical 및 코드명 미공개 프로그램을 더 넓게 포착. v2는 CT.gov snapshot과 일부 direct-TSHR deep curation 중심이라 이들이 빠짐 |
| v2만 | ATX-GD-59; Aflibercept; allogeneic CD19/BCMA CAR-T; Celecoxib; HN2301; Hydroxychloroquine; Iscalimab; Lanreotide; Otelixizumab; rabbit ATG; Rituximab; Secukinumab; SHR-1314; Sirolimus; 99Tc-MDP; Tocilizumab; Tofacitinib; unspecified immunosuppressive agent; WP1302; ZB001 | v2는 registry에서 historical, investigator-led, repurposed, stopped/failed trial까지 보존. legacy active commercial pipeline보다 범위가 넓음 |

### 차이 해석

- **범위:** legacy는 commercial pipeline와 preclinical scouting 중심, v2는 ClinicalTrials.gov intervention inventory 중심이다. 그래서 v2-only에는 오래된 완료/중단 시험과 adjunct가 많고, legacy-only에는 registry ID가 없는 preclinical 자산이 많다.
- **시점:** legacy는 2026-09-14 확인, v2 registry cut은 2026-09-10이다. 4일 차이보다 source refresh와 분류 정책 차이가 더 큰 원인이다.
- **DB:** Cortellis와 public registry는 자산 naming, 지역 임상, 회사의 internal/preclinical program 포착 범위가 다르다. 정규화는 동일성을 보여줄 뿐 각 DB의 누락을 오류로 단정하지 않는다.
- **상태 정책:** v2는 stopped/failed를 분석 이력으로 보존한다. 본 이슈는 active only이므로 아래 부표로 이동했다.

## 5. 본 매트릭스에서 제외했지만 누락하지 않은 자산

### 5.1 stopped/failed/suspended

| 자산 | 적응증 | 마지막 단계/상태 | 핵심 trial ID | source | 제외 이유 |
|---|---|---|---|---|---|
| Batoclimab | GD/TED | P2, interrupted/completed | NCT03922321; NCT03938545; NCT05907668 | both | legacy에서 discontinued, v2도 earlier program interrupted |
| Efgartigimod PH20 SC | TED만 | P3 terminated | NCT06307613; NCT06307626 | both | futility 종료. GD P3는 본표 유지 |
| Kamuvudine-9 | TED | P2 terminated | NCT06467435 | both | low enrollment로 종료 |
| Celecoxib | TED | P2 terminated | NCT02845336 | v2 | terminated |
| Iscalimab | GD | P2 completed, legacy discontinued | NCT02713256 | v2/legacy discontinued summary | active 후속 없음, legacy 중단 판정 우선 |
| Lanreotide | TED | P2 terminated | NCT00288522 | v2 | terminated |
| Otelixizumab | TED | P2 terminated | NCT01114503 | v2 | terminated |
| Secukinumab | TED | P3 terminated | NCT04737330 | v2 | terminated |
| SHR-1314 | TED | P2 terminated | NCT05394857 | v2 | terminated |
| WP1302 | GD | P2 suspended | NCT06240455 | v2 | suspended |

### 5.2 NDR/상태 불명 또는 적응증 직접성 부족

| 자산 | v2 상태 | 처리 |
|---|---|---|
| Rabbit anti-thymocyte globulin | registry `UNKNOWN`, phase NA | NDR로 제외 |
| Unspecified immunosuppressive agent | registry `UNKNOWN`, phase NA | NDR 및 자산 미특정으로 제외 |
| Aflibercept | TED P2 completed only | 현행 개발을 확인하지 못해 관찰 목록 |
| Rituximab | GD/TED 연구 completed, off-label | active registrational pipeline이 아니므로 제외 |
| 99Tc-MDP | TED P4 completed | completed investigator-led adjunct, active pipeline 아님 |
| ATX-GD-59 | GD P1 completed; follow-on WP1302 suspended | 후속 중단으로 본표 제외 |
| Cizutamig | autoantibody disease P1 | GD/TED 직접 등록시험이 없어 indication-specific matrix 제외 |
| Lonigutamab | TED P1/2 completed | 후속 active 시험 미확인, legacy도 전략 재검토 flag |

## 6. QA E6/E7 결론

| QA | 결과 | 근거 |
|---|---|---|
| E6 indication-specific staging | **PASS** | 모든 v2 임상 자산을 `trial_ids`와 trial의 `indication`, `phase`, `overall_status`로 재판정. Efgartigimod, GenSci098, MER511처럼 자산 최고단계와 적응증 단계가 다른 경우를 분리 표기 |
| E7 discontinued/NDR 제외 | **PASS** | stopped/failed/suspended 10개와 NDR/범위외 8개를 active 매트릭스 밖 부표에 명시적으로 보존. TED-terminated efgartigimod는 TED에서만 제외하고 GD는 유지 |

## 7. 해석상 한계

- 이 문서는 2026-09-10 frozen registry cut을 재분석한 산출물이며 live registry 조회가 아니다.
- legacy commercial DB의 자산별 원표는 public repo 정책상 재전재하지 않았다. legacy-only 목록은 C4 공개 요약에 이름이 나온 범위이며, 그 결과 비공개 원표의 51개 active program을 완전히 역산하는 용도로 사용하면 안 된다.
- `pipeline_assets_v2.csv`의 indication 요약과 trial row가 충돌하면 trial row를 우선하고, trial row 내부가 모순되면 frozen registry 원문을 우선했다. 대표적으로 GenSci098은 GD P2와 TED P1로 분리했고, efgartigimod는 GD active/TED terminated로 분리했으며, Rilzabrutinib은 CSV의 `Active TED` 대신 registry condition/title/FT4 endpoint에 따라 GD P2로 교정했다.
- `COMPLETED`는 성공, 중단 또는 후속 개발을 자동 의미하지 않는다. 따라서 완료-only 자산에 대해서는 보수적으로 `지속 확인 필요` 또는 관찰 목록을 사용했다.
