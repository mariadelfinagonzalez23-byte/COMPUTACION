---
name: research-synthesizer
description: Take multiple sources — articles, PDFs, transcripts, search results, reports — and produce a synthesized brief, executive summary, literature review, or decision memo. Use this skill whenever the user provides multiple sources and wants them combined into one output, or asks for research, a briefing, a literature review, a competitive intelligence report, or a summary across many inputs. Trigger on "research," "synthesize," "combine these sources," "write a brief," "executive summary of," or when given 3+ documents/links.
---

# Research Synthesizer

Take many inputs and produce one output that's clearer than any individual source. The value is in the synthesis — the connections, the contradictions, the weight of evidence — not in summarizing each source in turn.

## Step 1: Clarify the question

Before reading, establish:

1. **What's the question being answered?** — not the topic, the question
2. **Who's the audience?** — executive? team? investor? self?
3. **What decision or action does this inform?** — if any
4. **Desired length** — 1-page brief, 3-5 page report, detailed review
5. **Any sources to prioritize or exclude?**

A good research question is specific: "Should we launch in Germany before France?" beats "European expansion."

## Step 2: Read with intent

Read each source asking:

- What claim does this source make?
- What evidence does it rely on?
- Who is the source, and what's their bias or vantage?
- What does this add that other sources don't?
- Where does it conflict with other sources?

Don't just extract facts — extract positions. Note which sources agree and which disagree.

## Step 3: Synthesize, don't summarize

The difference matters:

- **Summary:** Source A says X. Source B says Y. Source C says Z.
- **Synthesis:** There's broad agreement that X, though A frames it as Y while B emphasizes Z. The key tension is between [perspective 1] and [perspective 2], with the evidence leaning toward [position] because [reasoning].

Always name the tensions. If all sources agree, say that clearly — but also note whether they're independent voices or echoing each other.

## Output formats

### Executive summary (1 page)
```markdown
# [Question or topic]

## Bottom line
[1-2 sentence answer]

## Key findings
- [Finding with 1-sentence support]
- [...]

## Areas of disagreement
- [Where sources diverge, and why it matters]

## Recommended next steps
- [Action 1]
- [Action 2]

## Sources
[List]
```

### Decision memo
```markdown
# [Decision to be made]

## Recommendation
[Clear recommendation]

## Reasoning
[2-3 paragraphs walking through the logic]

## Key evidence
- [Evidence point with source]

## Risks / counterarguments
- [What could make this wrong]

## What we still don't know
- [Open questions]
```

### Literature / competitive review (longer)
```markdown
# [Topic]

## Scope and method
[What was reviewed, how selected]

## The state of the conversation
[Synthesis of where the field / market / discourse stands]

## Key themes
### Theme 1
[Synthesis across sources, with citations]

### Theme 2
[...]

## Gaps and open questions
[What's underexplored]

## Implications
[What this means for the user's decision or project]

## Sources
[Full list with notes on each]
```

## Citation style

Inline. Short. Readable:

- "Gartner estimates X% of enterprises will do Y by 2028 [Gartner 2024]"
- "McKinsey argues the opposite [McKinsey 2023], pointing to Z."

Avoid academic-style bracketed numbers unless requested. Avoid footnotes in most cases.

## Writing rules

- **State the bottom line first.** Never bury it.
- **Use concrete numbers** where possible. "Most" and "many" are lazy.
- **Quote sparingly.** Paraphrase unless the exact phrasing carries the point. When you quote, keep it short — 10 words or less.
- **Flag your own inferences.** When you're connecting dots the sources didn't explicitly connect, say so: "This suggests..."
- **Distinguish strength of evidence.** "Three independent sources confirm" vs. "one vendor report claims."
- **Call out bias.** A vendor's white paper saying their product is best is not a neutral source.

## What to avoid

- The "one-paragraph-per-source" trap — that's not synthesis
- False balance — if the evidence overwhelmingly supports one side, say so
- Overconfident conclusions from thin evidence
- Including every data point — select for what matters
- Writing that reads like the user could've just skimmed the sources themselves

## Red flags when reading sources

- No methodology disclosed
- Sample sizes not stated
- Only one source behind a "widely reported" claim
- Vendor-sponsored "independent" research
- Dates missing — old data passing as current
- Correlational claims framed as causal

Flag these to the user. Don't silently launder weak sources into confident claims.

## Output completeness check

Before finishing, ask:
- Did I answer the question they actually asked?
- Would the user's decision be different based on this than without it?
- Is there anything important they'd be surprised I didn't mention?
