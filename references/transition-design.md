# Concept Transition Design

Use this reference when a lesson contains more than one major concept. The purpose is to preserve causal continuity for beginners: the learner should know why the next idea is necessary before meeting its name.

## The transition contract

Every major transition should answer three questions:

```text
What did we just establish?
What remains unexplained or unfinished?
Why does the next concept address that gap?
```

Use this shape:

```text
我们已经知道 A。
但 A 还不能解释/完成 X。
B 正好解决 X，所以现在进入 B。
```

## Four useful transition types

### 1. Knowledge dependency

Use when B cannot be understood without A.

```text
先知道什么是 FastAPI 应用，才能理解 app 变量保存的是什么；
因此从框架身份过渡到应用对象。
```

### 2. Causal flow

Use when A produces the input or state that B consumes.

```text
Uvicorn 收到请求后，需要把请求交给某个应用对象；
因此接下来学习 ASGI 如何连接服务器和 app。
```

### 3. Project evidence

Use when the generic concept has created the slot for a project code fact.

```text
现在已经知道分类路由的作用，回到 suan 就可以观察 api/routes.py 的 router 为什么被 server.py 引入。
```

### 4. Scope boundary

Use when a neighboring concept is relevant but belongs to another lesson.

```text
startup 也会影响应用运行，但它描述的是启动时机，不是路由匹配；本节先停在请求交给处理函数，生命周期放到下一课。
```

## Bad and good transitions

Bad:

```text
FastAPI 是框架。
下面介绍 APIRouter。
```

Good:

```text
FastAPI 负责提供统一的 Web 应用机制，但一个项目的接口不能都堆在同一个文件里。
因此需要一个只负责按功能收集路由的对象，这就是 APIRouter。
```

## Quality check

Before sending the lesson, mark each major heading transition as one of:

```text
[dependency] [causal] [project] [boundary]
```

If a transition cannot receive one of these labels, the order is probably a list rather than a lesson. Reorder, narrow, or defer the concept.
