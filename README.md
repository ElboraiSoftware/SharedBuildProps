# MSBuild configuration shared between Elborai Software projects

- .gitignore, a complete gitignore ruleset for Visual Studio projects
- .editorconfig, formatting/coding style rules for C#
- Directory.Build.props, ensure common assembly authorship information
- TheSolutionName.sln.DotSettings, Resharper solution-wide config
- LICENSE.txt, a "Free use, No derivatives" license

## How to use

Either copy manually files to a solution root, or use this repository as a template on GitHub.

### Directory.Build.props

1. Copy manually to a solution root directory.
2. Set `SOLUTION_PREFIX_DIRECTORY_BUILD_PROPS_FILE` to the correct value (empty if no prefix needed).

### TheSolutionName.sln.DotSettings

1. Copy manually to a solution root directory.
2. Rename to `<SolutionName>.sln.DotSettings`.
