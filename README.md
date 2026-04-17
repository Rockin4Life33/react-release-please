# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

Dependencies are managed with [pnpm](https://pnpm.io/). Install them with `pnpm install` (see [Corepack](https://nodejs.org/api/corepack.html) if you need to enable the pinned version from `package.json`).

## Available Scripts

In the project directory, you can run:

### `pnpm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `pnpm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `pnpm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `pnpm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Releases and versioning

Versioning is automated with [release-please](https://github.com/googleapis/release-please) via [`.github/workflows/release-please.yml`](.github/workflows/release-please.yml). Use [Conventional Commits](https://www.conventionalcommits.org/) on the default integration branches:

- `fix:` — patch bump
- `feat:` — minor bump
- `feat!`, `fix!`, or a `BREAKING CHANGE` footer — major bump

### Branches

- **`develop`** — prerelease line `X.Y.Z-beta.N` in `package.json`, tags `vX.Y.Z-beta.N`, changelog in [`CHANGELOG.prerelease.md`](CHANGELOG.prerelease.md).
- **`master`** — stable `X.Y.Z` in `package.json`, tags `vX.Y.Z`, changelog in [`CHANGELOG.md`](CHANGELOG.md).

### Release PR workflow

1. Merge your feature or fix PR into `develop` or `master` using conventional commit messages.
2. On push, release-please opens or updates a **Release PR** (version bump, manifest, changelog). It does not add a version commit to every feature PR.
3. When you are ready to publish that version, **merge the Release PR**. That merge creates the GitHub Release and the `v…` tag.

Enable **Allow GitHub Actions to create and approve pull requests** under repository Settings → Actions → General so release-please can open Release PRs. If other CI workflows must run on Release PRs, configure a personal access token for the workflow as described in the [release-please-action README](https://github.com/googleapis/release-please-action).

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).
