# Changelog

## 0.1.0-beta.3 — 2026-09-20

- Stream HTML report evidence and session JSON to reduce memory allocations while preserving atomic saves and existing data on cancellation or write failure.
- Add report search hints, delayed filtering, visible/total counts, filter reset and clearer empty states.
- Add a Follow latest log switch and steadier elapsed-time/Stop feedback while the worker is busy.
- Preserve history comparison selections after refresh and clear stale results when the selected pair changes.

Validation: Release build 0 warnings/errors, 28 executable regression tests, 6 WPF behavior groups including an owned-target stop, and self-contained portable launch/navigation smoke passed. Six pages were rendered at two viewport/DPI combinations; this does not replace physical display testing.

In an eight-image synthetic report fixture, managed allocations fell from about 75.6 MB to 0.75–0.96 MB, with identical HTML except for the version footer. This does not measure overall scan speed or peak application memory.

## 0.1.0-beta.2 — 2026-09-14

- Added narrowly verified UI handoff support when the selected launch creates exactly one new same-executable direct child that exposes the visible UI.
- Hardened handoff safety so pre-existing processes, different-executable children, and ambiguous multiple same-executable children are not adopted.
- Revalidated cleanup using PID plus creation time for the original launch and any adopted handoff instance.
- Expanded Windows 11 real-app validation to Notepad, Character Map, Paint, and Calculator launcher behavior.
- Expanded the executable regression suite to 24 passing tests, including positive and negative handoff cases.
- Kept shell-mediated packaged-app activation as a documented limitation when Windows does not expose a trustworthy caller-to-package-process relationship.

Release-candidate validation passed 24/24 executable tests with a Release build reporting 0 warnings and 0 errors. The public beta.2 portable ZIP was also downloaded from GitHub, hash-verified, freshly extracted, and launch/navigation smoke-tested after publication.

## 0.1.0-beta.1 — 2026-09-13

- Added Windows UI Automation based bounded exploration for accessible desktop UI.
- Added crash/potential-hang monitoring, layout observations, screenshot evidence, reproduction steps, standalone HTML reports, and local scan history.
- Added safety filtering that skips identified destructive or high-risk actions instead of blindly activating them.
- Added optional AI-assisted visual review, separate from deterministic findings.
- Added closed-source App Doctor Free Beta license terms while preserving third-party licenses.

Release-candidate validation on the current Windows 11 QA machine completed for the core Free Beta workflow. The executable regression suite passed 21/21 with a Release build reporting 0 warnings and 0 errors. The public Free Beta was published as `v0.1.0-beta.1`; remaining environment limitations are documented in `KNOWN_ISSUES.md`.
