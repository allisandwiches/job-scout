# 🎯 Job Scout — Your Personal Job-Hunting Assistant

**Job Scout** is a ready-made set of instructions you give to Claude (an AI assistant) so it searches job boards for you, filters out the roles that don't fit, rates how good a match each one is, and sends you a tidy digest — once a week, once a day, or whenever you like.

**No coding. No installing anything.** If you can fill out a form and copy-paste text, you can use this.

Originally built for game-industry producers, but it works for **any creative or studio job**: artists, animators, designers, writers, audio, QA, community, production — or any field at all.

---

## ✨ What you get

Each digest looks something like this:

> **🟢 Strong match — Senior Environment Artist, Example Studio (Remote, US)**
> Posted 3 days ago · Contract · $45–60/hr
> *Why it fits:* Matches your 5+ years in Unreal and stylized environments.
> *Watch out for:* Asks for Houdini, which isn't on your resume.
> [Apply here](https://example.com)

…grouped into **Strong / Possible / Stretch**, with a separate section for **staffing agencies**, and a reminder of anything you've already applied to. See a full fake example in [`examples/sample-digest.md`](examples/sample-digest.md).

---

## 🧰 What you need

| You need | Notes |
|---|---|
| A **Claude account** | Sign up free at [claude.ai](https://claude.ai). Web search and scheduled (automatic) runs may need a paid plan — check what your plan includes. |
| **Your resume** | Any format: Word, PDF, or pasted text. |
| **10–15 minutes** | One-time setup. |
| **Python 3+** | Download free at [python.org](https://www.python.org/downloads/) to allow hosting on your PC/Mac|
| *(Optional)* Google Sheets or Excel | To track applications with the included template. |

---

## 🚶 Setup walkthrough (5 steps)

### Step 1 — Download this kit
At the top of this GitHub page, click the green **`<> Code`** button → **Download ZIP**. Open the ZIP on your computer. *(No GitHub account needed.)*

### Step 2 — Fill in your settings
Open **[`1-MY-SEARCH-SETTINGS.md`](1-MY-SEARCH-SETTINGS.md)** in any text editor (Notepad, TextEdit, or even right here in your browser and copy it).

It's a fill-in-the-blanks form: job titles you want, titles you *don't* want, studios you love, job boards you trust, where you can work, and so on. Replace everything in `[square brackets]`. Leave anything blank that doesn't matter to you.

> 💡 **Tip:** Be specific about what you *don't* want. "No lead or director roles" and "no roles requiring a second language" save you tons of scrolling.

### Step 3 — Set up a Claude Project
A **Project** in Claude is a folder that remembers files and instructions between chats.

1. Go to [claude.ai](https://claude.ai) → **Projects** → **Create project**. Name it something like *Job Scout*.
2. **Add your resume** to the project's files/knowledge.
3. **Add your filled-in settings file** too.
4. Open **[`2-THE-PROMPT.md`](2-THE-PROMPT.md)**, copy the box of text, and paste it into the project's **instructions** (or just into your first chat in the project).

### Step 4 — Run it once to test
In a new chat inside your project, type:

> **Run my job scout now.**

Claude will search, filter, and give you a digest. Read it over. Too many results? Too few? Wrong kind of roles? Just tell Claude in plain English — *"skip anything over 3 years old"*, *"add Hitmarker as a source"* — and update your settings file to match so it sticks.

### Step 5 — Make it automatic (optional)
Ask Claude something like:

> **Turn this into a scheduled task that runs every weekday at 9am and emails/notifies me the results.**

Claude will set up the schedule if your plan supports it. You can change the timing any time — some people like once a week, others twice a day during an active search.

---

## 📊 Tracking your applications (optional)

Open **`3-JOB-TRACKER-TEMPLATE.xlsx`** in Excel, or upload it to Google Drive and open it with Google Sheets. It has four tabs:

| Tab | What goes there |
|---|---|
| **Open roles** | Jobs the scout found that you're considering |
| **Applied** | Jobs you've applied to, with date and status |
| **Archive** | Rejected, withdrawn, or expired roles — moved here so your main tabs stay clean |
| **Side gigs** | Part-time or non-industry work, if you're looking for that too |

Tell Claude when you apply to something (*"I applied to the Example Studio artist role today"*) and ask it to skip those in future digests.

---

## 🔧 Customizing

Everything lives in your settings file. Common tweaks:

- **Change how far back to look** — e.g. only roles posted in the last 14 days.
- **Add a "side gig" search** — part-time work near you in any field.
- **Add staffing / contract agencies** — they get their own highlighted section.
- **Ask for the hiring manager's name** — Claude includes it when it's publicly listed.

---

## ❓ FAQ & troubleshooting

**Is Claude actually applying to jobs for me?** No. It only finds and sorts listings. You review and apply yourself.

**It listed a job that's already closed.** Job boards don't always remove old posts. Add *"double-check the posting is still open"* to your settings, and always click through before applying.

**It's missing a studio I care about.** Add the studio's careers page link under *Must-check companies* in your settings.

**The match ratings seem off.** Make sure your resume is uploaded to the project, and add a line under *About me* describing what you're best at and what you're aiming for next.

**Is my resume shared with anyone?** Your files stay in your own Claude account. This kit contains **no** personal information — just templates.

**I found a bug / have an idea.** Open an *Issue* on this GitHub page, or share your improved settings with a friend!

---

## 📁 What's in this kit

```
job-scout/
├── README.md                     ← you are here
├── 1-MY-SEARCH-SETTINGS.md       ← fill this in
├── 2-THE-PROMPT.md               ← copy-paste into Claude
├── 3-JOB-TRACKER-TEMPLATE.xlsx   ← optional application tracker
├── examples/
│   ├── sample-settings-artist.md ← a filled-in example (3D artist)
│   └── sample-digest.md          ← what a digest looks like
├── guides/
│   └── sharing-on-github.md      ← how to post your own copy
└── LICENSE
```

---

Free to use, share, and remix (MIT License). Good luck out there — you've got this. 💛
