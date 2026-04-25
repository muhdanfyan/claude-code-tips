# Claude Code: Mastery & Advanced Workflows

This repository explains and demonstrates advanced techniques for using **Claude Code**, based on tips shared by its creator, Boris Cherny. These workflows are designed to improve efficiency, automate repetitive tasks, and enable seamless cross-device development.

## 🚀 Key Features & Slash Commands

### 1. Context-Aware Interruption (`/btw`)
The `/btw` (By The Way) command allows you to ask clarifying questions or side tasks without breaking Claude's current focus.
- **Why use it:** Keeps the main task clean while leveraging the full session context for quick answers.
- **Example:** `... [Claude is refactoring a large file] ... /btw "Wait, does this match the interface in types.ts?"`

### 2. Automation Loops (`/loop`)
Automate repetitive checks or monitoring tasks within the terminal.
- **How it works:** Runs a specific prompt at set intervals.
- **Usage:** `/loop "Every 30m, check my @gmail for urgent security alerts and summarize them."`

### 3. Persistent Tasks (`/schedule`)
Schedule tasks that outlive your current terminal session.
- **Desktop Tasks:** Run as long as the app is open.
- **Cloud Tasks:** Run on Anthropic’s servers (even if your PC is off).
- **Example:** `/schedule "Every Friday at 5pm, generate a summary of all git commits this week and save to reports/weekly.md"`

### 4. Cross-Device Mobility (`/teleport`)
Move your active development session between machines.
- **Workflow:** Start a session on your desktop, `/teleport` it to the cloud, and then pull it to your laptop or phone using `/remote-control`.

---

## 🛠️ Workspace & Configuration Tips

### Multi-Directory Access (`--add-dir`)
Reference multiple codebases or libraries simultaneously by adding directories at startup.
```bash
claude --add-dir ~/libs/utils --add-dir ~/projects/shared-types
```

### Persistent Settings (`settings.json`)
Automate your workspace setup by defining trusted folders in your configuration.
- **Location:** Typically in `~/.claude/settings.json` or project-specific config.
- *See `examples/settings.json` in this repo.*

---

## 👁️ Visual Verification (Chrome Extension)
Claude can now "see" the apps it builds.
1. Enable the **Claude in Chrome** beta extension.
2. Claude will automatically launch a browser to:
   - Verify UI changes.
   - Debug console errors.
   - Run end-to-end tests visually.

---

## 📱 Mobile & Remote Workflows
- **Code on Mobile:** Use the "Code" tab in the Claude iOS/Android app to edit your repo on the go.
- **Dispatch:** Use your phone as a remote control for your desktop Claude instance to handle emails, Slack, or file management.

---

## 🧪 Strategic Workflows
- **Parallel Sessions:** Don't wait for one task to finish. Run multiple `claude` instances in different terminal tabs for different sub-tasks.
- **Skill Creation:** Identify workflows you do more than 3 times (e.g., "Add license headers", "Fix lint errors") and ask Claude to create a persistent "Skill" for it.

---
*Reference: [XDA Developers - Claude Code Creator Tips](https://www.xda-developers.com/claude-codes-creator-keeps-sharing-tips-and-they-all-made-my-experience-better/)*
