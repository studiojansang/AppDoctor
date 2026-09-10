# App Doctor Free Beta — Known limitations

These limitations apply to the current 0.1.0-beta.1 validation candidate and should be reviewed again before a public binary release.

## UI coverage

- Best coverage is expected for WPF, WinForms, WinUI, and conventional Win32 applications that expose useful Windows UI Automation metadata.
- Electron applications can move their visible UI to a different process or reuse an already-running process, which can limit PID-scoped inspection.
- Games, DirectX/custom-rendered UI, browser canvases, remote surfaces, secure desktops, and other interfaces without useful accessibility metadata can be Limited or Unsupported.
- App Doctor does not use blind coordinate clicking to claim coverage where semantic UI Automation data is unavailable.

## Safety and side effects

- App Doctor skips identified destructive/high-risk actions, but UI Automation still invokes real application behavior. Incorrectly labelled controls or unusual application behavior can still cause side effects.
- Use test accounts, disposable data, and backups for applications that can modify important data or systems.
- App Doctor is not a VM or security sandbox.

## Detection limits

- Layout observations based on UIA bounding rectangles can produce low-confidence observations; not every clipping or overlap finding is visually provable from UIA alone.
- A single UI Automation timeout is not treated as proof of a permanent application hang.
- Normal application exit is not treated as a crash solely because the process ended.
- Scan bounds, time limits, accessibility quality, and dynamic UI can prevent complete state coverage.

## Environment validation still pending

- No broad compatibility certification has been completed across third-party Win32/WinForms/WinUI/Electron applications.
- Physical multi-monitor DPI transitions have not yet been fully validated for this candidate.
- A separate Windows 10 machine has not yet been used for final validation.
- Native file/folder picker and Explorer drag/drop paths require final release-candidate click-through validation.
- Optional OpenAI visual review has not been validated using a live paid API request; account entitlement, billing, and provider-side availability remain user-specific.

## Source repair scope

The Free Beta source-fix feature is intentionally narrow. It supports a deterministic WPF XAML target-size fix when the affected control can be matched exactly and the build/rescan verification gates succeed. It is not a general-purpose AI code repair system.
