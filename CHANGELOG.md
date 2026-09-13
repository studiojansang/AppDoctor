# Changelog

## 0.1.0-beta.1 — 2026-09-13

- Added Windows UI Automation based bounded exploration for accessible desktop UI.
- Added crash/potential-hang monitoring, layout observations, screenshot evidence, reproduction steps, standalone HTML reports, and local scan history.
- Added safety filtering that skips identified destructive or high-risk actions instead of blindly activating them.
- Added optional AI-assisted visual review, separate from deterministic findings.
- Added closed-source App Doctor Free Beta license terms while preserving third-party licenses.

Release-candidate validation on the current Windows 11 QA machine completed for the core Free Beta workflow. The executable regression suite passed 21/21 with a Release build reporting 0 warnings and 0 errors. The public Free Beta was published as `v0.1.0-beta.1`; remaining environment limitations are documented in `KNOWN_ISSUES.md`.
