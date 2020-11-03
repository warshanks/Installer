<h1 align="center">BetterDiscord Installer</h1>

<p align="center">
  <a href="#overview">Overview</a> |
  <a href="#development">Development</a> |
  <a href="#contributors">Contributors</a>
</p>

<p align="center">
  <img alt="Preview" width="524" alt="Hero image" src="https://i.imgur.com/OV4yQJG.png"/>
  <br/>
  A simple standalone program which automates the installation, removal and maintenance of <a href="https://github.com/BetterDiscord/BetterDiscord">BetterDiscord</a>.
  <br/>
  <br/>
  <a href="https://github.com/BetterDiscord/Installer/blob/main/package.json" target="_blank">
    <img src="https://img.shields.io/librariesio/github/BetterDiscord/installer?labelColor=0c0d10&color=3a71c1&style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyOCIgaGVpZ2h0PSIyOCIgdmlld0JveD0iMCAwIDI4IDI4IiBmaWxsPSJub25lIj4NCjxwYXRoIGQ9Ik0yMC44NDEgMi42NTUxQzE5Ljk2MjMgMS43NzY0MiAxOC41Mzc3IDEuNzc2NDMgMTcuNjU5IDIuNjU1MUwxMy41IDYuODE0MTFWNi4yNTM5M0MxMy41IDUuMDExMjkgMTIuNDkyNiA0LjAwMzkzIDExLjI1IDQuMDAzOTNINC4yNUMzLjAwNzM2IDQuMDAzOTMgMiA1LjAxMTI5IDIgNi4yNTM5M1YyNC4yNTRDMiAyNS4yMjA1IDIuNzgzNSAyNi4wMDQgMy43NSAyNi4wMDRIMjEuNzVDMjIuOTkyNiAyNi4wMDQgMjQgMjQuOTk2NiAyNCAyMy43NTRWMTYuNzQ5OUMyNCAxNS41MDczIDIyLjk5MjYgMTQuNDk5OSAyMS43NSAxNC40OTk5SDIxLjE5NDFMMjUuMzQ5IDEwLjM0NTFDMjYuMjI3NyA5LjQ2NjM5IDI2LjIyNzcgOC4wNDE3NyAyNS4zNDkgNy4xNjMwOUwyMC44NDEgMi42NTUxWk0xMy41IDEwLjY5NEwxNy4zMDU5IDE0LjQ5OTlIMTMuNVYxMC42OTRaTTEyIDE0LjQ5OTlIMy41VjYuMjUzOTNDMy41IDUuODM5NzIgMy44MzU3OSA1LjUwMzkzIDQuMjUgNS41MDM5M0gxMS4yNUMxMS42NjQyIDUuNTAzOTMgMTIgNS44Mzk3MiAxMiA2LjI1MzkzVjE0LjQ5OTlaTTMuNSAxNS45OTk5SDEyVjI0LjUwMzlINC4yNUMzLjgzNTc5IDI0LjUwMzkgMy41IDI0LjE2ODEgMy41IDIzLjc1MzlMMy41IDE1Ljk5OTlaTTEzLjUgMjQuNTA0VjE1Ljk5OTlIMjEuNzVDMjIuMTY0MiAxNS45OTk5IDIyLjUgMTYuMzM1NyAyMi41IDE2Ljc0OTlWMjMuNzU0QzIyLjUgMjQuMTY4MiAyMi4xNjQyIDI0LjUwNCAyMS43NSAyNC41MDRIMTMuNVoiIGZpbGw9IiMzYTcxYzEiLz4NCjwvc3ZnPg==" alt="Dependency tracking"/>
  </a>
   <a href="https://github.com/BetterDiscord/installer/releases/" target="_blank">
    <img src="https://img.shields.io/github/downloads/BetterDiscord/installer/total?labelColor=0c0d10&color=3a71c1&style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDgiIGhlaWdodD0iNDgiIHZpZXdCb3g9IjAgMCA0OCA0OCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTEyLjI1IDM4LjVIMzUuNzVDMzYuNzE2NSAzOC41IDM3LjUgMzkuMjgzNSAzNy41IDQwLjI1QzM3LjUgNDEuMTY4MiAzNi43OTI5IDQxLjkyMTIgMzUuODkzNSA0MS45OTQyTDM1Ljc1IDQySDEyLjI1QzExLjI4MzUgNDIgMTAuNSA0MS4yMTY1IDEwLjUgNDAuMjVDMTAuNSAzOS4zMzE4IDExLjIwNzEgMzguNTc4OCAxMi4xMDY1IDM4LjUwNThMMTIuMjUgMzguNUgzNS43NUgxMi4yNVpNMjMuNjA2NSA2LjI1NThMMjMuNzUgNi4yNUMyNC42NjgyIDYuMjUgMjUuNDIxMiA2Ljk1NzExIDI1LjQ5NDIgNy44NTY0N0wyNS41IDhWMjkuMzMzTDMwLjI5MzEgMjQuNTQwN0MzMC45NzY1IDIzLjg1NzMgMzIuMDg0NiAyMy44NTczIDMyLjc2OCAyNC41NDA3QzMzLjQ1MTQgMjUuMjI0MiAzMy40NTE0IDI2LjMzMjIgMzIuNzY4IDI3LjAxNTZMMjQuOTg5OCAzNC43OTM4QzI0LjMwNjQgMzUuNDc3MiAyMy4xOTg0IDM1LjQ3NzIgMjIuNTE1IDM0Ljc5MzhMMTQuNzM2OCAyNy4wMTU2QzE0LjA1MzQgMjYuMzMyMiAxNC4wNTM0IDI1LjIyNDIgMTQuNzM2OCAyNC41NDA3QzE1LjQyMDIgMjMuODU3MyAxNi41MjgyIDIzLjg1NzMgMTcuMjExNyAyNC41NDA3TDIyIDI5LjMyOVY4QzIyIDcuMDgxODMgMjIuNzA3MSA2LjMyODgxIDIzLjYwNjUgNi4yNTU4TDIzLjc1IDYuMjVMMjMuNjA2NSA2LjI1NThaIiBmaWxsPSIjM2E3MWMxIi8+Cjwvc3ZnPgo=" alt="Downloads"/>
  </a>
  <a href="https://github.com/BetterDiscord/Installer/blob/main/LICENSE" target="_blank">
    <img src="https://img.shields.io/github/license/BetterDiscord/installer?labelColor=0c0d10&color=3a71c1&style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTEwLjk2ODQgMi4zMjQ2NUMxMS41ODMgMS44NzYxNiAxMi40MTcgMS44NzYxNiAxMy4wMzE2IDIuMzI0NjVMMjAuNDUzNCA3Ljc0MDZDMjEuNDI5OSA4LjQ1MzE1IDIwLjkyNjggOS45OTgzNSAxOS43MTg5IDEwLjAwMDNINC4yODEwOEMzLjA3MzE4IDkuOTk4MzUgMi41NzAxMSA4LjQ1MzE1IDMuNTQ2NTcgNy43NDA2TDEwLjk2ODQgMi4zMjQ2NVpNMTMgNi4yNTAzNEMxMyA1LjY5ODA1IDEyLjU1MjMgNS4yNTAzNCAxMiA1LjI1MDM0QzExLjQ0NzcgNS4yNTAzNCAxMSA1LjY5ODA1IDExIDYuMjUwMzRDMTEgNi44MDI2MiAxMS40NDc3IDcuMjUwMzQgMTIgNy4yNTAzNEMxMi41NTIzIDcuMjUwMzQgMTMgNi44MDI2MiAxMyA2LjI1MDM0WiIgZmlsbD0iIzNhNzFjMSIvPgo8cGF0aCBkPSJNMTEuMjUgMTYuMDAwM0g5LjI1VjExLjAwMDNIMTEuMjVWMTYuMDAwM1oiIGZpbGw9IiMzYTcxYzEiLz4KPHBhdGggZD0iTTE0Ljc1IDE2LjAwMDNIMTIuNzVWMTEuMDAwM0gxNC43NVYxNi4wMDAzWiIgZmlsbD0iIzNhNzFjMSIvPgo8cGF0aCBkPSJNMTguNSAxNi4wMDAzSDE2LjI1VjExLjAwMDNIMTguNVYxNi4wMDAzWiIgZmlsbD0iIzNhNzFjMSIvPgo8cGF0aCBkPSJNMTguNzUgMTcuMDAwM0g1LjI1QzQuMDA3MzYgMTcuMDAwMyAzIDE4LjAwNzcgMyAxOS4yNTAzVjE5Ljc1MDNDMyAyMC4xNjQ1IDMuMzM1NzkgMjAuNTAwMyAzLjc1IDIwLjUwMDNIMjAuMjVDMjAuNjY0MiAyMC41MDAzIDIxIDIwLjE2NDUgMjEgMTkuNzUwM1YxOS4yNTAzQzIxIDE4LjAwNzcgMTkuOTkyNiAxNy4wMDAzIDE4Ljc1IDE3LjAwMDNaIiBmaWxsPSIjM2E3MWMxIi8+CjxwYXRoIGQ9Ik03Ljc1IDE2LjAwMDNINS41VjExLjAwMDNINy43NVYxNi4wMDAzWiIgZmlsbD0iIzNhNzFjMSIvPgo8L3N2Zz4K" alt="License"/>
  </a>
</p>

---

# Overview

This repository contains the source code for the BetterDiscord installer. This installer is written with [electron-webpack](https://webpack.electron.build/) and [Svelte 3](https://svelte.dev/).

## Downloads

These will link you to the latest builds found in the [releases](https://github.com/BetterDiscord/installer/releases/) tab of this repository.

| [Windows (7+)](https://github.com/BetterDiscord/Installer/releases/download/latest/BetterDiscord-Windows.exe)  | [macOS (10.10+)](https://github.com/BetterDiscord/Installer/releases/download/latest/BetterDiscord-Mac.zip) | [Linux](https://github.com/BetterDiscord/Installer/releases/download/latest/BetterDiscord-Linux.AppImage) |
| ------------- | ------------- | ------------- |



## Codebase

```
.
├──assets                  // Contains static assets (such as images) used by the installer.
└──src                     // The installer's source code.
    ├──main                // Electron "main" process. Creates and configures the BrowserWindow.
    └──renderer            // Electron "renderer" process. Contains most components and scripts.
        ├──actions         // Scripts performed by the installer such as installing, repairing and uninstalling.
        ├──common          // Common UI components such as buttons, checkboxes, radios, etc...
        ├──pages           // Component files for each page in the installer's setup process.
        ├──stores          // Svelte store used for storing global data.
        └──transitions     // Contains custom Svelte transitions and animations.
```

---

# Development

> This is a tutorial designed for people looking to contribute to, or work directly with the installer's source code. If you are just looking to download and install BetterDiscord, visit the [releases](https://github.com/BetterDiscord/installer) page of this repository.

## Prerequisites
- [Git](https://git-scm.com)
- [Node.js](https://nodejs.org/en/) with `npm`.
- Command line of your choice.

## Building

### 1: Clone the repository.
```ps
git clone https://github.com/BetterDiscord/installer | cd installer
```
This will create a local copy of this repostory and navigate you to the root folder of the repository.

### 2: Install Dependencies
Run this command at the root folder to install dependencies:
```ps
npm i
```

### 3: Run Build Script
To run the installer in development mode, simply run the following command:
```ps
npm run dev 
```

## Additional Scripts

### Linting
This project uses [ESLint](https://eslint.org/). Run this command to lint your changes:
```ps
npm run lint
```

### Compiling & Distribution

```ps
npm run dist
```

---

# Contributors

<a href="https://github.com/betterdiscord/installer/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=betterdiscord/installer" />
</a>
