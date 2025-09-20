# 🚀 setup-rokit

[![GitHub release](https://img.shields.io/github/v/release/notthebestdev/setup-rokit?logo=github&color=red)](https://github.com/notthebestdev/setup-rokit/releases)
[![GitHub Marketplace](https://img.shields.io/badge/marketplace-setup--rokit-blue?logo=github)](https://github.com/marketplace/actions/setup-rokit)

A GitHub Action to install [Rokit](https://github.com/rojo-rbx/rokit), the toolchain manager for Roblox projects — in your CI pipelines.  
It works across **Linux**, **macOS (Intel & Apple Silicon)**, and **Windows**.

---

## 📦 Features

- Install the latest Rokit release or pin to a specific version  
- Cross-platform support (Linux, macOS, Windows)  
- Easy to use with GitHub Actions  
- Adds `rokit` to the system `PATH`  

---

## ⚡ Usage

### Install latest Rokit
```yaml
name: CI with Rokit
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Setup Rokit
        uses: notthebestdev/setup-rokit@v1
      - name: Check version
        run: rokit --version
```

### Pin to a specific version
```yaml
- name: Setup Rokit v1.1.1
  uses: notthebestdev/setup-rokit@v1
  with:
    version: v1.1.1
```

## ⚙️ Inputs

| Name      | Description                                                                     | Default   | Example   |
|-----------|---------------------------------------------------------------------------------|-----------|-----------|
| `version` | Rokit version to install (tag name). Use `latest` for the newest release.       | `latest`  | `v1.1.1`  |

---

## 📝 License

This project is licensed under the [MIT License](LICENSE).

---

*Made with ❤️ for Roblox developers.*
