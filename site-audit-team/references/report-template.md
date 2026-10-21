# CEO report - <project name>

**To:** the website owner · **From:** the CEO, site audit team
**Date:** <YYYY-MM-DD> · **Branch:** `site-audit/<date>` · **Mode:** audit + fix | audit only
**Teams run:** UX, FE, BE, SEC, PERF (note any skipped, and why)
**Status:** READY | BLOCKED

## Bottom line

2-4 sentences in plain language: how healthy the site is now compared with before, the most important thing we fixed, and the most important thing still waiting on you.

## Health scorecard - before → after

| Area | Before | After | Why (one line) |
|------|--------|-------|----------------|
| Design & usability | At risk / Needs work / Good | ... | ... |
| Accessibility | | | |
| Frontend | | | |
| Backend & data | | | |
| Security | | | |
| Performance | | | |
| SEO | | | |

**Build / tests / lint, before → after:** e.g. `tests 41/45 → 47/47 passing`, `lint 23 errors → 0`

## By the numbers

| Team | Found | Confirmed | Fixed & accepted | Needs you | Rejected (false alarms) |
|------|------:|----------:|-----------------:|----------:|------------------------:|
| UX   |       |           |                  |           |                         |
| FE   |       |           |                  |           |                         |
| BE   |       |           |                  |           |                         |
| SEC  |       |           |                  |           |                         |
| PERF |       |           |                  |           |                         |

## What we fixed

Grouped by priority (P0 → P3), one line each, in plain words:
`what was wrong → what changed` (IDs, commit `<sha>`)

## What I need from you

A numbered list of needs-human items. For each: what it is, why we didn't fix it ourselves, and the exact next step.
**Put leaked secrets first, with the instruction to rotate the key at the provider: deleting it from the code isn't enough.**

## Still open

Confirmed medium and low items left for later, one line each.

## How much you can trust this

- Verdicts I spot-checked per team, and how many I overturned
- Supervisor ratings: TRUSTED / needed rework (and what changed)
- Fix acceptances I re-checked
- What we couldn't check, and why (no running server, no test data, etc.)
- Uncertain items, and what would settle each one

## How to review and undo

- See every change: `git log --oneline <base>..site-audit/<date>` and `git diff <base>...site-audit/<date>`
- Undo one fix: `git revert <sha>`
- Throw everything away: `git checkout <base>` and delete the branch
- Nothing was pushed or deployed.

Detailed files: `.site-audit/ceo/briefing.md`, `.site-audit/plan.md`, `.site-audit/verified/`, `.site-audit/findings/`, `.site-audit/fixes/`.
