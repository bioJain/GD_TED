# Graves’ disease–TED Landscape v2 Release-Gate Remediation Plan

## 1. 목표, 범위 및 v2 release contract

### 목표
2026-09-10 data cut을 유지한 채 기존 bundle의 다섯 핵심 차단 요인—(1) trial–asset/mechanism 누락, (2) 지역별 SoC·regulatory 근거 부족, (3) blanket `entailed` QA, (4) 15-slide deck source footer 부재, (5) self-referential/stale manifest와 미검증 checkpoint—를 제거한다. 기존 v1 결과는 수정하지 않고 별도의 `graves_ted_landscape_v2` 결과 폴더에 v2 세대를 만든다.

### 고정 정책
- ClinicalTrials.gov는 이미 고정된 2026-09-10 snapshot만 사용한다. 이후 live API 결과를 섞지 않는다.
- Korean narrative와 English scientific/endpoint/asset/trial terminology를 유지한다.
- negative, failed, terminated, withdrawn, suspended, discontinued 및 target-unknown 프로그램을 누락하지 않는다.
- biochemical control, off-ATD normalization, durable off-treatment remission, relapse, ablative/surgical control 및 cure를 계속 분리한다.
- cross-trial pooling·naïve ranking·quantitative meta-analysis는 수행하지 않는다.
- R&D potential과 evidence confidence는 분리한다.
- regulatory authorization, reimbursement/access 및 guideline recommendation을 서로 다른 필드와 주장으로 관리한다.
- 사용자가 선택한 계층형 fallback을 적용한다. 공식 원출처가 없으면 official status는 `unresolved`로 유지하고, 전문학회·HTA·현지 공공기관 등 권위 있는 보조근거는 별도 contextual field에만 기록한다.
- release gate는 Severity 1/2 unresolved 0건이다. 결론에 영향 없는 Severity 3만 `QA2`에 잔여 gap으로 공개할 수 있다.
- PDF는 만들지 않는다.

### 파일 세대와 불변성
기존 폴더와 파일의 시작 SHA-256을 `v1_baseline_hashes_v2.csv`에 기록하고 종료 시 다시 비교한다. 기존 파일이 하나라도 바뀌면 release를 차단한다. 새 결과 폴더의 사용자-facing 파일은 모두 v2 세대를 명시한다.

필수 v2 산출물:
- `plan2.md`, `execution_log2.md`, `QA2.md`, `QA2.json`
- `clinical_trials_v2.csv`, `pipeline_assets_v2.csv`, `soc_outcomes_v2.csv`, `evidence_claims_v2.csv`
- `result_trial_curation_v2.csv`, `asset_trial_crosswalk_v2.csv`
- `reference_v2.md`, `reference_catalog_v2.csv`, `citation_resolution_v2.csv`
- `report_graves_ted_landscape_v2.md`
- `presentation_graves_ted_landscape_v2.pptx`와 동일 stem의 `.slides/` sidecar
- `slide_source_map_v2.csv`, `visual_QA2.csv`
- `update_manifest_v2.json`, `release_manifest_v2.csv`, `release_attestation_v2.json`, `checkpoint_receipt_v2.json`
- `figures_v2/`의 여섯 figure 각각 `.svg`와 QA용 `.png`

내부 plan-mode 제안서가 승인되면 동일한 내용으로 `plan2.md`를 만들고, 기존 `plan.md`를 덮어쓰지 않는다. `execution_log2.md`는 새 machine-readable v2 event ledger에서 원자적으로 재생성하며 기존 log에 append하지 않는다. 안정적인 event ID로 재실행 시 중복 event가 생기지 않게 한다.

## 2. 데이터·근거 remediation 작업

### A. 168-trial asset/mechanism completeness
1. frozen snapshot, `clinical_trials.csv`, trial triage, mechanism provenance 및 result curation을 trial ID로 결합한다.
2. 각 registry intervention/arm 문자열을 원문 그대로 보존하고, dose·route·placebo·background therapy를 분리한 canonical asset alias를 만든다.
3. `asset_trial_crosswalk_v2.csv`는 최소한 `trial_id`, `raw_intervention`, `canonical_asset`, `aliases`, `role`, `asset_scope`, `target`, `mechanism_class`, `pipeline_inclusion`, `exclusion_reason`, `source_id`, `mapping_confidence`, `manual_review_status`를 가진다.
4. 168개 trial의 모든 intervention occurrence는 다음 중 하나로 100% disposition한다: `pipeline/approved asset`, `standard of care`, `adjunct/supportive`, `procedure`, `placebo/comparator`, `diagnostic/non-therapeutic`, `unknown-but-retained`. 무판정 행은 release blocker다.
5. `pipeline_assets_v2.csv`에는 모든 canonical investigational/approved disease-directed pharmacologic·biologic asset와 공개적으로 식별 가능한 direct-TSHR/autoantibody preclinical program을 포함한다. procedure, inert placebo 및 순수 diagnostic은 crosswalk에 사유를 남기고 pipeline table에서 제외할 수 있다.
6. MHB018A와 NTB003/BCG009는 필수 positive-control 누락 항목으로 검사한다. stopped/failed asset도 별도 status와 why-stopped를 유지하며 mechanistic failure와 operational failure를 구분한다. KHN939/SCTT11 등 target-unknown 자산은 추정하지 않고 retained watchlist로 둔다.
7. `clinical_trials_v2.csv`의 빈 `n_randomized`, `n_analyzed`, aliases, dose/schedule 및 publication link를 deterministic extraction과 targeted review로 정리한다. 값이 공개되지 않았으면 빈칸 대신 `NR (reason)` 또는 `NA (reason)`를 쓴다. publication field에는 정규화된 URL만 둔다.
8. 기존 25-trial exact result는 v2 curation으로 이관하되, 원출처 재검증이 실제 수정 근거를 제공하지 않는 한 승인된 수치와 해석을 변경하지 않는다.

완료 기준: 168 unique trial ID 유지, 모든 intervention occurrence disposition 완료, 모든 pipeline row가 하나 이상의 trial/preclinical source 또는 명시적 provenance를 가짐, MHB018A·NTB003/BCG009 포함, unexplained omitted asset 0건.

### B. 지역별 SoC·regulatory 재구축
`soc_outcomes_v2.csv`를 한 region template의 복제본이 아니라 `region × disease/stage × line × intervention × population` 단위로 다시 만든다. 최소 coverage는 미국, EU/EEA, 영국, 한국, 일본에서 다음을 분리한다.
- GD: ATD, RAI, thyroidectomy, relapse/refractory 선택지.
- TED: mild active, active moderate-to-severe, sight-threatening, chronic/inactive·rehabilitative stage.
- special populations: pediatrics, pregnancy/lactation, older adults 및 relapsed/refractory; 실제 지역별 근거가 없으면 보편 권고의 적용범위와 지역 gap을 명시한다.

새 schema는 `authorization_status/as_of/source`, `reimbursement_or_access_status/as_of/source`, `guideline_position/source`, `eligible_population`, `regimen`, `endpoint_definition`, `response/remission/relapse/durability`, `harms`, `next_option`, `fallback_context`, `uncertainty_reason`을 분리한다. 같은 source가 여러 지역에 정당하게 적용될 때만 `scope_of_authority`를 명시해 재사용한다.

공식 source 우선순위:
- US: FDA/Drugs@FDA/DailyMed, ATA 및 ATA/ETA.
- EU/EEA: EMA·EC/Union Register, EUGOGO/ETA.
- UK: MHRA product information, NICE 및 적절한 NHS/HTA record.
- South Korea: MFDS, HIRA 및 Korean Thyroid Association/Korean TED framework.
- Japan: PMDA, MHLW/NHI 및 Japan Thyroid Association.

Tepezza current SPL, Lumvoa, satralizumab, 한국 teprotumumab, EU/UK/Japan product status를 alias와 현지 상품명으로 검색한다. source가 data cut 이후 게시됐더라도 data cut 이전의 사건일을 명시적으로 증명할 때만 historical status 근거로 사용할 수 있다. 포털 검색 부재 자체를 “미승인” 근거로 사용하지 않는다. unresolved official status에는 계층형 fallback context와 검색일·query·잔여 한계를 남긴다.

완료 기준: 지역별 authorization/reimbursement/guideline이 분리되고, generic 5-region copy pattern이 제거되며, 각 행에 공식 source 또는 명시적 unresolved/fallback provenance가 있다.

### C. source infrastructure 재구축
1. source 복구 순서는 기존 local full text·structured evidence, frozen registry, expanded reference store, 구체적 transcript keyword recovery, 외부 official/primary retrieval, 권위 있는 fallback 순이다.
2. 기존에 표시된 source ID는 가능한 한 보존한다. `[1, 6–8, 274, 422, 444–445, 483, 521, 541, 564, 619, 645, 672, 675, 678–679, 683, 710–713]`를 우선 복구한다. ID를 복구할 수 없으면 그 citation을 유지하지 않고, 검증 가능한 대체 source에 새 ID를 배정한 뒤 모든 downstream artifact를 갱신한다.
3. LCA-0321 official CTIS record, Lilly/Merida closing, current Tepezza SPL 및 지역별 제품 status를 우선 unresolved queue로 처리한다. 찾지 못한 항목은 실패 query와 fallback을 기록하며 과장하지 않는다.
4. `reference_catalog_v2.csv`를 단일 source ledger로 사용하고 `reference_v2.md`를 여기서 생성한다. 각 record는 source ID, title/issuer, date/year, URL/DOI/registry ID, source type, evidence tier, access depth, exact locator availability, last verified 및 중요 R&D implication을 가진다.
5. 실제 `reference_v2.md` 형식인 `- [N] ...`를 파싱하는 validator로 report, CSV, figure metadata 및 deck footer의 모든 `[N]`을 점검한다. 각 ID는 reference에 정확히 한 번 존재해야 한다.

Literature deep-review workflow에서는 “모든 displayed claim에 exact resolvable anchor”와 “모든 displayed anchor에 stance-blinded verdict”라는 핵심 evidence contract를 적용한다. 다만 사용자가 PDF를 명시적으로 제외했고 이번 작업은 기존 bundle remediation이므로 해당 skill의 PDF/infographic terminal deliverable은 수행하지 않는다. ClinicalTrials landscape workflow도 live API 대신 승인된 frozen snapshot을 사용한다.

## 3. claim-level blind QA, report, figures 및 deck

### A. claim inventory와 stance-blinded second pass
현재 report 119개 sentence-like unit 중 54개, deck 118개 text line 중 43개가 숫자·날짜·통계·status 후보로 탐지되어, dedup 전 최대 약 97개 display claim 후보가 있다. 구현 시 다음을 atomize한다.
- report/deck/figure에 표시되는 모든 숫자, 날짜, denominator, effect estimate, CI, p-value, dose, schedule, count 및 status.
- 모든 approval, phase/status, trial ID, regimen, direct-TSHR/anti-TSHR MOA와 최종 R&D ranking 근거.
- 낮은 영향도의 비수치 배경문장은 고정 seed의 stratified 20% 표본.

`evidence_claims_v2.csv`는 `claim_id`, `artifact/location`, `claim_text`, `claim_type`, `population`, `comparator`, `endpoint`, `timepoint`, `value/unit`, `source_id/url`, `exact_anchor/locator`, `access_depth`, `first_pass_decision`, `blind_verdict`, `failure_mode`, `resolution`, `final_display_state`를 포함한다. table-derived count도 source artifact와 hash/row anchor를 기록한다.

blind pass 전 `blind_packet_v2.jsonl`을 만들되 first-pass stance, 결론, resolution 및 기존 verdict column을 제거하고 claim 순서를 고정 seed로 섞는다. 같은 coordinator가 이 packet과 source anchor만 보고 `support`, `contradict`, `insufficient`, `population_mismatch`, `endpoint_mismatch` 중 하나로 새 판정을 수행한다. 프로그램으로 blanket `entailed`를 할당하지 않는다. 이 절차는 within-agent bias-reduction이며 독립 검증이 아니라는 제한을 `QA2`와 report에 명시한다.

`contradict/insufficient/mismatch` claim은 source를 다시 확인해 문구·population·endpoint를 수정하거나 display에서 제거한 뒤 재추출·재판정한다. 최초 실패와 correction history는 보존한다. 최종 displayed claim은 `support`만 허용한다.

### B. report와 canonical consistency
`report_graves_ted_landscape_v2.md`는 v2 canonical tables와 claim ledger에서 재생성한다. 지역별 SoC, complete asset inventory, unresolved regional status 및 negative/stopped evidence를 명시한다. clinical control/remission/cure taxonomy와 cross-trial non-comparability를 유지한다. 모든 외부 수치·status·mechanistic claim은 inline `[N]`을 갖는다.

report, four canonical CSVs, six figures 및 deck에서 반복되는 값은 claim ID 또는 canonical row ID로 연결한다. 동일 claim의 값·denominator·timepoint·population·source가 불일치하면 release를 차단한다.

### C. 여섯 figure와 정확히 15-slide deck
여섯 figure를 v2 canonical data에서 다시 생성하고 editable-text SVG를 기본, PNG를 QA용으로 저장한다. trial/asset changes가 없는 figure도 v2 hash와 provenance로 재생성한다. selected PRR figure는 population, endpoint definition 및 timepoint가 서로 다름을 caption/metadata에 명시하고 descriptive display only로 유지한다.

`presentation_graves_ted_landscape_v2.pptx`는 16:9, 무애니메이션, 정확히 15장을 유지한다. v1의 논리 흐름은 유지하되 수정된 regional SoC, complete assets 및 QA-qualified claims만 표시한다. `slide_source_map_v2.csv`에서 slide별 claim ID와 source ID를 생성하고, claim이 있는 각 slide에 읽을 수 있는 concise source footer를 자동 삽입한다. footnote를 수동 복사하지 않는다. title/method slide의 내부 count는 frozen artifact/hash anchor로 연결한다.

Deck은 별도 staging copy에서 닫힌 파일로 생성한 후 다음 순서로 검증한다.
1. 15 slides, non-empty shapes, 16:9, no animations, expected font 및 source footer 존재를 구조적으로 확인.
2. 모든 slide를 PNG로 render하고 geometry inventory의 zero-size/off-slide flag를 검토.
3. 15개 slide PNG와 6개 figure PNG 모두에 explicit PASS/defect row를 `visual_QA2.csv`에 기록. Korean glyph, clipping, overlap, annotation, contrast, figure centering 및 source-footnote legibility를 검사.
4. PowerPoint package/relationship/font compatibility validator 통과.
5. staging과 published PPTX의 byte size 및 SHA-256이 동일한지 확인하고 rendered `.slides/` sidecar를 함께 배포.

`Read(media_output_check)`가 플랫폼 오류로 실패하면 동일 파일에 1회 재시도한다. 재실패 시 일반 visual read로 같은 checklist를 수동 판정하고 원 오류와 degraded method를 `QA2`에 Severity 3로 기록할 수 있다. 단, slide/figure를 실제로 보지 않았거나 structural/compatibility gate가 실패한 경우에는 release할 수 없다.

## 4. 검증, manifests, checkpoint 및 test cases

### QA severity
- Severity 1: 잘못된 pivotal 수치·승인상태·핵심 결론·data-cut 혼합.
- Severity 2: in-scope asset/trial 누락, 잘못된 regimen/endpoint/population, missing citation, canonical artifact 간 핵심 불일치, unreadable deck/figure.
- Severity 3: 결론에 영향 없는 metadata/access gap 또는 media-checker 자체 오류가 대체 visual inspection으로 보완된 경우.

Severity 1/2 unresolved는 0이어야 한다. Severity 3는 owner, 영향, mitigation 및 residual uncertainty가 `QA2`에 명시된 경우만 허용한다.

### deterministic tests
1. **Asset controls:** MHB018A와 NTB003/BCG009가 pipeline 및 crosswalk에 존재해야 한다. 모든 168 trial intervention occurrence가 disposition되어야 한다.
2. **Unknown retention:** KHN939/SCTT11 등 unknown target을 임의 기전으로 분류하면 실패한다.
3. **Critical fields:** blank critical field가 0이고, 공개되지 않은 값은 `NR/NA + reason`이어야 한다.
4. **SoC regionality:** region을 제외한 핵심 field가 완전히 같은 5-region template이면 실패한다. authorization, reimbursement, guideline field의 conflation도 실패한다.
5. **Citation integrity:** missing·duplicate·orphan `[N]` 하나라도 있으면 실패한다. 기존 parser가 놓친 `- [N]` 형식을 regression fixture에 포함한다.
6. **Blindness contract:** blind packet에 first-pass stance/verdict/resolution이 포함되면 실패한다. 모든 displayed anchor가 blind verdict를 가져야 한다.
7. **Perturbation test:** 대표 pivotal 수치 하나를 임시 fixture에서 변경하면 report–CSV–deck consistency checker가 반드시 실패해야 한다.
8. **Endpoint semantics:** on-treatment normalization을 remission/cure로, RAI/thyroidectomy를 immune cure로 표현하면 실패한다.
9. **Deck tests:** 정확히 15 slides, no animations, footer coverage, render 15/15, visual PASS 15/15, compatibility PASS가 모두 필요하다.
10. **Manifest tests:** self-entry·stale hash·zero-byte file·duplicate path·case-collision이 있으면 실패한다.
11. **v1 immutability:** 시작/종료 v1 hash가 다르면 실패한다.
12. **Checkpoint test:** source와 checkpoint의 expected paths, regular-file count, nonzero size 및 SHA-256이 모두 동일해야 한다.

### non-self-referential release design
1. v2 payload를 모두 닫고 `execution_log2.md`를 freeze한다.
2. `update_manifest_v2.json`은 data cut, schemas, queries, aliases, fallback policy, seeds 및 retrieval timestamps를 기록하되 자기 자신을 포함하는 file-hash map을 갖지 않는다.
3. `release_manifest_v2.csv`는 정렬된 relative path, bytes, SHA-256을 기록하되 자신과 후속 attestation/receipt는 제외한다.
4. `release_attestation_v2.json`은 `release_manifest_v2.csv`의 hash와 정렬된 manifest tuples에서 계산한 release root digest를 기록하며 자기 자신은 hash하지 않는다.
5. 결과 bundle 전체와 PPTX sidecar를 새 immutable v2 checkpoint increment로 복사한다.
6. 별도 verification pass가 source/checkpoint의 path set, count, bytes, SHA-256을 비교한다. 성공 후 `checkpoint_receipt_v2.json`을 양쪽에 마지막으로 저장하고 receipt 자체도 별도로 size/hash 확인한다.
7. manifest/attestation/receipt 생성 후 payload를 변경하지 않는다. 변경이 필요하면 manifest부터 전부 재생성하고 새로운 release ID를 쓴다.

## 5. 실행 순서, 컴퓨팅 및 최종 완료 기준

### 실행 순서
1. v1 baseline hash 및 v2 schemas/event ledger 초기화.
2. frozen 168-trial asset crosswalk와 complete pipeline inventory 구축.
3. 지역별 SoC·regulatory source retrieval 및 source catalog 복구.
4. canonical CSVs, reference 및 report v2 재생성.
5. displayed claim atomization, first pass, stance-hidden blind pass, correction loop.
6. 여섯 figure와 exact 15-slide deck 재생성 및 source footer 적용.
7. deterministic/visual/compatibility QA, Severity adjudication.
8. non-self-referential manifests, published-byte verification, immutable checkpoint 및 receipt.

각 gate가 끝날 때 재개 가능한 중간 상태를 session-shared checkpoint에 저장한다. 장시간 retrieval은 작은 batch로 나누며, 첫 20개 intervention mapping과 첫 10개 claim adjudication의 실제 처리율로 남은 ETA를 갱신한다.

### 실측 기반 compute estimate
- 현재 release 약 5.5 MB, frozen registry 약 4.63 MB, 168 trials, 133 raw asset strings, 기존 31 claims, dedup 전 report/deck quantitative/status 후보 약 97개, expanded scholarly reference store 266 records.
- 예상 resident RAM은 5 GB 미만, working storage는 source full text와 slide renders를 포함해 약 2–5 GB, 최종 v2 bundle은 보수적으로 200 MB 미만이다.
- HPC는 필요하지 않다. `worker-0`에서 수행하고, 대규모 OCR/full-text acquisition이 새로 발생하지 않는 한 추가 machine을 만들지 않는다.
- 누적 실행시간은 약 6–12시간으로 추정한다: asset/SoC 2–4 h, source recovery 1–3 h, claim QA 2–4 h, figure/deck/manifest 1–2 h. 실제 ETA는 위 pilot throughput으로 갱신한다. 30분 이상이고 독립적인 단계만 tracked background execution을 사용한다.

### 최종 완료 기준
- v1 파일 hash가 모두 보존됨.
- 168 trial의 모든 intervention이 disposition되고 unexplained asset omission 0건.
- MHB018A, NTB003/BCG009 및 모든 in-scope stopped/failed/unknown program 보존.
- 지역별 SoC·authorization·reimbursement·guideline이 근거와 함께 분리되고 generic duplication 제거.
- report/deck/figure의 모든 quantitative·status·core mechanism claim이 exact anchor와 stance-blinded verdict를 가지며 final displayed claim은 `support`만 존재.
- missing/duplicate/orphan citation 0건.
- 정확히 15-slide deck, slide source footer, six SVG+PNG figures, visual/compatibility PASS.
- Severity 1/2 unresolved 0건; 허용된 Severity 3는 `QA2`에 완전 공개.
- staging/published PPTX byte/hash 동일, sidecar 포함.
- release manifest가 self-reference 없이 검증되고 immutable checkpoint가 path/count/nonzero size/SHA-256 비교를 통과.
- `plan2.md`, `execution_log2.md`, `QA2.md/json` 및 모든 v2 deliverable이 열리고 non-empty이며 서로 일치함.
