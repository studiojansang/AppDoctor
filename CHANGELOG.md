# Changelog

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
