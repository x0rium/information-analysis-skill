---
name: information-analysis
description: Use when turning messy, incomplete, contradictory, or source-heavy information into a grounded analytical question, evidence map, competing hypotheses, uncertainty-aware conclusion, recommendation, briefing, or update protocol. Based on the Russian textbook “Аналитика как метод обработки информации”.
version: 1.1.0
author: analytics-textbook-ru / Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [analysis, information, uncertainty, hypotheses, sources, evidence, briefing, russian]
    related_skills: [write-native-russian]
---

# Information Analysis

## Overview

Use this skill to do disciplined information analysis, not just summarize material. The goal is to convert scattered data, observations, documents, claims, signals, and opinions into a conclusion that answers a clear question, shows its grounds, names uncertainty, and says what would change the answer.

Core cycle:

```text
question → context → sources → facts → hypotheses → checks → alternatives → uncertainty → conclusion → decision → revision
```

The skill is based on the textbook `analytics-textbook-ru`. It is deliberately practical: every analytical move should help the user decide what to believe, what to check next, what to do, or how strongly to trust a conclusion.

## When to Use

Use this when the user asks to:

- analyze a situation, market, product issue, organization, incident, source set, trend, or decision;
- turn a broad topic into a useful analytical question;
- evaluate sources, claims, evidence, rumors, reports, interviews, metrics, or conflicting accounts;
- compare explanations instead of defending one favorite version;
- produce an analytical note, briefing, recommendation, risk/unknowns map, scenario analysis, or decision memo;
- review another analysis for weak reasoning, hidden assumptions, overconfidence, or missing alternatives;
- update a previous conclusion after new information appears.

Do not use this as a substitute for domain-specific expertise where the task is primarily legal, medical, financial, engineering, statistical, or scientific calculation. In those cases, use this skill for reasoning structure and source discipline, then combine it with the relevant domain skill/tool.

## Non-Negotiable Principles

1. **A topic is not a question.** “Customer churn” is a territory. “Which two causes best explain the churn increase in SMB customers since March, and what should we check before changing onboarding?” is a question.
2. **Data is not a conclusion.** Tables, quotes, charts, links, and screenshots are material. Analysis starts when you say what they support, what they do not support, and what could change the interpretation.
3. **A hypothesis is not a conclusion.** First plausible explanations must compete with alternatives before becoming a working conclusion.
4. **Source quality is relative to a claim.** A source can be strong for one fact and weak for another. Judge proximity, freshness, completeness, independence, incentives, and verifiability.
5. **Uncertainty must be actionable.** Do not write “more data needed” unless you name which data, where to get it, what it would change, and what to do if it cannot be obtained.
6. **Recommendations cannot be stronger than conclusions.** If confidence is medium and key assumptions are weak, recommend a bounded test or reversible action, not a full irreversible move.
7. **Revision is part of analysis.** A good conclusion includes conditions under which it should be updated.

## Method Core

Analysis is controlled movement between claim types:

```text
source → claim → evidence → inference → hypothesis → conclusion → recommendation → revision
```

Do not jump from information to action. Each transition must be explicit enough to be checked.

### Valid analytical transitions

- **Source → claim:** use a source only for what it can know.
- **Claim → evidence:** a claim becomes evidence only relative to a question.
- **Evidence → inference:** state what follows and what does not follow.
- **Inference → hypothesis:** a hypothesis needs mechanism, expected signs, and weakening conditions.
- **Hypothesis → conclusion:** choose only after comparing real alternatives on shared evidence.
- **Conclusion → recommendation:** action strength must match confidence, cost of error, and reversibility.
- **New information → revision:** update the affected part of the chain; do not restart or overreact by default.

Central distinctions:

```text
information ≠ evidence
evidence ≠ fact
fact ≠ explanation
explanation ≠ conclusion
conclusion ≠ action
```

Use the method references when a task needs deeper control of reasoning:

- `references/method-core.md` — analytical objects, valid transitions, and operations.
- `references/evidence-and-confidence.md` — diagnosticity, evidence matrices, and confidence rules.
- `references/decision-and-revision.md` — coupling conclusions to action and updating conclusions after new information.

## Quick Mode Selector

Pick the smallest mode that fits the user’s request.

| User need | Use this mode | Output |
|---|---|---|
| “What is going on?” | Situation triage | question, 2–4 hypotheses, evidence gaps, next check |
| “Which explanation is right?” | Competing hypotheses | hypothesis/evidence matrix, diagnostic evidence, provisional conclusion |
| “Can we trust this?” | Source/evidence review | source map, fact/interpretation split, confidence limits |
| “What should we do?” | Decision support | conclusion, confidence, recommendation, assumptions, stop/revise conditions |
| “Write a note/briefing” | Analytical communication | concise memo with grounds, uncertainty, alternatives, next action |
| “New info arrived” | Update protocol | what changed, what did not, confidence shift, revised conclusion |
| “Review this analysis” | Red-team review | weak points, hidden assumptions, missing alternatives, fixes |

## Standard Workflow

### 1. Name the analytical question

Before collecting or summarizing, write the working question.

Minimum fields:

```text
Topic:
Decision or use:
Audience:
Working question:
Boundaries:
What would count as a sufficient answer:
```

Good question shapes:

- **Diagnostic:** What best explains X, and how can we distinguish the top explanations?
- **Prognostic:** Which outcomes are plausible over timeframe T, and what early signals distinguish them?
- **Decision:** Which action is most justified under current evidence, and what assumptions does it depend on?
- **Comparative:** Which option is stronger for goal G under constraints C?
- **Descriptive:** What is actually happening, after separating facts from interpretations?

Reject loaded questions. If the question already contains the answer, rewrite it neutrally.

### 2. Build context and boundaries

Name only context that changes the meaning of facts or the strength of the conclusion.

Check:

- object, segment, geography, period;
- decision deadline and reversibility;
- stakeholders and incentives;
- baseline for comparison;
- cost of being wrong;
- what is explicitly outside scope.

### 3. Map sources before trusting claims

For each important source, record:

```text
Source:
What it literally says:
How it knows:
Freshness:
Completeness:
Independence:
Possible incentives/distortions:
What it can support:
What it cannot prove:
Role in analysis: ground / signal / context / hypothesis / weak hint
```

Do not add dependent sources as independent confirmations. If three articles repeat one original report, count the original report once.

### 4. Separate facts, interpretations, assumptions, hypotheses, and conclusions

Use this classification:

| Type | Meaning | Test question |
|---|---|---|
| Observation | Something noticed or reported | Who saw/measured it and when? |
| Data | Recorded material | How was it collected and bounded? |
| Fact | Working claim sufficiently supported for this task | What are its limits? |
| Interpretation | What a fact might mean | What else could it mean? |
| Assumption | Temporarily accepted condition | What happens if it fails? |
| Hypothesis | Testable explanation or answer | What would we expect to see? |
| Conclusion | Best current answer to the question | Why this answer over alternatives? |
| Recommendation | Action implied by the conclusion | Is it proportional to confidence? |

When reviewing text, mark where the author jumps from one type to another without support.

### 5. Generate competing hypotheses

For diagnostic/explanatory tasks, create 3–5 hypotheses with different mechanisms.

Weak set:

```text
H1: Sales team is weak.
H2: Sales work is poor.
H3: Managers sell badly.
```

Strong set:

```text
H1: Lead quality fell in the new channel.
H2: Sales response time increased.
H3: Price became less competitive in one segment.
H4: Product fit changed because buyer needs shifted.
```

For each hypothesis, write:

```text
Mechanism:
Expected signs if true:
Evidence that would weaken it:
First check that distinguishes it from alternatives:
```

### 6. Compare hypotheses on the same evidence

Do not build a separate evidence list for each favorite hypothesis. Use one evidence set and test every hypothesis against it.

Marks:

```text
+  supports / expected
-  weakens / contradicts
0  neutral
≈  compatible with many hypotheses, weakly diagnostic
?  insufficient data
```

Look especially for:

- diagnostic evidence: distinguishes versions;
- contradictions: facts poorly compatible with a version;
- absence of expected signs;
- evidence that supports several hypotheses and therefore should not choose between them.

Do not count plus signs mechanically. One strong contradiction can matter more than five weak confirmations.

### 7. Map unknowns and uncertainty

Write unknowns as exact missing elements, not fog.

Bad:

```text
Need more data.
```

Good:

```text
Unknown: whether churn rose equally in old and new acquisition channels.
Why it matters: distinguishes product-regression and channel-quality hypotheses.
Check: cohort retention by acquisition source for the last six weeks.
If unavailable: keep confidence medium-low and avoid a full interface rollback.
```

Confidence scale:

- **Low:** few grounds, weak sources, strong alternatives, critical unknowns.
- **Medium:** several grounds, but important assumptions or alternatives remain.
- **High:** strong independent grounds, alternatives tested, critical assumptions checked, revision conditions clear.

Always explain why confidence is not higher.

### 8. Check load-bearing assumptions

Before a recommendation, find assumptions that carry the conclusion.

Procedure:

1. Take one conclusion or recommendation.
2. Rewrite it as: “If X is true, then Y is justified.”
3. List assumptions without which Y does not hold.
4. Separate load-bearing assumptions from background assumptions.
5. For each load-bearing assumption, name evidence strength and checkability.
6. Decide what changes if it fails.
7. Rewrite the conclusion with applicability and revision conditions.

### 9. Stress-test the conclusion

Choose one or more:

- **Red team:** attack the strongest grounds and find the best alternative.
- **Premortem:** assume the decision failed; list plausible causes of failure.
- **Scenario analysis:** if future uncertainty matters, build 3–4 plausible futures with indicators.
- **Indicator table:** if the situation evolves, define signals that strengthen/weaken the conclusion.

Stress-testing must change something: conclusion, confidence, assumptions, monitoring, or recommendation. If nothing can change, the test was decorative.

### 10. Synthesize a useful analytical output

A strong analytical conclusion includes:

```text
Answer:
Confidence:
Main grounds:
Best alternative explanation:
Key uncertainty:
What would change the answer:
Practical implication / recommended next step:
```

For longer memos, use:

```text
1. Question
2. Short answer
3. Confidence and why
4. Grounds / evidence
5. Alternatives considered
6. Unknowns and assumptions
7. Recommendation or next check
8. Revision conditions
```

## Output Formats

### Compact answer

Use when the user needs a quick answer.

```text
Working question:
Short answer:
Confidence:
Why:
Main alternative:
What to check next:
```

### Analytical note

Use when the user needs a deliverable.

```text
# Analytical note: <topic>

## Question
...

## Short answer
...

## Grounds
- ...

## Alternatives
- ...

## Uncertainty
- ...

## Recommendation / next step
...

## What would change this conclusion
...
```

### Review of another analysis

```text
Verdict:
Strong parts:
Weak reasoning:
Missing alternatives:
Hidden assumptions:
Overclaiming / confidence issues:
Concrete fixes:
```

## Common Analytical Failures

1. **Theme instead of question.** The work never chooses what answer is needed.
2. **First version becomes conclusion.** The analysis protects the first plausible explanation.
3. **Evidence pile.** Many facts, no argument about what follows from them.
4. **No alternative.** One hypothesis is discussed as if no other mechanism exists.
5. **Source laundering.** Dependent reports are counted as independent confirmation.
6. **False precision.** Numbers or probability words look exact but lack grounds.
7. **Decorative uncertainty.** “There are risks” appears, but no condition changes the conclusion.
8. **Recommendation overreach.** The action is stronger than the evidence.
9. **Template theater.** Forms are filled, but the answer, confidence, and next check are still unclear.
10. **No revision trigger.** The output does not say what would make it wrong.

## Verification Checklist

Before finalizing analysis, check:

- [ ] Is there a clear analytical question, not only a topic?
- [ ] Is the audience/decision/use named?
- [ ] Are facts separated from interpretations and assumptions?
- [ ] Are sources evaluated by proximity, freshness, completeness, independence, incentives, and verifiability?
- [ ] Are at least 2–3 competing hypotheses considered where relevant?
- [ ] Does the evidence comparison include contradictions and absent expected signs?
- [ ] Are key unknowns specific and tied to confidence or action?
- [ ] Is confidence stated with a reason?
- [ ] Are load-bearing assumptions named before recommending action?
- [ ] Is the recommendation proportional to confidence and reversibility?
- [ ] Does the output say what would change the conclusion?

## Linked References

Use the linked files for deeper work:

- `references/method-core.md` — analytical objects, valid transitions, and operations.
- `references/evidence-and-confidence.md` — diagnosticity, evidence matrices, and confidence rules.
- `references/decision-and-revision.md` — coupling conclusions to action and updating conclusions after new information.
- `references/method-map.md` — method chooser distilled from the textbook.
- `templates/analysis-brief.md` — reusable forms for analytical questions, source maps, unknowns, hypothesis matrices, assumptions, and conclusions.
- `references/quality-gate.md` — final checklist and failure patterns for reviewing analytical work.
