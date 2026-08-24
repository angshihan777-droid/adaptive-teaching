# Lesson Quality Gate

Run this gate after drafting a guided lesson and repair the draft before sending it.

## Scope And Title

- Can the title name one reusable knowledge system without a repository name or file path?
- Does every core section explain that same system?
- Has a neighboring system been deferred explicitly rather than blended into the explanation?

If not, narrow the lesson before writing more detail.

## Canonical-Example Fidelity

- Did the draft follow the finished-lesson shape in `正确教学示例.md`, rather than only repeating its abstract principles?
- Does `本节速览` preview the body’s real conceptual stages?
- After the opening, are there enough numbered concept sections to define the mechanism’s important parts before source mapping?
- Does the lesson include a final complete chain that connects generic terms with the project’s concrete evidence?
- Does the closing state both what was learned and what is deferred, then ask questions that directly follow from the body?

If a draft can be summarized as “a short outline, one generic chain, one code excerpt, and a question,” rewrite it against the canonical example.

## Causal Teaching

- Does the opening show a feature behavior, not merely a command or file list?
- Does it identify the missing capability that makes the why-question necessary?
- Does the generic chain cover input, processing, output, actors, and boundaries appropriate to this topic?
- Is there a minimal example that could survive if all project names were removed?
- Does each major concept follow from the previous one through an explicit dependency, causal, project, or scope-boundary transition?
- Does every transition explain why the next concept is needed, rather than merely announcing the next heading?

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
It presents major concepts as a glossary without explaining how one creates the need for the next.
It calls a question a lesson and stops before teaching the mechanism.
It introduces multiple systems because the project contains them.
```
