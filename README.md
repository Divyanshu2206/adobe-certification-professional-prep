# Marketo Engage Business Practitioner — Professional (AD0-E555) Study Guide

A single-page, source-verified study guide for the **Adobe Marketo Engage Business Practitioner Professional** certification, organised exactly like the official exam blueprint.

Every factual claim was researched against [Adobe Experience League](https://experienceleague.adobe.com/en/docs/marketo/using/home) product documentation and then fact-checked a second time, claim by claim. The handful of "facts" that circulate in the community but that Adobe does **not** actually document are flagged as unverified rather than repeated as truth.

**[→ Read the guide](https://YOUR-USERNAME.github.io/YOUR-REPO/)**

> Replace that link with your GitHub Pages URL after enabling Pages (see [Hosting](#hosting)).

---

## Contents

- [Which exam is this?](#which-exam-is-this)
- [What's covered](#whats-covered)
- [What's inside](#whats-inside)
- [How this was built](#how-this-was-built)
- [What this guide deliberately does not assert](#what-this-guide-deliberately-does-not-assert)
- [What this is not](#what-this-is-not)
- [Using it](#using-it)
- [Hosting](#hosting)
- [Contributing](#contributing)
- [Disclaimer](#disclaimer)
- [License](#license)

---

## Which exam is this?

**AD0-E555 — Adobe Marketo Engage Business Practitioner Professional.**

⚠️ **Do not confuse this with AD0-E559**, the *Expert* exam. It is a different certification with a completely different blueprint (Administration 12% / Marketing Activities 46% / Lead Management 12% / Data Management 10% / Reporting 4%). A large share of "Marketo certification practice questions" you'll find online are for E559 and will send you down the wrong path.

### Exam logistics

| | |
|---|---|
| Questions | 55 |
| Passing score | 36 of 55 |
| Duration | 110 minutes |
| Fee | $95 (+Taxes) USD |
| Format | Multiple choice |

> **Sourcing note:** these logistics come from third-party certification study sites, **not** from Adobe directly. Verify them on [certification.adobe.com](https://certification.adobe.com) before you book — Adobe changes exam parameters without notice.

---

## What's covered

All **36 blueprint items** across the four official sections, each with its own subsection:

| Section | Weight | Items |
|---|---|---|
| 1 · Building and managing programs | **39%** | 14 |
| 2 · Building assets | **19%** | 7 |
| 3 · Defining and targeting audiences | **33%** | 12 |
| 4 · Analyzing and building reports | **9%** | 3 |
| 5 · Beyond the blueprint | — | 5 |

Section 5 is not part of the official blueprint. It covers topics that practice questions keep hitting but the blueprint wording doesn't surface — notifying or copying a third party on an email (Email CC vs BCC vs Send Alert vs Interesting Moments vs subscriptions), a business-question-to-report decision table, month-over-month and period comparison, report time frames and grouping, and why two reports legitimately disagree with each other.

---

## What's inside

- **Plain-language explanations** of every blueprint item, written for someone learning the concept, not reviewing it
- **Exact UI click paths** — `Admin → Communication Limits → Edit` — because this exam rewards muscle memory of the interface
- **Simplified UI mocks** of the screens that matter (channel setup, communication limits, program Setup canvas, engagement streams, smart list filters, the trigger/filter evaluation flow). Real product screenshots aren't included for copyright reasons; the mocks reproduce the field names and labels the questions key off
- **Exam traps** — documented behaviours that contradict intuition, called out inline
- **Every number in one table** — all the limits, windows and defaults in a single sheet you can cover and recite
- **The 26 confusions** — pairs the exam is built to exploit, each with a one-line difference
- **52 flashcards** — click to flip
- **30 practice questions** with worked explanations
- **A two-week study plan** weighted to the 39/19/33/9 split

The guide is a **single self-contained HTML file**. No build step, no dependencies, no tracking. It works offline apart from the web font, which degrades gracefully to a system stack. It is theme-aware (light/dark) and prints cleanly — **printing or saving as PDF reveals every flashcard and practice answer automatically**, which is useful for studying away from a screen.

---

## How this was built

Transparency matters here, because the guide's whole value proposition is that you can trust the numbers.

1. **Research.** Each blueprint section was researched against Adobe Experience League product documentation, supplemented by Adobe's KCS knowledge base and the Experience League / Marketing Nation communities only where the product docs are silent.
2. **Verification.** The highest-risk claims — limits, retention windows, metric formulas, clone behaviour, scheduling lead times — were then re-checked individually against official Adobe pages, requiring a direct supporting quote.
3. **Correction.** That pass caught real errors. Two examples that made it into the guide as corrections:
   - The widely repeated claim that *Email Delivered* and *Send Email* are 90-day "high-volume" activities is **not** supported by Adobe's current data-retention table, which places email reports under the 25-month policy and names only Web Page Activity and Company Web Activity as 90-day.
   - *Cost per Member*, *Cost per New Name* and *Cost per Success* are real documented metrics, but they belong to the **Program Cost Analysis area in Revenue Cycle Analytics** — not to the basic Program Performance report, which documents Channel, New Names, Success and Total Cost.

This guide was researched and written with AI assistance (Claude), with a separate verification pass over every high-risk claim. That's worth knowing when you calibrate how much to trust it: the sourcing is real and checkable, and every contested claim carries a flag — but it is not a substitute for Adobe's own documentation, which is linked throughout.

---

## What this guide deliberately does not assert

These circulate widely and are **not** supported by official Adobe documentation. They're flagged inline in the guide, and collected in its Sources section. Know the community answer, but don't build a rule on it:

| Claim | Status |
|---|---|
| Operational channels are hidden from the Marketing Calendar | The Normal/Inclusive/Operational **reporting** behaviour is documented; the calendar claim is not |
| A maximum number of triggers per smart campaign | No maximum documented. Multiple triggers are explicitly supported, OR'd together |
| A maximum number of flow steps per campaign | No maximum documented. "~50" is community anecdote about UI performance |
| "Approved with Draft" sends the approved version | Universally accepted and follows from the documented approval model, but not stated in one quotable Adobe sentence |
| A fixed MQL score threshold | Adobe publishes none. Inherently organisation-specific |
| Native double opt-in | Not a shipped feature. It's a pattern you build |
| An "Anonymize Person" flow step | Does not exist. It's a community feature request |
| A unified "Admin → Privacy" GDPR panel | Not a discrete UI area. Privacy settings are spread across Munchkin, Web Personalization and the mailability fields |
| `Open Rate = unique opens ÷ delivered`, `Click Rate = clicks ÷ delivered` | Industry standard, but not found as official Marketo definitions. **Click-to-Open** *is* documented |
| A "Spam Complaints" report metric | Not found as a labelled column or KPI |
| Email Performance cannot group by time period | Strongly evidenced by the total absence of the feature across every page describing it — but inferred, not quoted |
| Report subscription frequency options | The dropdown is documented; its enumerated values are not |
| Bulk API import file size limit (~10 MB) | Community-sourced. The **100 MB UI import limit** is well documented |
| Blackout dates as a Schedule-tab feature | Not native. Built with filters or suppression lists |

---

## What this is not

**This repository contains no exam dumps and no real exam questions.**

The 30 practice questions were written from the blueprint and from Adobe's documentation. They are not drawn from any question bank, and nobody involved has seen the live exam. They are useful for finding gaps in your understanding; they will **not** predict your score, and their section balance is deliberately weighted for learning rather than simulation.

If you come across sites selling "actual AD0-E555 questions" — please don't. Using them breaches Adobe's certification agreement and is grounds for revoking a credential you've paid for and earned.

---

## Using it

**Read it online** via the GitHub Pages link at the top, or:

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPO.git
cd YOUR-REPO
open index.html          # macOS
# xdg-open index.html    # Linux
# start index.html       # Windows
```

That's the whole setup. One file, no dependencies.

**Suggested approach**, if you're starting from zero:

1. Read *Start here* and the vocabulary table before anything else — most wrong answers come from blurring two terms.
2. Work through the sections in blueprint order, in weighted proportion. Sections 1 and 3 are 72% of the exam.
3. Build things in a real Marketo instance or sandbox. The difference between reading that the Schedule tab has Qualification Rules and having clicked *Edit Settings* is worth several marks.
4. Finish on the numbers table, the confusions, and the practice questions cold.

The guide includes a two-week plan built around exactly this.

---

## Hosting

To publish your fork with GitHub Pages:

1. **Settings → Pages**
2. **Source:** Deploy from a branch
3. **Branch:** `main`, folder `/ (root)`
4. Save. Your guide will be live at `https://YOUR-USERNAME.github.io/YOUR-REPO/` within a minute or two.

`index.html` is already named for root-level Pages hosting.

### Repository structure

```
.
├── index.html    # the complete guide — single self-contained file
├── README.md
└── LICENSE
```

---

## Contributing

Corrections are genuinely welcome — especially ones that make the guide *more* rigorous.

**Please include a source.** A pull request that changes a factual claim should link the Experience League page that supports it, ideally with the supporting sentence quoted in the PR description. Claims sourced only to community posts are fine, but should be labelled as such using the existing `Not documented` callout style rather than presented as fact.

Particularly useful contributions:

- Adobe documentation that **resolves** one of the unverified items in the table above, in either direction
- Blueprint changes, if Adobe re-weights or revises the exam guide
- Product changes that make something here stale — Marketo's UI and limits do move
- Additional exam traps you hit in practice, with the documentation that explains them

Please don't submit real or recalled exam questions. They'll be declined.

---

## Disclaimer

This is an **independent, unofficial** study resource. It is not affiliated with, authorised by, endorsed by, or sponsored by Adobe Inc.

*Adobe*, *Marketo*, and *Marketo Engage* are trademarks of Adobe Inc. All product names, logos and brands are the property of their respective owners and are used here for identification only.

Content is derived from publicly available Adobe documentation. Factual information (limits, behaviours, click paths) is not itself copyrightable; the explanations, tables, mocks, questions and structure in this guide are original work.

Adobe revises certification blueprints and product behaviour periodically. **Always verify against the current official exam guide at [certification.adobe.com](https://certification.adobe.com) and the live [Experience League documentation](https://experienceleague.adobe.com/en/docs/marketo/using/home) before relying on anything here.** No guarantee is made as to accuracy, currency, or exam outcome.

---

## License

> **Choose one before publishing.** Two sensible options for a study guide:
>
> - **[CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)** — others may share and adapt, including commercially, provided they credit you and license derivatives the same way. Best fit for prose/educational content, and keeps improvements open.
> - **[MIT](https://opensource.org/license/mit)** — maximally permissive, familiar to developers, but designed for code rather than writing.
>
> Add your chosen text as `LICENSE` and replace this block.
