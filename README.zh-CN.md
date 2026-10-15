<p align="center">
  <img src="assets/task-brief-header.svg" alt="Task Brief · 开工前对齐 — THROVIA 出品的开源 AI 技能" width="100%">
</p>

<p align="center">
  <a href="#快速开始">快速开始</a> &nbsp;·&nbsp;
  <a href="#真实项目案例">真实案例</a> &nbsp;·&nbsp;
  <a href="#如何工作">如何工作</a> &nbsp;·&nbsp;
  <a href="README.md">English</a>
</p>

<p align="center"><strong>说清目标 · 明确边界 · 确认交付</strong><br>
Task Brief · 开工前对齐：帮助你与 AI 在复杂任务开始前，先把问题说清楚。</p>

---

你还没说清要解决什么，AI 就开始写方案、做页面，结果方向不对，又要返工。Task Brief 帮你核清意图、对象、边界、交付要求和完成标准，发现遗漏、挑明分歧，再确定下一步。

适合规划、分析、写作、资料编纂和开发。**简单任务直接处理，已对齐的工作继续推进。** 简报记录对齐结果，填表本身不是目标。

## 真实项目案例

**先说清关系，再考虑怎么画图**

我在更新一套文件管理流程。旧方案里的时间线和关系图很直观，希望新版也能保留这些优点。

在动手修改前，AI 提出了一个值得讨论的判断：

**图之所以好懂，是因为它说清了：谁来自谁、谁替代谁、谁是谁的上游。**

因此，除了考虑图怎么画，还应在文件登记表中补上“上游／替代关系”字段，让这些关系有明确的记录。

我认可了这个判断，并同意增加该字段。

**这轮对齐带来的具体变化：把“保留好用的图”，进一步明确为“记录图所表达的关系”。**

*根据作者 2026 年 8 月的真实项目对话脱敏、压缩改写。原对话同时使用 K14（内部任务对齐协议）与其他协作规则；不是逐字聊天记录，也不是当前开源版的独立测试。*

## 快速开始

已安装 Node.js 和 npm 时，可通过以下命令安装到 **Claude Code**：

```sh
npx skills add THROVIA/Task_Brief --skill task-brief -a claude-code
```

按提示完成安装后，在 Claude Code 中输入：

```text
/task-brief 我想做一个志愿者活动报名页，帮我先理清需求，先别写代码。我还没决定报名是否需要审核。
```

<details>
<summary><strong>也可以手动安装</strong></summary>

1. 在仓库页面选择 **Code → Download ZIP** 并解压。
2. 将直接包含 `SKILL.md` 的文件夹命名为 `task-brief`。
3. 把该文件夹放入项目的 `.claude/skills/` 目录，最终入口为 `.claude/skills/task-brief/SKILL.md`。
4. 在该项目中打开 Claude Code，输入上面的示例提示。

如需跨项目使用，可放到 `~/.claude/skills/task-brief/`；选择一种安装位置即可。

</details>

[Skills CLI 文档](https://github.com/vercel-labs/skills) · [Claude Code 技能配置](https://code.claude.com/docs/en/skills)

## 使用示例

**你带来一个想法：**“我需要一个志愿者活动报名页。”

**Task Brief 帮你把它变成可以执行的任务：**

| 开工前 | 需要说清的问题 |
| :--- | :--- |
| 目标 | 谁来报名？参加什么活动？ |
| 边界 | 只做报名页，还是也包括审核流程？ |
| 交付物 | 需要需求说明、页面原型，还是可以运行的代码？ |
| 完成标准 | 看到什么可验证的结果，才算完成？ |
| 待决事项 | 报名是否需要审核？由谁决定？ |

*以上为使用示意，不是固定输出格式，也不代表这些事项已经决定。*

你说了先别写代码，就先完成需求对齐。对齐后形成共同认可的任务定义，并保留未解决的问题。确认任务定义与授权执行是两件需要分别判断的事。

## 如何工作

六项检查帮助对话推进，不等于六轮提问。

1. **核清意图。** 复述任务与目的，检查遗漏。
2. **定义工作。** 明确对象、范围与交付物。
3. **检查进展。** 处理关键缺口，取得必要确认。
4. **挑明分歧。** 将不兼容的要求摆到明面上。
5. **建立定义。** 判断执行是否已获授权，让变化明确可见。
6. **收束对齐。** 同一任务定义最多四轮，保留未决事项并明确下一步。

已有信息和授权会被沿用；清楚的单步任务直接处理。回复跟随你的语言。

完整规则见 [SKILL.md](SKILL.md)。

## 项目文件

仓库根目录就是技能目录。

| 文件 | 用途 |
| :--- | :--- |
| [SKILL.md](SKILL.md) | 技能指令与发现描述 |
| [README.md](README.md) | 英文安装与使用说明 |
| [CHANGELOG.md](CHANGELOG.md) | 版本与目录修订记录 |
| [LICENSE](LICENSE) | MIT 许可证 |
| [assets/](assets/) | README 视觉素材与 THROVIA 品牌资产 |

## 反馈

欢迎[提交 Issue](https://github.com/THROVIA/Task_Brief/issues)：描述任务、实际回复，以及哪些地方有帮助或增加了负担；附上所用客户端、模型与调用方式。分享前请去掉私人信息。

关注 [Brenda Shi 的 X](https://x.com/brenda_50555)，交流人机协作与产品实践。如果 Task Brief 对你有帮助，也欢迎点亮 Star。

---

<img src="assets/throvia-lockup.svg" alt="未见之地 · THROVIA" width="200">

创作者：**Brenda Shi · THROVIA**。发布方：**上海未见之地科技有限公司**。

AI 辅助准备；设计与发布决策由人主导。

Copyright (c) 2026 Brenda Shi · THROVIA。采用 [MIT 许可证](LICENSE)。
