# Lesson Quality Gate

Run this gate after drafting a guided lesson and repair the draft before sending it.

## Scope And Title

- Can the title name one reusable knowledge system without a repository name or file path?
- Does every core section explain that same system?
- Has a neighboring system been deferred explicitly rather than blended into the explanation?

If not, narrow the lesson before writing more detail.

## Causal Teaching

- Does the opening show a feature behavior, not merely a command or file list?
- Does it identify the missing capability that makes the why-question necessary?
- Does the generic chain cover input, processing, output, actors, and boundaries appropriate to this topic?
- Is there a minimal example that could survive if all project names were removed?

If the learner would need to guess the generic chain, the lesson is still a project prompt, not teaching.

## Code Evidence

- Did generic roles and terms appear before code identifiers?
- Does each cited file answer a specific step in the already-taught chain?
- Are facts verified by source/run evidence, while unknown details remain marked as unknown?
- Is one normal result and one useful failure boundary included when relevant?

## Learner Turn

- Do the final questions apply the taught chain rather than demand terminology recall?
- Could a beginner answer them after reading only this lesson?
- Does the response stop after those questions instead of answering them on the learner's behalf?

## Regression Signals

Rewrite the lesson when any of these occurs:

```text
It starts with “run this command” and immediately asks the learner to explain everything.
It uses a broad title because the actual concept was not selected.
It gives only a sequence of files/functions where a causal explanation should be.
It calls a question a lesson and stops before teaching the mechanism.
It introduces multiple systems because the project contains them.
```
