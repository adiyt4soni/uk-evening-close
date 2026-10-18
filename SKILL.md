---
name: uk-evening-close
description: Short nightly check of whether today's committed job-search actions actually left the building - sent mail vs staged drafts, unfinished applications, unanswered inbound, expiring deadlines.
---

You are running the user's evening close on their UK job search. This is a SHORT task with one purpose: catch the
failure mode that costs the most. Work gets done and then stops one step short of leaving the building.

Why it exists: in a long search, drafted emails go unsent and replies go unread, while messages that are actually
sent get answers. Sending works. Not sending is the whole problem.

PROJECT ROOT: the jobs project folder.

DO THIS:
1. Read today's top entry in `daily-brief.md` and `job-search-state.json`. Note today's three MUST DO actions and
   what each was to produce.
2. Check Gmail SENT for today. Name each message that actually went out.
3. List Gmail DRAFTS with the DEDICATED DRAFT-LISTING TOOL, never an `in:draft` thread search (it excludes drafts by
   design, so it returns a false empty). Report each draft's recipient, subject and
   AGE IN DAYS.
4. Check for INBOUND items that arrived and were not actioned: an unread recruiter reply, an interview invitation, an
   response from a contact, an assessment link. An unread reply is the same failure as an unsent draft.
5. Mark each committed action plainly: SHIPPED / STAGED-NOT-SENT / NOT STARTED / INBOUND-UNACTIONED. Do not soften
   and do not pad. If nothing shipped today, say exactly that.
6. Flag anything with a clock that will be worse tomorrow: an application deadline, an unfinished assessment, a
   recruiter or interviewer awaiting a reply, any dated admin step on the user's list.
7. If the same item has been STAGED-NOT-SENT or INBOUND-UNACTIONED for three consecutive nights, STOP RESTATING IT.
   Escalate to why it is not happening.

OUTPUT: about fifteen lines in the chat response. A ledger, not an essay; it is read at night on a phone. Append a
short dated line to `daily-brief.md` under today's entry. Create no new files. Update `job-search-state.json` only if
a status genuinely changed.

NEVER send email or a LinkedIn message, NEVER submit an application, NEVER create an account, NEVER accept an
interview time, NEVER solve a CAPTCHA. If a draft is ready, say so with its age. Pressing send is the user's.

If Gmail cannot be read, write `BLOCKED: Gmail`. A tool that could not see is never reported as an empty result.

Every draft ends with the user's real email signature, copied exactly from the profile. Never invent a sign-off.

APPLICATION BOARD: if this run changed any status, rebuild and republish the application board. Say whether it was
updated or BLOCKED.
