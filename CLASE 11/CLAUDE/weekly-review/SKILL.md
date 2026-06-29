---
name: weekly-review
description: Run a structured weekly review — wins, blockers, priorities, lessons, and next week's plan. Use this skill whenever the user wants to do a weekly review, end-of-week reflection, weekly planning, week recap, team update, investor update, or any structured look-back-and-look-forward exercise. Trigger on "weekly review," "end of week," "review my week," "plan next week," "weekly update," or similar.
---

# Weekly Review

A weekly review is less about documenting what happened and more about noticing patterns, resetting priorities, and catching problems early. Keep it tight.

## Step 1: Gather the raw material

Ask the user (or pull from context if they've already shared):

1. **What got done this week?** — completed projects, shipped work, wins
2. **What didn't get done?** — things slipped, abandoned, or pushed
3. **What problems came up?** — blockers, surprises, things going sideways
4. **What's on next week's plate?** — commitments, deadlines, priorities
5. **Any numbers to track?** — revenue, leads, MRR, workouts, writing streak — whatever they measure

If they just say "do my weekly review" with no info, prompt them for a brain-dump first.

## Step 2: Structure the review

Use this skeleton. Adapt length based on the user's preference — some people want a one-page summary, others want more depth.

### Wins
- Concrete accomplishments, not activities. "Shipped the pricing update" not "worked on pricing."
- 3-7 items usually. If it's 15, help them consolidate.

### Misses / slips
- What didn't get done and why
- Distinguish between "ran out of time" and "wrong priority" and "blocked by someone else"

### Lessons
- 1-3 things learned or noticed
- Not platitudes — actual specific observations

### Numbers (if tracking)
- Key metrics with deltas from last week
- Flag any trending the wrong direction

### Next week's priorities
- 3-5 priorities, ranked
- Each one concrete enough to tell if it happened
- Flag any deadlines or dependencies

### Risks / things to watch
- Anything that might derail next week
- Decisions needed from others

### One-liner for the week
- A single sentence capturing what this week was about
- Useful for scrolling back later

## Formats by use case

### Personal weekly review (solo)
More reflective. Include:
- Energy check — what drained you, what energized you?
- What would you do differently if you could redo the week?

### Team update (sharing with manager or team)
More public-facing. Include:
- What shipped
- What's next
- Blockers you need help with
- Skip personal reflection

### Investor update (monthly usually, but applies)
Structured, numbers-forward:
- Top-line metrics
- Wins
- Lowlights / challenges (be honest — investors value this)
- Asks (intros, hires, feedback)

### Founder weekly review
Hybrid — mix metrics with reflection:
- Company metrics + personal energy
- What got built, what got sold, what got learned
- One thing to start, one to stop, one to continue

## Questions that force better reviews

If the user's answers are vague, use these to push:

- "What surprised you this week?"
- "What's something that didn't go as planned?"
- "If you could only work on one thing next week, what would it be?"
- "What should you be saying no to?"
- "What did you avoid this week that you shouldn't have?"

## What to avoid

- "Crushed it this week!" energy — overly positive reviews miss the point
- Padding with activities that don't connect to outcomes
- Priorities so vague they can't be checked ("work on strategy")
- Never noting lessons — which means no actual learning
- Making it so long the user won't reread it

## Output format

Use markdown with clear headers. Example:

```markdown
# Week of [date range]

## One-liner
[Single sentence]

## Wins
- [Concrete win]
- [Concrete win]

## Misses
- [What slipped] — [why]

## Lessons
- [Specific insight]

## Numbers
| Metric | This week | Last week | Δ |
|--------|-----------|-----------|---|
| [Metric] | [Value] | [Value] | [Delta] |

## Next week — priorities
1. [Priority + why it matters]
2. [...]
3. [...]

## Watch list
- [Risk or pending decision]
```

End with a short prompt for next week's first action: "The first move Monday morning is [X]."
