# Onboarding Follow-Up Playbook

One rule of thumb behind all of this: match the message to the cause, not the calendar. A confused person and a busy person both go quiet — they need different messages, not just a later timestamp.

## The flow

| Situation | Wait | Send | If they respond | If still nothing |
|---|---|---|---|---|
| Just sent the link | Immediately | "Go for it! I'll check in [specific day] — tag me sooner if you get stuck." (Locks a checkpoint even if they self-start — don't push a live session if they don't want one.) | Move to next row on their check-in day | Send the 48h nudge below |
| No reply, 24–48h | 48h | "Did the doc make sense, or did it choke on something?" | They're engaged, go to whichever row fits (signed in / stuck / started) | Wait to day 5, send the "do it live" offer |
| Signed in but did nothing (same day) | Hours, not days | Skip the question — hand them one action: "Next step is just [X], takes 30 sec. Want me to do it with you real quick?" | Walk them through that one step live | Treat as confusion, not priority — repeat with an even smaller single action, don't just re-ping |
| Started, then stalled 3+ days | 3 days | Reference exactly where they stopped: "Looked like you got through [X] — anything block you on [Y]?" | Fix the specific blocker directly | Move to Silent |
| No reply anywhere, 10+ days | 10 days | Final, low-pressure: "Totally fine if it's not the moment — I'll leave it here. Shout if it becomes useful later." | If interested, restart at the row that fits; if "not now," mark Revisit-later with their timeframe | Mark Cold, stop outreach |

## Two calls you make by judgment, not timer

- Deflection twice in a row ("busy," vague) → ask directly: "Is this just bad timing, or does it not seem useful for what you're doing? Either's fine, just don't want to keep bugging you." → answer decides Cold vs. Revisit-later.
- Same blank-canvas freeze happening across several people → stop treating it as a follow-up problem. It's a gap in the getting-started flow itself — fix that upstream instead of messaging around it.

## Ground rules

- 3 outbound touches max before someone is Cold or Revisit-later — more reads as pressure.
- Confusion gets an action, not a question. Priority gets a check-in, not more instructions.
- Automate the "who's due today" tracking. Keep the actual message and the Cold/Revisit-later call manual — that part needs judgment.
- Channel updates: email and WhatsApp both feed status; never let an email sync overwrite a manual WhatsApp note — most recent timestamp wins if they conflict.

---

## Applying this automatically

*Support section. The playbook above is the authority; this only maps the labels
the tracking produces onto the rows above, so automated reminders can point at
the right row. It adds no new advice.*

Activation is measured as **content added**, not sign-in — signing in is not
starting. The automated status labels resolve as follows:

| Automated label | Meaning | Row above |
|---|---|---|
| `too_early` | Account under 3 days old | *Just sent the link* — checkpoint only, no nudge yet |
| `never_started` | Account exists, never signed in | *No reply, 24–48h* → then the day-5 "do it live" offer |
| `logged_in_no_content` | Signed in, added nothing | *Signed in but did nothing* — hand them one 30-second action, live. Not a re-sent link: they have it and it did not help |
| `went_quiet` | Added something, silent 14+ days | *Started, then stalled* — reference where they stopped |
| `active` | Adding content recently | No row. Leave them alone |

Where a person's situation matches no row, say so rather than improvising one.

A note on evidence: an empty inbox is evidence about **one channel**, not about
the relationship. Never conclude "they did not respond" from a source that only
sees email — say "no reply on this channel since &lt;date&gt;" and check the others
before acting.

## Related

- [Getting-started onboarding guide](getting-started.md) — the first session.
- [Conversation-history use-case playbook](onboarding.md) — finding a first folder worth creating.
- [Live demo guide](demo-guide.md) — everything before the account exists.
- [Setup links and interface guide](setup-links.md) — what to send when the blocker is a missing connection.
