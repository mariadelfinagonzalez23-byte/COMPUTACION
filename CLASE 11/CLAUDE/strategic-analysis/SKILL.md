---
name: strategic-analysis
description: Run SWOT analyses, market analyses, Porter's five forces, 4Ps, or similar strategic frameworks on a business, product, or market. Use this skill whenever the user wants a SWOT, market analysis, competitive analysis at a market level, Porter's five forces, strategic overview, or any structured strategic assessment. Trigger on "SWOT," "market analysis," "Porter's," "strategic analysis," "industry overview," "assess this market," or "should I enter [market]."
---

# Strategic Analysis

Frameworks are tools, not outputs. The value comes from rigorous thinking within the framework — honest assessment, specific evidence, and clear implications. A "balanced" SWOT with 5 items per quadrant usually means nothing was actually analyzed.

## Step 1: Pick the right framework

Match the framework to the question:

- **SWOT** — for a single company, product, or decision; snapshot of internal + external factors
- **Porter's Five Forces** — industry-level attractiveness and competitive dynamics
- **PESTEL** — macro environment (political, economic, social, tech, environmental, legal)
- **4Ps (or 7Ps)** — marketing mix for a product or brand
- **BCG Matrix / GE Matrix** — portfolio decisions across multiple products
- **Value chain analysis** — internal activities and where value is created
- **Jobs-to-be-done** — user-centric: what job is the customer hiring the product for?

If the user asks for a SWOT but their real question is "should I enter this market?" — suggest the right framework instead of defaulting to SWOT.

## Step 2: Gather the inputs

Ask or gather:

1. **Subject** — the specific company, product, or market
2. **Context** — why this analysis, what decision it informs
3. **Time horizon** — current snapshot vs. 2-5 year outlook
4. **Sources available** — internal data, public info, interviews, all of the above?

## SWOT — done well

### Strengths (internal, positive)
- What the business does genuinely better than alternatives
- Specific, not generic — "strong brand" is lazy; "85% unaided brand recall in [segment]" is useful
- Must be defensible — if a competitor could replicate it in 6 months, it's not a strength

### Weaknesses (internal, negative)
- Be honest. If the user can't name real weaknesses, push them.
- Focus on weaknesses relative to competitors or to customer expectations
- Structural issues (cost base, team capability, tech debt) vs. fixable ones

### Opportunities (external, positive)
- Market trends, regulation, customer behavior shifts, tech enablers
- Not: "we could launch a new feature" — that's an initiative, not an opportunity
- Yes: "Aging population in [region] creates demand for [category]"

### Threats (external, negative)
- Competitor moves, platform risk, regulatory risk, market contraction
- Time-sensitivity matters — a threat 5 years out is different from one this quarter

### SWOT output format
Don't just list. Also generate:

- **TOWS crossover** — matching strengths to opportunities (offensive moves), weaknesses to threats (defensive moves)
- **Top 3 strategic priorities** — flowing from the analysis
- **Honest critique** — which quadrant has the weakest analysis and why?

## Porter's Five Forces — done well

Assess each force as **low / medium / high** with evidence:

1. **Threat of new entrants** — capital requirements, regulation, distribution, brand loyalty
2. **Bargaining power of suppliers** — concentration, switching costs, uniqueness
3. **Bargaining power of buyers** — concentration, alternatives, price sensitivity
4. **Threat of substitutes** — adjacent solutions, including "do nothing"
5. **Competitive rivalry** — number and similarity of competitors, industry growth, exit barriers

End with:
- **Industry attractiveness** — overall assessment
- **Where the power sits** — who captures the value in this industry, and why
- **Implications** — for someone in this industry, what does this mean?

## Market analysis — done well

For "should I enter this market" questions, cover:

### Market sizing
- TAM / SAM / SOM — with sources for each estimate
- Growth rate and trajectory
- Flag sizing assumptions (top-down vs. bottom-up)

### Customer segmentation
- Who are the buyers? Who are the users? (often different)
- Key segments, their size, and what they care about
- Underserved segments

### Competitive landscape
- Who's competing — direct, indirect, substitute
- Market share concentration
- Basis of competition (price, features, distribution, brand)

### Go-to-market reality
- Typical CAC and LTV
- Distribution channels that work
- Sales cycle length
- Barriers specific to this market

### Macro factors
- Regulatory environment
- Technology shifts
- Cultural / behavioral trends

### Recommendation
- Clear yes/no/conditional recommendation
- If yes — entry strategy and positioning
- If conditional — what needs to be true

## Writing rules

- **Be specific.** Numbers, examples, named competitors.
- **Flag your confidence.** Distinguish facts from educated guesses.
- **Honest over balanced.** If the analysis says "don't enter this market," say that. Don't find 3 opportunities to match 3 threats just for symmetry.
- **Actionable ending.** Every analysis should end with "so what?" — what should change based on this?

## What to avoid

- Generic bullet points that could apply to any company
- Padding to hit a format ("let me find a 5th weakness because the template asks for 5")
- Hiding weak analysis behind framework jargon
- Ignoring the strategic "enemy" — who's this analysis really about beating?
- Analysis paralysis — the point is a decision, not a document

## Output format

For each framework, produce:

1. **Executive summary** — the finding in 3-4 sentences
2. **The analysis itself** — using the framework
3. **Implications** — what this means strategically
4. **Priorities** — top 3-5 things to do (or not do) based on the analysis
5. **Open questions / assumptions** — what would change the answer

Use markdown tables for SWOT and Porter's. Use prose with clear headers for broader analyses.
