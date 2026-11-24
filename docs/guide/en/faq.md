[Contents](README.md) · **FAQ** · [中文](../zh/faq.md)

# FAQ

## Installing and starting

### "Windows protected your PC"

Make sure the file came from this repository's Releases or the Qunxing website, then click **More info** → **Run anyway**.
- To check the file, see [Install](install.md#check-the-file-optional).

### The top right says "Reconnecting…"

The event stream between the window and Qunxing's background service dropped.
- It reconnects by itself and catches up on missed events; usually there's nothing to do.
- If it never reconnects, close Qunxing and open it again.

### The top right says "Connection expired"

The background service no longer accepts this window. Close the window and reopen Qunxing.

### Downloads from GitHub are slow

Use the mirror on the [download page](https://www.qunxingmath.org/en/download/). The files are identical.

## Connecting agents

### The setup guide can't find my agent

1. **Check that it works in a terminal**: run `codex`, `claude` or `gemini`, have a short chat, and make sure you're signed in.
2. **Click Search again** in the setup guide.
3. **Still not found?**
   - If you installed it somewhere unusual, make sure it's on the system PATH: typing the command in a new terminal must start it.
   - Restart Qunxing and try again.
   - If that doesn't help, [open an issue](https://github.com/qunxingmath-org/qunxing-app/issues) with your Windows version and the agent's name and version.

### The card says "ACP adapter missing"

Codex CLI and Claude Code need a small bridge program (an ACP adapter) to work with Qunxing. Gemini CLI doesn't.
- Click **Install adapter** on the card, read what it will do, then click **Install**.
- The adapter comes from npm and goes into Qunxing's own folder. Your global settings stay unchanged.

**If it fails to install**:
- most likely npm can't be reached; try another network;
- paste the error message into an issue, with any personal information removed.

### Test connection fails

- **Make sure you're signed in**: open the agent in a terminal and see whether it answers.
- **On a subscription**: check whether your quota has run out.
- **On an API key**: check the key and your balance.
  - Keys are set in the agent itself; Qunxing never handles them.

### What is the console, and do I need it?

The console is your own agent, running inside the Qunxing window. It can find problems, start runs and keep an eye on them.
- You don't need it: you can draw, set up and run everything yourself.
- Any public submission the console makes needs your own confirmation.
- Its cost goes into the separate "Control" ledger.

## Cost

### How much will it cost?

Qunxing itself is free. AI usage is charged to your own subscription or API key.

**On a subscription**:
- there's no extra charge; it uses your plan's quota;
- the amounts shown are converted at API prices, for reference.

**On an API key**: you pay per use, and every charge goes into the ledgers.

**Three safeguards**:
- before each problem you set separate solving and verification budgets; the run stops to ask you when one is reached;
- a daily spending cap: at the cap, no new runs start;
- novelty checks have their own ledger and never use the solving budget.

### My subscription quota ran out

Qunxing waits until the quota resets and then continues by itself. The waiting time isn't counted.
- If you don't want to wait, switch that role to an API key in "Who solves".
- To get back to that step, run the setup guide again from Settings.

### The budget was reached

See [Your first problem](first-problem.md#budget-reached). Three choices:
- add budget;
- take the current progress to the Lean check;
- wrap up.

## While it runs

### The AI is waiting for my approval, but I didn't see a window

- Look at the taskbar: Qunxing's icon flashes, and there's a system notification.
- The top right of the run page shows "Needs your answer".
- To have the window jump to the front: Settings → **Bring Qunxing to the front when it needs my approval**.
- If it asks too often: Settings → **Run mode**, choose "Ask at key steps" or "Fully automatic".

### Does the result still count after I add budget or send a hint?

Yes. The run is just labeled as having an intervention or as human-assisted, and statistics compare it separately.

### Can I continue after stopping?

Yes. If you clicked **Stop here**, the result page has a **Continue** button that picks up from the step where you stopped.

## Results

### What does "lit" mean, and can I trust it?

A star is lit when both pass:
- Lean compiles the proof on your computer using only standard axioms;
- the statement check confirms the Lean statement is the original problem.

Lighting rests on the checks done on your computer. Qunxing does no manual verification and takes no responsibility for the result.

After a proof is submitted, Qunxing reruns Lean in public CI. When it passes, the star gets the "Lean rerun" mark.

### The Lean check is slow

The first check downloads the Mathlib cache, which takes a while. Later checks are much faster. See [Lean](lean.md).

### The problem-bank update failed

- If the new bank fails its check, Qunxing keeps the old one, and everything still works.
- Try again later; GitHub can be unreachable on a poor connection.

## Data and privacy

### Where is my data?

By default in `C:\Users\<your user name>\Qunxing`, one folder per run. See [Uninstall and where your data lives](uninstall.md).

### Can I use it offline?

Turn on **Run locally only** in Settings: no updates, no uploads, and the problem bank stays as it is.
- The AI calls still need the internet, because the AI tools themselves do.
- See [Privacy and uploads](privacy-and-uploads.md).

### Does Qunxing upload my conversations?

No. Nothing is uploaded by default. Once uploads open, they happen only when you click, and transcripts and prompts are never part of them.

## Feedback

### How do I report a problem?

[Open an issue](https://github.com/qunxingmath-org/qunxing-app/issues) with:
- your Qunxing version and Windows version;
- what you did, what you saw, and what you expected;
- a screenshot.

**Before taking a screenshot**, cover API keys, tokens, your user name and any paths you don't want public.

**Security issues** must not be reported in public; see [SECURITY.md](../../../SECURITY.md).
