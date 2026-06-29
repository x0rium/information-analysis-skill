# Decision and Revision

Analysis becomes useful when it controls action and future updates. This reference defines how to move from conclusion to recommendation, and how to revise without overreacting.

## 1. Recommendation cannot outrun conclusion

The practical action must be proportional to:

```text
confidence × decision urgency × reversibility × cost of error
```

This is not a numeric formula. It is a discipline for preventing overreach.

## 2. Action matrix

| Confidence | Error cost | Reversibility | Usually justified action |
|---|---|---|---|
| Low | High | Low | Do not act; seek diagnostic evidence |
| Low | Low | High | Small reversible test |
| Low | Medium | Medium | Clarify question and check assumptions first |
| Medium | Low | High | Bounded experiment or partial rollout |
| Medium | Medium | High | Limited action with monitoring |
| Medium | High | Low | Additional check before action |
| High | Low/Medium | High | Act and monitor revision triggers |
| High | High | Low | Act only with explicit stop condition and owner |

## 3. From conclusion to action

Before recommending, fill this logic:

```text
Conclusion:
Confidence:
Decision needed:
Cost of being wrong:
Reversibility:
Time pressure:
Load-bearing assumptions:
Recommended action:
Why this action matches confidence:
Stop or revise condition:
```

If the recommended action is much stronger than the confidence, change the action, not the confidence wording.

## 4. Load-bearing assumptions

A load-bearing assumption is one that can break the conclusion or action if false.

Procedure:

1. Write the recommendation.
2. Rewrite it as: `If <assumption>, then <action> is justified.`
3. List assumptions required for the action.
4. Separate load-bearing assumptions from background assumptions.
5. For each load-bearing assumption, write support, check, and failure effect.

Template:

```text
Recommendation:

Load-bearing assumption:
Current support:
How to check:
What changes if false:
Action implication:
```

## 5. Good recommendation shapes

### Low confidence

```text
Do not choose a full action yet. The first move is to check X, because it distinguishes H1 from H2. If X is unavailable, keep the conclusion low-confidence and only run reversible tests.
```

### Medium confidence

```text
Proceed with a bounded test in the affected segment. Do not generalize to the whole system until assumption A is checked. Stop if signal B does not appear within timeframe T.
```

### High confidence

```text
Proceed with the main action. Monitor revision triggers R1 and R2 because they would weaken the conclusion or change the action boundary.
```

## 6. Revision method

New information can affect different parts of the analysis. Identify where it lands before changing the conclusion.

| New information affects | Meaning | Possible update |
|---|---|---|
| Source trust | A source becomes more or less reliable | Reweight affected claims |
| Fact base | A working fact changes | Rebuild dependent inferences |
| Hypothesis ranking | Evidence distinguishes explanations | Change strongest hypothesis |
| Assumption | A load-bearing premise strengthens/fails | Change confidence or action |
| Confidence only | Same conclusion, stronger/weaker support | Keep answer, adjust confidence |
| Recommendation | Same conclusion, different action constraints | Change action, not necessarily belief |
| Boundary | Conclusion applies to narrower/wider scope | Restate applicability |
| Background | Interesting but not load-bearing | Note without changing answer |

## 7. Revision rules

1. **Do not restart analysis automatically.** Update the affected chain segment.
2. **Do not treat recency as strength.** Fresh evidence still needs source and diagnostic checks.
3. **Do not overreact to compatible evidence.** It may strengthen confidence slightly without changing ranking.
4. **Respect diagnostic weak signals.** A small but discriminating fact may matter more than a large pile of background material.
5. **Separate belief update from action update.** A conclusion may stay the same while action becomes more cautious.
6. **Name what remains unchanged.** This prevents drift.

## 8. Update note format

```text
Previous conclusion:
Previous confidence:
New information:
Source quality:
Affected chain element: source / fact / hypothesis / assumption / confidence / recommendation / boundary / background
Diagnostic value:
What changes:
What does not change:
Revised conclusion:
Revised confidence:
Revised action or next check:
Next revision trigger:
```

## 9. Stop and revise conditions

A good analytical output names what would change it.

Examples:

```text
Revise the channel-quality conclusion if cohort retention drops equally in old channels.
Stop the rollout if activation does not improve by at least X in the test segment within Y days.
Change from H1 to H2 if price objections rise across all acquisition channels.
Keep the recommendation bounded until source S is verified independently.
```

## 10. Decision self-check

Before finalizing a recommendation, answer:

```text
Is the action stronger than the conclusion?
What is the cost of being wrong?
Can the action be reversed?
Which assumption carries the recommendation?
What should be checked before acting, if anything?
What signal stops or changes the action?
What new information would change belief versus only change action?
```
