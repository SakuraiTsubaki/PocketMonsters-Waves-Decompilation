# Bug Eradication Policy

Pocket Monsters Waves uses a zero-known-defect objective for maintained reconstructed or modified builds.

Original behavior is preserved as evidence, but confirmed defects are corrected in the maintained build. Every report must remain traceable to an identified version and a reproducible test.

## Covered defect classes

Track crashes, freezes, save failures, progression blockers, softlocks, battle logic errors, AI errors, map/collision problems, out-of-bounds behavior, event and quest state errors, duplication problems, capture/evolution/encounter defects, inventory and reward errors, graphics/animation/UI/text/localization/audio problems, input/controller problems, performance/loading/resource problems, communication/online/HOME problems, date/time/weather errors, version or language specific defects, update regressions, invalid-state handling errors, boundary-condition errors, and unintended cross-system interactions.

## Status values

Use `unverified`, `reproduced`, `confirmed`, `fixed`, `verified-fixed`, `not-a-bug`, `duplicate`, or `cannot-test`.

A report is not `confirmed` until evidence identifies the affected build and reproduces the behavior. A defect is not `verified-fixed` until the corrected build passes a repeatable regression check and relevant adjacent behavior has also been checked.

## Required record

For each defect record the target version/update/DLC, region, language, build identifiers or hashes when available, reproduction steps, expected and actual behavior, root cause, fix reference, regression test, affected versions, and verification result.

Complete game images stay outside Git. Store hashes, manifests, extracted non-ROM work products, patches, tests, logs, and documentation according to `ARTIFACT_POLICY.md`.

## Cross-version rule

A defect found in Waves must trigger a check of the corresponding Winds subsystem when applicable. Shared-root defects should use aligned IDs and cross-links.

## Historical preservation

Never delete the original defect record after fixing it. If an official update later fixes the same issue, record the official fixed version separately from this project's correction.

## Working files

- `manifests/bugs.csv` — master catalog.
- `.github/ISSUE_TEMPLATE/bug.yml` — structured report intake.
- `tests/` — regression checks.
- `patches/` — corrective patch artifacts and manifests.
- `logs/` — reproduction and verification logs.

Goal: no known reproducible defect remains unfixed in the maintained build, while original behavior remains documented.