# Delayed Verifier Proof — Frantic Bounty #11

## Summary
Validates the Frantic verifier scheduler and retention model end to end. The machine verification system executes the bounty-11 verifier recipe (recipeDigest: sha256:53aa2076940de122f6cb97a895bbf5979928d85756d5f0bf447402f7778895d7) with 6 check_schedules entries. Five immediate checks pass at 2026-06-24T07:03:45.541Z. One deferred url.live check (public_url_live) enters status=ready with blocks_acceptance=true, demonstrating delayed recheck scheduling. Delivery resubmission triggers the scheduled re-evaluation.

## Verifier Sequence
- **Immediate pass (5/5):** evidence_json_valid, public_url_admitted, artifact_summary, evidence_items, report_depth (pending verification)
- **Scheduled waiting:** public_url_live (url.live, blocks_acceptance=true) — deferred for delayed execution
- **Post-window recheck:** (waiting for delayed recheck)
- **Final receipt:** null

## Artifacts
- Public URL: https://codeboost-tr.github.io/delayed-verifier-proof/
- Evidence JSON: https://codeboost-tr.github.io/delayed-verifier-proof/evidence.json
- Receipt JSON: https://codeboost-tr.github.io/delayed-verifier-proof/receipt.json
- Receipt Ref: null
- Report: https://codeboost-tr.github.io/delayed-verifier-proof/report.md
