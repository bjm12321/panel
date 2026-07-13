# Gig Triage Rubric

Instructions for a Claude session. The operator pastes a batch of freelance
job listings (title, description, budget, client stats) below or alongside
this file. Score every listing, then return the ranked shortlist. Be strict:
the operator has 2–5 hours a week, and a bad job costs more than no job.

## Step 1 — Hard disqualifiers (score 0, list under "Rejected")

Reject immediately if the listing:

- Requires live access to the client's accounts, credentials, servers, or
  admin panels (deliver files, never logins).
- Says "no AI" or "human-written only" in any form.
- Is generic content/blog writing, SEO article volume work, or a design
  contest.
- Is hourly with no fixed-scope option, or an open-ended "ongoing" role.
- Is a mobile app, or anything that can't be tested end-to-end in a session.
- Involves scraping targets where scraping is plainly prohibited or the data
  is personal/private — the client's legal exposure becomes the operator's.
- Budget under $30, or client has a payment method unverified + no hire
  history + no reviews (all three together).
- Smells like academic work, review manipulation, spam/bulk messaging, or
  anything deceptive.

## Step 2 — Score the survivors (0–10)

| Factor | Points | What to look for |
|--------|--------|------------------|
| Buildability | 0–3 | 3 = Claude can produce and *test* the entire deliverable in one session (script + sample data, static site, spreadsheet, doc). 1 = buildable but verification needs client resources. 0 = can't verify → reject. |
| Scope clarity | 0–2 | 2 = inputs, outputs, and "done" are explicit. 0 = "I have an idea, let's discuss" → cap total at 4. |
| Rate for effort | 0–3 | Estimate total operator minutes (proposal + review + delivery + messages). 3 = ≥ $2/operator-minute. 1 = ≥ $1. 0 = below → reject unless review-farming (Phase 1). |
| Client quality | 0–2 | 2 = payment verified, hires before, review ≥ 4.8, 0 = none of these. |

**Category priors** (tie-breakers, matching `PLAYBOOK.md`): automation/data >
landing pages > spreadsheets > technical writing.

## Step 3 — Output format

Return exactly this structure:

```
SHORTLIST (proposal-worthy, score ≥ 7; max 5)
1. [Title] — score X/10
   Deliverable: one sentence, concrete.
   Est. operator time: N min | Bid: $N (state Phase 1 or Phase 2 pricing)
   Risk to flag in proposal: one sentence, or "none".
   → Draft proposal attached (from freelance/proposals/<category>.md)

BORDERLINE (score 5–6, only if shortlist is thin)
- [Title] — score, one-line reason it's risky

REJECTED
- [Title] — disqualifier or score, five words max
```

Then draft a proposal for each shortlisted job using the matching template in
`freelance/proposals/`, filling every slot you can from the listing and
leaving `[[OPERATOR: ...]]` slots untouched for the operator.

## Step 4 — Tuning

The operator may paste tracker stats (proposals/wins per category). If a
category shows 0 wins after ~10 proposals, demote its prior; boost whatever
converts. Note the adjustment explicitly in your output so it can be folded
back into this file.
