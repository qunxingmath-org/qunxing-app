[Contents](README.md) · **Uninstall and where your data lives** · [中文](../zh/uninstall.md)

# Uninstall and where your data lives

## Where your data lives

**Everything is in the data folder you chose**:
- the default is `C:\Users\<your user name>\Qunxing`;
- Settings → **Data folder** shows where it is, with **Copy path**;
- **Change…** moves it somewhere else; existing files move with it.

**Each run gets its own folder**, by problem ID and then by run time:

```text
C:\Users\<your user name>\Qunxing\runs\<problem ID>\<run time>\
```

**Inside**:
- `run.json`: the run record and usage;
- `proof.md`: the proof in plain language;
- `lean\`: the Lean statement, proof and local check results;
- `verdicts\`: conclusions such as the statement check;
- `novelty\`: novelty reports;
- `originals\`: copies of the session logs;
- `failure-path.md`: a failure-path summary, if one was written.

**To find a problem's files**:
- on the result page, under "Local files", click **Show in folder**;
- on the star map, click the star; the details on the right show its folder on this computer;
- folders are named by problem ID, so Windows search finds them too.

**The data folder also holds**: the problem-bank snapshot, your research plans, and a local index the star map uses to find each problem's files.

## Uninstall Qunxing

- **Installer version**: Windows Settings → **Apps** → **Installed apps**, find "Qunxing", click **…** → **Uninstall**.
  - On Windows 10: Settings → Apps → Apps & features → Qunxing → Uninstall.
- **Full app package**: delete the extracted folder.

**Uninstalling doesn't delete your data folder.** Your runs and proofs are still there. Delete the folder yourself if you no longer need it.

## Things outside Qunxing

You installed these yourself, so uninstalling Qunxing leaves them alone. To remove them, follow their own instructions:
- **AI tools**: Codex CLI, Claude Code, Gemini CLI.
- **Lean**: run `elan self uninstall` in a terminal. It removes elan and every Lean version it installed.
- **WebView2**: a Windows component that other apps use too. Usually leave it installed.

Back to [Contents](README.md)
