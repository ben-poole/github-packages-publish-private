# github-packages-publish-private

Publish from a private github repository (https://github.com/ben-poole/github-packages-publish-private) to a public one (https://github.com/ben-poole/github-packages-publish-public)

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
