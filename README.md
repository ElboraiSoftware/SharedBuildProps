# MSBuild configuration shared between Elborai Software projects

- .gitignore, a complete gitignore ruleset for Visual Studio projects
- .editorconfig, formatting/coding style rules for C#
- Build.props, reduce need to manually specify common namespaces
- Directory.Build.props, ensure common assembly authorship information

## How to use

Be sure to clone this repository in an `ElboraiSoftware` directory.

```psh
PS> cd Development\ElboraiSoftware
C:\Users\Sam\Development\ElboraiSoftware PS> git clone git@github.com:ElboraiSoftware/SharedBuildProps.git
```

### .gitignore

1. Copy manually to a solution root directory.

### .editorconfig

1. Copy manually to a solution root directory.

### Build.props

1. Copy manually to a solution root directory.
2. Replace `SOLUTION_NAME_UPDATE_BUILD_PROPS_FILE` in the copied Build.props.

### Directory.Build.props

Two solutions:

1. (preferred) Manually copy the file to the solution directory and commit into git. It will have to be updated by hand if something changes in this shared build props repository.

2. (may cause issues) Create a symlink in the directory tree, above directories containing visual studio projects.

```psh
PS> cd Development
C:\Users\Sam\Development PS> new-item -path Directory.Build.props -itemtype SymbolicLink -value C:\Users\Sam\Development\ElboraiSoftware\SharedBuildProps\Directory.Build.props
```

⚠️ Unfortunately git will just add the symbolic link instead of its target, so that's not too ideal as the props file won't be included in the repository.
