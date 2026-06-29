# Method Core

This reference turns the skill from a checklist into a controlled reasoning method. Its central rule is simple:

```text
Do not jump from information to action. Move through explicit claim types, and make every transition checkable.
```

Core chain:

```text
source → claim → evidence → inference → hypothesis → conclusion → recommendation → revision
```

A strong analysis is not one with more material. It is one where the movement between these objects is lawful enough that another person or agent can inspect it.

## 1. Analytical objects

| Object | Meaning | Quality question | Common failure |
|---|---|---|---|
| Source | Where a claim comes from | How can this source know? | Treating authority as proof |
| Claim | What is asserted | What exactly is being said? | Treating wording as reality |
| Observation | Something noticed or reported | Who observed it, when, and how? | Ignoring collection limits |
| Data | Recorded material | What does the recording include and exclude? | Treating a dataset as complete reality |
| Evidence | A claim/data point that bears on the question | Which hypothesis or conclusion does it affect? | Calling any relevant-looking fact evidence |
| Fact | A working claim accepted for this task | What are its boundaries? | Forgetting that facts are scoped |
| Interpretation | Meaning assigned to a fact | What else could it mean? | Smuggling interpretation into fact |
| Assumption | A temporarily accepted condition | What breaks if it is false? | Hiding the load-bearing premise |
| Hypothesis | A testable explanation or answer | What should we see if it is true? | Falling in love with the first plausible version |
| Inference | A reasoning move from grounds to implication | Is the move valid and bounded? | Jumping farther than evidence allows |
| Conclusion | Best current answer to the analytical question | Why this answer over alternatives? | Making the answer stronger than its grounds |
| Recommendation | Action justified by the conclusion | Is the action proportional to confidence and reversibility? | Turning medium confidence into irreversible action |
| Revision trigger | Condition that changes the answer or action | What new information would matter? | Ending with no update mechanism |

## 2. Valid transitions

### Source → claim

Use a source only for what it can know.

Valid move:

```text
The support team log can support claims about reported issues, timestamps, and labels.
It cannot by itself prove the true root cause of churn.
```

Invalid move:

```text
The support team says customers leave because of price; therefore price is the cause.
```

Check:

- proximity to the event;
- freshness;
- completeness;
- independence;
- incentives;
- verifiability.

### Claim → evidence

A claim becomes evidence only relative to a question.

Valid move:

```text
Claim: conversions fell only in the new ad channel.
Question: what explains the conversion drop?
Evidence role: diagnostic signal for channel-quality hypothesis.
```

Invalid move:

```text
The claim is interesting, so include it as evidence.
```

Check:

- Which hypothesis does it support or weaken?
- Does it distinguish alternatives?
- Does it only provide background?

### Evidence → inference

An inference must state what follows and what does not follow.

Valid move:

```text
Evidence supports that the drop is channel-specific. It does not prove the ads are the only cause.
```

Invalid move:

```text
The evidence fits my hypothesis, so the hypothesis is true.
```

Check:

- Is the inference deductive, probabilistic, diagnostic, or merely suggestive?
- What alternative inference is still compatible?
- What expected sign is absent?

### Inference → hypothesis

A hypothesis must include mechanism and expected signs.

Valid move:

```text
Hypothesis: lead quality fell in the new channel.
Mechanism: campaign targeting changed; visitors have weaker intent.
Expected signs: lower activation in that channel, stable conversion elsewhere, worse downstream retention.
```

Invalid move:

```text
Hypothesis: marketing is bad.
```

Check:

- Is there a mechanism?
- What would we expect to observe?
- What would weaken it?
- Which check distinguishes it from alternatives?

### Hypothesis → conclusion

A conclusion is a ranked answer after alternatives have been compared.

Valid move:

```text
H1 is currently strongest because it explains the channel-specific drop and retention pattern.
H2 remains plausible because price-sensitivity data is missing.
Conclusion confidence: medium.
```

Invalid move:

```text
H1 has several supporting facts, so H1 is the conclusion.
```

Check:

- Were at least two real alternatives considered?
- Was shared evidence tested against all hypotheses?
- Are contradictions and absent expected signs named?
- Why is confidence not higher?

### Conclusion → recommendation

Action strength must not exceed conclusion strength.

Valid move:

```text
Medium confidence + reversible action → run a bounded test in the affected channel.
```

Invalid move:

```text
Medium confidence → redesign the whole onboarding flow.
```

Check:

- confidence;
- cost of error;
- reversibility;
- decision deadline;
- what can be checked before acting;
- stop/revise condition.

### New information → revision

New information should update the affected part of the chain, not automatically restart everything.

Valid move:

```text
New cohort data weakens the channel-quality hypothesis and strengthens onboarding-regression.
Conclusion changes from H1 medium to H3 medium.
```

Invalid move:

```text
New data appeared, so the previous analysis is obsolete.
```

Check:

- Does it affect source trust, fact base, hypothesis ranking, confidence, assumption, recommendation, or only background context?
- Is it diagnostic or merely compatible?
- Does it change the action?

## 3. Analytical operations

Use these operations deliberately. Do not run all of them by default.

| Operation | Purpose | Input | Output | Failure prevented |
|---|---|---|---|---|
| Reframe | Turn a topic into a question | Topic, decision/use | Bounded question | Endless collection |
| Classify | Separate claim types | Text, notes, source material | Facts, assumptions, hypotheses, conclusions | Smuggled assumptions |
| Decompose | Split a broad issue | System, process, claim | Parts and interfaces | Vague causality |
| Compare | Judge options or hypotheses on shared criteria | Options, criteria, evidence | Trade-off map | One-sided advocacy |
| Triangulate | Check claims from different angles | Sources with different access/incentives | Stronger or weaker claim status | Source laundering |
| Infer | State what follows from evidence | Evidence + question | Bounded implication | Unsupported leap |
| Falsify | Seek what would weaken a hypothesis | Hypothesis + expected signs | Contradictions, absent signs, tests | Confirmation hunting |
| Bound | Set scope and limits | Claim or conclusion | Applicability conditions | Overgeneralization |
| Weigh | Judge relative strength | Evidence, alternatives, assumptions | Confidence and ranking | Mechanical plus-counting |
| Stress-test | Attack the conclusion | Conclusion + grounds | Revised confidence/action | Brittle answer |
| Synthesize | Build the useful answer | Question + grounds + alternatives | Conclusion and next action | Evidence pile |
| Revise | Update after new information | Prior conclusion + new signal | Changed/unchanged elements | Overreaction or clinging |

## 4. Transition self-check

Before finalizing, answer:

```text
What is the question?
Which sources support which claims?
Which claims became evidence, and for what?
Which hypotheses were compared?
Which evidence distinguished them?
What is the conclusion and why not stronger?
What action is justified by this confidence and reversibility?
What would change the conclusion or action?
```

If these cannot be answered, the output is probably formatted reasoning, not analysis.
