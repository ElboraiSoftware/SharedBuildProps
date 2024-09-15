# Elborai Software .NET Project Templates

This repository contains templates for Elborai Software .NET projects.

## Installation

To install a template, such as `elboraisoftware`, use the following command:

```psh
PS> dotnet new --install https://github.com/ElboraiSoftware/SharedBuildProps/main/elboraisoftware
```

## Usage

After installation, create new .NET solutions/projects with:

```psh
PS> dotnet new elboraisoftware -n MyCoolProject
```

### Template Options

The template supports the following options:

- `--useElboraiPackages`: Include Elborai Software's private GitHub Packages source in the nuget.config file.

Example usage with options:

```
dotnet new elboraisoftware -n MyCoolProject --useElboraiPackages true
```

## `elboraisoftware` Template Structure

- `src/`: Contains the source code projects
- `tests/`: Contains the test projects
- `.github/workflows/`: GitHub workflows
- `.editorconfig`: Editor configuration file
- `.gitignore`: A complete gitignore ruleset for Visual Studio projects
- `Directory.Build.props`: Common build properties, ensure common assembly authorship information
- `LICENSE.txt`: A "Free use, No derivatives" license
- `nuget.config`: NuGet configuration
- `README.md`: Project readme file
- `<The templated name>.sln`: Solution file
- `<The templated name>.sln.DotSettings`: ReSharper/Rider settings file

## How to use NuGet packages from ElboraiSoftware's GitHub Packages

```psh
PS> dotnet nuget add source --username "<USERNAME>" --password "<PERSONAL_ACCESS_TOKEN>" --configfile ./nuget.config
```
