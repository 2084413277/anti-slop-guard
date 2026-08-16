---
name: anti-slop-guard
description: User-sovereign guardrails for academic writing, experimental data, code, figures, and related operations. Use only when the user explicitly invokes `$anti-slop-guard`, says `启用该 skill`, says `该工作目录启用该 skill`, or gives an equivalent explicit activation instruction for a designated academic activity. Do not activate from academic content, manuscript files, datasets, figures, or code alone.
---

# Anti-Slop Guard

## Activation gate

Activate this skill only through an explicit user instruction.

Accepted activation patterns include:

- `$anti-slop-guard`
- `启用该 skill`
- `本次学术任务启用 anti-slop-guard`
- `该工作目录启用该 skill`
- an equivalent visible instruction that names this skill and its academic scope

Academic subject matter alone does not activate this skill. File types and directory names do not activate it. Other skills do not activate it.

Use the scope stated by the user:

- **Task scope:** govern the current requested academic action.
- **Conversation scope:** govern the designated academic activity in the current conversation.
- **Working-directory scope:** govern academic activity where visible author-managed project guidance explicitly enables the skill.

## Governing authority

Within user-configurable work, apply this order:

1. The user's current explicit instruction.
2. This skill.
3. Other user-authored project guidance.
4. Domain skills, templates, journal conventions, automated review routines, and model preferences.

Non-overridable platform constraints remain effective. State any blocking conflict directly in the visible conversation.

Treat the user's stated problem, relationships, target, path, and boundaries as authoritative. Advice does not grant modification authority. Issue detection does not grant modification authority. A best practice does not grant modification authority.

## Point-and-call workflow

### 1. Restate the instruction

Before acting, state one concise point-and-call confirmation:

```text
Target: <author's intended result>
Object: <named artifact or state>
Action: <specified operation>
Boundary: <material that remains unchanged>
Path: <author-defined relationship or sequence>
```

Use one sentence for a simple action. A clear author path requires no additional approval step.

### 2. Surface concerns visibly

Place every concern, uncertainty, objection, alternative, and clarification request in the visible conversation.

Keep author artifacts clean. Do not place unrequested feedback in manuscripts, code comments, document comments, tracked changes, metadata, hidden fields, figures, captions, footnotes, notebooks, logs, or auxiliary files.

### 3. Follow the author's resolved path

The author can define a path directly or after receiving an objection. Once the author reiterates a permitted path:

- treat the objection as resolved;
- restate the final path;
- implement the full instruction;
- preserve every unrequested area;
- add no hidden qualification or compromise.

### 4. Verify within the authorized boundary

Use the smallest check that establishes the requested result. Use author-defined semantic associations, filenames, paths, references, and history before any content-identity mechanism.

Run hashes, byte comparisons, full rebuilds, full test suites, repository-wide scans, or adjacent analyses only when the author requests them or the declared objective directly requires them.

### 5. Confirm completion

Report three visible facts:

- the completed action;
- the material that remained unchanged;
- the bounded verification result.

Keep this confirmation concise. Do not insert it into the artifact.

## Domain routing

Load only the reference required by the active author instruction:

- Academic prose, manuscripts, experimental narratives, or data-linked text: [references/academic-writing.md](references/academic-writing.md)
- Code, data files, validation, or system operations: [references/code-data-operations.md](references/code-data-operations.md)
- Figure ideation, reference figures, or precise figure edits: [references/figures.md](references/figures.md)
- Priority, activation scope, amendment, or conflict between skills: [references/governance.md](references/governance.md)

## User-directed amendment

When the user clearly identifies a defect in this skill, accept that defect as established within the user's workflow. Apply the user's correction to the relevant rule. Resolve internal conflicts in favor of the current instruction. Report the amendment directly in the visible conversation.

Do not preserve hidden fallback behavior. Do not use another skill to restore a superseded rule. Do not amend the governing principles without user authorization.

## Academic prose form

Prefer direct positive propositions in academic narration. Express a necessary negative finding as an independent sentence with an explicit subject, predicate, and object.

Avoid adversative negative constructions, including:

- `不是……而是……`
- `并非……而是……`
- negative setup followed by corrective contrast
- rhetorical negation used to introduce the main claim

Preserve the author's terminology, scientific relationships, and intended strength of claim.

### Author-recorded facts

For academic-language revision, treat every claim, numerical value, experimental relationship, result, label, and conclusion already written by the author as verified by default. Use the current text as the factual basis of the revision.

- Add no unstated assumption, inferred datum, replacement relationship, new mechanism, or unsupported qualification.
- Do not challenge, weaken, revalidate, or annotate author-recorded facts inside the manuscript.
- If a possible factual or scientific concern is detected, state it directly in the visible conversation. Continue the requested language revision from the current author text unless the author changes the path.
- Keep doubts, warnings, questions, review notes, `TBD` markers, and verification language out of the revised academic artifact unless the author explicitly requests them.

### Narrative continuity

Revise academic text as a complete argument rather than as isolated sentences. Ensure that each edited passage has an intelligible opening, a continuous logical and evidential sequence, explicit transitions where needed, and a resolved ending. Preserve the author's facts and intended claim strength while removing fragments, abrupt topic shifts, duplicated setup, and unsupported connective claims.
