# github-packages-publish-private

Publish from a private github repository (https://github.com/ben-poole/github-packages-publish-private) to a public one (https://github.com/ben-poole/github-packages-publish-public)

## Publishing to GitHub Packages

### Using a GitHub Actions workflow

### Authenticating the workflow with a personal access token

1. A personal access token (PAT) with the `write:packages` scope needs creating by a user with write access to the target repository (github-packages-publish-public): https://github.com/settings/tokens/new

2. Store this PAT in GitHub Actions secrets as `PUBLISH_PAT`: https://github.com/ben-poole/github-packages-publish-private/settings/secrets/actions

### Running the workflow

1. Navigate to the workflow GitHub actions: https://github.com/ben-poole/github-packages-publish-private/actions/workflows/build-and-publish.yml
2. Click "Run workflow"
3. Select the branch
4. Click "Run workflow"

### Locally

An `~/.npmrc` file is required with a PAT.

```
//npm.pkg.github.com/:_authToken=ghp_PAT
```

```
npm run build
npm publish
```
