# Voice-Preserving Analect Normalization

This guide defines how to normalize `analects/*.md` without flattening the author's voice. The repository contract lives in `README.md`. This document explains how to preserve language while still making the collection easier for retrieval and reuse.

## Core Principle

Preserve the author's language unless there is a concrete retrieval reason to change it.

Good normalization:

- rename a file to fit the contract
- split one mixed note into several cleaner leaflets
- remove redundant metadata
- relink related notes
- rewrite factual canon when a stronger current authority exists
- fix broken Markdown or obvious copy errors when meaning does not change

Bad normalization:

- paraphrasing literary or reflective writing into flatter prose
- converting first-person self-representation into generic third-person copy
- keeping several audience postures in one file because they happen to be adjacent
- preserving an outdated canon note after a stronger current source contradicts it

## Governing Rules

1. One leaflet should do one retrieval job.
2. Canonical self/company notes must be first-person.
3. Third-person remains acceptable for external research, recaps, and quoted source material.
4. Roles, education, leadership, and URL identity surfaces should be atomic `fact` files.
5. Use separate `fragment` files for audience-specific wording.
6. Use `related` to connect concept, fact, and audience leaflets.
7. Do not rely on a standard `Boundaries` section inside canonical notes. If a limitation matters, store it as its own related leaflet.
8. Treat the YC founder profile and YC application as the current authority for founder/company canon when they conflict with older notes.

## Preservation Classes

### Class A: Frozen Literary / Poetic

Use for writing whose line breaks, rhythm, or imagery are part of the meaning.

Rules:

- do not rewrite the body
- do not normalize line breaks
- add only light scaffolding around the text when needed

Typical kinds:

- `reflection`
- `fragment` only when the text is intentionally reusable as wording

### Class B: Voice-Preserved Reflective / Philosophical

Use for personal essays, worldview notes, and reflective prose.

Rules:

- preserve original sentences where possible
- add routing context outside the body
- split only when the note is clearly doing multiple jobs

Typical kinds:

- `reflection`
- `claim`
- `approach`

### Class C: Reusable Prose

Use for bios, application answers, pitch language, scholarship text, or audience-specific wording.

Rules:

- preserve reusable wording when it is already good
- separate audience variants into sibling `fragment` files
- keep each fragment narrowly scoped to one prompt or audience

Typical kind:

- `fragment`

### Class D: Technical / Factual / Procedural

Use for identity facts, role history, definitions, processes, and operational instructions.

Rules:

- prefer precise first-person factual wording for self/company canon
- keep one role, one URL, one degree, or one leadership item per file
- keep dates explicit when the fact can drift

Typical kinds:

- `fact`
- `description`
- `procedure`

### Class E: Recap / Historical Synthesis

Use for meetings, correspondence, interviews, or prior agent sessions.

Rules:

- preserve event context
- extract durable sibling notes only when they stand on their own
- do not treat recap language as timeless canon unless it is separately affirmed

Typical kind:

- `recap`

## Canonical Authority

For current founder/company canon, prefer the YC founder profile and YC application over older repository wording when they disagree. This includes:

- degree names and dates
- work history dates, titles, and short descriptions
- founder/company URLs
- current founder/company role framing
- current commitment and company-stage phrasing

If an older contradictory file still matters historically, archive it or mark it as superseded. If it does not, rewrite or delete it.

## Role And URL Normalization

Use `fact` for atomic identity surfaces:

- one role per file
- one education item per file
- one leadership item per file
- one URL per file

Dating rule:

- ongoing item -> filename date is the start date
- ended item -> filename date is the end date

Examples:

- `2025-11-00-fact-fruitful_network_development_founder_ceo.md`
- `2023-08-00-fact-university_of_akron_bs_applied_mathematics.md`
- `0000-00-00-fact-dylan_montgomery_github.md`

## Audience Variants

When the same underlying concept needs different wording for different audiences:

1. keep or create one smaller canonical concept note
2. create one `fragment` per audience or prompt
3. connect them with `related`

Do not keep one large file that mixes startup, customer, academic, and resume language together.

## Workflow

### 1. Read Before Editing

Identify:

- the note's real retrieval job
- whether the wording itself is part of the value
- whether the file is canonical self/company representation
- whether a stronger current authority already exists

### 2. Decide Whether The File Is Canonical

Canonical self/company files should be rewritten into first-person when needed.

Non-canonical files may remain third-person if they are:

- external research
- dated recap
- preserved historical wording

### 3. Choose The Correct Kind

- `fact` for atomic retrieval
- `fragment` for reusable wording
- `claim` for one assertion
- `description` for one explanatory concept
- `approach` for one method or operating decision
- `reflection` for literary/personal writing
- `procedure` for instructions
- `recap` for dated event synthesis

### 4. Clean Metadata

Keep only useful standard fields:

- `status`
- `audience`
- `tags`
- `related`
- `superseded_by` when needed

### 5. Split By Function

Split when one file combines:

- factual canon and audience wording
- dated recap and timeless claim
- multiple audience postures
- technical description and fundraising pitch
- role bundles that hide several canonical items

### 6. Preserve Voice Where It Matters

- literary bodies stay intact
- reflective wording stays intact unless the canon itself is wrong
- factual self/company canon may be rewritten for precision, current authority, and first-person consistency

## Default Outcome

The preferred end state is a lossless collection of smaller leaflets that:

- preserve author voice
- store current founder/company canon cleanly
- expose audience variants as separate fragments
- let retrieval compose meaning through `related` instead of through oversized mixed notes
