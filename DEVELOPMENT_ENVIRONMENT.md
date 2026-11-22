# SIGNALBREAKERS — Development Environment Audit

**Computer:** Greyspire  
**Audit Date:** November 22, 2026  
**Auditor:** qwen3.6-35b-a3b via LM Studio  

---

## Hardware Summary

| Component | Specification | Notes |
|-----------|--------------|-------|
| **OS** | Windows 11 Pro Insider Preview 25H2 (Build 26220) | x64-based PC — Insider Preview may have stability quirks |
| **CPU** | Intel Core i9-10850K, 10 cores / 20 threads @ ~3.60 GHz | Excellent for compilation and AI inference |
| **RAM** | 128 GB (130,897 MB reported) | Massive headroom; no memory constraints expected |
| **GPU 1 (Primary)** | NVIDIA GeForce RTX 3090, 24 GB VRAM | Drives 5120×1440 ultrawide OLED @ 240 Hz G-SYNC |
| **GPU 2** | NVIDIA GeForce RTX 3090, 24 GB VRAM | Second card — status unclear (NVML failed) |
| **GPU 3 (Integrated)** | Intel UHD Graphics 630, 1 GB VRAM | For secondary display / fallback |
| **Display 1** | 5120×1440 ultrawide OLED @ 240 Hz | Primary development screen |
| **Display 2** | 1920×1080 portrait (SMI USB Display) | Secondary monitor |
| **Storage C:** | ~639 GB used / ~1,223 GB free (~1.8 TB SSD total) | Ample space for builds and assets |
| **DirectX** | DirectX 12 | Supported by Godot 4.x |

---

## GPU Configuration Notes

- **NVML initialization failed** — common on Windows Insider Preview with dual GPUs or when the NVIDIA driver hasn't fully enumerated both cards.
- **Primary RTX 3090 confirmed** via `Get-CimInstance Win32_VideoController`: Driver version `32.0.16.2124` (Game Ready Driver).
- **LM Studio GPU usage:** Needs verification — LM Studio may use only one GPU or split across both. Check LM Studio settings → GPU layers.
- **Recommendation:** For game development, Godot will use the primary RTX 3090 via DirectX 12. Dual-GPU splitting is not required for a 2D/2.5D puzzle game.

---

## Installed Development Tools — Verified November 22, 2026

| Tool | Version | Status | Path / Notes |
|------|---------|--------|--------------|
| **Python** | 3.12.10 | ✅ VERIFIED | `C:\Users\linco\AppData\Local\Programs\Python\Python312` |
| **Git** | 2.56.1.windows.1 | ✅ VERIFIED | `C:\Program Files\Git\cmd\git.exe` |
| **Godot** | Not installed | ⚠️ NEEDS INSTALL | See INSTALLATION_GUIDE.md — Godot 4.7.2 stable recommended |
| **Java / JDK** | Not found in PATH | ⚠️ NEEDS INSTALL | See INSTALLATION_GUIDE.md — Temurin JDK 17 or 21 LTS |
| **Android SDK** | Not verified | ⚠️ PENDING | Will install via Godot's built-in Android module installer after JDK |
| **Gradle** | Not verified | ⚠️ PENDING | Bundled with Android SDK |
| **ADB** | Not verified | ⚠️ PENDING | Bundled with Android SDK |
| **LM Studio Endpoint** | ✅ VERIFIED WORKING | `http://localhost:1234/v1` — Ollama-compatible, multiple models loaded including Qwen 3.6-35B, Qwen 3.8-27B, DeepSeek R1, nomic-embed-text-v1.5 embedding model |

---

## Tool Installation Priority

### MUST INSTALL BEFORE PHASE 4 (Technical Prototype):

1. **Godot 4.7 Stable** — Download from https://godotengine.org/download/archive/
   - Use the `.zip` portable version (no installer needed)
   - Extract to `C:\Tools\Godot\godot.windows.editor.x86_64.exe`
   - Add to PATH or create a shortcut

2. **Java JDK 17 or 21** — Required for Android builds via Godot
   - Download from https://adoptium.net/ (Eclipse Temurin)
   - Set `JAVA_HOME` environment variable

3. **Android SDK Command-Line Tools** — For building Android App Bundles (.aab)
   - Can be installed via Godot's built-in Android module installer
   - Or download from https://developer.android.com/studio#command-tools

### SHOULD INSTALL FOR CONVENIENCE:

4. **LM Studio** — If not already installed, for local AI assistance
   - Endpoint typically at `http://localhost:1234/v1` (Ollama-compatible) or `http://localhost:1244/v1` (LM Studio native)
   - Load model: `qwen3.6-35b-a3b-uncensored-hauhaucs-aggressive`

---

## Compatibility Risks — Windows Insider Preview 25H2

| Risk | Severity | Mitigation |
|------|----------|------------|
| Godot editor may crash on unstable builds | Low-Medium | Use stable Godot 4.7; avoid nightly builds |
| Android SDK tools may have path issues | Medium | Test Android export early in Phase 4 |
| NVML/GPU enumeration unreliable | Low | Primary GPU confirmed working via WMI |
| Insider Preview driver updates may break temporarily | Low | Driver version 32.0.16.2124 is current and stable |

---

## LM Studio Integration Plan — VERIFIED ✅

**Endpoint:** `http://localhost:1234/v1` (Ollama-compatible)  
**Status:** ACTIVE and responding as of November 22, 2026  
**Loaded models confirmed via API:**
- `qwen3.6-35b-a3b-uncensored-hauhaucs-aggressive`
- `text-embedding-nomic-embed-text-v1.5` (embedding model)
- `qwen/qwen3.6-35b-a3b`
- `qwen/qwen3-coder-30b`
- `deepseek/deepseek-r1-0528-qwen3-8b`
- `qwen3.5-9b-the-defiant-fable-uncensored-heretic-neo-imatrix-max-mtp`
- `qwen/qwen3.8-27b`

**Usage in development:**
- Code generation and review (Godot GDScript scenes, scripts)
- Dialogue drafting and story iteration
- Puzzle generation and test case creation
- Documentation writing and refactoring
- Development checklists and milestone planning

---

## Project Directory

**Actual path:** `C:\linco\forecast_commonwealth\Signalbreakers`  
**Preferred path (D: drive unavailable):** `D:\Projects\Signalbreakers` — will use C: for now.

---

## Next Steps

1. **Install Godot 4.7.2 stable** — See INSTALLATION_GUIDE.md (Priority: HIGH)
2. **Install Temurin JDK 17 or 21 LTS** — See INSTALLATION_GUIDE.md (Priority: HIGH)
3. Verify LM Studio endpoint and model loading ✅ DONE
4. Git repository already initialized (`53251fc`)
5. Begin PHASE 1 Research with web searches for competitor data and platform requirements

---

*This file will be updated as new tools are installed and verified.*
