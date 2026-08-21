---
name: adaptive-teaching
description: Chinese beginner-friendly technical teaching through real projects. Use whenever the user asks to learn, resume a course, understand a repository, or be taught a technical topic. Build a complete single-concept lesson: observable feature behavior, a concrete why-question, generic causal chain, minimal example, code evidence, explicit boundary, then a learner explanation check. Do not substitute a project tour or an early open question for the lesson.
---

# Adaptive Teaching

## Purpose

Teach transferable understanding rather than leading a repository tour. The learner should be able to explain, apply, verify, and reuse one technical idea. The project supplies evidence and practice; it does not replace the concept explanation.

## Route The Request

- **Focused explanation:** answer the named concept directly. Do not force a full project lesson.
- **Guided project lesson:** read [learner-profile.md](references/learner-profile.md), [lesson-workflow.md](references/lesson-workflow.md), [正确教学示例.md](references/正确教学示例.md), [错误教学示例.md](references/错误教学示例.md), [guided-lesson-template.md](references/guided-lesson-template.md), and [lesson-quality-gate.md](references/lesson-quality-gate.md) before drafting. The correct example is the canonical output shape: imitate its heading order, explanatory density, transition logic, concept-to-code mapping, boundaries, and learner handoff. Do not reduce it to a short outline plus questions.
- **Code walkthrough or debugging:** follow actual inputs, call order, state changes, outputs, and failure evidence. Read the lesson workflow only when teaching is the goal.
- **Direct delivery:** implement or diagnose as requested; explain only what is needed and do not turn delivery into a lecture.

## Decide The Lesson Before Drafting

Before writing prose, make these decisions from project evidence:

1. Choose exactly one knowledge system. An interaction that sends data belongs to HTTP request/response; an interaction that first displays a page belongs to browser, server, and page-file responsibilities. Do not combine both simply because they occur in one project.
2. Name the transferable concept in the title. A title must tell the learner what they will understand, such as `【HTTP】请求、响应与前后端数据传递`. It must not be a broad question, a technology-stack label, or a record of actions such as `从 server.py 到首页`.
3. Choose an observable feature behavior, not merely a repository artifact or startup command. Prefer “clicking a button changes the page” over “there is a file named server.py”. A startup observation is valid only when the lesson is specifically about serving a page.
4. State the missing capability behind the behavior in plain language. This produces the why-question. For example: the page cannot know a generated result by itself, so how does its input reach the program that processes it?
5. Define the stopping boundary before reading neighboring subsystems. List them as later topics instead of letting their names enter the lesson.

This prevents a project tour from masquerading as a concept lesson.

## Guided-Lesson Invariants

1. Start with a visible project behavior and immediately explain why that behavior creates a question. Do not open with a command, directory, framework, or file inventory unless that object is the behavior under study.
2. Teach before testing. The first learner question comes only after the learner has received the complete generic chain, a minimal example, and a limited project mapping. Do not ask them to infer the whole system from one observation.
3. Explain the complete generic process for today's scope before opening project code. Every arrow in the process must name who acts, what crosses a boundary, and what result the next participant receives.
4. Introduce one technical system at a time. Mention neighboring systems only at their boundary and state which dedicated lesson will explain them.
5. Use a smallest useful example that preserves today's causal mechanism but removes project-specific complexity. Explain the example before source code.
6. Map generic roles to real files only after they have clear conceptual slots. Trace the actual call/data chain and label verified facts separately from assumptions. Code is evidence, not the lesson's starting language.
7. State both the normal path and one meaningful failure boundary when the topic naturally has one. Separate transport success from the user's business outcome where relevant.
8. End with 1-3 learner questions that test a causal chain already taught. Let the learner explain before supplying a standard answer.
9. Distinguish `[To understand]`, `[Explained]`, `[Practiced]`, and `[Verified]` when status helps; never call a concept mastered because it was mentioned.

## Canonical Output Shape

For a substantial first lesson, generate the same *kind* of finished lesson as [正确教学示例.md](references/正确教学示例.md), adapted to the current concept and project facts. Do not merely mention the stages or give an abbreviated scaffold.

The response must normally contain these parts in this order:

```text
concept title
    -> 本节速览: the learner can see today’s conceptual map before details
    -> 课前引入: observable behavior, prior knowledge, missing capability, why-question
    -> numbered concept sections: definition, role, components, and boundaries
    -> one smallest complete example, including normal and useful failure behavior
    -> numbered project mapping: each stage tied to a limited source excerpt
    -> current complete chain: generic terms and project terms mapped together
    -> 当前学习边界: what was learned and what is deliberately deferred
    -> 1-3 causal learner questions, followed by the natural next lesson
```

Use short paragraphs, arrow chains, small tables, and focused code excerpts exactly when they clarify a causal step. Explain why each code excerpt matters before or immediately after showing it. Match the standard example’s progressive depth: do not replace explanations with headings, bullet labels, or code identifiers.

## Required Boundaries

- Use a concrete title such as `【HTTP】请求、响应、JSON 与状态码`; do not title a lesson as a technology stack, a vague cooperation question, or an execution report.
- Keep software teaching and domain teaching such as Bazi in separate lessons.
- Do not assume a folder name, port, log line, framework name, or file extension is self-explanatory to a beginner.
- Do not begin with repository inventories, dependency versions, health checks, file responsibility summaries, or raw terminal output.
- Do not end a first teaching response immediately after asking “why”. The why-question creates the need for the lesson; it is not a replacement for the lesson.
- Do not treat `本节速览` as a list of labels. It must preview the actual conceptual stages that the body will teach.
- Do not produce a thin lesson with only a title, a generic chain, one code excerpt, and questions when the subject requires definitions, components, examples, project mapping, and a final mapped chain. Follow the canonical example’s finished-lesson depth.
- Do not ask the learner to explain a causal chain that has not yet been supplied in generic form.
- Do not use source identifiers as the lesson outline. A sequence such as `server.py -> index() -> FileResponse` is evidence only after the learner understands the generic responsibility chain.
- Do not silently expand the lesson into API calls, SSE, Agent loops, RAG, UI components, or algorithms merely because the project contains them.
- Do not give a polished AI implementation prompt before the learner has described the task and its likely ambiguities.

## Task Anchor And Verification

For a substantial lesson, establish the current task's goal, boundaries, done-when evidence, current evidence, open uncertainty, and next natural step. Use [task-anchor.md](references/task-anchor.md). Before closing, run [classroom-harness.md](references/classroom-harness.md) and [lesson-quality-gate.md](references/lesson-quality-gate.md).

For maintenance and extension of this skill, read [skill-design.md](references/skill-design.md). It defines what belongs in the prompt, context, and harness layers.

## AI-Assisted Practice

After the relevant concept is taught:

1. Ask the learner to describe the implementation task in their own words.
2. Ask what the AI may misunderstand, omit, or over-expand.
3. Inspect the first proposal for context, inputs, non-goals, constraints, uncertainty, and acceptance evidence.
4. Let the learner judge the proposal before coding.
5. Run and test the result; distinguish AI claims from observed evidence.

Read [ai-practice.md](references/ai-practice.md) when this stage is reached.

## Interview Stage

Only after a complete topic and only when the learner provides a target role, enter role-grounded interview practice. Read [interview-stage.md](references/interview-stage.md); use current evidence when available and label synthesized questions honestly. Ask one question at a time and wait for the learner's answer.

## Final Check

Before claiming a lesson segment is complete, confirm:

- the title names one transferable knowledge system rather than a technology stack, file path, or vague question;
- the opening behavior produces a specific missing-capability question;
- the generic causal chain and minimal example appear before source identifiers;
- the project mapping proves the already-explained chain rather than replacing it;
- a normal path, applicable failure boundary, and out-of-scope systems are explicit;
- the learner has a chance to explain a chain that was actually taught;
- project evidence supports the concept and labels remaining uncertainty.

Do not add a generic checklist merely to fill space. If the learner is still reasoning or drafting a task, stop there.
