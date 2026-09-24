# QA2 — Graves’ disease / thyroid eye disease landscape v2

- Release ID: `graves-ted-landscape-v2-cut-2026-09-10-r001`
- Data cut: **2026-09-10**
- Overall pre-checkpoint release verdict: **PASS**
- Unresolved Severity 1: **0**
- Unresolved Severity 2: **0**
- Disclosed conclusion-neutral Severity 3: **3**
- Final checkpoint authority: `checkpoint_receipt_v2.json` (created last)

## Claim and semantic gates

- Ledger claims: 202; blind support: 196; six non-support claims are ledger-only; displayed non-support: 0.
- Report/canonical consistency failures: 0.
- Slide 15 correction: removed unsupported `Thyroid hormones + ATD taper` and `TED structural + GD biochemical concordance`; retained bounded CONCLUSION-004 readouts.
- Same-coordinator stance-hidden review reduces anchoring bias but is not independent validation.

## Source and presentation gates

- Source-ID and claim-ID unresolved: 0; query-level absence assertions: 0.
- Exactly 15 slides, six SVG + six PNG figures, 21/21 visual PASS, structural and compatibility PASS.
- No PDF created.

## Severity 3 disclosures

### S3-KR-RAI-5.3
- Finding: Korean RAI Recommendation 5.3 narrative says prophylaxis 'may be considered' while Table 3 says 'Steroid prophylaxis recommended'.
- Owner: Evidence curation lead
- Impact: Conclusion-neutral source-internal strength discrepancy; no pivotal number or authorization conclusion changes.
- Mitigation: Preserved both exact anchors and disclosed the discrepancy in report/canonical claim SOC-CONFLICT-KR-RAI; rejected uniform historical wording.
- Residual uncertainty: The source does not provide an explicit reconciliation between narrative and table strength.

### S3-MEDIA-CHECK-FALLBACK
- Finding: Read(media_output_check) failed twice because the platform rejected its temperature parameter, including the Step 8 slide-15 recheck.
- Owner: Release visual-QA owner
- Impact: QA-method degradation only; no structural or visual defect identified.
- Mitigation: Manual visual inspection with Read(mode=low), structural validation, render inventory, and compatibility validation; all 15 slides and six figures retain PASS rows, with corrected slide 15 rechecked.
- Residual uncertainty: Automated media-check model output is unavailable.

### S3-REGIONAL-STATUS-GAPS
- Finding: Some authorization/reimbursement/access statuses remain unresolved (including Korean Tepezza/Lumvoa, non-US Lumvoa contexts, EU/UK access, and Japanese reimbursement).
- Owner: Regional source-surveillance owner
- Impact: Conclusion-neutral metadata/access gap because no negative determination is made.
- Mitigation: Official-search records 745-752 and authoritative fallback context are retained; query-level unresolved records are prohibited from proving absence.
- Residual uncertainty: Status may change or require jurisdiction-specific confirmation after the frozen cut.

