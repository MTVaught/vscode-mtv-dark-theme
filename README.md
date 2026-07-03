# MTV Dark Color Theme

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

This produces a `mtv-dark-<version>.vsix` file in the project root.

### Install Locally

Install the packaged extension directly in VS Code:

```bash
code --install-extension mtv-dark-<version>.vsix
```
