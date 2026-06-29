# Evidence and Confidence

This reference strengthens two weak points common in analytical work:

1. treating compatible facts as if they prove a hypothesis;
2. stating confidence without showing what controls it.

## 1. Evidence is claim-relative and question-relative

A fact is not automatically evidence. It becomes evidence when it bears on a specific question.

```text
Question: Why did conversion fall in May?
Claim: Conversion fell in May.
Role: observation to explain, not evidence for a cause.

Claim: Conversion fell only in traffic from the new ad channel.
Role: evidence that can distinguish channel-quality from site-wide product regression.
```

Always ask:

```text
Evidence for what?
Evidence against what?
Evidence compared to which alternative?
```

## 2. Compatibility is weak

Many facts are compatible with many hypotheses. Compatibility alone should not choose between them.

Example:

```text
Observed: sales fell.
H1: lead quality fell.
H2: price became less competitive.
H3: onboarding broke.
```

The sales drop is compatible with all three. It is the thing to explain, not a decisive argument for any one version.

## 3. Diagnosticity scale

Use this scale when evaluating evidence against competing hypotheses.

| Level | Meaning | Analytical value |
|---|---|---|
| Background | Adds context but does not affect the answer | Low |
| Compatible | Does not contradict a hypothesis | Very low |
| Supportive | Expected if the hypothesis is true | Medium if alternatives do not expect it as strongly |
| Diagnostic | Better explained by one hypothesis than by others | High |
| Critical | The hypothesis depends on it; absence would seriously weaken the hypothesis | Very high |
| Contradictory | Opposes an expected sign of the hypothesis | High |
| Disconfirming | Makes the hypothesis unlikely unless an auxiliary assumption is added | Very high |

Do not count all positive marks equally. One diagnostic contradiction can outweigh many compatible details.

## 4. Evidence matrix discipline

Use one shared evidence list against all hypotheses.

Marks:

```text
+   supports / expected
-   weakens / contradicts
0   neutral
≈   compatible with many hypotheses; weakly diagnostic
?   insufficient data
!!  diagnostic or critical item
```

For every important evidence item, add a note:

```text
Note: diagnostic / generic / contradiction / absent expected sign / source-limited
```

Example:

| Evidence | H1 lead quality fell | H2 price issue | H3 onboarding broke | Note |
|---|---:|---:|---:|---|
| Drop only in new ad channel | + | 0 | - | diagnostic for H1 |
| Existing customers unaffected | + | 0 | + | compatible with H1/H3 |
| Price complaints rose in all segments | - | + | 0 | diagnostic for H2 if source reliable |
| Activation fell after onboarding release | 0 | 0 | + | diagnostic for H3 |

## 5. Expected signs and absent signs

A hypothesis should predict something observable. If expected signs are absent, confidence should fall.

```text
Hypothesis: price caused the conversion drop.
Expected signs: more price objections, worse conversion in price-sensitive segments, competitor price changes.
Absent signs: no increase in price objections; drop concentrated in one ad channel.
Effect: price hypothesis weakens or becomes segment-limited.
```

Absence is only meaningful when the sign should have been visible. Do not overuse absence where observation is weak.

## 6. Source strength affects evidence strength

Evidence strength depends on both diagnosticity and source quality.

```text
strong evidence = diagnostic signal + source that can know + clear boundary
weak evidence = compatible signal + distant/interested/incomplete source
```

Check:

- proximity: direct measurement, participant report, hearsay, synthesis;
- freshness: current enough for the claim;
- completeness: what is missing;
- independence: whether sources share origin or incentive;
- incentives: why the source may distort;
- verifiability: can the claim be checked.

## 7. Confidence model

Do not use pseudo-precise percentages unless the task has real statistical grounds. Use low / medium / high with reasons.

Confidence rises when:

- the question is bounded;
- sources are close, fresh, independent, and verifiable;
- evidence is diagnostic, not merely compatible;
- alternatives were compared on the same evidence;
- expected signs and contradictions were checked;
- load-bearing assumptions are named and supported;
- the conclusion states its limits.

Confidence falls when:

- a strong alternative remains untested;
- evidence is mostly compatible rather than diagnostic;
- the source base is dependent or interested;
- a conclusion depends on a fragile assumption;
- key expected signs are absent;
- the scope is broad or poorly bounded;
- the recommendation is costly or hard to reverse.

## 8. Confidence levels

| Confidence | Use when | Output discipline |
|---|---|---|
| Low | Few grounds, weak sources, strong alternatives, or critical unknowns | Say what can be believed now and name the first diagnostic check |
| Medium | Several grounds support one answer, but important assumptions or alternatives remain | Give a provisional conclusion and bounded action/check |
| High | Strong independent grounds, diagnostic evidence, alternatives tested, assumptions checked | Recommend action with revision triggers |

## 9. Confidence cannot be high if...

Confidence should not be high when any of these hold:

- there is only one source and it is interested;
- the main evidence is only compatible, not diagnostic;
- a strong alternative has not been tested;
- a load-bearing assumption is unsupported;
- the conclusion generalizes beyond the evidence boundary;
- an expected sign of the chosen hypothesis is absent and unexplained;
- the action is irreversible but evidence is still medium.

## 10. Wording confidence

Use exact confidence language.

Weak:

```text
It is likely that the problem is marketing.
```

Stronger:

```text
The channel-quality hypothesis is currently strongest, with medium confidence. It explains the segment-specific drop better than product regression. Confidence is not higher because price sensitivity by segment has not been checked.
```

## 11. Evidence self-check

Before choosing a conclusion, answer:

```text
Which evidence is merely compatible?
Which evidence is diagnostic?
Which evidence contradicts the favored hypothesis?
Which expected sign is missing?
Which source limit weakens the evidence?
What would most efficiently distinguish the top two hypotheses?
```
