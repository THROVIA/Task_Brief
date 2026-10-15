<p align="center">
  <img src="assets/task-brief-header.svg" alt="Task Brief — Align before you build. An open-source agent skill by THROVIA." width="100%">
</p>

<p align="center">
  <a href="#quick-start">Quick start</a> &nbsp;·&nbsp;
  <a href="#a-real-project-example">Real example</a> &nbsp;·&nbsp;
  <a href="#how-it-works">How it works</a> &nbsp;·&nbsp;
  <a href="README.zh-CN.md">简体中文</a>
</p>

<p align="center"><strong>AI is ready to start. Is the task clear?</strong><br>
An agent skill for task clarification before complex work.</p>

---

Use Task Brief when the goal is still fuzzy, requirements conflict, or a change needs clarification before work continues. It is designed to help you and AI agree on the work before planning, writing, analysis, or development.

The quick start below uses **Claude Code**. The skill focuses on clarifying the task, including work that does not involve coding.

**Simple tasks stay simple. Already aligned work moves forward.** A brief records the agreement; filling out a template is not the goal.

## Why use a skill instead of saying “clarify first”?

For a straightforward task, that instruction may be enough. Task Brief packages more specific rules: check for omissions, make conflicting requirements explicit, and reuse decisions already established in the conversation.

The aim is to make the next action clearer while respecting what you have already decided. These are intended behaviors; the historical example below shows one concrete suggestion and the author's response.

## A real project example

**Record the relationships before drawing the diagram**

I was updating a file-management workflow. The timeline and relationship diagrams in an earlier version were easy to understand, and I wanted to preserve those strengths in the next version.

Before editing, the AI raised a point worth discussing:

**The diagrams worked because they showed where files came from, which files replaced others, and what depended on what.**

Alongside deciding how to draw the diagrams, it suggested adding an “upstream / replacement relationships” field to the file register, so those relationships would be explicitly recorded.

I agreed with that reasoning and accepted the proposed field.

**What changed through clarification:** “Keep the useful diagrams” became a more concrete requirement: “Record the relationships those diagrams convey.”

*Adapted and anonymized from the author's real project conversation in August 2026. The original used K14, an internal task-clarification protocol, alongside other collaboration rules. This is a condensed retelling, not a verbatim transcript or an independent test of the current open-source release.*

## Quick start

Install for **Claude Code** with Node.js and npm available:

```sh
npx skills add THROVIA/Task_Brief --skill task-brief -a claude-code
```

Follow the installer prompts, then try:

```text
/task-brief Before coding, help me clarify the requirements for a volunteer signup page. I have not decided whether applications need approval.
```

**What should a useful first run do?**

Look for a missing decision, a clearer trade-off, or a more concrete next step. Check whether it reuses details you already provided. If it only restates your request or repeats settled questions, that is useful feedback too—[share what happened](https://github.com/THROVIA/Task_Brief/issues).

<details>
<summary><strong>Try it on a task you already have</strong></summary>

Replace the brackets with your own task and decisions:

```text
/task-brief I am preparing to [specific task].
Already decided: [decisions and constraints].
Still unclear: [open questions].
Help me clarify the requirements and next step. Do not start executing yet.
```

This is a starting prompt, not a completed case or a fixed output format.

</details>

<details>
<summary><strong>Prefer a manual installation?</strong></summary>

1. Download this repository using **Code → Download ZIP** and extract it.
2. Rename the extracted folder containing `SKILL.md` to `task-brief` if needed.
3. Copy that folder into your project's `.claude/skills/` directory. The skill entry point should be `.claude/skills/task-brief/SKILL.md`.
4. Open Claude Code in the project and use the prompt above.

For personal use across projects, place the folder in `~/.claude/skills/task-brief/` instead. Choose one installation location.

</details>

[Skills CLI documentation](https://github.com/vercel-labs/skills) · [Claude Code skill setup](https://code.claude.com/docs/en/skills)

## In practice

**You bring an idea:** “I need a volunteer signup page.”

**Task Brief helps make it actionable:**

| Before starting | What to clarify |
| :--- | :--- |
| Purpose | Who is signing up, and for which activity? |
| Scope | Is this just a signup page, or also an approval workflow? |
| Deliverable | Do you need a requirements brief, a prototype, or working code? |
| Success criteria | What observable result would make the work complete? |
| Open decisions | Do applications need approval, and who decides? |

*Illustrative example, not a fixed response or a completed decision.*

If you asked to clarify before coding, implementation waits. The outcome is a shared working definition with unresolved decisions visible. A confirmed definition and permission to execute are assessed separately.

## How it works

Six checks guide the conversation. They do not require six rounds of questions.

1. **Understand the intent.** Restate the task and purpose; check for omissions.
2. **Define the work.** Clarify the subject, scope, and deliverable.
3. **Check progress.** Resolve consequential gaps and obtain necessary confirmation.
4. **Surface disagreements.** Make incompatible requirements explicit.
5. **Establish the definition.** Clarify execution authorization and make changes visible.
6. **Conclude alignment.** Within four rounds for the same definition, retain unresolved matters and establish the next step.

Existing information and authorization are reused. Clear single-step actions are handled directly. The response follows your language.

Read the full [skill instructions](SKILL.md).

## Project guide

The repository root is the skill directory.

| File | Purpose |
| :--- | :--- |
| [SKILL.md](SKILL.md) | Skill instructions and discovery description |
| [README.zh-CN.md](README.zh-CN.md) | 中文安装与使用说明 |
| [CHANGELOG.md](CHANGELOG.md) | Version and packaging history |
| [LICENSE](LICENSE) | MIT license |
| [assets/](assets/) | README artwork and THROVIA brand assets |

## Save, share feedback, or follow

- **Keep the skill handy.** Star this repository if you want to find it again.
- **Tell us what happened when you used it.** What did it catch—or ask again unnecessarily? [Open an issue](https://github.com/THROVIA/Task_Brief/issues) with a short, anonymized excerpt. Include the client/model, how you invoked the skill, and what changed in your next step. If you used it again on another task, tell us why; if you stopped using it, that is useful too.
- **Follow the thinking behind Task Brief.** Follow [Brenda Shi on X](https://x.com/brenda_50555) for human–AI collaboration and product practice. Task Brief is a THROVIA project.

Found a useful moment worth sharing? Include the original request, the key response, and the decision that followed. Remove private information and label edits or paraphrases; keep claims tied to what the conversation actually shows.

---

<img src="assets/throvia-lockup.svg" alt="未见之地 · THROVIA" width="200">

Created by **Brenda Shi · THROVIA**. Published by **上海未见之地科技有限公司**.

AI-assisted preparation; human-directed design and release decisions.

Copyright (c) 2026 Brenda Shi · THROVIA. Licensed under the [MIT License](LICENSE).
