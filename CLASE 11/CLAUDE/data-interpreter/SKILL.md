---
name: data-interpreter
description: Analyze CSVs, spreadsheets, or tabular data and surface insights, patterns, anomalies, and suggested visualizations. Use this skill whenever the user shares a CSV, spreadsheet, Excel file, or data table and wants analysis, insights, "what does this tell me," trends, breakdowns, or charts. Trigger on "analyze this data," "what do you see," "find patterns," "CSV," "spreadsheet," or when the user uploads tabular data.
---

# Data Interpreter

Look at data the way a smart analyst would — structure first, then signal, then story. Don't just describe what's in the file; tell the user what's actually interesting.

## Step 1: Understand the context

Before diving in, ask or infer:

1. **What is this data?** — where did it come from, what does each row represent?
2. **What's the question?** — "what happened with Q3 sales" vs. "find outliers" vs. "just explore"
3. **Any known context?** — a launch, a price change, a seasonality pattern?
4. **What kind of output?** — a brief summary, a deep analysis, a dashboard-ready chart spec?

If the user just says "analyze this" — do a preliminary scan first, then suggest 2-3 threads worth pulling.

## Step 2: Structural scan

First pass, always:

- **Row count** — how many records?
- **Columns** — name, type (numeric, categorical, date, text), example values
- **Completeness** — any columns with missing data? how much?
- **Date range** — if there's a time dimension
- **Obvious anomalies** — negative revenue, dates in the future, impossibly large values

Flag any data quality issues before analyzing. Bad data → bad insights.

## Step 3: Generate hypotheses

Before computing, jot down what you expect to see. Then check if the data confirms or contradicts.

Useful lenses:

- **Trends over time** — is it growing, flat, declining, seasonal?
- **Distribution** — is there a long tail? bimodal? concentrated?
- **Segmentation** — how do groups differ? (by channel, product, region, cohort)
- **Correlations** — what moves together? (caveat: correlation ≠ causation)
- **Outliers** — individual rows or days that break the pattern
- **Ratios** — conversion rates, unit economics, per-capita figures

## Step 4: Analysis

For most business datasets, produce:

### Summary stats
- Total, mean, median, min, max for key numeric columns
- Counts and proportions for key categoricals
- Time range + completeness

### Key findings
- 3-5 substantive observations, each with a number to back it up
- Not: "There are 1,000 rows." That's a stat, not a finding.
- Yes: "Revenue grew 23% WoW for 4 weeks straight, then flattened — the flattening aligns with the July ad budget cut."

### Segment breakdowns
- Where relevant, break the data by the most meaningful dimension
- Show proportions, not just totals — a 10x difference in a 0.1% segment doesn't matter

### Anomalies
- Individual outlier rows
- Date ranges that look unusual
- Segments behaving differently from the rest

### Visualization suggestions
- For each key finding, suggest the right chart
- Simple rules:
  - Trends over time → line chart
  - Composition at a point in time → bar chart (not pie unless 2-3 segments)
  - Distribution → histogram
  - Relationship between two numerics → scatter
  - Segment comparison → small multiples (one chart per segment)

## Step 5: Tell the story

The difference between data and analysis is narrative. Organize findings as:

1. **Headline** — the single most important thing the data says
2. **Supporting findings** — 2-4 things that reinforce or qualify the headline
3. **What's surprising** — anything that broke your prior expectation
4. **What's missing** — data you'd want but don't have
5. **Next questions** — threads worth investigating further

## Writing rules

- Lead with the finding, then the evidence. Not the reverse.
- Use absolute numbers AND percentages. "Sales dropped 40% ($12K)."
- Specify the comparison. "Up 20%" from what?
- Distinguish signal from noise. A 2% change on a small sample isn't a trend.
- Name the limitation. "This is directional — the sample is small / the data is noisy / etc."

## What to avoid

- Drowning the user in stats with no hierarchy
- Generating charts for every column just because you can
- Declaring causation from correlation ("ad spend caused the increase")
- Ignoring base rates — 50% growth from 2 to 3 is not the same as from 1M to 1.5M
- Finding patterns in random noise (p-hacking)
- "The data shows an interesting trend" — be specific or cut it

## Red flags to raise with the user

- Duplicates in rows that should be unique
- Columns where "missing" means something different from "zero"
- Sudden step changes that look like tracking errors, not real events
- Sampling that makes totals misleading (e.g., incomplete weeks)
- Timezone issues in date columns
- Currency or unit mismatches

## Output format

Unless the user specifies otherwise:

```markdown
# Data analysis — [dataset name]

## TL;DR
[Headline finding in 1-2 sentences]

## What the data shows
1. **[Finding headline]** — [evidence with numbers]
2. **[Finding headline]** — [evidence with numbers]
3. ...

## Breakdown by [segment]
[Table or ranked list showing how segments differ]

## Anomalies
- [Outlier + what makes it unusual]

## Data quality notes
- [Any issues flagged]

## Suggested next steps
- [Questions worth investigating]
- [Charts worth building]

## Recommended visualizations
- [Chart 1 — what it shows, what columns to use]
- [Chart 2 — ...]
```

If the user wants the output in a specific format (slide, report, Notion doc), adapt accordingly.
