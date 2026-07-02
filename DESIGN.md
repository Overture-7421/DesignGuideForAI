# 🤖 Software Design Document (AI-Assisted)
### A planning template for FRC / FTC / FLL student software projects

> **What this is:** A fill-in-the-blanks document that helps you *think before you build*. You answer the questions, an AI assistant (Claude, ChatGPT, Copilot, etc.) helps you fill the gaps, and the finished document becomes the spec the AI uses to actually build your app, website, or tool.
>
> **The golden rule:** *An AI can only build what you can clearly describe.* This document forces you to describe it clearly. A vague plan produces a vague app. A precise plan produces a working app.
>
> **This is a LIVING document.** It must always describe the app *as it actually is right now* — not just what you planned at the start. Whenever the app changes (a feature is added, a rule changes, an idea is dropped), this document gets updated to match. The document and the app stay in sync, always. This file is the **single source of truth**: if it's not written here, it's not part of the app.

---

## 📋 How to use this document

1. **Start from the template repo.** This document lives in our team's GitHub *template repository*. Click **"Use this template" → "Create a new repository"** to get your own copy of this file inside a fresh repo for your project. Don't edit the master template — your work happens in *your* repo.
2. **Fill it top to bottom.** Don't skip ahead. Each section builds on the one before it.
3. **Use AI as a thinking partner, not an autopilot.** When you're stuck on a section, paste the section into your AI tool and ask: *"Help me think through this part. Ask me questions until you understand what I want."*
4. **Mark what you finish.** Replace every `[ ... ]` placeholder. Leave `🟡 TODO` where you're still deciding.
5. **When the doc is done, build.** Jump to the last section, *"Hand it to the AI,"* and use the ready-made prompt.
6. **Keep it in sync as you build.** Every time you change something about the app, update the matching section here *and* add a line to the Change Log (Section 17). The AI is told to do this for you — but check that it actually did. A document that no longer matches the app is worse than no document.

**Two levels of detail:**
- 🟢 **CORE** — every project fills these in. If you only do the green sections, you still have a usable plan. *(Good starting point for FLL teams and first-time builders.)*
- 🔵 **ADVANCED** — fill these in for bigger or more serious projects. *(Recommended for FTC/FRC scouting systems, team websites with logins, anything other people will rely on.)*

> ⚠️ **One safety rule, read it first:** **Never** put secrets or personal information into this document, into a public AI chat, or into your GitHub repo. That means no passwords, no API keys (the secret codes for services like The Blue Alliance), and no personal details about teammates (full names + contact info, etc.). Once something is pushed to GitHub or pasted into a chat, treat it as public forever. If your app needs a secret key, ask a mentor how to store it safely. *(More on this in Section 11.)*

---
---

# PART 1 — WHAT ARE WE BUILDING?

## 🟢 1. The one-line summary

*Why this matters: If you can't say it in one sentence, you don't understand it yet.*

**Prompt to answer:** Fill in this exact sentence —
> "We are building a **[type of thing]** that helps **[who]** to **[do what]**."

**Example (scouting app):**
> "We are building a **mobile-friendly web app** that helps **our scouts** to **record what other teams' robots do during matches, so we can pick good alliance partners**."

**Your answer:**
> We are building a **[ ... ]** that helps **[ ... ]** to **[ ... ]**.

---

## 🟢 2. The problem & the objective

*Why this matters: Software exists to solve a problem. Name the problem first.*

**Questions to answer:**
- What problem or annoyance are we trying to fix right now? (What do people do today, and why is it bad/slow/error-prone?)
- What does success look like? How will we know the app actually helped?

**Example (scouting app):**
- *Problem:* Scouts write notes on paper. The notes get lost, the handwriting is messy, and on alliance-selection day we can't quickly compare teams.
- *Success:* By the end of a competition, we can open the app and instantly see the top 8 robots by average scoring, with no paper involved.

**Your answer:**
- **Problem:** [ ... ]
- **Success looks like:** [ ... ]

---

## 🟢 3. Goals and NON-goals (scope)

*Why this matters: This is the most important section. Most student projects fail because they try to do everything. Decide what you are NOT building.*

**In scope (we WILL build this):**
- [ ... ]
- [ ... ]
- [ ... ]

**Out of scope (we will NOT build this — at least not now):**
- [ ... ]
- [ ... ]

**Example (scouting app):**
- ✅ In scope: record match data, view team averages, works offline at the venue.
- ❌ Out of scope: user accounts/logins, live syncing between phones, fancy graphs, predicting match winners. *(Maybe version 2.)*

> 💡 **Tip:** When in doubt, put it in "out of scope." You can always add it later. A small app that works beats a big app that doesn't.

---

# PART 2 — WHO USES IT AND WHAT DO THEY DO?

## 🟢 4. The users

*Why this matters: You're not building for "everyone." Build for specific people.*

| Who they are | What they need from the app | Tech skill level |
|---|---|---|
| [e.g. Scouts in the stands] | [Fast data entry on a phone] | [Low — must be obvious] |
| [ ... ] | [ ... ] | [ ... ] |
| [ ... ] | [ ... ] | [ ... ] |

---

## 🟢 5. What it should do (user stories)

*Why this matters: This is your feature list, written from the user's point of view. The AI will turn each one into a feature.*

**Format:** *"As a **[user]**, I want to **[do something]**, so that **[benefit]**."*

**Example (scouting app):**
- As a **scout**, I want to **tap buttons to count game pieces scored**, so that **I don't have to type during a fast match**.
- As a **strategy lead**, I want to **see each team's average score sorted high-to-low**, so that **I can build a pick list**.
- As a **scout**, I want the app to **save my data even with no internet**, so that **I don't lose it in a crowded venue**.

**Your user stories** (write 5–15; the most important ones first):
1. As a **[ ... ]**, I want to **[ ... ]**, so that **[ ... ]**.
2. As a **[ ... ]**, I want to **[ ... ]**, so that **[ ... ]**.
3. As a **[ ... ]**, I want to **[ ... ]**, so that **[ ... ]**.
4. [ ... ]
5. [ ... ]

> 💡 Sort them. Put a ⭐ next to the 3 you can't live without — build those first.

---

## 🟢 6. The rules (this is the brain of your app)

*Why this matters: "Rules" are the logic that makes your app smart. They're the decisions the app makes for you. AI gets these wrong unless you spell them out.*

Write rules as **"When X happens, the app should do Y."** Be picky. Include the weird cases.

**Example (scouting app):**
- When a scout submits a match, the app should **check that a team number and match number were entered**, otherwise show an error.
- When two scouts enter data for the same team in the same match, the app should **keep both and average them** (don't overwrite).
- When a robot's score is **left blank**, the app should treat it as **0, not as "skip."**
- A team's "average" should only count matches where they **actually played** (ignore no-shows).

**Your rules:**
- When [ ... ], the app should [ ... ].
- When [ ... ], the app should [ ... ].
- When [ ... ], the app should [ ... ].
- [ ... ]

**Edge cases / "what if" list** *(the situations that break apps):*
- What if the user enters [bad/empty/huge] input? → [ ... ]
- What if two people do the same thing at once? → [ ... ]
- What if there's no internet? → [ ... ]
- What if [ ... ]? → [ ... ]

> 💡 **Ask your AI:** *"Here are my rules. What edge cases am I forgetting?"* AI is great at spotting holes in logic.

---

# PART 3 — THE INSIDES

## 🟢 7. The data — what does the app remember?

*Why this matters: Almost every app stores information. Listing it now saves huge headaches later.*

List the "things" your app keeps track of and what details each one has.

**Example (scouting app):**
- **Match Entry**: team number, match number, scout name, points scored (auto), points scored (teleop), did the robot break down? (yes/no), notes
- **Team** (calculated from entries): team number, average score, number of matches scouted

**Your data:**
- **[Thing 1, e.g. "User"]**: [field, field, field ...]
- **[Thing 2]**: [field, field, field ...]
- **[Thing 3]**: [field, field, field ...]

**Where is the data stored?** (pick one to start)
- [ ] Just on the device (simplest — good for offline tools)
- [ ] A shared online database (needed if multiple people share data) 🔵
- [ ] A Google Sheet / spreadsheet (easy for teams already using one)
- [ ] 🟡 TODO — ask AI to recommend based on my needs

---

## 🟢 8. The screens (what the user sees)

*Why this matters: Listing the screens/pages is like sketching the app before building it.*

List each screen and what's on it. **Even a rough description or a phone-photo of a paper sketch helps the AI a lot.**

**Example (scouting app):**
1. **Home screen** — buttons: "New Match Entry", "View Team Rankings".
2. **Entry screen** — fields for team #, match #, +/- counters for scoring, a "save" button.
3. **Rankings screen** — a table of teams sorted by average score.

**Your screens:**
1. **[ ... ]** — [what's on it]
2. **[ ... ]** — [what's on it]
3. **[ ... ]** — [what's on it]

**How do users move between screens?** (the flow)
> [e.g. Home → tap "New Entry" → Entry screen → tap Save → back to Home]

> 💡 Hand-draw your screens on paper, take a photo, and give it to the AI. It can read sketches.

---

## 🟢 9. The tech (what it's built with)

*Why this matters: Pick tools that match your team's skills and that AI knows well.*

**Not sure? Use these student-friendly defaults and let the AI guide you:**

| You want to build... | Good beginner choice | Notes |
|---|---|---|
| A website / web app (works on any phone/laptop) | **HTML + CSS + JavaScript**, or **React** | Easiest to share — just send a link. Best default for scouting apps. |
| A phone app you install | A web app first, then wrap it | Real native apps are harder; start with a web app. |
| A robot dashboard / data tool | **Python** | Pairs well with robot code. |
| Quick data crunching | **Python** or a **Google Sheet + scripts** | |

**Our choice:**
- **Language / framework:** [ ... or "🟡 TODO — ask AI"]
- **Where it runs:** [ phone browser / laptop / installed app / ... ]
- **Where it's hosted / shared:** [ GitHub Pages / a link / just on our laptop / ... ]
- **Tools we already know:** [ ... ]

> 💡 **Ask your AI:** *"I want to build [my app] and our team knows [these tools]. What's the simplest stack that an AI can help us build and that we can actually host for free?"*

---

## 🔵 10. Architecture overview (advanced)

*Why this matters: For bigger projects, sketch how the pieces fit together.*

Describe (or draw) the main parts and how they talk to each other.

**Example (scouting app with online sync):**
> Phones (web app) → send data → Online database → Rankings page reads from the same database.

**Your architecture:**
> [ ... or paste a simple diagram / "Phone → does X → sends to Y → shows Z" ]

---

## 🔵 11. Outside connections / APIs (advanced)

*Why this matters: If your app talks to other services, list them.*

**Examples for FIRST teams:** The Blue Alliance API (team & match data), Statbotics (predictions), Google Sheets, FIRST's event API.

**Connections we need:**
- **[Service name]** — used for [ ... ] — link to its docs: [ ... ]
- [ ... ]

> ⚠️ **Security note:** Some services need a secret "API key." **Never** paste real keys, passwords, or personal info into a public AI chat or a public GitHub repo. Ask an adult mentor how to keep secrets safe.

---

# PART 4 — IS IT GOOD AND DOES IT WORK?

## 🟢 12. How we'll know it works (success criteria & testing)

*Why this matters: "It looks done" is not the same as "it works." Decide the tests up front.*

**The app is finished when it can pass these checks:**
- [ ] [e.g. A scout can record a full match in under 30 seconds.]
- [ ] [e.g. Rankings show the correct average for a team with 3 entries.]
- [ ] [e.g. Data is still there after closing and reopening the app.]
- [ ] [ ... ]
- [ ] [ ... ]

**Things to try to break it (test the edge cases from Section 6):**
- [ ] [e.g. Submit an empty form — does it warn me?]
- [ ] [e.g. Turn off wifi — does it still save?]

> 💡 **Ask your AI:** *"Write a test checklist for this app based on my rules and success criteria."*

---

## 🔵 13. Quality requirements (advanced)

*Why this matters: How fast, safe, and usable does it need to be?*

- **Speed:** [e.g. A screen should load in under 2 seconds on a phone.]
- **Works on:** [which phones / browsers / screen sizes?]
- **Privacy & safety:** [Does it store personal info? Who can see the data?]
- **Accessibility:** [Big tap targets? Readable in bright sunlight at a venue? Works one-handed?]
- **If it crashes:** [What should happen? Lose data, or recover it?]

---

# PART 5 — THE PLAN

## 🟢 14. Build plan (small steps)

*Why this matters: Build in small, working pieces. A working tiny app beats a half-finished big one.*

| Step | What we'll have working | Done? |
|---|---|---|
| 1 | [The smallest version that does ONE useful thing — your ⭐ feature] | ⬜ |
| 2 | [Add the next most important feature] | ⬜ |
| 3 | [ ... ] | ⬜ |
| 4 | [ ... ] | ⬜ |
| 5 | [Polish: make it look nice, test edge cases] | ⬜ |

> 💡 The "minimum first version" is whatever lets a real person do the #1 task. Build *that*, test it with a teammate, then grow.

---

## 🟢 15. Open questions & risks

*Why this matters: Writing down what you don't know yet keeps it from becoming a surprise.*

- ❓ Things we haven't decided: [ ... ]
- ⚠️ What might go wrong: [e.g. "No wifi at the venue" / "Only one person knows the code" / "We run out of time"]
- 🛟 Backup plan: [ ... ]

---

## 📖 16. Glossary

*Define any words a new teammate (or the AI) might not know.*

- **[Term]** — [plain-language meaning]
- **Auto / Teleop** — [the autonomous and driver-controlled periods of a FIRST match]
- **Pick list / alliance selection** — [ ... ]
- [ ... ]

---

## 📝 17. Change Log

*Why this matters: This is how the document stays a living, trustworthy record. Every time the app changes, add a line here. New entries go on top. This lets anyone — a teammate, a mentor, a judge, or next year's team — see how the app grew and why.*

**Who writes each entry:** *Whoever makes the change records it.* When you're building with the AI, the AI writes the entry and shows you what it changed — your job is to check it. When you change something on your own (filling in a section, a scope decision in a team meeting, dropping a feature the AI never saw), you write the entry yourself.

| Date | What changed | Why | By |
|---|---|---|---|
| [YYYY-MM-DD] | [e.g. Added "robot broke down?" field to Match Entry] | [Scouts needed to flag unreliable robots] | [name / AI] |
| [YYYY-MM-DD] | [e.g. Dropped user logins from scope] | [Too complex for v1; not needed at venue] | [ ... ] |
| [YYYY-MM-DD] | Document created | First version of the plan | [ ... ] |

> 💡 A change isn't "done" until both the app *and* this document reflect it. If you only change one, they drift apart and the document stops being trustworthy.

---
---

# 🚀 HAND IT TO THE AI

Once the green sections are filled in, you're ready to build. **Copy the prompt below**, paste it into your AI tool, then paste your filled-in document right after it.

> **Prompt to start building:**
>
> *"You are helping a student robotics team build software. Below is our completed software design document. Please do the following, one step at a time:*
> 1. *First, read the whole thing and ask me about anything that is unclear, contradictory, or missing — especially in the Rules and Edge Cases sections. Don't write code yet.*
> 2. *Then propose the simplest tech stack that matches our skills and can be hosted for free, and wait for me to agree.*
> 3. *Then build 'Step 1' from our Build Plan only — the smallest working version. Explain the code simply, as if teaching a beginner.*
> 4. *After each step works, we'll move to the next one together.*
> 5. ***Keep our design document up to date.** Treat it as the single source of truth. Any time we add, change, or remove a feature, rule, screen, data field, or tech choice, update the matching section of the document AND add a dated line to the Change Log (Section 17). At the end of every work session, show me the updated document and point out exactly what you changed so it always describes the app as it really is.*
> *Here is our document:"*
>
> *[paste your filled-in document here]*

**While building, keep asking the AI to teach, not just type:**
- *"Explain what this code does, line by line, like I'm new to this."*
- *"Why did you choose to do it this way?"*
- *"Here's an error I got: [paste it]. What does it mean and how do I fix it?"*
- *"How do I test that Step 2 actually works?"*
- *"We just changed [X]. Update the design document and the Change Log to match, and show me what you changed."*

> 🏆 **Remember:** The goal isn't just a finished app — it's that *you* understand and can explain how it works. At a FIRST event, judges (and your teammates) will ask. The student who planned it with this document will have the answer.

---

*Template made for FRC / FTC / FLL student software projects. Copy it, improve it, and share it with next year's team.*
