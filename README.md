# UK evening close

A short nightly check that catches the most expensive failure in a job search: work that gets done and then never actually gets sent.

**Type:** Claude scheduled task · **Area:** Job search automation

## What it does

- Reads the day's three committed actions from the morning brief.
- Checks sent mail, lists real drafts with their age in days, and looks for inbound replies nobody answered.
- Marks each action SHIPPED / STAGED-NOT-SENT / NOT STARTED / INBOUND-UNACTIONED and flags anything with a clock.
- After three nights of the same stall, it stops repeating the item and asks why it isn't happening.

## Guardrails

- Never sends, submits or accepts anything. Pressing send stays with the user.
- Uses the dedicated draft-listing tool, because a draft search excludes drafts by design.

## When it triggers

> Short nightly check of whether today's committed job-search actions actually left the building - sent mail vs staged drafts, unfinished applications, unanswered inbound, expiring deadlines.

## What's in this repo

- `SKILL.md`: the skill itself, the file Claude or Codex reads.
- Not included: Project files are personal and not published.
- Written to be generic: where the skill relies on the user's own files, it names them by role, not by content.

## Install

This is a Claude scheduled-task prompt. Create a scheduled task in the Claude desktop app and paste the body of `SKILL.md` as its prompt, or save it as `~/.claude/scheduled-tasks/uk-evening-close/SKILL.md`. It expects the project files it names to exist.
