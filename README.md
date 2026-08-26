# scriptingvb

VB.NET WinForms host that compiles VB or C# scripts at runtime against plugin interfaces. The Host WinExe uses CodeDom (`VBCodeProvider` / `CSharpCodeProvider`) to compile an `IScript` plugin in memory, then calls `Method1`–`Method4` from the main form. `Interfaces` is a class library that defines `IScript` and `IHost`. Open `Scripting/Scripting.sln` in Visual Studio.

**Source last updated:** 2008-10-02  
**Language:** VB.NET  
**Target:** Visual Studio 2005 (.NET 2.0 era, ProductVersion 8.0.50727)  
**Output:** Library, WinExe

## What it is

This is Dave Robinson’s VB.NET sample: a WinForms host that compiles VB or C# at runtime via CodeDom against plugin interfaces. Edit the script in `frmScript`, compile against `Interfaces.dll`, and the host locates the `IScript` type in the in-memory assembly. The technique follows Tim McCurdy’s (Divil) article on adding scripting to .NET applications; that article is provenance for the approach, not a third-party source dump of someone else’s tree.

## Solution structure

| Project | Language | Output | Path |
|---------|----------|--------|------|
| `Interfaces` | VB.NET | Library | `Interfaces/Interfaces.vbproj` |
| `Host` | VB.NET | WinExe | `Scripting/Host/Host.vbproj` |

## How to open

Open `Scripting/Scripting.sln` in Visual Studio.

## Attribution and provenance

- **Author:** Dave Robinson / VaderConsulting
- Technique comment in `Scripting/Host/Scripting.vb` points to <http://www.divil.co.uk/net/articles/plugins/scripting.asp> (Tim McCurdy / Divil). This repository is Dave’s sample, not a dump of third-party source.

## License

MIT. See `LICENSE`.
