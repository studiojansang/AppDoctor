# App Doctor

**Automated QA testing for Windows desktop apps.**

App Doctor is a Windows desktop QA automation tool that launches a target application, inspects UI exposed through Windows UI Automation, performs bounded safety-filtered interactions, and records evidence for issues it can observe.

Current development version: **0.1.0-beta.1**. A public Free Beta binary release has not been published yet.

## What it does

- Launches a Windows application and tracks the target process
- Explores accessible UI controls using Windows UI Automation
- Tests supported buttons, tabs, menus, inputs, and navigation where safely possible
- Detects crashes and potential hangs
- Checks for common UI layout problems such as overlap, clipping, off-screen controls, and unusably small targets
- Captures screenshots and reproduction steps as evidence
- Generates a standalone HTML QA report
- Keeps scan history so results can be compared over time

## Beta status and support scope

App Doctor is currently a **Free Beta** project. Best support is expected for applications that expose standard Windows UI Automation information, especially WPF, WinForms, WinUI, and conventional Win32 desktop applications.

Electron applications, custom-rendered interfaces, DirectX applications, games, remote surfaces, security desktops, and other UI that does not expose usable accessibility information may have limited or experimental coverage. App Doctor does not claim to perfectly inspect every Windows application or every UI state.

## Safety

App Doctor does not blindly activate potentially destructive actions. Controls associated with actions such as deleting, removing, uninstalling, purchasing, paying, formatting, erasing, sending, submitting, uploading, or shutting down are skipped when identified and recorded in the report.

UI automation can still cause real application behavior. Use test accounts, disposable data, and an appropriate test environment for applications that can modify important data or systems.

## Privacy

The beta is designed to work locally by default. AI-assisted visual review, when enabled by the user, is optional and separate from deterministic QA findings. The application does not require an App Doctor account, telemetry service, or license server for the Free Beta.

## Reporting a bug

Found something broken? Please open an issue and include:

1. App Doctor version
2. Windows version and display scaling if relevant
3. Target application and version
4. What you expected to happen
5. What actually happened
6. Scan/report evidence if available and safe to share

Do not post API keys, credentials, private source code, or sensitive application data in a public issue.

## Project links

- **Issues:** Use GitHub Issues to report bugs and request features.
- **Releases:** Published Free Beta builds will be available from GitHub Releases after release validation is complete.

## License

App Doctor itself is **closed-source Free Beta software**, not open-source software. The Free Beta license permits no-charge use for evaluation, software testing, development QA, and internal use, but does not grant source-code access or a general right to resell or redistribute App Doctor. See `LICENSE` for the distribution terms.

Microsoft/.NET and other third-party components remain under their original licenses. See `THIRD-PARTY-NOTICES.md` and the notices included with a portable build.

This public repository is for documentation, issue tracking, and release information. App Doctor source code is maintained separately in a private repository.
