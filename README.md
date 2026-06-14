# 100hires-task-1

AI tools onboarding task for the 100Hires application.

This document records how I set up my development environment with Cursor and used its AI agent to clone this repository.

> **Note:** I used Cursor's AI agent (with Claude Code and Codex) throughout this process. I gave instructions in natural language, reviewed the agent's actions and outputs, and verified the results myself rather than running every command manually.

---

## 1. Installed Cursor IDE

I downloaded and installed [Cursor](https://cursor.com) on Windows.

**Steps:**
1. Downloaded the Windows installer from the Cursor website.
2. Ran the installer and completed the setup wizard.
3. Launched Cursor and signed in to enable AI features.

**Result:** Cursor IDE was installed and ready to use with built-in AI agent capabilities.

---

## 2. Installed the Claude Code Extension in Cursor

I added the Claude Code extension to extend Cursor with Claude-powered coding assistance.

**Steps:**
1. Opened Cursor.
2. Went to the Extensions view (`Ctrl+Shift+X`).
3. Searched for **Claude Code**.
4. Clicked **Install** on the official extension.
5. Reloaded Cursor when prompted.

**Result:** The Claude Code extension was installed and available in the editor.

---

## 3. Installed the Codex Extension in Cursor

I also installed the Codex extension for additional AI-assisted development support in Cursor.

**Steps:**
1. Opened the Extensions view (`Ctrl+Shift+X`).
2. Searched for **Codex**.
3. Clicked **Install** on the extension.
4. Reloaded Cursor when prompted.

**Result:** The Codex extension was installed alongside Claude Code.

---

## 4. Cloned This Repository Using Cursor's AI Agent

I used Cursor's AI agent to clone this GitHub repository instead of running the commands manually in a terminal.

**Steps:**
1. Opened a new Cursor chat and pasted the repository URL:
   `https://github.com/anantait10-star/100hires-task-1.git`
2. Asked the agent to clone the repository.
3. The agent cloned it to:
   `C:\Users\aryab\Projects\100hires-task-1`
4. Verified the clone by checking that `README.md` and the `.git` directory were present.

**Result:** The repository was cloned successfully and is ready for further work.

---

## Issues Encountered and How I Solved Them

### Issue 1: GitHub CLI (`gh`) was not installed

When the AI agent tried to inspect the repository with `gh repo view`, PowerShell returned:

```
The term 'gh' is not recognized as the name of a cmdlet, function, script file, or operable program.
```

**Solution:** The agent fell back to standard `git clone`, which worked without the GitHub CLI. No action was required on my part for the clone to succeed.

**Optional follow-up:** Install the [GitHub CLI](https://cli.github.com/) if I want richer GitHub integration from the terminal later.

---

### Issue 2: Workspace move tool was unavailable

The agent attempted to switch the workspace root to the cloned project folder using an internal MCP tool, but the call failed with:

```
Tool not found: CallMcpTool
```

**Solution:** This did not block the clone. The repository files were still created on disk at `C:\Users\aryab\Projects\100hires-task-1`. I can open that folder directly in Cursor via **File → Open Folder** if I want the project as my active workspace.

---

### Issue 3: Some shell commands returned no output

During automated inspection, a few terminal commands completed without printing visible output in the agent session.

**Solution:** The agent verified the clone by reading files directly (for example, `README.md` and `.git/refs/heads/main`) instead of relying only on terminal output. The repository contents were confirmed to be present and correct.

---

## Repository Contents

After cloning, the repository contains:

- `README.md` — this documentation file
- `.git/` — Git metadata linking the local copy to the remote on GitHub

---

## Summary

| Step | Status |
|------|--------|
| Cursor IDE installed | Done |
| Claude Code extension installed | Done |
| Codex extension installed | Done |
| Repository cloned via Cursor AI agent | Done |

All setup steps for this onboarding task are complete. This repository is ready for the next steps in the 100Hires application process.
