# 🔍 Finding the Real Requirements

> **What this is:** how to work out what your app actually needs to do — *before* you or an AI write a line of code.
>
> **Why it's the hard part:** the AI will build whatever you describe, fast and cheerfully, including the wrong thing. Nothing in a coding tool will ever tell you that you solved a problem nobody had.

---

## 🧠 The one idea

**Requirements don't live in your head, and they don't live in the AI. They live with the people who'll use the thing.**

You cannot get them by thinking harder at your desk, and you cannot get them by asking an AI to imagine them. You get them by **watching, asking, and arguing with real people** — then writing down what you learned.

That's the work. It's the part judges ask about, and it's the part that decides whether your app gets used at competition or ignored.

---

## 👀 Watch the job being done today

Whatever your app replaces, somebody is doing it right now — on paper, in a group chat, in their head. **Go watch them do it once, without helping.**

Take notes on:

- **Where they slow down or hesitate.** That's where the app earns its keep.
- **What they write down** — the actual fields they care about. That's your data section, free.
- **What they get wrong,** and what it costs them.
- **The shortcuts they've invented.** Those are requirements in disguise. If every scout has been abbreviating team names, your app needs that.
- **What they never do,** even though you assumed they would.

> 💡 **One match of watching a scout beats an hour of guessing about scouts.** Bring a notebook. Don't offer suggestions — you're there to see what's true, not to sell your idea.

---

## 🗣️ Ask the people who'll use it

**What people say they want and what they actually do are different things.** Not because they're lying — because nobody can describe their own habits accurately. So ask about the past, not the future.

| ❌ Weak question | ✅ Better question |
|---|---|
| "Would you like a rankings screen?" | "Walk me through the last time you picked an alliance. What did you look at?" |
| "Should it work offline?" | "Tell me about the last time the wifi died on you. What happened?" |
| "Is this useful?" | "What did you do about this at the last competition?" |
| "What features do you want?" | "What's the most annoying part of scouting right now?" |

**Everyone says yes to "would you like…"** — it's free to agree with a hypothetical. Stories about last week are real evidence.

> ⚠️ **Ask at least two people, and pick different ones.** A rookie scout and a strategy lead will describe completely different apps. If they disagree, you just found a requirement worth writing down — and a decision worth making on purpose.

---

## ❓ Keep asking "why" until it stops moving

The first answer is almost never the real one. Keep going:

> *"We need a rankings screen."*
> — Why? *"So we can pick alliance partners."*
> — Why does that need a screen? *"Because on selection day we're rushing."*
> — Why the rush? *"We only get a few minutes and the data's spread across six phones."*

The stated requirement was *a rankings screen*. The real one is **"one place, fast, on selection day."** Those lead to different apps — and the second one you can actually test.

**Three or four whys is usually enough.** You'll know you've hit the bottom when the answer stops changing.

---

## 🔨 Sweep for the cases that break things

Once you have a rule, attack it. Take every input and every action in your app and run it through this list. **Write down what should happen** — each answer is a requirement, and each one you skip is a bug you've agreed to have.

| What if it's… | Ask yourself |
|---|---|
| **Empty** | Blank field, no matches yet, first-ever use. What shows? |
| **Huge** | 200 teams, a 500-character note, a season's worth of data. |
| **Wrong** | Letters in a number field. Team 99999. A negative score. |
| **Doubled** | Two scouts, same match. The same button tapped twice, fast. |
| **Out of order** | Match 12 entered before match 4. |
| **Interrupted** | The phone dies, the browser closes, the app is backgrounded mid-entry. |
| **Offline** | No wifi at the worst moment. *(See `DEPLOY.md`.)*|
| **Late** | Someone edits a match from yesterday. |

> 💡 Most of your Section 6 edge cases come straight out of this table. Work down it once, honestly, and you'll be ahead of most student projects — and a fair number of professional ones.

---

## 🤖 Using AI without handing over the thinking

AI is genuinely good here — but **only in one direction.**

**The rule: you draft, it attacks. Never the reverse.**

If you ask an AI to write your requirements, it will invent plausible ones based on every other scouting app it has ever seen. They'll look great. They'll be about somebody else's team, and you'll have no idea which parts are wrong — because you never made the decisions yourself.

**Good prompts** *(you've done the thinking; the AI stress-tests it)*:

- *"Here are my rules. What situations do they not cover? Just list the holes — don't fix them."*
- *"Argue against this plan. What's the strongest reason this app fails at competition?"*
- *"I said the app should be 'fast.' Ask me questions until that's specific enough to test."*
- *"Pretend you're a scout in the stands who's never seen this. Where do you get confused?"*
- *"Which of my requirements contradict each other?"*

**Prompts that quietly do your job for you:**

- ❌ *"Write the requirements for a scouting app."*
- ❌ *"What features should my app have?"*
- ❌ *"Write a test checklist for this."*

The difference isn't politeness — it's **who made the decision.** You have to be able to say *why* your app works the way it does. "The AI suggested it" is the one answer that doesn't hold up, to a judge or to a teammate at 8am on selection day.

---

## 🚩 You're not ready to build yet if…

- You can't say who the *one* main user is.
- Every feature feels equally important. *(Then you haven't prioritized — you've listed.)*
- Your rules have no numbers in them. "Fast," "a lot," "recent" aren't testable.
- You haven't talked to anyone who'll actually use it.
- You can't name a single thing you've decided **not** to build.
- Someone asks "what happens if…" and your answer is "we'll figure that out later." *Later is now.* That's the cheapest it will ever be to decide.

---

## ✅ You're ready when

You can hand your `DESIGN.md` to a teammate who's never seen it, and they can tell you what the app does, who it's for, and what happens in the weird cases — **without asking you a single question.**

That's the real test. If they have to ask, the answer belongs in the document.

> 🏆 Then go do the out-loud check at the end of `DESIGN.md`, and build.

---

*Part of our FRC / FTC / FLL software project template. If something here confused you, tell a mentor so we can fix the wording for the next student.*
