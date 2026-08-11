# Anti-Slop Guard

`anti-slop-guard` is an explicitly activated Codex skill for author-directed academic writing, experimental data, code, scientific figures, and related operations.

The skill keeps author intent authoritative, limits changes to the named surface, places feedback in the visible conversation, and uses bounded verification.

## Activation boundary

The skill activates only through an explicit instruction for a designated academic activity.

Examples:

```text
$anti-slop-guard
启用该 skill 处理本次论文修改。
本次学术任务启用 anti-slop-guard。
该工作目录启用该 skill。
```

Academic keywords, manuscript files, datasets, figures, and code do not activate the skill by themselves.

## Installation

Clone the repository into a Codex skill directory:

```bash
git clone https://github.com/2084413277/anti-slop-guard.git ~/.codex/skills/anti-slop-guard
```

Project-local installation can use an agent-compatible skill directory:

```bash
git clone https://github.com/2084413277/anti-slop-guard.git .agents/skills/anti-slop-guard
```

Installation makes the skill available. Explicit activation remains required.

## Working-directory activation

Add a visible declaration to the academic project's `AGENTS.md`:

```markdown
## Academic activity

For academic activities in this working directory, enable `$anti-slop-guard`.
Apply it only within academic tasks identified by the user.
```

Chinese form:

```markdown
## 学术活动

本工作目录中的学术活动启用 `$anti-slop-guard`。
该规则仅适用于使用者明确指明的学术任务。
```

This declaration provides visible, author-managed directory scope. The skill creates no background service, global hook, hidden marker, or automatic activation state.

## Governing principles

1. **Author authority** — the author's stated problem, relationship, target, path, and boundary govern the work.
2. **Scoped experimental data** — data changes follow the author's exact instruction and carry no automatic downstream propagation.
3. **Semantic artifact identity** — filenames, paths, project references, history, and author mappings establish code and data relationships. Hash checks require explicit scope.
4. **Figure inspiration** — open ideation uses a small set of strong exemplars and distinct visual directions. Precise edits remain precise.
5. **Visible feedback** — concerns and alternatives appear in the conversation. Author artifacts contain authorized content.
6. **User governance** — the user's current instruction governs the skill. User-identified defects authorize direct amendment.
7. **Point-and-call execution** — the assistant restates the target, object, action, boundary, and path, then follows a clear author path fully.
8. **Explicit academic activation** — the skill operates only in the academic scope designated by the user.
9. **Academic declarative style** — academic narration uses direct positive propositions. Necessary negative findings use independent subject-verb-object sentences. Adversative negative constructions remain excluded.

## Point-and-call example

Author instruction:

```text
启用该 skill。更新 experiment_2.csv 中指定数据，并用它重绘 Figure 2。正文保持不动。
```

Assistant confirmation:

```text
指差确认：更新 experiment_2.csv 中作者指定的数据，并用该文件重绘 Figure 2；正文及其他实验保持不变。
```

Completion confirmation:

```text
已完成指定数据更新和 Figure 2 重绘；正文及其他实验未修改；验证限于指定文件与图形输出。
```

## Academic prose style

Preferred positive proposition:

```text
处理组在低氧条件下提高了蛋白 X 的表达水平。
```

Necessary independent negative statement:

```text
处理组在常氧条件下未改变蛋白 X 的表达水平。
```

The skill excludes `不是……而是……`, `并非……而是……`, negative setup followed by corrective contrast, and related adversative negative narration from generated academic prose.

## Repository structure

```text
anti-slop-guard/
├── SKILL.md
├── agents/openai.yaml
├── references/
│   ├── academic-writing.md
│   ├── code-data-operations.md
│   ├── figures.md
│   └── governance.md
├── openspec/
├── AGENTS.md
├── LICENSE
└── README.md
```

## Design references

- [BetterUp and Stanford Social Media Lab: Workslop](https://www.betterup.com/workslop)
- [Google Engineering Practices: Small CLs](https://google.github.io/eng-practices/review/developer/small-cls.html)
- [Google Engineering Practices: What to look for in a code review](https://google.github.io/eng-practices/review/reviewer/looking-for.html)
- [ICMJE: AI use by authors](https://www.icmje.org/recommendations/browse/artificial-intelligence/ai-use-by-authors.html)
- [Anthropic skills: document co-authoring](https://github.com/anthropics/skills/blob/main/skills/doc-coauthoring/SKILL.md)

These sources informed the initial design. The user's explicit rules govern the skill's active behavior.

## Contributing

Issues and pull requests are welcome. A proposed rule change should identify:

- the observed defect;
- the affected author workflow;
- the intended corrected behavior;
- one concrete example that distinguishes the corrected behavior.

## License

[MIT](LICENSE)
