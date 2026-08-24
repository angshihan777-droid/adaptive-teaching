# Guided Lesson Template

Use this template for a first response in a substantial guided project lesson. Replace every placeholder with evidence from the current project. Omit a section only when it would be empty; do not replace it with a repository tour.

```markdown
# 【<knowledge system>】<specific transferable concepts>

## 本节速览

<A 4-8 step generic arrow chain for this one topic.>

## 课前现象：<visible feature behavior>

<Describe only what the learner can see or do.>

<Why-question: explain the capability the visible behavior lacks by itself.>

## 先看完整的通用过程

<Explain the generic chain from input to output. For each step state the actor,
the data or object crossing the boundary, and what the next actor does with it.>

## 基础概念

<Introduce each new term in this order: problem solved -> plain-language meaning
-> position in the chain -> precise term.>

<Before each major concept, add a bridge explaining what the previous concept
already established, what remains unresolved, and why this concept is next.>

## 最小例子

<Use a small, non-project-specific example that preserves the causal mechanism.>

## 回到当前项目：代码如何证明这条链

<Map generic roles to a small number of verified files/functions. Follow the real
input, processing, output, caller, consumer, and failure boundary.>

## 当前边界

<Name related systems deliberately deferred and their future topic.>

## 你先用自己的话解释

<Ask 1-3 questions that require application of the chain already taught.>
```

## Title Test

A title is acceptable only if the learner can infer the reusable concept without knowing the repository. Compare:

```text
Good: 【HTTP】请求、响应与前后端数据传递
Good: 【Web 应用】浏览器、服务程序与网页文件的分工
Bad: FastAPI + React 启动流程
Bad: 为什么 server.py 能显示网页？
Bad: 从 server.py 到 v2.html
```

The first good title belongs to a button-click/data-transfer lesson. The second belongs to a page-serving lesson. Do not make one lesson cover both.

## Opening Test

An opening is usable when it follows this shape:

```text
visible behavior
    -> what the page/program cannot do by itself
    -> why-question
    -> today’s concept provides the missing mechanism
```

For example:

```text
The user clicks “Start” and later sees a generated result.
    -> the visible page cannot calculate or obtain that result by itself
    -> how does its input reach the program that can process it?
    -> HTTP request/response supplies that communication mechanism
```

Do not stop after the why-question. Continue with the generic chain, minimal example, and project evidence before asking the learner to answer.
