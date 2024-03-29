# MSBuild configuration shared between Elborai Software projects

[![.Net build and test](https://github.com/ElboraiSoftware/REPLACE_ME/actions/workflows/dotnet_build_and_test.yml/badge.svg)](https://github.com/ElboraiSoftware/REPLACE_ME/actions/workflows/dotnet_build_and_test.yml)
[![Publish NuGet package](https://github.com/ElboraiSoftware/REPLACE_ME/actions/workflows/publish_nuget_package.yml/badge.svg)](https://github.com/ElboraiSoftware/REPLACE_ME/actions/workflows/publish_nuget_package.yml)
[![WPF build and test](https://github.com/ElboraiSoftware/REPLACE_ME/actions/workflows/wpf_build_and_test.yml/badge.svg)](https://github.com/ElboraiSoftware/REPLACE_ME/actions/workflows/wpf_build_and_test.yml)
[![UWP build and test](https://github.com/ElboraiSoftware/REPLACE_ME/actions/workflows/uwp_build_and_test.yml/badge.svg)](https://github.com/ElboraiSoftware/REPLACE_ME/actions/workflows/uwp_build_and_test.yml)

- .gitignore, a complete gitignore ruleset for Visual Studio projects
- .editorconfig, formatting/coding style rules for C#
- .github/workflows, default github actions to test, build, and publish .Net projects
- Directory.Build.props, ensure common assembly authorship information
- TheSolutionName.sln.DotSettings, Resharper solution-wide config
- LICENSE.txt, a "Free use, No derivatives" license
- nuget.config, config to use private nuget packages, requires credentials

## How to use

Either copy manually files to a solution root, or use this repository as a template on GitHub.

### Directory.Build.props

1. Copy manually to a solution root directory.
2. Set `SOLUTION_PREFIX_DIRECTORY_BUILD_PROPS_FILE` to the correct value (empty if no prefix needed).

### TheSolutionName.sln.DotSettings

1. Copy manually to a solution root directory.
2. Rename to `<SolutionName>.sln.DotSettings`.

### How to use NuGet packages from ElboraiSoftware's GitHub Packages

```psh
PS> dotnet nuget add source --username "<USERNAME>" --password "<PERSONAL_ACCESS_TOKEN>" --configfile ./nuget.config
```
