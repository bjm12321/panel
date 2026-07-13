# Freelance Playbook

Operating manual for making money on freelance marketplaces with Claude as the
production engine and you as the operator. Written to be re-read at the start
of any working session — by you or by a Claude session you paste it into.

## The model in one paragraph

You sell small, well-scoped digital deliverables on Upwork. You find and win
the work by hand (platforms ban scraping and auto-bidding — an account ban ends
the whole project). Claude does the triage and nearly all of the production.
Your 2–5 hours a week go to the only parts that must be human: searching,
personalizing proposals, submitting, client messages, and final review before
delivery. You are openly an AI-augmented builder — never claim otherwise.

## Ground rules (non-negotiable)

1. **No scraping or automated submission on any marketplace.** You paste
   listings into a session; Claude never touches the platform.
2. **Honesty about AI.** Profile and proposals describe you as using AI
   tooling. If a listing says "no AI," skip it — don't argue, don't sneak.
3. **Never take work requiring live access to client credentials or systems.**
   Deliver files, not logins.
4. **Review every deliverable yourself before sending.** You are the quality
   gate; "the AI did it" is never an excuse a client hears.
5. **No client names, dollar amounts, or personal data committed to this
   repo.** It serves a public page. Pipeline data lives in `tracker.html`'s
   localStorage on your device only.

## Platform setup (week 0, ~2 hours once)

1. Create an **Upwork** freelancer account. One platform only until the ramp
   milestone below — a fresh account spread across sites earns reviews nowhere.
2. Profile positioning: *"I build small automations, data-cleanup scripts,
   landing pages, and spreadsheet tools — fast, using modern AI-assisted
   development, with every deliverable personally tested before handoff."*
   Specific beats impressive. List the four categories below as skills.
3. Portfolio: build 2–3 sample pieces in Claude sessions before bidding
   (e.g., a CSV-cleanup script with README, a one-page site, a Sheets
   dashboard). Fresh accounts with visible work win against empty ones.
4. **Fiverr comes later**, at the ramp milestone — 2–3 productized gigs
   ("I will convert your CSV/Excel data into a clean report," etc.) as a
   passive storefront.

## What to sell (ranked by rate × win-odds × buildability)

| # | Category | Typical fixed price | Why it works |
|---|----------|--------------------|--------------|
| 1 | Small automation & data work — Python scripts, CSV/Excel cleanup, format conversion, API glue, scraping *for clients* | $50–300 | Highest $/effort; fully buildable and testable in a session |
| 2 | Landing pages, small static sites, site fixes | $75–400 | Delivered as files; buyers judge visible quality |
| 3 | Spreadsheet/Sheets automation & dashboards | $40–200 | Huge demand, few real devs competing |
| 4 | Technical writing — READMEs, API docs, how-tos | $30–150 | Lower rate but near-zero production cost |

**Do not bid on:** generic blog/content writing (AI-saturated race to the
bottom), logo/design contests, hourly engagements (blows the time budget),
mobile apps (testing/delivery overhead), anything touching client credentials,
and client-scraping jobs that target sites where scraping is plainly
prohibited or the data is personal — that's their legal exposure becoming
yours. See `TRIAGE.md` for the full red-flag list.

## Pricing ladder

- **Phase 1 — review farming (jobs 1–5):** bid $30–150, priced to win against
  established freelancers. Goal is five 5-star reviews and a 100% completion
  rate, not profit. Deliver fast (24–48h) — speed is the one axis where you
  outclass everyone.
- **Phase 2 — market rate (after 5 reviews):** move to the table prices above.
  Raise ~20% every 5 completed jobs while the win rate stays above ~15%.
- **Phase 3 — productize (after ~15 jobs):** open the Fiverr storefront with
  fixed-scope gigs derived from whatever category converted best in the
  tracker.

Never bid below $30 — sub-$30 buyers are the highest-maintenance segment on
every platform, and one bad review on a fresh account is catastrophic.

## The weekly loop (2–5 hours)

1. **Search (~30 min, you):** browse Upwork with saved searches for the four
   categories. Copy the full text of 10–20 plausible listings (title,
   description, budget, client stats) into one paste.
2. **Triage (Claude):** paste the batch into a session along with
   `TRIAGE.md`. Claude scores every listing and returns the top 3–5 with
   drafted proposals built from `proposals/`.
3. **Submit (~30 min, you):** personalize each draft — the template marks
   exactly which slots need you — and submit by hand. Log each as *Proposed*
   in the tracker.
4. **Build (Claude, on a win):** paste the client's spec into a session.
   Claude builds, you test against the acceptance checklist in the proposal,
   you deliver, you request the review. Move the card to *Delivered*, then
   *Paid*.
5. **Tune (5 min):** glance at the tracker's win rate. If a category has
   0 wins after ~10 proposals, drop it and rebalance toward what converts.

## Honest expectations

Month 1 is review farming: expect $100–400 total and treat it as buying a
sellable account. Months 2–3 at market rates and ~3 wins/week is roughly
$300–900/month within the 2–5 hr budget. Anyone promising more, faster, on a
zero-review account is selling something. The compounding asset is the review
history plus a tracker full of data about which gigs *you* actually win.

## Ramp milestones

- [ ] Upwork profile live with 3 portfolio pieces
- [ ] First proposal submitted
- [ ] First job won
- [ ] 5 reviews → switch to Phase 2 pricing
- [ ] 15 jobs → open Fiverr storefront (Phase 3)
