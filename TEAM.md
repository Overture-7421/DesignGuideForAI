# 🤖 Team Context — Overture (FRC 7421 · FTC 23619)

> **What this is:** A short description of our team and how we build software, so an AI doesn't have to re-ask the same questions every chat — it already knows our tools, our limits, and who to point students to.
>
> **Where it lives:** in our **Claude Project knowledge** and in our **GitHub template repo**, so it travels with every project. Keep it up to date.
>
> ⚠️ This file may end up in a public repo. **No names, no contact info, no addresses, nothing private.** Describe people by *role* ("a software mentor"), never by name.
>
> **Another team?** You're welcome to use this template. Replace this file with your own team's details — and keep it name-free like this one.

---

## 👋 Who we are
- **Team name:** Overture
- **Programs & numbers:**
  - **FRC** — Team **7421**
  - **FTC** — Team **23619**
  - **FLL** — number changes each season
- **Who's on the team:** students from ~9-year-old FLL members up to high-school FRC members. **Always match the explanation to the person.**
- **Season:** changes every year. If it matters for a project, ask the student which season they're building for.

## 🛠️ What we build (software)
The kinds of software projects our students take on:
- **Scouting apps** — record and rank other teams' robots at competition
- **Dashboards** — show robot data / team info at a glance
- **Mentor apps** — tools that help mentors run the team
- ...and other team tools as needs come up

## 🧠 What we know (skills & tools)
- **Overall level: ALWAYS ASSUME BEGINNERS. Always.** Explain everything from scratch, define every piece of jargon, and never assume prior coding knowledge — no matter who's asking.
- **Tools we already use:** GitHub, VS Code, and WPILib (for robot code).
- **But don't assume they know Git.** Most students meet GitHub for the first time here — explain as you go, and point them to `GIT-BASICS.md`.
- Prefer the **simplest possible tech** that does the job and that a beginner can understand and explain.

## 📦 Where our stuff lives
- **Code:** GitHub — **github.com/Overture-7421**
- **New projects start from:** our template repo — **github.com/Overture-7421/DesignGuideForAI** → click **"Use this template" → "Create a new repository."**
- **Domain:** the team owns a domain, but **a mentor manages it** — ask a mentor before pointing anything at it.

## ☁️ Hosting & deployment
- **Nothing goes online without a mentor.** Hosting means accounts, sometimes billing, and a public address — adult decisions. Students demo by **running the app on their own laptop**; that's the normal way a project gets shown here, judges included.
- **The decision is a conversation, not a default.** A student proposes a host, or a mentor proposes one — either direction. **We have no house default:** GitHub Pages, Firebase, Supabase, a mentor-run server — each fits some projects and not others, and the right answer depends on what the app actually needs. That's why the conversation happens *after* you know what you built.
- **A mentor does the setup, under the team account.** Team-owned projects grant access to student accounts, so nobody hits a billing surprise and nothing important ends up stranded on a graduating senior's personal login.
- **Build so the answer doesn't matter.** Every app should run from a plain folder on a laptop and work anywhere it's later put — relative paths, no hardcoded addresses, all saving/loading in one file. The rules are short and free if you follow them from day one: see `DEPLOY.md`.
- **Record the outcome** in `DESIGN.md` (Section 9): which host, who approved it, and the live link.
- 💡 **Never wait on hosting to start building.** A complete app can be built, tested, and demoed before anyone picks a host. Most projects need the conversation late; plenty never need it at all.

## 💻 Devices
- Everyone uses their **own phone and laptop** — all different kinds, no shared team devices.
- **So:** build things that run in a **normal web browser** on a phone or laptop. Safest target when everyone's on different hardware.

## 📶 Internet at competitions
- **Usually unreliable.** Venue Wi-Fi at FRC/FTC events is crowded or spotty.
- **Default rule:** anything used *in the stands* (like a scouting app) should **work offline**.
- **But not every project needs it** — a mentor app or a laptop dashboard is fine online. **Ask the student whether offline actually matters** before assuming; don't force it on a project that doesn't need it.
- ⚠️ **Hosted ≠ offline.** A hosted app still has to be loaded once with internet, and keeps working after that only if it was *built* to. Hosting never provides offline on its own — don't let a student assume it does.

## 🤝 How we work with AI
- **Plan first:** every software project starts by filling in `DESIGN.md` — no code until the plan is clear.
- **Smallest version first:** build one small working piece, test it, then grow.
- **Build host-agnostic:** the app runs from a folder on a laptop and doesn't know or care where it's hosted. Hosting is a separate, mentor-approved decision — see `DEPLOY.md`.
- **Understand, don't just copy:** a student should be able to explain their own code to a judge.
- **Keep `DESIGN.md` in sync:** when the app changes, update the matching section and add a dated line to its Change Log.

## 🙋 Who to ask
- **Software help:** ask a software mentor at a team meeting. *(No names in this file — it's public.)*
- **Domain, secrets & API keys:** a mentor manages these. **Never** put real keys, passwords, or teammates' personal info in code, chats, or the repo — ask a mentor to store them safely.

## 📖 Team words (glossary)
*Terms a new member — or the AI — might not know:*
- **FRC / FTC / FLL** — the three FIRST robotics programs our team competes in (oldest/most advanced to youngest).
- **Scouting** — watching and recording what other teams' robots do, to help pick alliance partners.
- **Auto / Teleop** — the autonomous (pre-programmed) and driver-controlled parts of a match.
- [ add your own... ]

---
*Last updated: 2026-08-13*
