# Memory Skill System

[English](./README.md) | [简体中文](./README.zh-CN.md)

A structured memory skill for recall, continuation, routing, and durable write-back across ongoing work, personal projects, and reusable methods.

一个结构化的 memory skill，用于在持续工作、个人项目和可复用方法中处理 recall、continuation、memory routing 和 durable write-back。

This repository provides a reusable public version of the memory skill system.
It is designed to help memory work stay structured instead of turning into chat recap, context leakage, or unmaintainable notes.

---

## Why this exists

In many AI-assisted workflows, memory breaks down in predictable ways:
- prior context is hard to find
- recall turns into recap instead of continuation
- personal and formal-work context get mixed together
- durable knowledge is not separated from temporary discussion
- memory starts to duplicate detailed project artifacts

This repository tries to solve that by providing a clearer memory operating model.

---

## What makes this repository different

### 1) Routing-first memory model
The memory skill is built around four routing axes:
- permission layer
- domain
- anchor
- memory type

This helps reduce context mixing and makes memory usage more deliberate.

### 2) Continuation first, recap second
The goal is not to summarize chat for its own sake.
The goal is to continue work effectively.

That means the skill emphasizes:
- current stage
- confirmed rules
- unresolved points
- reusable methods
- the smallest useful recall set

### 3) Clear separation from project assets
This repository treats memory as a summary-and-continuation layer, not as a replacement for detailed project artifacts.

Memory should manage:
- concise continuation context
- durable summaries
- reusable methods
- safe routing

Memory should not become a dump for full project baselines, demos, or version packages.

### 4) Can be used alone or with PM workflow
This repository can be used as a standalone memory layer.
It can also be used together with:
- `pm-workflow-system`

Recommended relationship:
- **PM workflow** manages requirement/demo/embedded-PRD/project assets/versions
- **Memory skill** manages recall/continuation/routing/write-back summaries

---

## What is included

- `skills/memory-skill/`
- `UPDATE-NOTES.md`
- `LICENSE`
- `CONTRIBUTING.md`

---

## Repository structure

```text
skills/
  memory-skill/
    SKILL.md

UPDATE-NOTES.md
LICENSE
CONTRIBUTING.md
README.md
README.zh-CN.md
```

---

## How to use

### Option A: use it as a standalone memory layer
Use this repository when the main problem is:
- recalling prior work
- continuing ongoing topics
- separating stable memory from temporary discussion
- routing memory by permission/domain/type

### Option B: use it together with PM workflow
Use it together with `pm-workflow-system` in workflows where:
- detailed assets stay in structured project folders
- memory holds concise summaries and continuation pointers
- boundaries between project artifacts and memory context need to stay clear

---

## Scope of this public version

This repository provides a shareable public version of the memory skill.
It is not the author's private self-use memory layer.

That means the public version is intended to be:
- easier to trial
- easier to explain
- easier to combine with shared workflow systems
- less tied to one person's private context

---

## Version context

This repository uses the current public-shareable memory-skill variant as its main skill content.

For version-change context relative to earlier public packaging, see:
- `UPDATE-NOTES.md`

---

## Packaging position

This repository is organized as the public repository form of the current memory skill line:
- centered on the full current skill content
- with version/update notes preserved separately
- with standalone usage and PM-workflow companion usage both documented clearly

---

## License

This repository currently uses the **MIT License**.

See:
- `LICENSE`

---

## Contributing

See:
- `CONTRIBUTING.md`
