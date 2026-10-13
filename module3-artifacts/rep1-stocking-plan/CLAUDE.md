# Xavier University Bookstore

Shared context. Every agent in this folder reads this file. Anything specific to
one agent's job belongs in that agent's brief, not here.

## The store

One campus store at Xavier University. One buyer, no warehouse, no overflow
storage. We sell course materials in four forms — new copies, used copies bought
back from students, rental copies, and digital access codes — plus a small
amount of branded apparel.

Anything we order and do not sell sits on our floor until it is worthless, or
goes back to the publisher if that publisher takes returns. Not all of them do.

## The decision

What to order for **spring 2027**, title by title: which format, and how many.

- Publisher orders are committed **2026-12-12**.
- Spring classes begin **2027-01-12**.
- We do not know what students actually bought until **late January**, which is
  after most publisher return windows have closed.

Money committed in December cannot be recovered once a return window closes.

## The budget

**$26,000.00** for everything ordered for the spring term. The figure is firm
and there is no mid-semester supplement. Full memo in `data/budget.md`.

## The data

Everything is in `data/`. No agent reads all of it.

**Read only the files your own brief names under "The data you own." Do not open
any other file in `data/`, and do not read another agent's brief or another
agent's memo.** If your brief does not give you what you need to answer your
question, say so in your memo rather than going to look for it.

That rule is what makes the four of you independent. Break it and you are one
agent doing four jobs in one window.

| File | What it holds |
|---|---|
| `orders-fall.csv` | Every line item sold in fall 2026 |
| `enrollment-spring.csv` | Spring sections and projected seats, with fall seats alongside |
| `supplier-prices.csv` | Our cost, list price, format economics, and the publishers' terms |
| `returns-log.csv` | What came back last fall, why, and what it cost us |
| `budget.md` | What we have to spend |

## What a memo contains

Every analyst writes exactly one file to `findings/`, named after itself —
`findings/demand.md`, and so on. Every memo has four sections, in this order:

1. **Method.** The arithmetic, in one paragraph, so somebody can check it.
2. **Title by title.** A table covering every title. Never a summary only. Your
   own brief says what its rows and columns are.
3. **What matters most.** The three findings that would change the order.
4. **What you could not determine.** Say it plainly rather than estimating
   around it.

Write numbers, not adjectives. "Thin margin" is not a finding. "$47.49 a copy,
25%" is a finding.

## The agents

There are five of us and only one of us can delegate.

| | What it is | Can delegate? |
|---|---|---|
| **main agent** | the Claude Code session | **yes** |
| `demand` | `.claude/agents/demand.md` | no |
Look into how much demand there is for each class - use past data about enrollment and class size that you have available to make this information most accurate 

Trying to solve this "How many units will we sell in spring, in what format mix? The attach rate is the way in: units sold in fall over fall seats, applied to spring seats."
| `margin` | `.claude/agents/margin.md` | no |
Look to determine the margin between what we would purchase the book from wholesalers vs sell it for pull from data or other resources needed - this can be a little hypotchetical and not completely exact - but pretty close


| `risk` | `.claude/agents/risk.md` | no |
Determine the risk of ordering books for students in these classes

Trying to solve this "What could cost us money between the December order and the end of spring that nobody has priced in?"
| `planner` | `.claude/agents/planner.md` | no |


The three analysts do not depend on each other and can run at the same time.
`planner` must not run until all three memos exist in `findings/`, because the
memos are the only thing it is allowed to read.

## The job

You are the main agent. You do not analyse anything and you do not decide
anything. You dispatch, you wait, and you report what landed.

- **"Run the analysts."** Dispatch `demand`, `margin` and `risk`. Wait for all
  three. Then tell me which memos were written and nothing else — do not
  summarise them, the memos are the output.
- **"Build the plan."** Dispatch `planner`. If any of the three memos is missing
  from `findings/`, stop and say which one rather than running it short.

