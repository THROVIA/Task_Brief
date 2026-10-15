# Task Brief · 开工前对齐

**Clarify the problem before starting complex work.**  
**复杂任务开工前，先把问题说清，再动手。**

[English](#english) · [中文](#中文) · [MIT License](LICENSE)

## English

AI can start producing an answer before you have agreed on what to solve. Task Brief helps you clarify intent, the subject of the work, scope, deliverables, and completion criteria before planning, writing, analysis, or development.

It brings overlooked questions and disagreements into the conversation, then establishes a working definition and the next action. A brief records the outcome; producing a table is not the goal.

### Install and try it

**Claude Code — manual installation**

1. Download this repository using **Code → Download ZIP** and extract it.
2. Rename the extracted folder containing `SKILL.md` to `task-brief` if needed, then copy that folder into your project's `.claude/skills/` folder. The resulting file path is `.claude/skills/task-brief/SKILL.md`.
3. Open Claude Code in that project and enter:

```text
/task-brief Before coding, help me clarify the requirements for a volunteer signup page. I have not decided whether applications need approval.
```

For personal use across projects, place the folder in `~/.claude/skills/task-brief/` instead. Choose one installation location for the skill.

**Optional: install with the skills CLI**

With Node.js and npm available, open a terminal in the extracted repository root and run:

```sh
npx skills add . --skill task-brief -a claude-code
```

Follow the installer prompts. The CLI also accepts GitHub repository URLs for remote installation; use this repository's actual URL as the source. See the [skills CLI documentation](https://github.com/vercel-labs/skills).

See [Claude Code skills documentation](https://code.claude.com/docs/en/skills) for client setup.

### What to expect

For the signup-page example, the response should restate the task, identify consequential gaps, and clarify scope and the intended deliverable. Whether applications require approval remains an open decision. The request is to clarify requirements before coding, so implementation waits.

When alignment is complete, the working definition states:

- The task and its purpose.
- The scope and constraints.
- The deliverable and its intended user.
- Observable completion criteria, plus unresolved decisions affecting the next step.

A confirmed definition and permission to execute are assessed separately.

### Six checks

1. Restate the task and intent; check for omissions.
2. Clarify the subject, scope, and deliverable.
3. Check whether the conversation is making progress, including necessary confirmation.
4. Make disagreements and incompatible requirements explicit.
5. Establish the definition and determine whether execution is authorized; make changes explicit.
6. Conclude alignment within four rounds for the same definition, keeping unresolved matters visible.

Six checks do not mean six rounds of questions. Clear single-step actions are handled directly. Already aligned tasks retain their definition, and existing information and authorization are reused. The response follows your language.

### Repository files

The repository root is the skill directory. It contains four files:

| File | Purpose |
|---|---|
| `SKILL.md` | Skill instructions and discovery description |
| `README.md` | Installation and usage |
| `LICENSE` | MIT license |
| `CHANGELOG.md` | Version history |

### Feedback

Open an issue in this repository with your task, the response, and what helped or added friction. Client/model details and how you invoked the skill help us understand the context. Remove private information before sharing.

Follow [Brenda Shi on X — @brenda_50555](https://x.com/brenda_50555) for human–AI collaboration and product practice. If Task Brief helps your work, a star helps others discover it.

## 中文

### 它解决什么问题

你还没说清要解决什么，AI 就开始写方案、做页面，结果方向不对，又要返工。Task Brief 用于复杂任务开工前：核清意图、对象、边界、交付要求和完成标准，发现遗漏、挑明分歧，再确定下一步。

适合规划、分析、写作、资料编纂和开发等任务。简报是对齐结果的呈现形式，做出一张表不是目的。

### 安装与第一次使用

在仓库页面选择 **Code → Download ZIP**，解压后，将直接包含 `SKILL.md` 的文件夹命名为 `task-brief`，再把这个文件夹放进你的项目的 `.claude/skills/` 目录。

最终路径应为 `.claude/skills/task-brief/SKILL.md`。在该项目中打开 Claude Code，输入：

```text
/task-brief 我想做一个活动报名页面，帮我先理清需求，先别写代码。
```

如需跨项目使用，可改放到 `~/.claude/skills/task-brief/`；选一种安装位置即可。

也可以在已安装 Node.js 和 npm 的环境中，进入解压后的仓库根目录，运行上方 `npx skills add . --skill task-brief -a claude-code` 命令，按提示安装。

仓库根目录就是技能目录，包含 `SKILL.md`、`README.md`、`LICENSE` 和 `CHANGELOG.md` 四个文件。

### 你会得到什么

AI 应说明它对任务的理解，指出关键遗漏，核清对象、边界与交付要求。报名是否需要审核等未定事项会保留为待决问题；你说了先别写代码，就先完成需求对齐。

对齐结束时，形成任务、边界、交付物和完成标准，并说明下一步是否可以执行。六步检查不等于六轮提问；同一任务定义最多四轮，条件满足就提前结束。简单任务直接处理，已对齐的任务沿用现有定义，不反复索要已有信息和批准。

遇到问题可在仓库 Issues 反馈：给出任务、实际回答和你认为有帮助或增加负担的地方，分享前去掉私人信息。

## Credits and license · 署名与许可

Created by **Brenda Shi · THROVIA**  
Published by **上海未见之地科技有限公司**

AI-assisted preparation, human-directed design and release decisions.  
AI 辅助准备；设计与发布决策由人主导。

Copyright (c) 2026 Brenda Shi. Licensed under the [MIT License](LICENSE).
