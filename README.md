# MTVaught Dark Theme

A dark color theme for Visual Studio Code.

## Development

### Prerequisites

Install the [vsce](https://github.com/microsoft/vscode-vsce) packaging tool:

```bash
npm install -g @vscode/vsce
```

### Build & Package

Package the theme into a `.vsix` file:

```bash
vsce package
```

This produces a `vscode-mtvaught-dark-theme-<version>.vsix` file in the project root.

### Install Locally

Install the packaged extension directly in VS Code:

```bash
code --install-extension vscode-mtvaught-dark-theme-<version>.vsix
```

## Release Process

Nightly prereleases run from GitHub Actions on a schedule and can also be
started manually. The workflow finds the latest successful `Build` workflow run
on `main`, downloads its VSIX artifact, and creates a GitHub prerelease if that
commit has not already been prereleased as `nightly-*`.

To publish a stable GitHub release, run the `Release` workflow manually and
provide the nightly tag or commit SHA to promote. The workflow packages that
exact ref and creates a stable release tagged from the extension version in
`package.json`.

Marketplace publishing is intentionally commented out in the workflows until a
VS Code Marketplace publisher account and `VSCE_PAT` repository secret are set
up.
