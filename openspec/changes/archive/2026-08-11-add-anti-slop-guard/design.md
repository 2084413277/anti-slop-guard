## Context

The repository distributes one portable Codex skill. The author requires explicit activation, direct governance, visible feedback, and narrow academic execution. The implementation needs readable rules and no runtime service.

## Goals / Non-Goals

**Goals:**

- Keep the activation boundary explicit and observable.
- Preserve the eight author-defined governance principles and the academic declarative-style rule.
- Keep operational detail in small references loaded only for relevant tasks.
- Support task-level and working-directory academic activation.
- Publish a public repository with clear installation and contribution guidance.

**Non-Goals:**

- Automatic activation from academic keywords or file types.
- A background process, hook, telemetry service, hash index, or artifact database.
- Automatic manuscript auditing, data propagation, or repository-wide verification.
- Replacement of platform-level constraints.

## Decisions

### Explicit activation in skill metadata

The `description` states the accepted activation conditions and explicitly excludes implicit routing from academic content. This keeps ordinary academic work unaffected until the author invokes the skill.

### Directory scope through visible project guidance

Working-directory activation uses an author-managed `AGENTS.md` instruction. This provides durable and reviewable scope. The repository creates no hidden activation state.

### Compact router with domain references

`SKILL.md` contains governance, activation, point-and-call execution, and reference routing. Detailed academic writing, code/data/operations, and figure rules live in `references/`. This structure limits context usage while keeping every rule readable.

### Conversation as the feedback channel

The visible conversation carries concerns and alternatives. Author artifacts carry authorized content. The implementation creates no feedback metadata or hidden commentary mechanism.

### Documentation requested by the author

The repository includes `README.md` because public installation, activation, governance, and contribution instructions form part of the requested open-source interface.

### MIT licensing

The MIT license supports broad reuse and modification while retaining a concise attribution requirement.

## Risks / Trade-offs

- [Explicit activation may be omitted] → README examples provide exact task and directory activation phrases.
- [A broad directory instruction may affect non-academic work] → The recommended `AGENTS.md` entry limits scope to academic activities.
- [Author rules can evolve] → User-identified defects authorize direct, visible amendments to the skill.
- [Other agents may overread governance language] → The skill states the platform boundary explicitly and keeps user-configurable precedence precise.
