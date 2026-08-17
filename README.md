# 🤖 [Project Name] — Team [####]

> **[One line: what this project is.]** *(e.g. "A scouting web app for recording and ranking other teams' robots at competition.")*
>
> Built by students for **FRC / FTC / FLL** — planned and coded with AI help, using our team's project template.

---

## 🏁 New here? Start in 4 steps

> 🌳 **Never used GitHub before?** Read [`GIT-BASICS.md`](./GIT-BASICS.md) first — one page, and it's how you get this project onto your laptop without losing work later.

1. **🔍 Work out what's actually needed.** Not at your desk — go watch someone do the job your app would replace, and ask them about it. [`THINKING.md`](./THINKING.md) shows you how. *Skipping this is how a team builds a beautiful app nobody uses.*
2. **📄 Open [`DESIGN.md`](./DESIGN.md) and fill it in.** This is the plan for your app — what you're building, who it's for, the rules, the data. *Don't write any code yet.* A clear plan is the difference between an app that works and one that doesn't.
3. **🗣️ Defend the plan, then hand it to an AI and build step by step.** Say it out loud to a teammate first — the checklist is near the bottom of `DESIGN.md`, right before the ready-made prompt. The prompt then tells the AI to question you, build the smallest working version first, refuse to guess at anything you left vague, and teach you as it goes.
4. **🔄 Keep `DESIGN.md` in sync — and commit whenever something works.** When the app changes, the document changes too, plus a line in its Change Log. **`DESIGN.md` is the single source of truth:** if it's not written there, it's not part of the app.

---

## 📂 What's in this repo

| File / folder | What it's for |
|---|---|
| `DESIGN.md` | **Start here.** Your living plan + the AI build prompt. Always kept up to date. |
| `README.md` | This file — the front page of your project. Update the title and one-liner above. |
| `TEAM.md` | Our team's context for the AI — our tools, our limits, who to ask. You usually don't need to change this. |
| `THINKING.md` | **How to work out what to build** — watching, asking, and stress-testing your ideas before any code exists. |
| `GIT-BASICS.md` | **New to GitHub?** How to save your work so you never lose it. One page. |
| `DEPLOY.md` | **Running it & getting it online.** How to demo on your laptop, how to keep your app portable, and how hosting gets approved. |
| `.gitignore` | Lists files Git should ignore — **including anything with secrets.** |
| `LICENSE` | The rules for reusing this (MIT — basically "use it, keep the credit line"). |

> 💡 **There's no code folder yet — that's normal.** You don't have one until you start building. When you get there, you and the AI will make one together (usually called `/src`).

---

## 🔄 The workflow: find out → plan → build → keep in sync

```
Find out       ─►  Fill in     ─►  Defend    ─►  Hand it   ─►  Build ONE
what's needed      DESIGN.md       the plan      to the AI     small step
      ▲                                                            │
      │                                                            ▼
      │                                                       Works? And can
      │                                                       I explain it?
      │                                                            │
      └── Update DESIGN.md ◄──── Commit & push ◄───────────────────┘
          + Change Log            (right now!)
```

**Three of these get skipped, and each one costs you something different:**

- **Find out what's needed** — skip it and you build the wrong app, beautifully.
- **Defend the plan** — skip it and you find the hole after you've built on top of it.
- **Can I explain it?** — skip it and the code works but isn't really yours. A judge will find out before you do.

**Commit whenever something works** — right then, not at the end of the day. See [`GIT-BASICS.md`](./GIT-BASICS.md).

Most trips round this loop are short: build, test, commit, update the doc, build the next thing. Occasionally one sends you all the way back out to the people who use it, because you learned the plan was wrong. **That's the loop working, not you failing.**

---

## 🔐 Handling secrets — read this before you push anything

Some apps need **secret keys** — an API key for The Blue Alliance or Statbotics, say. They're like passwords. **Never commit them to GitHub:** once something is pushed, treat it as public forever.

**The rules:**
- ❌ Never put real keys, passwords, or teammates' personal info in `DESIGN.md`, in code, in the README, or in an AI chat.
- ✅ Keep real secrets in a file that Git ignores (the `.gitignore` already lists common ones).
- 🧑‍🏫 If you're unsure, **ask a mentor before pushing.** It's much easier to keep a secret out than to remove one after it's public.

> ⚠️ **A key inside your app's code is not hidden.** Anyone who opens a web app can read the JavaScript in it — that's how browsers work. "It's not in a file called `secrets`" doesn't help. If your app needs a key to talk to a service, that's a mentor conversation, not something to solve yourself.

> 😬 **Already committed something you shouldn't have?** Deleting it in your next save does *not* remove it — Git keeps the old version. Tell a mentor today; see [`GIT-BASICS.md`](./GIT-BASICS.md). Nobody's in trouble, but it needs fixing fast.

---

## ▶️ Running & sharing this project

**You run this on your own laptop** — that's how student projects get demoed here, judges included. Putting an app **online is a mentor's decision**, so talk to one before hosting anything. Details, plus the rules that keep your app ready for either: [`DEPLOY.md`](./DEPLOY.md).

*(Fill this in as you build — the AI can help you write it.)*

- **To run it locally:** [ ... e.g. "open `src/index.html` in a browser" ]
- **Who it's for:** [ ... ]
- **Hosting:** [ not hosted — runs on a laptop *(normal)* · approved by a mentor on YYYY-MM-DD → link ]

---

## ✅ Before you call it "done"

Check it against the **success criteria and test checklist in `DESIGN.md` (Section 12).** The app is finished when it passes those — not when it merely looks finished. Then make sure `DESIGN.md` matches the final app.

---

## 🏁 After competition — close it out

This project has an ending. Most of our apps are built for **one season** and then replaced, so next year's students get to plan their own (see [`TEAM.md`](./TEAM.md)).

**Spend twenty minutes on [`DESIGN.md` Section 18](./DESIGN.md#-18-after-the-season--what-we-learned)** — what competition taught you, which requirements you got wrong, what you'd do differently — then set the document's Status to **📦 Season complete**.

> 🏆 Next year's team won't inherit your code. They'll inherit **what you figured out.** That's worth twenty minutes.

---

## 🧑‍🏫 For mentors & next year's team

This repo was created from our team's **software project template**, so every student project has the same structure and the same planning document.

**Most of our apps are rebuilt fresh each season** so new students get to do the planning themselves — which means the thing worth reading here is [`DESIGN.md`](./DESIGN.md): how this team decided what to build, what they cut, and what turned out to be wrong. **Steal the thinking, not the code.**

Improving the template itself? Edit the *template repo*, not this copy.

**From another team?** You're welcome to use this — that's why it's public. It's [MIT licensed](./LICENSE): take it, change it, make it yours; just keep the credit line in `LICENSE`.

---

*Made for FRC / FTC / FLL student software projects. Plan it, build it, understand it. 🏆*
