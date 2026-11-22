# Signalbreakers — Installation Guide

**Created:** November 22, 2026  
**Purpose:** Step-by-step instructions for installing required development tools  

---

## Prerequisites Checklist

- [x] Python 3.12.10 installed and in PATH
- [x] Git 2.56.1 installed and in PATH
- [x] LM Studio running at `http://localhost:1234/v1` (verified)
- [ ] Godot 4.7.2 stable — **install now**
- [ ] Temurin JDK 17 or 21 LTS — **install now**

---

## Step 1: Install Godot 4.7.2 Stable

### Why Godot?
- MIT license (free forever, no royalties)
- Excellent 2D rendering pipeline
- Native Android export (~15–30MB builds)
- GDScript — Python-like syntax, AI-friendly
- Latest stable: **4.7.2** (released August 18, 2026)

### Download
1. Go to: https://godotengine.org/download/windows/
2. Click **"Godot 4.7.2"** → **"Windows — x86_64"**
3. This downloads a portable `.zip` file (no installer needed)

### Extract
1. Create folder: `C:\Tools\Godot\`
2. Extract the downloaded zip into that folder
3. You should have: `C:\Tools\Godot\godot.windows.editor.x86_64.exe`

### Verify Installation
Open Command Prompt and run:
```cmd
"C:\Tools\Godot\godot.windows.editor.x86_64.exe" --version
```
Expected output: `Godot Engine v4.7.2.stable.official`

### Optional: Add to PATH
For convenience, add to your system PATH so you can launch Godot from any terminal:
1. Open System Properties → Environment Variables
2. Edit the `Path` variable under "User variables"
3. Add: `C:\Tools\Godot\`

---

## Step 2: Install Temurin JDK 17 or 21 LTS

### Why Eclipse Temurin?
- Free, open-source OpenJDK builds
- No licensing fees
- Enterprise-grade quality (AQAvit verified)
- Trusted by millions of developers

### Download
1. Go to: https://adoptium.net/
2. Select **JDK 21 LTS** (recommended) or JDK 17 LTS
3. Platform: Windows, x64
4. Package: HotSpot (default)
5. Click **"Download"** — this downloads an `.msi` installer

### Install
1. Run the downloaded `.msi` file
2. Accept defaults (install to `C:\Program Files\Eclipse Adoptium\jdk-21.x.x-hotspot`)
3. **Important:** Check the box "Add to PATH" during installation, or set it manually:

#### Manual PATH setup (if not checked during install):
1. Open System Properties → Environment Variables
2. Under "User variables", click New:
   - Variable name: `JAVA_HOME`
   - Variable value: `C:\Program Files\Eclipse Adoptium\jdk-21.x.x-hotspot` (use your actual version number)
3. Edit the existing `Path` variable and add: `%JAVA_HOME%\bin`

### Verify Installation
Open a **new** Command Prompt (must restart after PATH changes):
```cmd
java -version
javac -version
echo %JAVA_HOME%
```
Expected output for JDK 21:
- `java version "21.x.x"`
- `javac 21.x.x`
- `%JAVA_HOME%` should show the JDK path

---

## Step 3: Install Android SDK (via Godot)

After installing Godot and JDK, you can install Android tools through Godot's built-in installer:

### Method A: Via Godot Editor (Recommended)
1. Open Godot editor (`godot.windows.editor.x86_64.exe`)
2. Go to **Tools → Manage Android Export**
3. Click **"Install Android Build Tools"**
4. Godot will download and configure the Android SDK, command-line tools, and Gradle automatically

### Method B: Manual Installation
1. Download Android Command-Line Tools from: https://developer.android.com/studio#command-tools
2. Extract to a folder (e.g., `C:\Tools\AndroidSDK\`)
3. Set environment variable `ANDROID_HOME` to that path
4. Run: `%ANDROID_HOME%\cmdline-tools\bin\sdkmanager "platform-tools" "build-tools;34.0.0"`

### Verify Android Setup
```cmd
adb version
```
Expected: Android Debug Bridge version info

---

## Step 4: Install Godot Android Export Templates

1. Open Godot editor
2. Go to **Tools → Manage Android Export**
3. Click **"Install Android Export Templates"**
4. This installs templates for both debug and release builds

### Verify
In the Android Export dialog, you should see no errors listed under "Export Errors."

---

## Troubleshooting

### Godot won't start / crashes on launch
- Ensure your RTX 3090 drivers are up to date (current: 32.0.16.2124)
- Try running as Administrator once
- If using the Insider Preview build, check for known issues at godotengine.org

### Java "not recognized" after installation
- Close and reopen Command Prompt (PATH changes don't apply to existing terminals)
- Verify `JAVA_HOME` is set correctly
- Check that `%JAVA_HOME%\bin` is in your PATH

### Godot Android export fails with JDK errors
- Ensure JDK 17+ is installed (not just JRE)
- Verify `JAVA_HOME` points to the JDK root, not a subfolder
- Run Godot as Administrator at least once to trigger SDK installation

### LM Studio endpoint unreachable
- Open LM Studio → Local Server tab
- Confirm port is set to 1234 (or whichever you configured)
- Click "Start Server" if not running
- Test: `curl http://localhost:1234/v1/models` in Command Prompt

---

## Post-Installation Checklist

After installing all tools, verify everything works together:

1. [ ] Godot editor launches successfully
2. [ ] Create a new empty Godot project to confirm no errors
3. [ ] `java -version` returns JDK 17 or 21 in Command Prompt
4. [ ] `curl http://localhost:1234/v1/models` returns model list
5. [ ] Android export templates installed in Godot (no red error messages)

---

## Estimated Installation Time

| Task | Time |
|------|------|
| Download + extract Godot 4.7.2 | ~5 minutes |
| Download + install Temurin JDK 21 | ~10 minutes |
| Install Android SDK via Godot | ~15–30 minutes (depends on network) |
| Verify all tools | ~5 minutes |
| **Total** | **~35–50 minutes** |

---

*This guide will be updated as new tool versions are released.*
