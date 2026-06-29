# Information Analysis Skill

A Hermes Agent skill for disciplined information analysis.

It helps turn scattered material into a useful answer: a clear question, source map, competing hypotheses, uncertainty, conclusion, and next action.

The skill is based on the method work from the Russian textbook project **“Аналитика как метод обработки информации”**. The book text is not included in this repository.

## What this is for

Use it when a task is not just “summarize this”, but requires judgment:

- define the real analytical question behind a vague topic;
- separate facts, interpretations, assumptions, hypotheses, and conclusions;
- evaluate sources by proximity, freshness, independence, incentives, and limits;
- compare competing explanations instead of defending the first plausible one;
- state confidence and name what would change the answer;
- produce an analytical note, decision memo, briefing, review, or update.

## What it is not

- Not a collection of prompts for sounding clever.
- Not a replacement for domain expertise in law, medicine, finance, engineering, or statistics.
- Not a source pack or dataset.
- Not the textbook itself.

## Repository structure

```text
SKILL.md                         Main Hermes skill
references/method-map.md         Method selector: which analytical move to use when
references/quality-gate.md       Checklist and scoring gate for analytical outputs
templates/analysis-brief.md      Reusable brief templates
```

## Install for Hermes Agent

Clone the repository and place it under your Hermes skills directory:

```bash
git clone https://github.com/x0rium/information-analysis-skill.git
mkdir -p ~/.hermes/skills/research
ln -s "$PWD/information-analysis-skill" ~/.hermes/skills/research/information-analysis
```

Or copy it instead of symlinking:

```bash
cp -R information-analysis-skill ~/.hermes/skills/research/information-analysis
```

Then start a fresh Hermes session and load the skill as `information-analysis`.

## Minimal workflow

```text
1. Name the question.
2. Set the context and boundaries.
3. Map source quality and limits.
4. Split facts from interpretations and assumptions.
5. Generate competing hypotheses.
6. Compare evidence across hypotheses.
7. Name uncertainty and load-bearing assumptions.
8. State the conclusion, confidence, next check, and revision condition.
```

The point is not to run every step every time. Pick the smallest method that fixes the weak point of the analysis.

## License

MIT.
