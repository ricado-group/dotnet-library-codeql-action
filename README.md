# .NET Library CodeQL Action
A Composite Action that runs CodeQL to Analyze a .NET 6/7 Library

## Inputs

### `private-nuget-url`

**Required** The URL of the Private NuGet Repository (e.g. https://nuget.pkg.github.com/myname/index.json)

### `private-nuget-token`

**Required** The Token used for Authentication with the Private NuGet Repository

## Example Usage

```yml
uses: ricado-group/dotnet-library-codeql-action@v1
with:
  private-nuget-url: 'https://nuget.pkg.github.com/myname/index.json'
  private-nuget-token: ${{ secrets.PERSONAL_ACCESS_TOKEN }}
```

## Stay Updated with Dependabot

Use [Dependabot](https://docs.github.com/en/github/administering-a-repository/keeping-your-actions-up-to-date-with-github-dependabot) to update your GitHub Actions by creating a `.github/dependabot.yml` file:

```yaml
version: 2
updates:
  # Maintain Dependencies for GitHub Actions
  - package-ecosystem: "github-actions"
    directory: "/"
    schedule:
      interval: "daily"
```