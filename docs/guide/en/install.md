[Contents](README.md) · **Install** · [中文](../zh/install.md)

# Install

## What you need

- **System**: Windows 10 or 11, 64-bit. A macOS version is in progress.
- **An AI coding tool**, installed and signed in. At least one of:
  - Codex CLI;
  - Claude Code;
  - Gemini CLI.
  - A subscription or an API key both work.
- **Lean 4**: optional. You need it only for results to pass the Lean check. See [Lean](lean.md).
- **Internet access**: for problem-bank updates, novelty checks and the AI calls themselves.

## Download

Either one works; the contents are the same.

| File | For |
|---|---|
| [Installer `Qunxing-Setup.exe`](https://github.com/qunxingmath-org/qunxing-app/releases/latest/download/Qunxing-Setup.exe) | Most people |
| [Full app package `Qunxing-Windows-x64.zip`](https://github.com/qunxingmath-org/qunxing-app/releases/latest/download/Qunxing-Windows-x64.zip) | No installation: work computers, USB drives |

- If GitHub is slow for you, use the mirror on the [download page](https://www.qunxingmath.org/en/download/). The files are identical.
- All versions and release notes: <https://github.com/qunxingmath-org/qunxing-app/releases>

## Using the installer

1. Double-click `Qunxing-Setup.exe`.
2. Follow the steps.
   - It installs for the current user and **does not need administrator rights**.
   - It adds Start menu and desktop shortcuts.
3. If WebView2 is missing, the installer tells you first, then downloads it from Microsoft.
   - WebView2 is the Microsoft component that draws Qunxing's window.
   - Windows 11 includes it, and most Windows 10 computers already have it.
4. Open "Qunxing" from the Start menu.

## Using the full app package

1. Right-click the zip → **Extract All**, and extract it to any folder, such as `D:\Qunxing`.
   - Don't run it from inside the zip.
2. Double-click `Qunxing.exe` in the extracted folder.

## "Windows protected your PC"

You may see this for builds without a code signature, and for new releases.

1. Make sure the file came from this repository's Releases or the Qunxing website.
2. Click **More info**, then **Run anyway**.

We are applying for free open-source code signing. Signing will make this warning much rarer. A new release can still trigger it for a while, because Microsoft builds trust from download history.

## Check the file (optional)

To make sure the download wasn't changed:

1. Open a terminal in your Downloads folder: right-click an empty area and choose "Open in Terminal". On Windows 10, hold Shift while right-clicking and choose "Open PowerShell window here".
2. Run:

```powershell
Get-FileHash .\Qunxing-Setup.exe -Algorithm SHA256
```

3. Compare the result with the matching line in the release's `SHA256SUMS.txt`. They must be identical.
   - The website's download page lists the SHA-256 of each file too.

## Updates

- **Qunxing tells you when there's a new version.** "Download" in that notice opens the website's download page.
- **Choose how it tells you** in Settings → **Updates and network** → **When an update arrives**:
  - **Automatically**;
  - **Ask me** (the default);
  - **Don't receive**.
- **Installing the new version**:
  - Installer: download the new installer and run it over the old version.
  - Full app package: extract it to a new folder and use the new `Qunxing.exe`.
- **Your runs are safe**: they live in your data folder, not the app folder. See [Uninstall and where your data lives](uninstall.md).

Next: [First launch](first-run.md)
