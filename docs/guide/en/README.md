[中文](../zh/README.md) · **English**

# Qunxing user guide

Qunxing is a Windows desktop app. It sends the AI coding tools you already have installed and signed in to work on open math problems:
- you can see every step;
- you can pause, send a hint or add budget at any time;
- proofs can be checked with Lean.

This guide covers the first beta. Where the app and this guide disagree, trust the app, and please [open an issue](https://github.com/qunxingmath-org/qunxing-app/issues) to tell us.

## Contents

1. [Install](install.md): download, install, the Windows warning, checking the file
2. [First launch](first-run.md): the setup guide; connecting Codex CLI, Claude Code or Gemini CLI
3. [Your first problem](first-problem.md): draw, set up, step in while it runs, read the result, the star map
4. [Lean](lean.md): why to install it, how, and how Qunxing uses it
5. [Research plans](research-plans.md): run a batch of problems
6. [Privacy and uploads](privacy-and-uploads.md): what goes over the network, what is uploaded, how to turn it off
7. [FAQ](faq.md)
8. [Uninstall and where your data lives](uninstall.md)

## The short version

- **Qunxing itself is free.** AI usage goes through your own subscription or API key:
  - you set a budget before each problem, and the run stops to ask you when it is reached;
  - there is also a daily spending cap.
- **Nothing is uploaded by default.** Run records, proofs and costs stay on your computer.
- **A star is lit only when both checks pass**:
  - Lean compiles the proof on your computer;
  - a statement check confirms the Lean statement is the original problem.

## Links

- Download: <https://www.qunxingmath.org/en/download/>
- The problem bank on the website: <https://www.qunxingmath.org/en/problems/>
- Bug reports: <https://github.com/qunxingmath-org/qunxing-app/issues>
- Security issues: see [SECURITY.md](../../../SECURITY.md); please don't report them in public
