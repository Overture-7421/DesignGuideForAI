# 🚀 Running & Hosting — where your app lives

> **What this is:** how you show your app to people, and how it would one day get on the internet.
>
> **The short version:** you run your app **on your own laptop** — that's the normal way projects get demoed here. Putting one **online is a mentor's decision**, not a student's. Build it right and both work.

---

## 🛑 The one rule

**Nothing this team builds goes online without a mentor.**

Not a formality. Putting an app on the internet means accounts, sometimes billing, and a public address anyone can find — those are adult decisions. So:

| You want to... | What you do |
|---|---|
| Show your app to a teammate, a mentor, or a judge | **Run it on your laptop.** Go right ahead. |
| Put it on the internet so anyone can open a link | **Talk to a mentor first.** Always. |

Nobody's trying to slow you down — **you can build an entire finished app without ever hosting it.** Most student projects never need it.

---

## ▶️ Running it on your laptop

This is your default. It should be *boring* — no setup, no internet, no accounts.

**If it's a plain website (HTML/CSS/JavaScript):** find `index.html` in your project folder and **double-click it.** It opens in your browser. That's the whole thing.

*(Some things — like loading a data file — need a "local server" instead of double-clicking. If your AI says you need one, ask it: "Set that up for me and explain what a local server is." It's a one-line command, not a big deal.)*

**If it's Python:** run it from VS Code, or ask your AI to show you the command.

> 💡 **This is also your demo.** Laptop on the table, app running, you explaining it — that's a complete project demo. A live link adds nothing a judge cares about.

---

## 🧳 Build it portable (this is the important part)

**Portable** means: your app doesn't know or care where it lives. Laptop folder, USB stick, a web host someone picks next year — it just works.

Do these from day one. They cost nothing now and save a rewrite later.

**1. Use relative paths. Never start a path with `/`.**

| ❌ Breaks | ✅ Works |
|---|---|
| `<link href="/style.css">` | `<link href="./style.css">` |
| `<img src="/logo.png">` | `<img src="./logo.png">` |

That leading `/` means "the very top of the website" — which is your whole hard drive when you're local, and the wrong folder on most hosts. It is the **number one cause** of "it works on my laptop but the hosted page is blank."

**2. Never type a website address into your code.** No `https://something.github.io/...` hardcoded anywhere. Link to your own pages with plain relative links (`./rankings.html`).

**3. Keep all saving and loading in one file.** All of it — `saveMatch()`, `getMatches()`. Make them `async` from the very start, even while you're only saving on the device. If the team ever moves to a shared database, **only that one file changes.** *(This is the same advice as `DESIGN.md` Section 7 — it matters that much.)*

**4. Keep settings and keys in one separate file, named `config.secret.js`.** Then pointing your app at something new is a settings change, not a code change. **Use that exact name** — our `.gitignore` already knows to keep `config.secret.*` out of GitHub, and a file called `config.js` would get committed like any other. Never put real keys anywhere else; see `README.md`.

**5. Avoid a build step if you can.** A "build step" is a command you must run to turn your code into the thing people actually open. Plain HTML/CSS/JS needs none — the file you edit is the file that runs. Tools like React do need one, which limits where the app can go. **Not forbidden — just ask a mentor before choosing one.**

> ✅ **Ten-second portability check:** move your project folder somewhere else on your laptop — Desktop, USB stick, anywhere — and open it again. Still works? You're portable. Broken? Something's hardcoded, and it would have broken online too.

---

## 🤝 If you think you need hosting

Some projects genuinely do — usually when **several people's phones need to see the same live data**, or someone outside the team needs a link.

**Start the conversation early.** Around the time you're building your second or third feature — not the week before competition. Approval and setup take real time.

**Come to a mentor with these four answers.** It turns a vague ask into a five-minute decision:

1. **Why does it need to be online?** What breaks if it just runs on a laptop?
2. **Who opens it?** Just the team, or the public?
3. **Does it store shared data,** or is it only files people look at?
4. **Does it need a build step?** (See rule 5 above.)

**Then what happens:** a mentor either approves your suggestion or proposes a different host — either direction is normal. There is **no house default**; the right host depends on what your app actually needs, which is why the conversation happens *after* you know. A mentor does the setup under the **team account**, so nothing important ends up stranded on a graduating senior's personal login.

**Then record it** in `DESIGN.md` Section 9: which host, who approved it, and the live link. Add a line to the Change Log too.

> 💡 **Keep building while you wait.** Hosting should never block you — that's exactly what the portability rules above buy you.

---

## 🌐 What hosting actually involves

You don't need this section until a mentor has approved a host. It's here so nothing is a surprise.

- **It's never automatic.** No host puts your app online just because you pushed to GitHub — someone has to switch it on and point it at your project. A mentor does this with you.
- **You get a link with your project's name in it,** usually a subfolder rather than a bare domain. That's exactly why rule 1 matters.
- **Changes take a minute or two to appear** — and your browser may keep showing you the old version. Wait, then force-refresh (`Ctrl+Shift+R`) before you assume it's broken.
- **Most simple hosts only serve files** — HTML, CSS, JavaScript, images. They **can't run Python.** A Python tool stays a laptop tool unless a mentor sets up something bigger.
- **Assume anything you host is public.** Anyone with the link can open it, and anyone can read the JavaScript inside it. Nothing secret goes in your app's code — ever.

---

## 📴 Hosted is not the same as offline

Worth knowing before competition, because it surprises people.

Our team's rule is that anything used **in the stands works offline** (`TEAM.md`). Hosting does *not* give you that. A hosted app still has to be **loaded once with internet**, and only keeps working after that if it was **built** to — saving to the device, not to a server it can't reach.

**So:** if your app is for the stands, it must work with the wifi off. Test it that way — actually turn wifi off and try. Don't assume a host handles it. Nothing does that for you.

---

## ✅ Quick self-check

- [ ] I can open my app by double-clicking a file (or one simple command).
- [ ] I moved the folder somewhere else and it still worked.
- [ ] No path in my code starts with `/`.
- [ ] No website address is typed into my code.
- [ ] All saving and loading lives in one file, with `async` functions.
- [ ] No real keys or passwords anywhere in the project.
- [ ] If it's for the stands: I turned wifi off and it still worked.

> 🤖 **Ask your AI:** *"Look through my project and tell me if anything assumes where it's hosted — hardcoded addresses, paths starting with `/`, or saving code spread across multiple files. Explain what you find like I'm new to this."*

---

*Part of our FRC / FTC / FLL software project template. If something here confused you, tell a mentor so we can fix the wording for the next student.*
