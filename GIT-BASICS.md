# 🌳 Git Basics — how to not lose your work

> **What this is:** the smallest amount of Git you need to keep your work safe — not a full tutorial, just the part you'll use every meeting.
>
> **You don't have to memorize anything.** Your AI can run Git for you. You just need to **recognize these words** when it uses them, and know what to do when something looks scary.

---

## 🤔 What Git is, in one paragraph

Git is a **save button with a memory**. A normal save replaces the old version — yesterday's work is gone. Git keeps **every** version, each with a note about what changed. **GitHub** stores that history online, so your work survives a dead laptop and your teammates can see it too.

Four words you'll hear constantly:

| Word | What it actually means |
|---|---|
| **Repository** ("repo") | The project folder that Git is watching. |
| **Commit** | One save point, plus a short note about what you did. |
| **Push** | Send your save points *up* to GitHub. |
| **Pull** | Bring your teammates' save points *down* to your laptop. |

> 💡 A commit is a checkpoint in a video game. Push uploads your save file to the cloud.

---

## 🚀 Getting your copy (you do this once)

1. On GitHub, open the team's template repo → **"Use this template" → "Create a new repository."**
2. Open **VS Code** → `Ctrl+Shift+P` → type **"Git: Clone"** → paste your repo's link → pick a folder on your laptop.
3. That's it — the project is on your computer and Git is watching it.

*(Typed out, step 2 is `git clone https://github.com/...` — same thing.)*

> ⚠️ **Work in *your* repo, never in the template.** The template is everyone's starting point; your changes belong in your copy.

---

## 💾 The loop you'll actually use

This is 95% of Git. Do it every time you get something working:

1. **Commit** — make a save point with a note.
2. **Push** — send it to GitHub.

**In VS Code:** click the **Source Control** icon in the left sidebar (a little branching path). You'll see your changed files. Type a short message, click **Commit**, then **Sync Changes** (that's push).

**When should you commit?** *Whenever something works* — right then, not at the end of the day. Small and often beats big and rare: break something an hour later, and you can get back to the version that worked.

**Write messages a human can read:**

| ❌ Not useful | ✅ Useful |
|---|---|
| `stuff` | `Add the match entry screen` |
| `fix` | `Fix average score ignoring blank entries` |
| `asdfgh` | `Update DESIGN.md — dropped logins from scope` |

> 💡 **Working with a teammate? Pull first, before you start.** It brings down their latest work so you're not both editing an old version.

**The same thing typed out.** The buttons are all you need — but tutorials, mentors and your AI use these commands, so it helps to recognize them:

| What you clicked | What it's called in the terminal |
|---|---|
| Commit | `git add .` then `git commit -m "Add the match entry screen"` |
| Sync Changes | `git push` |
| (getting teammates' work) | `git pull` |
| *(no button — very handy)* | `git status` — *"what have I changed so far?"* |

> 💡 VS Code has all of this built in. **You don't need any other Git program** — one less thing to install.

---

## 😰 When something goes wrong

Git error messages are famously confusing. They're almost never as bad as they look.

**The rules:**
- 🛑 **Don't delete the folder and start over.** That's the one move that actually loses work.
- 😌 **Anything you committed is safe** and can be recovered, however chaotic the screen looks.
- 🙋 **Ask a mentor, or paste the exact error to your AI:** *"What does this mean and what should I do? Explain it simply."*
- ⚠️ **Never run a command you don't understand** because you found it online — especially `--force` or `reset --hard`. Those really do delete work.

---

## 🔐 If you accidentally commit a secret — read this now, not later

Say you commit an API key, a password, or a teammate's personal info.

**Deleting it in your next commit does NOT remove it.** Git keeps every version — the secret is still sitting in the history. If it's been pushed to GitHub, treat it as **public and permanently leaked**.

**What to do:**
1. **Tell a mentor immediately.** Today, not next meeting. Nobody is in trouble — this happens to professionals.
2. **Don't try to clean up the history yourself.** It's easy to make it worse.
3. The key will need to be **turned off and replaced**. That's the mentor's job.

> Better: keep real secrets in a file listed in `.gitignore`, and never paste them into `DESIGN.md`, your code, or an AI chat. See `README.md`.

---

## 🤖 Letting the AI do the Git part

You don't have to click any of this yourself. In an AI coding tool, just ask:

- *"Save my work with a clear commit message and push it to GitHub."*
- *"What changed since my last commit?"*
- *"I got this error: [paste it]. What does it mean, and what should I do?"*
- *"Explain what you just did with Git, like I've never used it before."*

**But check what it did.** If the AI says it pushed, make sure your changes really show up on GitHub. Understanding your own project is the point — a judge may ask how your team keeps its code.

---

*Part of our FRC / FTC / FLL software project template. If something here confused you, tell a mentor so we can fix the wording for the next student.*
