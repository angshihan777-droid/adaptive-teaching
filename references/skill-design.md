# Skill Design Principles

These principles describe how to maintain this teaching Skill. They are design guidance, not lesson content.

## Prompt, Context, Harness

- **Prompt:** defines teacher behavior: what to do, in what order, and what boundaries to preserve.
- **Context:** gives the teacher the learner profile, current project evidence, course plan, and relevant references.
- **Harness:** checks whether the lesson actually followed the behavior: observable opening, concept-before-code, one-system boundary, learner explanation, and evidence-backed closure.

A Skill that has only Prompt may sound correct but drift in long sessions. A Skill that has Context but no routing loads too much irrelevant material. A Skill without Harness can appear compliant while skipping the learner's reasoning turn.

## Activation over storage

`SKILL.md` is a navigation center, not a knowledge encyclopedia. Keep always-needed rules in the entrypoint and route deep guidance to references. Every reference file must have an independent reason to be read; if two files are always read together and have one responsibility, merge them.

The frontmatter `description` is a trigger description, not a marketing summary. It should cover the user's likely ways of asking for this teaching mode while excluding unrelated direct-delivery work.

## Reusable structure, fresh content

Reuse the classroom structure, checks, and boundaries. Derive the actual opening phenomenon, generic chain, examples, code evidence, and learner question from the current project and answer. Do not prewrite project conclusions that the teacher will repeat without observation.

## Principle plus check

Write important rules as a behavior plus a question the teacher can verify afterward.

```text
Rule: explain the general concept before project code.
Check: could the learner understand the concept if the project file names were removed?
```

Use real failures and learner feedback to add new checks. Do not invent a large list of hypothetical agent excuses or failure patterns.
