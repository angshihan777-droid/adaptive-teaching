# Guided Project Lesson Workflow

Use this for substantial project lessons. It is a reusable structure; derive the actual content from the current project instead of filling in a prewritten answer.

## Sequence

```text
observable project phenomenon
    -> plain-language why question
    -> the missing capability or limitation
    -> complete generic process for today's scope
    -> one foundational concept at a time
    -> smallest useful example
    -> project code as evidence
    -> explicit boundary and non-goals
    -> learner explains the chain
```

## Opening

Describe only what the learner can directly observe. Say that the unfamiliar words need not be known yet. Ask a natural “why” question from that observation. Do not reveal the project conclusion before the learner has a causal slot for it.

## Concept phase

For every new term, use:

```text
the immediate problem it solves
    -> plain-language definition
    -> position in today's chain
    -> minimal generic example
    -> precise technical name
```

Explain inputs, processing, outputs, state changes, normal cases, failure boundaries, and why the concept belongs at this point.

## Project mapping

Only now inspect the relevant files. Trace the actual call or data chain:

```text
who starts it -> what input crosses the boundary -> who receives it
-> what chooses the next step -> what object or result is produced
-> who consumes it next -> what happens on failure
```

State which facts were verified by reading or running code and which remain assumptions.

## Lesson handoff

Stop after asking the learner to explain the chain in their own words. Do not answer that check before they respond.
