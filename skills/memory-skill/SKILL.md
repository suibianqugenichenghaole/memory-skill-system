---
name: memory-skill-public
description: Use when work requires recalling, continuing, classifying, or updating memory across ongoing formal work, personal projects, or reusable methods. Triggers on requests like continuing the same requirement/version/project, writing follow-up requirement docs, recalling prior decisions or context, updating memory after important progress, answering finalized requirement questions, or reusing past creative/project context. Helps route memory by permission, domain, anchor, and type while preventing unsafe context mixing.
---

# Memory Skill

Use memory as a working system, not a chat recap.

## Core goal

Do four things well:
1. find the right memory quickly
2. avoid mixing contexts
3. continue work instead of merely recalling it
4. write back only what will matter later

## Core routing model

Before doing anything else, classify memory along these four axes.

### 1) Permission layers (P)
- `P1` Private — private personal context; do not expose by default
- `P2` Internal — internal analysis, drafts, unannounced work
- `P3` Public — confirmed wording safe to repeat to team/public work contexts
- `P4` Meta — reusable methods, norms, patterns, and experience

### 2) Domains (D)
- `D1` Formal-work — employed work, formal collaboration, requirements, versions, Q&A
- `D2` Personal-projects — personal projects, content creation, private experiments

### 3) Anchors (A)
- `A-work` — current formal-work anchor
- `A-content` — content creation / personal creative work
- `A-openclaw` — OpenClaw usage, configuration, and method evolution

### 4) Types (T)
- `T1` Facts — stable facts
- `T2` Confirmed — confirmed conclusions
- `T3` Discussion — draft/process content
- `T4` Repeated — repeated questions or misunderstandings
- `T5` Transferable — reusable experience and methods

## Default routing

### Formal work
- internal analysis / unreviewed requirement work → `P2-D1-A-work`
- finalized wording / team-safe answer → `P3-D1-A-work`
- reusable requirement methods → `P4`

### Personal projects
- personal project / creative context → `P1/P2-D2-A-content`
- reusable creative methods → `P4`

### Tooling or operating context
- tool usage, configuration, and operating lessons → prefer `A-openclaw`

## Main route 1: Requirement continuation

Use when continuing the same requirement/version/project, writing follow-up requirement docs, or recalling prior decisions.

### Read in this order
1. current conversation context
2. main requirement record
3. abstract anchors or companion pointers inside that main record
4. only then expand to relevant sibling/detail records if the question still has a gap
5. related version records if needed
6. relevant `P4` method rules if useful

### Minimum recall set
Recall these first:
- background
- goal
- scope/module
- current stage
- confirmed rules
- unresolved points
- version delta

If the task clearly involves pages/flows, also recall:
- key scenarios
- state transitions
- multi-end handoff points

### Write back when useful
Prefer writing back only:
- newly confirmed rules
- meaningful edge cases / scenarios
- stage changes
- version deltas
- context needed to continue later

---

## Main route 2: Personal creation

Use when continuing a personal topic, structure, content direction, or creative workflow.

### Read in this order
1. current project/topic record
2. related direction/structure records
3. reusable method records

### Minimum recall set
- direction
- audience
- current stage
- proven effective patterns
- proven ineffective patterns

### Write back when useful
- direction changes
- structure results
- effective patterns
- ineffective patterns
- stable methods worth abstracting to `P4`

### Safety rule
Do not casually mix personal-project memory into formal-work contexts.

---

## Main route 3: Finalized requirement Q&A

Use when answering developers, coworkers, or group/version questions about already-settled work.

### Read in this order
1. `P3` public wording if available
2. confirmed requirement records
3. `P2` internal background only if necessary
4. relevant `P4` explanation methods

### Output rule
Default to using only:
- `P3`
- `P4`

Use `P2` only as internal support, not as directly exposed wording.
Do not expose `P1` or personal-project context.

---

## Memory write rules

Write memory when it will help future work continue.
Do not write every chat fragment.

Prefer storing:
- stable context
- confirmed conclusions
- stage changes
- recurring constraints
- reusable methods

Avoid durable storage for:
- one-off chatter
- temporary emotion
- weak guesses
- fragments with no reuse value

When the same confusion appears repeatedly, do not only store the raw question.
Try to extract the underlying gap and store it as `P4-T4` or `P4-T5` when reusable.

## Retrieval-friendly writing rules

Do not assume search will always infer everything from loose phrasing.
If a memory entry should be reliably found later, write it in a retrieval-friendly way.

### 1) One topic = one canonical anchor
For each ongoing topic, choose exactly one canonical anchor name.
Use that same anchor repeatedly instead of switching between near-synonyms.

Good pattern:
- Canonical anchor: `project-x`
- Aliases: `x workflow`, `project x`, `x-system`

Bad pattern:
- one file uses project name
- another uses package name
- another uses repo name
- no place declares which one is primary

### 2) Write aliases explicitly
If a topic is likely to be referred to by different names, add an explicit alias line.
Do not rely on future semantic search to infer all variants.

Recommended alias sources:
- project name
- repo name
- package / delivery name
- skill name
- user shorthand

### 3) Use a fixed summary block for important entries
For durable entries, prefer a compact block with stable labels.

Recommended fields:
- `Topic:` canonical anchor
- `Aliases:` common alternative names
- `Domain:` one of the memory domains
- `Permission:` safest intended layer
- `Stage:` current stage/status
- `Confirmed:` confirmed facts or conclusions
- `Pointers:` where detailed artifacts live
- `Next:` likely next step

This should stay concise. The goal is reliable continuation and retrieval, not verbose journaling.

### 4) Separate the main object from its derivatives
Do not mix these layers without labeling them:
- the main project/topic
- related skills
- repo/publication names
- package/delivery artifacts
- one-off bug-fix or shipping events

### 5) Prefer summary + pointer over scattered detail
If detailed project assets already exist elsewhere, memory should record:
- what this thing is
- what stage it is in
- what is already confirmed
- where the detailed material lives
- what to continue next

Do not spread the same topic across multiple daily notes with no canonical summary.

### 6) Promote repeated/important topics upward
If a topic is likely to be revisited across days, do not leave it only in a transient chat summary or one-off bug log.
Create or update at least one durable memory entry that uses the canonical anchor and summary block.

### 7) Name once, reuse everywhere
When you choose a canonical anchor, reuse that exact string in:
- memory summaries
- follow-up notes
- companion meta notes
- related project summaries when reasonable

Consistency is part of retrieval quality.

## Recommended durable-entry template

Use this when a topic is likely to be revisited across days or needs reliable retrieval.
Keep it short.

```md
## Topic summary — <human-readable title>
- Topic: `<canonical-anchor>`
- Aliases: `<alias-1>`, `<alias-2>`, `<alias-3>`
- Domain: `<domain-anchor>`
- Permission: `<P-layer>`
- Stage: <current stage in one line>
- Confirmed:
  - <confirmed point 1>
  - <confirmed point 2>
  - <confirmed point 3>
- Pointers:
  - `<path-or-artifact-1>`
  - `<path-or-artifact-2>`
- Next:
  - <next likely continuation step>
```

### Minimal fill rule
If you are in a hurry, do not skip the whole entry.
At minimum, fill:
- `Topic`
- `Aliases`
- `Stage`
- `Confirmed`
- `Pointers`

A short structured entry is better than a long unstructured recap.

---

## Shared-context safety

In groups or coworker-facing contexts, default to:
- `P3`
- `P4`

Be conservative with `P2`.
Never surface `P1`.
When uncertain, answer conservatively and mark what still needs confirmation.

---

## Relationship to PM workflow

This memory skill does not replace PM workflow project assets.

### PM workflow project assets manage
- requirement artifacts
- demo artifacts
- embedded PRD artifacts
- versions, snapshots, and baselines

### Memory manages
- concise continuation context
- durable summaries
- reusable methods
- safe routing across contexts

Short version:
- project assets = detailed operational layer
- memory = summary and continuation layer

When detailed project assets already exist, prefer storing summary + pointer in memory instead of duplicating the full artifact set.

---

## No-embeddings / FTS-only fallback mode

If memory search is effectively running without embeddings (for example `provider: none` or `mode: fts-only`), do not pretend semantic recall still works normally.

### Operating assumptions in this mode
- retrieval is much closer to keyword / anchor matching than semantic recall
- canonical anchor naming becomes critical
- explicit aliases matter more than usual
- scattered mention-only logs are much easier to lose

### Writing rules in this mode
- always include one canonical `Topic`
- always include explicit `Aliases` for likely user phrasing variants
- prefer durable summary entries over process-only scattered notes
- reuse the exact anchor string across follow-up notes
- keep `Pointers` explicit so file-based fallback lookup is easy

### Reading / answering rules in this mode
- try memory search first if required by policy, but do not overtrust an empty result
- if search returns empty, say you checked and then fall back to anchor/keyword/file lookup
- prefer exact project names, package names, file names, and stable section titles
- ask for the most likely anchor term if the wording is vague

### User guidance in this mode
When helpful, ask for one of these:
- canonical topic name
- package / repo / skill name
- likely file name
- distinctive phrase used in the saved summary

Short version:
without embeddings, memory can still work, but it must be written and queried more explicitly.

## Fallback rule

If unsure where to look or write:
1. check the nearest business/project main record first
2. then check the relevant method record
3. use the safest layer for output
4. ask the smallest clarifying question if needed

## Iteration rule

Keep this skill lean.
Update it only when real usage repeatedly shows that:
- the same routing mistake keeps happening
- the same context is repeatedly missing
- a rule is too vague to execute reliably
- a section adds friction without helping

Prefer small edits driven by real usage over speculative expansion.
