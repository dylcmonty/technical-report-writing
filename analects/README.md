# Analects

Normalized leaf notes live directly in this directory. An analect is a retrieval unit for author voice, durable claims, reusable prose, addressable facts, or event-bound recaps. Nested source collections stay under `raw/` until they are worth normalizing.

## Layout

- `analects/*.md` - normalized single-file notes
- `analects/raw/_template.snippet.md` - starter template for new entries
- `analects/raw/technical/` and `analects/raw/corespond/` - nested source collections not yet normalized
- `analects/archive/` - archival reference material

## File Contract

Filename convention:

```text
YYYY-MM-DD-<kind>-<slug>.md
```

Date forms:

| Date form | Meaning |
|---|---|
| `0000-00-00` | Timeless / undated |
| `YYYY-00-00` | Year known, month and day unknown |
| `YYYY-MM-DD` | Fully dated |

Rules:

- `<kind>` and `<slug>` use underscores as internal separators.
- Segments are separated by hyphens.
- `<kind>` must be one of the eight values below.

## Kind Taxonomy

| Kind | What it holds |
|---|---|
| `fact` | Atomic addressable data: URLs, skills, role titles, dates, contacts |
| `claim` | Assertive statement with reasoning |
| `description` | Definitional or descriptive explanation |
| `approach` | Operating stance, strategy, or posture |
| `reflection` | Personal, literary, poetic, or metacognitive writing |
| `fragment` | Reusable prose for applications, bios, proposals, statements |
| `procedure` | How-to or step-by-step instructions |
| `recap` | Summary or synthesis of a dated conversation, interview, or meeting |

Disambiguation:

- `claim` argues.
- `description` defines or explains.
- `approach` declares posture or method.
- `fragment` stores wording worth reusing verbatim.
- `recap` stays tied to a specific event.

Legacy note:

- `boundary` is not a kind. Put scope limits in a `## Boundaries` section inside a `claim`, `approach`, `fragment`, or `procedure`.
- `literary` and `ponderence` should usually normalize to `reflection`.
- `source` should normalize to `fact` only when the entry itself is an addressable fact. Source-heavy dossiers usually belong in `raw/` or should be distilled into `claim`, `description`, `fact`, or `recap`.

## Front Matter

Only four fields are standard. Omit any field that does not apply.

```yaml
---
status: draft | stable | archived
audience: [proposal, investor, journalist, general, technical]
tags: [tag1, tag2]
related: [0000-00-00-kind-other_slug]
---
```

- `status` - trust level or editorial state
- `audience` - intended retrieval context
- `tags` - cross-cutting topics not already captured by kind or slug
- `related` - filenames without extension

Do not keep empty fields. Empty structure is worse than absent structure.

Fields not included in normalized front matter: `date`, `name`, `title`, `slug_convention`, `classification`, `kind`, `source_path`, `source_type`, `source_ref`, `summary`.

Exception:

- `superseded_by` may be added when the evolution between two dated notes is itself meaningful to preserve.

## Writing For Retrieval

The best analects are written or normalized with these rules:

1. One analect, one retrieval job.
2. Keep the author text primary. Add retrieval scaffolding around it instead of paraphrasing it.
3. Preserve literary and poetic text exactly. Add `Retrieval Gist`, `Use When`, or `Interpretive Note` outside the body.
4. Put facts, claims, fragments, and recaps in separate files when they serve different retrieval purposes.
5. Use specific slugs. Avoid vague buckets such as `background`, `notes`, or `thoughts`.
6. Add `Boundaries` to any file that could otherwise be overextended by a model.
7. When a reflection contains reusable wording, duplicate that passage into a sibling `fragment` instead of rewriting the reflection.
8. Keep time-sensitive material explicitly dated.
9. Use tags to improve routing, not to compensate for an imprecise kind or slug.

## Preservation-First Normalization

Normalization in this repo is structural, not stylistic.

- Rename files to valid kinds.
- Strip redundant front matter.
- Split mixed-use notes into separate retrieval units.
- Add retrieval scaffolding where it helps.
- Preserve author wording unless there is a concrete reason to change it.

Detailed operating procedure:

- [voice_preserving_normalization.md](/home/smohn/LCL/oeuvre/analects/voice_preserving_normalization.md)

## Timeless Becomes Dated

When a previously `0000-00-00` entry becomes time-bounded:

- Default: rename the file to the date it was last accurate, then create a new entry for the current state.
- Lossless option: add `superseded_by: <filename>` to the old entry only when the trajectory itself matters.

Default to the simpler historical split unless the change history is important.

## Migration State

The collection is still mid-migration.

- Legacy kinds such as `slug`, `literary`, `business`, `control`, `source`, `boundary`, `company_approach`, and others remain in the tree.
- The `slug` files are still the primary cleanup queue.
- Long source-derived question/answer notes often need to be split into a durable `claim`, `description`, or `fact` plus an event-bound `recap`.
- Literary notes should be preserved, not rewritten, during cleanup.
