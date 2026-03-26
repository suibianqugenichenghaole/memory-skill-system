# Update Notes

This file records the main changes represented by the current public repository package relative to earlier public-facing memory-skill packaging.

The repository itself remains the main public repository form of the current memory-skill line.

---

## Main changes represented here

- keeps the core routing model: permission / domain / anchor / type
- keeps the three main routes:
  - requirement continuation
  - personal creation
  - finalized requirement Q&A
- trims some overly detailed self-operating explanations
- makes the boundary with PM workflow project assets clearer
- keeps the skill leaner and easier to trial in shared/public contexts
- adds retrieval-friendly writing rules for stronger continuation and recall consistency
- adds a durable-entry template for important memory topics
- adds explicit no-embeddings / FTS-only fallback guidance for degraded retrieval environments

---

## Why this update / 为什么更新

### EN
This update was driven by real usage rather than speculative polish.

Two practical gaps showed up during actual memory-recall work:
- important memories had been written down, but later retrieval was still unreliable when anchor naming and aliases were inconsistent
- degraded environments without embeddings needed explicit fallback guidance instead of silently assuming semantic recall still worked

Because of that, this update focuses on two things:
- stronger retrieval-friendly writing conventions
- clearer no-embeddings / FTS-only operating guidance

### 中文
这次更新不是为了“润色一下”，而是被真实使用问题逼出来的。

在实际的 memory 回忆与续写过程中，暴露了两个明显缺口：
- 有些重要记忆其实已经写下来了，但因为锚点命名和别名不统一，后续仍然不容易稳定找回
- 在没有 embeddings 的降级环境里，不能再默认语义召回存在，必须明确给出 fallback 使用规则

所以这次更新主要补的是两件事：
- 更适合检索的书写规范
- 更明确的 no-embeddings / FTS-only 降级使用说明

---

## Important boundary

This memory skill is not the same thing as PM workflow project-ops.

- **PM workflow project assets** manage detailed requirement/demo/PRD/version artifacts
- **Memory skill** manages summary, continuation, reusable method context, and safe routing

If both are used together:
- detailed artifacts should stay in project assets
- memory should store summary + pointer rather than duplicating full assets

---

## Repository position

This repository presents the current public memory-skill version in repository form.

That means:
- the skill content is the main body
- update notes stay as change context
- the repository can be used on its own
- the repository can also be used together with `pm-workflow-system`
