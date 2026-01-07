# OMLMSC-VSBTWSL  
**Open Multi-Library Microsoft SDK Clusters — Visual Studio BuildTools Windows System Library**  
*Empowering native Windows development with open, safe, and modular toolchains.*

[![License: PMOLP v1](https://img.shields.io/badge/License-PMOLP%20v1-blue)](LICENSE.md)
[![WSL2 Compatible](https://img.shields.io/badge/WSL2-Ready-green)](https://learn.microsoft.com/en-us/windows/wsl/)

---

## 🎯 Vision

**OMLMSC-VSBTWSL** — это *единая точка входа* для разработчиков, создающих высокопроизводительные, безопасные и совместимые приложения под Windows, используя:
- Современные C/C++/Rust/C# и (в будущем) RedStone.Script 🌟  
- Официальные Microsoft SDK (WinUI 3, DirectX 12, MSIX, WebView2, WMI, COM, Win32 modernized)  
- Build Tools Visual Studio (v142+, Clang/LLVM, MSVC, Ninja)  
- Безопасные абстракции поверх системных API (на основе принципов ABRS-Lib 🔐)

> 🔧 *Designed for hobbyists, researchers, and indie developers — no enterprise lock-in.*

---

## 📦 Core Features

| Module | Description |
|--------|-------------|
| `sdk/` | Обёртки для Windows SDK: WinRT, COM, Registry, Services, DeviceIoControl — с проверками границ, RAII и memory-safe patterns |
| `build/` | Автоматизация сборки: `.vcxproj`/`.sln` генераторы, кэширование MSVC/Clang, поддержка WSL2 ↔ Windows toolchain sync |
| `interop/` | Мосты: Rust ↔ C++ ↔ C# ↔ Python (через PyO3/napi-rs), WSL2 ↔ Win32 IPC |
| `security/` | Hardened memory allocators, syscall auditors, compile-time checks (inspired by ABRS-Lib) |
| `utils/` | CLI tools: `oml-init`, `oml-build`, `oml-deploy` (MSIX/pkg installer gen) |

---

## 🚀 Quick Start

### Требования
- Windows 10/11 (21H2+)
- Visual Studio 2022 (или Build Tools)  
- WSL2 с Ubuntu 22.04+ (опционально, но рекомендовано)
- Python 3.10+ (для генераторов)

### Установка
```bash
# Клонируйте репозиторий
git clone https://github.com/IvanProgramer01/OMLMSC-VSBTWSL-Open-Library-
cd omlmsc-vsbtwsl

# Инициализируйте окружение (настроит PATH, SDK-путь, кэш)
python -m utils.oml-init --wsl2
