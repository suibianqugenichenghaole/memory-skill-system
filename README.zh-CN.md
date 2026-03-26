# Memory Skill System

[English](./README.md) | [简体中文](./README.zh-CN.md)

这是一个结构化的 memory skill，用于在持续工作、个人项目和可复用方法中处理 recall、continuation、memory routing 和 durable write-back。

这个仓库提供的是一套面向公开复用的 memory skill 系统。它的目标是让 memory 工作保持结构化，而不是逐渐退化成聊天 recap、上下文串味或不可维护的零散笔记。

---

## 为什么会有这个仓库

在很多 AI 协作场景里，memory 往往会卡在这些问题上：
- 过去的上下文难找
- recall 很容易变成 recap，而不是 continuation
- personal 和 formal-work 的内容容易混用
- durable knowledge 和临时讨论没有被分开
- memory 逐渐开始复制详细的项目资产

这个仓库想解决的，就是这些结构性问题。

---

## 这个仓库的特点

### 1）以 routing 为核心的 memory 模型
这个 memory skill 建立在 4 个 routing 维度之上：
- permission layer
- domain
- anchor
- memory type

这样做的价值是：减少上下文混用，让 memory 的使用更加可控。

### 2）continuation 优先，recap 其次
这个 skill 的目标不是为了总结聊天而总结聊天。
它的目标是帮助后续工作继续推进。

所以它更强调：
- 当前阶段
- 已确认规则
- 未解决问题
- 可复用方法
- 最小但有用的 recall 集合

### 3）和项目资产明确分层
这个仓库把 memory 定义为一个“summary + continuation”层，而不是详细项目资产的替代品。

memory 更适合管理：
- concise continuation context
- durable summaries
- reusable methods
- safe routing

memory 不应该变成详细项目基线、demo 文件或版本包的堆放区。

### 4）可以单独使用，也可以和 PM workflow 配合使用
这个仓库可以作为独立 memory layer 使用。
它也可以和下面这个仓库配合：
- `pm-workflow-system`

推荐的关系是：
- **PM workflow** 负责 requirement / demo / embedded-PRD / project assets / versions
- **Memory skill** 负责 recall / continuation / routing / write-back summaries

---

## 仓库里包含什么

- `skills/memory-skill/`
- `UPDATE-NOTES.md`
- `LICENSE`
- `CONTRIBUTING.md`

---

## 仓库结构

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

## 如何使用

### 方式 A：把它当作独立 memory layer 使用
当主要问题是下面这些时，可以单独使用这个仓库：
- 回忆过往工作
- 延续同一主题
- 把稳定 memory 和临时讨论分开
- 按 permission / domain / type 路由 memory

### 方式 B：与 PM workflow 配合使用
如果工作流中已经使用 `pm-workflow-system`，这个仓库更适合作为 companion layer：
- 让详细资产继续留在结构化项目目录里
- 让 memory 负责 concise summaries 和 continuation pointers
- 让 project artifacts 和 memory context 的边界保持清晰

---

## 这个公开版的范围

这个仓库提供的是一个可公开分享的 memory skill 版本，而不是作者私有自用的完整 memory layer。

这意味着这个公开版会更偏向：
- 更容易试用
- 更容易解释
- 更容易和共享工作流系统配合
- 更少依赖单个人的私有上下文

---

## 当前版本说明

当前仓库采用的是更新后的公开可分享 memory-skill 版本，并以当前完整 skill 内容作为主干。

相对早期公开包装的变化说明见：
- `UPDATE-NOTES.md`

---

## 仓库定位

这个仓库采用的是当前 memory skill 产品线的公开仓库形态：
- 以当前完整 skill 内容为中心
- 把版本/更新说明单独保留
- 同时清楚说明 standalone usage 与和 PM workflow 的配合关系

---

## License

当前仓库使用的是 **MIT License**。

见：
- `LICENSE`

---

## Contributing

见：
- `CONTRIBUTING.md`
