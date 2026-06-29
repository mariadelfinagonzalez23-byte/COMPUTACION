---
name: meeting-notes-processor
description: Turn raw meeting notes, transcripts, or voice memos into clean summaries with decisions, action items, owners, and deadlines. Use this skill whenever the user pastes meeting notes, shares a transcript, or asks you to summarize a meeting, extract action items, write follow-up emails from a meeting, or process a recording. Trigger on "meeting notes," "transcript," "action items," "summarize this meeting," "what did we decide," or when the user pastes raw meeting content.
---

# Meeting Notes Processor

Transform messy meeting input — transcripts, bullet dumps, Zoom recordings, voice memos, scrawled notes — into structured output people will actually use.

## Step 1: Assess the input

Identify what you've been given:

- **Transcript** — verbatim dialogue, often noisy and redundant
- **Bullet notes** — someone's live typing, incomplete sentences
- **Voice memo** — stream of consciousness, needs structure
- **Mixed** — some combination of the above

And ask (or infer) context:

1. **What kind of meeting?** — standup, 1:1, client call, strategy session, interview, brainstorm
2. **Who attended?** — if not obvious from the notes
3. **What's the output needed?** — internal summary, follow-up email, decision log, project plan update?

## Step 2: Extract the essentials

Pull these elements from the input:

### Decisions made
- What was explicitly agreed to
- Who owns the decision
- Any caveats or conditions

### Action items
Format each one as: **[Owner] will [specific action] by [deadline]**

If an owner or deadline is missing, flag it — don't invent one. Mark as "TBD" or "[needs owner]".

### Open questions
- Things raised but not resolved
- Questions that need input from someone not in the meeting
- Follow-ups to schedule

### Key discussion points
- The substantive content that's worth remembering — not the chitchat
- Tradeoffs discussed
- Context that explains why decisions were made

### Risks / concerns flagged
- Anything the group identified as a risk
- Who flagged it, what the concern is

## Output format

Use this template. Adjust for informal meetings (skip sections that don't apply):

```markdown
# [Meeting name] — [Date]

**Attendees:** [List]
**Length:** [If known]
**Purpose:** [One line]

## TL;DR
[2-3 sentence summary of what happened]

## Decisions
- [Decision + owner + any relevant context]
- ...

## Action items
| Owner | Action | Deadline |
|-------|--------|----------|
| [Name] | [Specific action] | [Date or "TBD"] |

## Discussion highlights
- [Substantive point]
- [Substantive point]

## Open questions
- [Question + who needs to answer]

## Risks / concerns
- [Risk + who flagged]

## Next steps
- [Next meeting, next milestone, or next check-in]
```

## If asked for a follow-up email

Different format. Something like:

```
Subject: [Meeting name] — recap + next steps

Hi all,

Thanks for the [meeting]. Quick recap:

**What we decided:**
- [Decisions in plain language]

**What's next:**
- [Owner] is [action] by [date]
- [Owner] is [action] by [date]

**Still open:**
- [Open question]

Let me know if I missed anything or got something wrong.

[Signature]
```

## Processing rules

- **Cut filler ruthlessly.** "Um," "like," "you know," throat-clearing openers — gone.
- **Attribute accurately.** If the transcript is clear about who said what, keep it. If it's ambiguous, use "the group" or "someone raised."
- **Don't invent.** If a deadline wasn't stated, say "[TBD]." If an owner wasn't named, flag it.
- **Preserve nuance.** If the group was split on something, don't flatten it into "we decided X."
- **Name the tension.** If two people disagreed, note it — often that's what the manager needs to see.

## What to avoid

- Paraphrasing quotes so much they lose meaning
- "John said he thinks maybe..." — just say "John suggested X"
- Overly corporate output ("The team synergized on key initiatives")
- Including every tangent — a team offsite transcript shouldn't summarize the lunch debate
- Drowning the signal in detail — if 90% of the meeting was filler, the summary should be short

## Edge cases

- **Very long transcripts (30+ min):** Offer to produce both a short summary (for leadership) and a detailed one (for the team).
- **Interviews:** Structure around the candidate's answers, not the questions. Group by theme.
- **1:1s:** Often more personal — ask the user if this is for them only or to share.
- **Client calls:** Output is usually a follow-up email + internal notes. Produce both if useful.
