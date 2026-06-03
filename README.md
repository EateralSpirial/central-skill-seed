# 🌱 Central Skill Seed / 中央 Skill 种子

> EN: A minimal seed skill that teaches an agent how to complete itself into a full central project-bootstrap skill.
>
> 中文：一个最小化的种子 skill，用来指导 agent 先把自己补全成完整的中央项目初始化 skill。

## 🧭 What This Is / 这是什么

**EN:** `central-skill-seed` is not a finished project bootstrap system. It is the seed of that system. Its first job is controlled self-completion: it grows from three core files into a full central skill, and only then can that full skill initialize or manage project-level agent context for other repositories.

**中文：** `central-skill-seed` 不是一个已经完成的项目初始化系统。它是这个系统的种子。它的第一任务是可控地补全自身：先从三个核心文件成长为完整中央 skill，然后完整中央 skill 才能为其他仓库初始化或管理项目级 agent 上下文。

## ✨ Core Idea / 核心思想

```text
seed
-> full central skill
-> project-level agent context
```

**EN:** The important design is second-order bootstrapping. The seed does not directly create project-level context. It first creates the central skill that will create project-level context.

**中文：** 关键设计是二阶自举。种子不直接生成项目级上下文，而是先生成一个完整中央 skill，再由完整中央 skill 去生成项目级上下文。

## 📦 Seed Files / 种子文件

The operational seed contains three core files:

| File | EN | 中文 |
| --- | --- | --- |
| `SKILL.md` | Defines identity, state detection, target structure, and operational boundaries. | 定义身份、状态判断、目标结构和操作边界。 |
| `ITERATION_RULES.md` | Defines seed completion rules and full skill iteration rules. | 定义种子补全规则和完整 skill 迭代规则。 |
| `PROJECT_REFERENCES.md` | Indexes evidence sources, trusted local projects, and managed projects. | 索引证据源、本地可信项目和已管理项目。 |

`README.md` is publishing documentation for GitHub. It is not part of the operational seed protocol.

`README.md` 是用于 GitHub 发布的说明文档，不属于种子运行协议。

## 🔎 Effective Sources / 有效源

**EN:** The seed may use only sources explicitly listed in `PROJECT_REFERENCES.md`. Accessibility is not authorization: a local directory, GitHub repository, browser-visible page, or plugin search result is not an effective source until it appears in the allowlist or the user explicitly approves it.

**中文：** 种子只能使用 `PROJECT_REFERENCES.md` 中明确列出的有效源。能访问不等于被授权：本地目录、GitHub 仓库、浏览器页面或插件搜索结果，只有被写入 allowlist 或由用户明确批准后，才是有效源。

**EN:** The recovered open-source skill source chain currently includes the official `evomap` skill document and the related `EvoMap/evolver` GitHub repository. Other previously intended open-source skill repositories must be added by exact name or URL before they become effective sources.

**中文：** 当前已恢复的开源 skill 来源链包括官方 `evomap` skill 文档和相关的 `EvoMap/evolver` GitHub 仓库。其他此前计划加入的开源 skill 仓库，必须用明确仓库名或 URL 补充后，才会成为有效源。

## 🧬 Lifecycle / 生命周期

1. **Phase 0: Seed exists / 种子存在**
   Only the core protocol exists.

   只存在核心协议。

2. **Phase 1: Seed self-inspection / 种子自检**
   The agent checks whether the skill is still in seed state.

   agent 判断当前 skill 是否仍处于种子态。

3. **Phase 2: Evidence collection / 证据收集**
   The agent reads `PROJECT_REFERENCES.md`, trusted projects, managed project experience, and approved external references.

   agent 读取 `PROJECT_REFERENCES.md`、可信项目、已管理项目经验和经批准的外部参考源。

4. **Phase 3: Central skill synthesis / 中央 skill 合成**
   The agent generates templates, schemas, policies, scripts, and docs.

   agent 生成模板、schema、策略、脚本和文档。

5. **Phase 4: Validation / 校验**
   The completed central skill must prove it can initialize a project-level agent context.

   补全后的中央 skill 必须证明自己能够初始化项目级 agent 上下文。

6. **Phase 5+: Project bootstrap and experience harvesting / 项目初始化与经验回收**
   The full central skill initializes projects and harvests reusable experience.

   完整中央 skill 初始化项目，并从项目中回收可复用经验。

## 🚫 What It Does Not Do Yet / 它现在还不做什么

**EN:**

- It does not include generated `templates/`, `schemas/`, `policies/`, `scripts/`, or `docs/`.
- It does not directly initialize target projects.
- It does not assume empty reference lists are enough to invent central policy.
- It does not collapse the two-stage bootstrap into a single step.

**中文：**

- 它还不包含生成后的 `templates/`、`schemas/`、`policies/`、`scripts/` 或 `docs/`。
- 它不直接初始化目标项目。
- 它不会因为参考列表为空就自行编造中央策略。
- 它不会把二阶段自举压缩成一步。

## 🛠️ How To Use / 如何使用

### Install locally / 本地安装

Copy or clone this folder into your Codex skills directory:

将这个目录复制或克隆到你的 Codex skills 目录：

```text
~/.codex/skills/central-skill-seed
```

On Windows, the path usually looks like:

在 Windows 上，路径通常类似：

```text
C:\Users\<you>\.codex\skills\central-skill-seed
```

### Invoke the seed / 调用种子

Ask Codex to use `central-skill-seed` when you want to complete the seed into a full central project-bootstrap skill.

当你想把种子补全成完整中央项目初始化 skill 时，让 Codex 使用 `central-skill-seed`。

Example:

示例：

```text
Use central-skill-seed to complete itself into a full central project-bootstrap skill.
```

## ✅ Validation Goals / 校验目标

A completed central skill is valid only if it can:

完整中央 skill 只有满足以下条件才算有效：

- Create a project-level `AGENTS.md`.
- Generate a project-level self-iteration skill.
- Create experience capture files.
- Create review and eval policies.
- Register the managed project.
- Explain how future agents can continue without depending on the central skill.

中文对应：

- 创建项目级 `AGENTS.md`。
- 生成项目级自我迭代 skill。
- 创建经验捕获文件。
- 创建 review 和 eval 策略。
- 注册被管理项目。
- 说明未来 agent 如何在不依赖中央 skill 的情况下继续工作。

## 🧯 Anti-Drift Principles / 防漂移原则

**EN:**

- Keep the seed small.
- Keep the three core files authoritative.
- Promote project experience into central policy only with evidence.
- Preserve project-level independence.
- Treat missing references as gaps, not permission to invent rules.

**中文：**

- 保持种子足够小。
- 保持三个核心文件的权威性。
- 只有在有证据时，才把项目经验提升为中央策略。
- 保持项目级上下文的独立性。
- 把缺失参考视为缺口，而不是编造规则的许可。

## 📁 Repository Layout / 仓库结构

```text
central-skill-seed/
  README.md
  SKILL.md
  ITERATION_RULES.md
  PROJECT_REFERENCES.md
```

## 🪪 License / 许可证

No license has been selected yet.

尚未选择许可证。
