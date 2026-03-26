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
