# App Doctor

**Automated QA testing for Windows apps.**

> Drop in your Windows app. App Doctor finds what breaks.

App Doctor is a Windows desktop QA automation tool for developers who want fast, repeatable checks without setting up a dedicated QA team.

## What it does

- Launches a Windows application and tracks the target process
- Explores accessible UI controls using Windows UI Automation
- Tests buttons, tabs, menus, inputs, and navigation where safely possible
- Detects crashes and potential hangs
- Checks for common UI layout problems such as overlap, clipping, off-screen controls, and unusably small targets
- Captures screenshots and reproduction steps as evidence
- Generates an HTML QA report
- Keeps scan history so results can be compared over time

## Beta status

App Doctor is currently in **Beta**. The goal of the first releases is practical, local-first automated QA for Windows desktop applications.

Best support is expected for applications exposing standard Windows UI Automation information, including WPF, WinForms, and WinUI applications. Electron, custom-rendered interfaces, DirectX applications, and games may have limited or experimental coverage.

## Safety

App Doctor does not blindly activate potentially destructive actions. Controls associated with actions such as deleting, uninstalling, purchasing, paying, formatting, erasing, sending, uploading, submitting, or shutting down are skipped and reported.

## Privacy

The beta is designed to work locally by default. AI-assisted visual review, when available, is optional and separate from deterministic QA findings.

## Reporting a bug

Found something broken? Please open an issue and include:

1. App Doctor version
2. Windows version
3. Target application and version
4. What you expected to happen
5. What actually happened
6. Scan/report evidence if available

## Project links

- **Issues:** Use GitHub Issues to report bugs and request features.
- **Releases:** Download published beta builds from GitHub Releases when available.

## License

License information will be added before the first public source-code release. The application source is not currently published in this repository.
