<p align="center">
  <img src="assets/task-brief-header.svg" alt="Task Brief · 开工前对齐 — 复杂任务开始前，先把问题说清楚" width="100%">
</p>

<p align="center">
  <a href="#快速开始">快速开始</a> ·
  <a href="#更多使用场景">更多场景</a> ·
  <a href="#为什么使用-task-brief">规则特点</a> ·
  <a href="README.md">English</a>
</p>

# Task Brief · 开工前对齐

**AI 已经准备开工，你们说的是同一件事吗？**

Task Brief 是一款开源的任务对齐 Skill，帮助你和 AI 发现遗漏、挑明分歧，明确任务范围、交付要求和下一步，并沿用当前对话中已经确认的决定。

适用于规划、写作、分析、资料整理和开发。可在 **Codex、Claude Code 等支持 Agent Skills 的工具**中使用。

**简单任务直接处理，已对齐的工作继续推进。** 简报记录对齐结果，填表本身不是目标。

## 快速开始

选择你使用的工具。以下为本地安装方式，需要先安装对应客户端；命令行安装还需 Node.js 和 npm。没有 Node.js？可使用下方的手动安装。

### Codex

在终端运行，安装到个人范围：

```sh
npx skills add THROVIA/Task_Brief --skill task-brief -a codex -g
```

按提示完成安装后，在 Codex CLI 或 IDE 扩展的**对话输入框**输入以下内容；也可以通过 `/skills` 选择 `task-brief`：

```text
$task-brief 我准备写一份新员工入职指南。
已经确定：面向第一次加入团队的人，控制在两页以内。
请先帮我发现遗漏、说清范围和交付要求，再确定下一步；这轮先不写正文。
```

### Claude Code

在终端运行，安装到个人范围：

```sh
npx skills add THROVIA/Task_Brief --skill task-brief -a claude-code -g
```

按提示完成安装后，在 Claude Code 的**对话输入框**输入：

```text
/task-brief 我准备写一份新员工入职指南。
已经确定：面向第一次加入团队的人，控制在两页以内。
请先帮我发现遗漏、说清范围和交付要求，再确定下一步；这轮先不写正文。
```

只想用于当前项目？在项目目录运行安装命令时去掉 `-g`。

### 第一次怎样算有帮助？

看它是否指出了一个影响结果的遗漏、说明了要求之间的冲突或取舍，或者让下一步更明确；也看它是否沿用了你已经提供的信息。

如果只是复述任务、重复问已确定的问题，这同样值得[提交反馈](https://github.com/THROVIA/Task_Brief/issues)。以上输入是使用示例，不是运行结果。

<details>
<summary><strong>手动安装</strong></summary>

1. 在仓库页面选择 **Code → Download ZIP** 并解压。
2. 将直接包含 `SKILL.md` 的文件夹命名为 `task-brief`。
3. 选择一个安装位置，放入该文件夹：

| 工具 | 个人使用，跨项目 | 仅当前项目 |
| :--- | :--- | :--- |
| Codex | `~/.agents/skills/task-brief/` | `.agents/skills/task-brief/` |
| Claude Code | `~/.claude/skills/task-brief/` | `.claude/skills/task-brief/` |

最终结构应是所选目录下直接存在 `SKILL.md`，不要重复套一层 `task-brief`。`~` 表示用户主目录。重新打开对应客户端，使用上方调用示例。

</details>

<details>
<summary><strong>其他支持 Agent Skills 的工具，或手动使用规则</strong></summary>

其他支持 Agent Skills 的工具：按该工具的技能安装说明导入包含 `SKILL.md` 的目录，并使用其调用方式。

普通 AI 对话：可以打开 [SKILL.md](SKILL.md)，把指令正文复制到新对话，明确要求 AI 按这些规则处理随后提供的任务。这是手动提供规则，不是原生 Skill 安装；加载方式与执行表现取决于所用工具和模型。

</details>

[Skills CLI 文档](https://github.com/vercel-labs/skills) · [Codex 技能说明](https://learn.chatgpt.com/docs/build-skills) · [Claude Code 技能说明](https://code.claude.com/docs/en/skills)

## 更多使用场景

选择 `task-brief` 后，可以把下面任一请求作为任务内容；手动输入调用名时，Codex 使用 `$task-brief`，Claude Code 使用 `/task-brief`。

**分析：**

```text
我想分析最近客户咨询减少的原因。
已经有三个月的咨询记录，但来源标记不完整。
先帮我明确分析对象、能回答的问题和需要补充的信息，再确定下一步；这轮先不下结论。
```

**开发：**

```text
我想做一个志愿者活动报名页。
已经确定：不收费，最多30人；报名是否需要审核还没决定。
先帮我明确需求、关键取舍和下一步，先别写代码。
```

也可以换成你正在规划的项目、准备的文稿或整理的资料。提供你已有的条件即可，不必先把所有问题都想明白。上述请求均为输入示例，没有预设输出。

## 为什么使用 Task Brief？

**发现还没说清的，沿用已经确认的。**

对简单任务，一句“先对齐”可能已经足够。Task Brief 把复杂任务中的协作要求整理成可复用规则：主动检查遗漏，明确对象、范围、交付物和完成标准，挑明不兼容的要求，并沿用当前对话中已有的信息与授权。

它同时约束澄清过程：简单任务不套完整流程，已对齐的任务只检查变化，同一任务定义最多四轮；到限时说明未决事项与下一步，不把轮数用完当成问题已经解决。

确认任务定义与授权执行分别判断。已有明确授权会被沿用；你要求“先讨论”时，就停在讨论范围。

完整六步规则见 [SKILL.md](SKILL.md)。

## 方法来源：一次历史项目对话

**从“保留好用的图”，到“记录图表达的关系”。**

我在更新一套文件管理流程，希望保留旧版直观的时间线与关系图。讨论中，AI 提出：图之所以好懂，是因为它说清了谁来自谁、谁替代谁、谁是谁的上游。因此，除了考虑图怎么画，还应在文件登记表中补上“上游／替代关系”字段。

我认可了这个判断，并同意增加该字段。这让接下来具体要修改什么变得更明确。

*根据作者 2026 年 8 月的真实对话脱敏、压缩改写。当时同时使用早期任务对齐规则及其他协作指令；这是方法来源，不是当前开源版的运行记录。*

## 项目文件

仓库根目录就是技能目录。

| 文件 | 用途 |
| :--- | :--- |
| [SKILL.md](SKILL.md) | 技能指令与发现描述 |
| [README.md](README.md) | 英文安装与使用说明 |
| [CHANGELOG.md](CHANGELOG.md) | 版本与文档修订记录 |
| [LICENSE](LICENSE) | MIT 许可证 |
| [assets/](assets/) | README 视觉素材与 THROVIA 品牌资产 |

## 收藏、反馈与关注

- **收藏工具：**给仓库点亮 Star，方便以后找到。
- **反馈使用：**[提交 Issue](https://github.com/THROVIA/Task_Brief/issues)，告诉我们它发现了什么，或重复问了什么。附一小段脱敏对话、客户端与模型，以及下一步因此发生的变化即可。再次使用或停止使用的原因也很有价值。
- **关注后续实践：**关注 [Brenda Shi 的 X](https://x.com/brenda_50555)，交流人机协作、产品设计与使用中的具体发现。

---

<img src="assets/throvia-lockup.svg" alt="未见之地 · THROVIA" width="200">

创作者：**Brenda Shi · THROVIA**。发布方：**上海未见之地科技有限公司**。

AI 辅助准备；设计与发布决策由人主导。

Copyright (c) 2026 Brenda Shi · THROVIA。采用 [MIT 许可证](LICENSE)。
