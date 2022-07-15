# github-packages-publish

Publish from a private github repository (github-packages-publish) to a public one (github-packages-publish-public)

## Publish locally

An `~/.npmrc` file is required.

```
//npm.pkg.github.com/:_authToken=ghp_PAT
```

Replace `ghp_PAT` with a personal access token generated for a GitHub account with write access to: github-packages-publish-public

```
npm run build
npm publish
```