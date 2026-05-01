# Analects

Normalized leaf notes live directly in this directory. Nested raw collections (`raw/technical/`, `raw/corespond/`) remain in place for later normalization work.

## Layout

- `analects/*.md` — the normalized single-file note collection
- `analects/raw/_template.snippet.md` — starter template for new entries
- `analects/raw/technical/` and `analects/raw/corespond/` — nested source collections not yet normalized
- `analects/archive/` — archival reference material

## Filename Convention

```
YYYY-MM-DD-<kind>-<slug>.md
```

| Date form | Meaning |
|---|---|
| `0000-00-00` | Timeless / undated |
| `YYYY-00-00` | Year known, month and day not |
| `YYYY-MM-DD` | Fully dated |

Rules:
- `<kind>` and `<slug>` use underscores as internal separators.
- Segments are separated by hyphens.
- `<kind>` must be one of the seven values in the taxonomy below.

## Kind Taxonomy

| Kind | What it holds |
|---|---|
| `fact` | Atomic addressable data: URLs, GPA, skills, role titles, contacts |
| `claim` | Assertive statement with reasoning — argues something is true |
| `description` | Definitional — "what is X" |
| `approach` | Operating stance, strategy, posture — "how we do it" |
| `reflection` | Personal, literary, metacognitive writing |
| `fragment` | Reusable prose for applications, bios, proposals |
| `procedure` | How-to / step-by-step instructions |
| `recap` | Summary or synthesis of a conversation, interview, or meeting |

**Disambiguation:** a `claim` argues; a `description` defines; an `approach` declares posture; a `recap` synthesizes a specific event. If a `slug` file is reusable narrative (not a fact, claim, or reflection), it is a `fragment`.

## Front Matter

Only four fields. Omit any field that doesn't apply — an empty field is worse than no field.

```yaml
---
status: draft | stable | archived
audience: [proposal, investor, journalist, general, technical]
tags: [tag1, tag2]
related: [0000-00-00-kind-other_slug]
---
```

- `status` — whether the content is trustworthy. Omit for entries with no meaningful draft/stable distinction.
- `audience` — which contexts this file is meant to serve. Omit when general-purpose.
- `tags` — cross-cutting topics not captured by kind or slug. Omit when the slug is already precise enough.
- `related` — filenames (without extension) of related entries.

Fields explicitly not included: `date`, `name`, `title`, `slug_convention`, `classification`, `kind`, `source_path`, `source_type`, `source_ref`, `summary`. All of these either derive from the filename or are vestigial.

## Timeless Becomes Dated

When a previously `0000-00-00` entry becomes time-bounded:

- **Default (lossy):** rename the file to the date it was last accurate; create a new entry for the current state. The old file is the historical record.
- **Lossless:** add `superseded_by: <filename>` to the old entry's front matter when the trajectory itself is meaningful to track.

Default to lossy. Use `superseded_by` only when the evolution matters.

## Migration State

Existing entries use the old 34-kind schema and carry redundant front matter fields. Normalize opportunistically: when you open a file for any reason, update the kind to the new taxonomy and strip the redundant fields. The 45 `slug` files are the primary cleanup queue — most should become `fragment`.
