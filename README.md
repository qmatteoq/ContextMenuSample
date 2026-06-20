# File Explorer context menu sample (Shell Extension + MSIX)

A sample that shows how to add a custom **File Explorer context menu** entry from a desktop
application, using a Windows **Shell Extension** (an `IExplorerCommand` COM handler) that is
registered through **MSIX package** declarations rather than the registry.

## What's included

| Project | Stack | Responsibility |
| --- | --- | --- |
| `ExplorerCommandVerb` | C++ | The COM shell extension (`IExplorerCommand` / `IExplorerCommandState`) that adds and handles the context-menu verb. |
| `ContextMenuSample` | C# / WPF | The desktop application the menu launches / interacts with. |
| `ContextMenuSample.Package` | Windows Application Packaging Project | Packages the app + shell extension as **MSIX** and declares the context-menu extension in `Package.appxmanifest` (`com.microsoft.windows.fileexplorercontextmenu`). |

## Prerequisites

- Windows 10/11
- Visual Studio 2019/2022 with:
  - **Desktop development with C++**
  - **.NET desktop development**
  - **Universal Windows Platform / MSIX packaging tools** (Windows Application Packaging Project)

## Getting started

1. Clone the repository and open `ContextMenuSample.sln`.
2. Set `ContextMenuSample.Package` as the startup project.
3. Build and deploy (F5) — Visual Studio registers the MSIX package locally.
4. Right-click a file in File Explorer to see the custom command.

## License

This sample is provided **as-is**, for demonstration purposes. No explicit license has
been specified.
