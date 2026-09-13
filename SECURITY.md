# Security Policy

## Supported version

Security reports for the current public Free Beta, `0.1.0-beta.1`, are welcome.

## Reporting a security issue

Do not publish exploit details, credentials, API keys, private source code, private reports, or sensitive application data in a public issue.

If GitHub shows a **Report a vulnerability** option for this repository, use that private reporting flow.

If a private vulnerability form is not available, open a minimal public issue titled `[Security] Private report requested` and include only a non-sensitive summary plus the affected App Doctor version. Do not include reproduction secrets, exploit details, credentials, or private files. A maintainer can then arrange a private channel for the full report.

Ordinary product bugs that do not involve a security vulnerability can use the normal Bug Report template.

## Scope notes

App Doctor performs real Windows UI Automation actions and is not a virtual machine or security sandbox. Testing applications that can modify important data or systems should be done with test accounts, disposable data, and appropriate backups.

The current Free Beta binary is unsigned. Verify the release asset against the published `SHA256SUMS.txt` when integrity matters.

## Sensitive information

Before sharing screenshots, HTML reports, logs, or reproduction steps, remove credentials, tokens, personal information, proprietary source code, and any other data that should not be public.
