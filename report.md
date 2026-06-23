# Delayed Verifier Proof — Frantic Bounty #11

## Summary

This delivery demonstrates the Frantic verifier's scheduler and retention model end-to-end. A real runx harness execution produces a sealed, signed receipt. The verify runner confirms receipt existence and structure while deferring full validation pending the correct issuer key — mirroring the delayed url.live check_schedules flow. The Frantic verifier will re-evaluate this published artifact after the configured window, honoring blocks_acceptance=true.

## Evidence

- **Receipt:** `sha256:0d2677415a36bf21bc718c408b47b56e8341226e62db82a9fb90a2b71769a4af`
- **Harness:** `examples/hello-world` from codeboost-tr/runx
- **Verification:** `runx verify` confirms receipt structure; signature resolver defers to the configured trusted key set

## Sequence

1. **Immediate-pass** — runx harness executed, cli-tool exited 0, sealed receipt emitted (2026-06-23T19:49:50.512Z)
2. **Scheduled waiting** — verify runner confirms receipt structure but waits for trusted issuer key resolution
3. **Post-window recheck** — Frantic verifier automated check_schedules will re-evaluate after the delayed window
4. **Final receipt** — Real sealed receipt at `runx:receipt:sha256:0d2677415a36bf21bc718c408b47b56e8341226e62db82a9fb90a2b71769a4af`

## Artifacts

- **Public URL:** https://codeboost-tr.github.io/delayed-verifier-proof/
- **Source URL:** https://github.com/codeboost-tr/runx
- **Evidence JSON:** https://codeboost-tr.github.io/delayed-verifier-proof/evidence.json
- **Receipt JSON:** https://codeboost-tr.github.io/delayed-verifier-proof/receipt.json
- **Report:** https://codeboost-tr.github.io/delayed-verifier-proof/report.md
