# github-packages-publish-private

Publish from a private github repository (this) to a public one (https://github.com/ben-poole/github-packages-publish-public)

## Publishing to GitHub Packages

### Using GitHub Actions

A personal access token (PAT) with the `write:packages` scope needs creating by a user with write access to the target repository (github-packages-publish-public): https://github.com/settings/tokens/new

Store this PAT in GitHub Actions secrets as `PUBLISH_PAT`: https://github.com/OWNER/REPO/settings/secrets/actions

### Locally

An `~/.npmrc` file is required with a PAT.

```
//npm.pkg.github.com/:_authToken=ghp_PAT
```

```
npm run build
npm publish
```
