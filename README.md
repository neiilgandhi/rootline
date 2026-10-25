# Rootline

**Money plans for immigrant families, from the first credit card to the kids' biggest milestones.**

Built at HackPSU Fall 2026 for the **FNB Challenge: Trust, Decisions & Financial Confidence**.

**Try it:** https://neiilgandhi.github.io/rootline/

---

## The problem

Immigrant families make big money decisions without guidance they can trust.

- **They start from zero.** Good credit from back home usually doesn't count in the U.S.
- **Advice is everywhere, and much of it is wrong.** Tips arrive through WhatsApp groups, relatives and social media. Scams target newcomers directly.
- **Kids often translate for their parents.** The CFPB found that many immigrant parents rely on their minor children to interpret financial transactions, which raises the risk of poor decisions.
- **Some deadlines are invisible until it's too late.** A child on an H-4 dependent visa is no longer eligible for H-4 at 21. Moving to student (F-1) status means the family must prove it can pay for up to a year of school. And F-1 students can't get federal student aid.

Existing tools help **one person get a credit card**. Nothing helps **a family see what's coming**.

## What Rootline does

| Tab | What it does |
|---|---|
| **1. Your family** | A few quick questions about the parent and each child. Never asks for Social Security numbers, account numbers or visa documents. |
| **2. Plan** | A step-by-step credit plan for the parent, "Do this month" actions, questions to ask any bank, a **safety fund calculator** for families whose visa depends on a job, **free tax help**, and a head start for each child as an authorized user. |
| **3. Kids' timeline** | Milestones for each child up to age 21: how visa status can change **what college costs**, **who can work to pay for it**, a **proof-of-funds tracker**, and a list of **questions to bring to an immigration attorney** so families pay less for legal help. |
| **4. Check advice** | Paste advice from WhatsApp, a relative or social media. Each claim gets a verdict (Supported, Not supported, Depends, Talk to an expert) with a source and "do this instead." |
| **5. Ask** | Questions answered only from checked sources, in English, Spanish, Hindi, Chinese or Vietnamese. |

## How trust is built in

- **Every claim links to its source.** 20 fact cards checked against the CFPB, IRS, SSA, FTC, DHS, USCIS, the Department of Justice, the Department of Education and the Federal Reserve. Non-government sources are labeled.
- **Confidence labels.** "Well-established" only when the source is official and has no caveat. Otherwise "Depends on your situation, please verify."
- **It says "I don't know."** If no source covers a question, Rootline says so and points to the right person.
- **No immigration advice.** Visa and status questions go to a licensed immigration attorney. Rootline covers only the money side.
- **No product pushing.** It never recommends a specific bank or card, including the challenge sponsor's.
- **No AI math.** The plan, timeline, savings tracker and safety fund calculator are plain rules in code. The same family always gets the same answer, and numbers are never made up.
- **Clear about privacy.** Answers are saved only in the browser, and savings amounts are never sent anywhere. On this public GitHub Pages site, nothing you type leaves your browser. In the Claude version, Check advice and Ask send the message (and, for Ask, a short family summary) to Claude, and the page says so.
- **AI answers are labeled.** Every live answer says it was written by Claude from our sources and asks you to open the source link before acting.

## How it works

- **One web page:** HTML, CSS and JavaScript, with no build step and no server.
- **Rules engine:** if-then logic builds the plan, the timeline and the savings math.
- **Fact cards:** [`sources.json`](sources.json) holds the 20 sources. A copy is built into the page.
- **AI (Claude):** the *Check advice* and *Ask* tabs send the question or message, a short family summary and the fact cards to Claude, with strict rules to cite sources and refuse legal questions. See [`system-prompt.md`](system-prompt.md).

**Live AI answers** work when the app is opened inside Claude while signed in. On this GitHub Pages copy, the example questions and messages show **saved example answers**, clearly labeled, written from the same sources.

## Run it

Open `index.html` in any web browser. That's it.

## Limits

- Rootline is a guide, not a lawyer, tax professional or financial advisor.
- Claude can still make mistakes, even with sources. Every answer links to its source so you can check it.
- Sources were checked on October 24, 2026. Rules change, so check the links before relying on them.
- Some card companies don't report authorized users under 18. Rootline tells families to ask their card company.
- Rootline is not affiliated with or endorsed by FNB or any bank.

## What's next

- Goal-specific plans (renting an apartment, financing a car) once we've checked sources for them.
- A shared view so parents and kids read the plan side by side in two languages.
- Optional, secure account connections so families can track savings automatically.
- More languages, reviewed by native speakers.

## Built with

HTML, CSS, JavaScript, and [Claude](https://claude.ai) by Anthropic. Claude helped research the sources and write the code.
