# Analects

Normalized leaf notes live directly in this directory. An analect is a small retrieval unit for author voice, durable claims, reusable phrasing, addressable facts, or event-bound recaps. Nested source collections stay under `raw/` until they are worth normalizing.

## Layout

- `analects/*.md` - normalized leaflets
- `analects/raw/` - source material not yet distilled into leaflets
- `analects/archive/` - superseded or historical material kept for reference

## File Contract

Filename convention:

```text
YYYY-MM-DD-<kind>-<slug>.md
```

Date forms:

| Date form | Meaning |
|---|---|
| `0000-00-00` | timeless / undated |
| `YYYY-00-00` | year known, month and day unknown |
| `YYYY-MM-00` | year and month known, day unknown |
| `YYYY-MM-DD` | fully dated |

Rules:

- `<kind>` and `<slug>` use underscores as internal separators.
- Segments are separated by hyphens.
- Keep the outer filename contract stable even when the internal policy changes.

## Kind Taxonomy

| Kind | What it holds |
|---|---|
| `fact` | atomic identity, role, education, leadership, URL, or other addressable data |
| `fragment` | reusable wording for a specific audience or prompt |
| `claim` | one bounded assertion |
| `description` | one explanatory concept or definition |
| `approach` | one method, stance, or operating decision |
| `reflection` | literary, poetic, personal, or metacognitive writing |
| `procedure` | instructions or workflow |
| `recap` | dated conversation, meeting, or event summary |

## Front Matter

Only these fields are standard, and only when they help retrieval:

```yaml
---
status: draft | stable | archived
audience: [proposal, investor, journalist, general, technical]
tags: [tag1, tag2]
related: [0000-00-00-kind-other_slug]
---
```

Optional exception:

- `superseded_by` when preserving the evolution between two dated notes is itself useful.

Do not keep empty fields.

## Normalization Rules

1. One analect, one retrieval job.
2. Canonical self/company representation must be first-person.
3. Third-person is still acceptable for external-person research, dated recaps, and quoted historical material.
4. Audience variants belong in separate `fragment` files. Link them through `related`; do not mix startup, customer, academic, and other postures into one compound note.
5. Roles, education, leadership, and founder/company positions should be one dated `fact` per item.
6. Use the dating rule for role-like facts:
   - ongoing item -> date from start
   - ended item -> date from end
7. URL identity surfaces stay one URL per file.
8. For current founder/company canon, prefer the YC founder profile and YC application whenever they conflict with older notes.
9. Literary and reflective bodies should remain unchanged except for non-substantive cleanup.
10. `Boundaries` is not a default internal section. If a limitation matters, express it as its own related leaflet instead of embedding a standard constraint block.

## Retrieval Guidance

- Keep author wording primary whenever the wording itself matters.
- Split mixed files by semantic function instead of preserving adjacency inside one note.
- Use `fact` for atomic retrieval, not for opinion or posture.
- Use `fragment` when the main value is reusable wording.
- Use `related` as the compound logic layer.
- Remove duplicate canonical URLs or repeated role facts from unrelated notes when they do not add retrieval value.

## Authority Rule

The YC founder profile and YC application are the current authority for:

- current founder/company role framing
- founder and company URLs
- education dates and degree names
- work history dates, titles, and short descriptions
- current commitment framing when older canon conflicts

Older contradictory notes can remain only when they still matter as dated history, recap, or preserved rhetoric. Otherwise, rewrite or archive them.

## Preservation-First

Normalization here is structural, not stylistic.

- rename, split, relink, and trim metadata
- preserve literary voice
- rewrite factual canon when the current authority changed
- avoid flattening reflective writing into summaries

Detailed workflow:

- [voice_preserving_normalization.md](/home/smohn/LCL/oeuvre/analects/voice_preserving_normalization.md)
