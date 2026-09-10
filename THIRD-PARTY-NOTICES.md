# Dependency and license inventory

App Doctor application code is proprietary closed-source Free Beta software under the terms in `LICENSE`. That App Doctor license does not alter any third-party license listed below.

The application uses Microsoft .NET 8, WPF, Windows Forms drawing support in the isolated screenshot worker, Microsoft UI Automation, and built-in Windows APIs. Third-party components remain under their original licenses and terms.

| Dependency | License / terms | Source |
|---|---|---|
| .NET runtime and SDK libraries | MIT | https://github.com/dotnet/runtime/blob/main/LICENSE.TXT |
| Windows Desktop / WPF | MIT | https://github.com/dotnet/wpf/blob/main/LICENSE.TXT |
| Windows Forms / System.Drawing in worker | MIT | https://github.com/dotnet/winforms/blob/main/LICENSE.TXT |
| Windows UI Automation, DPAPI, Win32 APIs | Components of the user's licensed Windows installation | https://learn.microsoft.com/en-us/windows/win32/winauto/entry-uiauto-win32 |

Self-contained portable archives redistribute the Microsoft runtime. The packaging process includes the restored runtime license and third-party notice files in the portable `licenses/` directory. Those notices should remain with the distributed build.

Optional OpenAI API use is a network service rather than a bundled library. It requires the user's own API credentials and is subject to the provider's applicable API terms and charges.

No App Doctor source code is published in this public repository.
