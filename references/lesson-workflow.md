# Guided Project Lesson Workflow

Use this workflow for a substantial project lesson. It defines the order in which a learner builds a mental model; it is not a checklist for describing a repository.

## Before Reading Source

Decide these five items from the learner's goal and a small amount of project evidence:

```text
one transferable knowledge system
    -> a title that names it
    -> one visible feature behavior
    -> the missing capability behind that behavior
    -> today's boundary and deferred neighboring systems
```

For example, a page that appears after startup can motivate a lesson about page serving. A button that submits input and later shows a result can motivate a lesson about HTTP request/response. They occur in the same product but are separate lessons.

## Classroom Sequence

```text
visible feature behavior
    -> missing capability and plain-language why-question
    -> complete generic causal chain
    -> foundational concepts, one at a time
    -> smallest useful example
    -> project source as evidence
    -> normal result and failure boundary
    -> explicit non-goals
    -> learner explains the taught chain
```

The why-question creates a reason to learn. It is not a request for the learner to infer the system before it is taught.

## Opening

Describe only what the learner can directly see or do in the project. Explain what that visible object cannot accomplish on its own, then ask why. Do not begin with a framework, command, path, port, log line, or directory unless it is the actual object being taught.

Good opening shape:

```text
The learner clicks a visible button and later sees a result.
    -> the displayed page cannot know that result by itself
    -> how does its input reach the program that can process it?
```

Continue immediately to the generic process. Do not stop for the learner's answer here.

## Concept Phase

For every new term, use:

```text
immediate problem it solves
    -> plain-language definition
    -> position in today's causal chain
    -> minimal generic example
    -> precise technical name
```

Explain inputs, processing, outputs, state changes, normal cases, and failure boundaries that belong to the chosen knowledge system. Do not introduce a neighboring system merely because source code contains it.

## Project Mapping

Only after the generic mechanism is clear, inspect a small number of relevant files. Trace the real chain:

```text
who starts it -> what input crosses the boundary -> who receives it
-> what chooses the next step -> what result is produced
-> who consumes it next -> what happens on failure
```

State which claims were verified by source or execution, and which remain assumptions. A file/function sequence is evidence for this chain, not a substitute for the chain.

## Lesson Handoff

State what this lesson deliberately does not teach. Then ask the learner 1-3 plain-language questions that apply the generic chain already explained. Do not supply their answer until they respond.
