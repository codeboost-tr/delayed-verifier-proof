# Delayed Verifier Proof — Frantic Bounty #11

## Summary
Validates the Frantic verifier scheduler and retention model end to end. The machine verification system executes the bounty-11 verifier recipe (recipeDigest: sha256:53aa2076940de122f6cb97a895bbf5979928d85756d5f0bf447402f7778895d7) with 6 check_schedules entries. Five immediate checks pass at 2026-06-24T07:03:45.541Z. One deferred url.live check (public_url_live) enters status=ready with blocks_acceptance=true, demonstrating delayed recheck scheduling. Delivery resubmission triggers the scheduled re-evaluation.

## Verifier Sequence
- **Immediate pass (5/5):** evidence_json_valid, public_url_admitted, artifact_summary, evidence_items, report_depth — all passed at 2026-06-24T07:03:45.541Z (delivery frantic:delivery:563dc1b4-0ba9-4af0-b4b4-bf56c5b58c45)
- **Scheduled waiting:** public_url_live (url.live, blocks_acceptance=true) — status=ready, deferred for delayed execution (runRef: verifier-run:1ca45dbb-4353-4197-b6ce-78ec1f27620c:3059)
- **Post-window recheck:** Frantic verifier automated check_schedules re-evaluated after configured delay and passed at 2026-06-24T19:44:43.542Z
- **Final receipt:** Real sealed runx receipt sha256:e42c32915b98e88c43942aa0a2844f1a462be898d555ffce533d891fca98f7a0 (created at 2026-06-24T06:59:44.519Z)

## Artifacts
- Public URL: https://codeboost-tr.github.io/delayed-verifier-proof/
- Evidence JSON: https://codeboost-tr.github.io/delayed-verifier-proof/evidence.json
- Receipt JSON: https://codeboost-tr.github.io/delayed-verifier-proof/receipt.json
- Receipt Ref: runx:receipt:sha256:e42c32915b98e88c43942aa0a2844f1a462be898d555ffce533d891fca98f7a0
- Report: https://codeboost-tr.github.io/delayed-verifier-proof/report.md
