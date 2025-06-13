# DMS.Demo.Dependency.Management.Dependabot

## Dependabot Setup

### Enabling Dependabot
1. In your GitHub repository, navigate to the "Settings" tab.
2. Scroll down to the "Security" section.
3. Click on "Advanced Security".
4. Find & enable "Dependency graph".
5. Under, "Dependabot", enable the "Dependabot alerts" option.

### Automatic Updates
To enable automatic dependency updates with Dependabot:
*** Ensure that either "Dependabot security updates" or "Dependabot version updates" is enabled. 
   - "Dependabot security updates" will automatically update dependencies with known vulnerabilities.
   - "Dependabot version updates" will automatically update dependencies to the latest versions.

1. Create a `.github` directory in the root of your repository if it does not exist.
2. Inside `.github`, create a file named `dependabot.yml` with the following content:
3. Add the following configuration to the file:
```yaml
# To get started with Dependabot version updates, you'll need to specify which
# package ecosystems to update and where the package manifests are located.
# Please see the documentation for all configuration options:
# https://docs.github.com/code-security/dependabot/dependabot-version-updates/configuration-options-for-the-dependabot.yml-file

version: 2
updates:
  - package-ecosystem: nuget # See documentation for possible values
    directory: "/" # Location of package manifests
    schedule:
      interval: daily
```