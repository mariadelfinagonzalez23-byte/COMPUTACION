---
name: inbox-triage
description: Process email or message backlogs — categorize messages by urgency and type, draft replies, identify what can be ignored, and suggest what needs a meeting vs. a quick response. Use this skill whenever the user pastes or shares multiple emails/messages and wants help processing them, or asks about inbox zero, clearing their inbox, prioritizing emails, or drafting replies to multiple messages at once. Trigger on "inbox," "triage," "clear my emails," "help me respond to these," or when the user pastes multiple messages.
---

# Inbox Triage

Help the user get through a pile of messages fast. Not every email needs a reply. Not every reply needs to be long. Sort, then act.

## Step 1: Understand the pile

Ask or infer:

1. **Channel** — email, Slack, LinkedIn messages, mixed?
2. **Time pressure** — is this "top 5 most urgent" or "clear everything"?
3. **Reply style** — the user's typical voice (casual, professional, terse)
4. **Any relationships to flag** — is the user's boss in this pile? Their biggest client?

## Step 2: Categorize each message

Use a simple 5-bucket system:

1. **URGENT — reply now** — time-sensitive, from someone important, or requires quick action
2. **REPLY — within 24-48h** — real ask, but not burning
3. **FYI — no reply needed** — informational, archive or file
4. **IGNORE — safe to delete** — newsletters, notifications, spammy cold outreach
5. **DELEGATE / SCHEDULE** — not a reply question, needs a meeting, or should go to someone else

For each message, assign a bucket and a one-line rationale.

## Step 3: For each REPLY / URGENT message

Draft a reply. Calibrate length to the relationship and the ask:

- **Quick yes/no:** one line
- **Simple question:** 1-3 sentences
- **Complex ask:** short response + suggest a call if genuinely needed
- **Political / sensitive:** careful draft, flag for user review before sending

Don't over-write. Most emails should be 1-4 sentences.

## Reply patterns

### Quick acknowledgment
> Got it, will do. Back to you by Friday.

### Polite decline
> Thanks for thinking of me — this isn't a fit right now, but appreciate you asking. Good luck with it.

### Need more info
> Can you send over [specific thing]? Hard to weigh in without seeing it.

### Redirect
> I'm not the right person — [Name] on our team handles this. Looping them in now.

### Schedule a call
> Easier to talk this through — got 15 min Tuesday or Wednesday afternoon?

### Set expectations / push back
> Appreciate the ask. Realistically, [X] won't be possible by [date]. Could do [alternative] instead — does that work?

## Voice rules

- Match the sender's tone — don't be formal when they're casual, or vice versa
- Cut "I hope this email finds you well" and similar filler
- Don't apologize for normal response times
- First person, direct, no throat-clearing
- Sign off naturally — "Thanks," "Best," or just their name

## Special categories

### Cold outreach you're not interested in
Default: don't reply. Ignoring is kinder than "Not interested, please remove me" (which signals your inbox is active).

If it's borderline: "Not a fit right now — thanks for reaching out." Two sentences max.

### Newsletters / promotional
Unsubscribe or archive. Don't reply unless you actually want to engage.

### Internal team messages
Usually shorter and more casual. Match the team's norms.

### Anything from a VIP (boss, key client, investor)
Flag for the user — even if it looks routine, they should eyeball it before you send.

## Output format

Deliver a triage summary, then the drafts:

```
## Triage summary
| # | From | Subject | Bucket | Note |
|---|------|---------|--------|------|
| 1 | [Sender] | [Subject] | URGENT | [One-line reasoning] |
| 2 | ... | ... | ... | ... |

## Drafts

### #1 — Reply to [Sender]
[Draft]

### #3 — Reply to [Sender]
[Draft]

(etc.)

## Recommend you ignore
- #2, #5, #7 — [one-line reasoning each]

## Recommend you delegate / schedule
- #4 — Book a call, don't try to resolve via email
- #6 — Forward to [team member]
```

## What to avoid

- Drafting replies to every message just to be thorough
- Generic responses that feel templated
- Over-apologizing for delays
- Committing the user to things without flagging ("Happy to hop on a call whenever" — not unless they asked you to say that)
- Revealing private info in replies without confirming

## When to ask before drafting

- Messages involving money, contracts, or legal stakes
- Emotionally charged messages (conflict, grief, firings)
- Anything where the user's relationship with the sender is complicated
