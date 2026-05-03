# Voice-Preserving Analect Normalization

## Purpose

This guide defines how to assess, normalize, and split `analects/*.md` files without flattening the author's language. The `README.md` defines the repository contract. This document defines the preservation and normalization behavior that should govern edits.

The collection exists to support retrieval of the author's actual perspective, tone, literary posture, reusable phrasing, claims, and facts. The safest normalization strategy is therefore structural rather than stylistic.

## Core Rule

Preserve the author's language unless there is a concrete operational reason to change it.

Good normalization:

- rename the file
- strip redundant front matter
- add retrieval scaffolding
- split one mixed note into several clean retrieval units
- fix broken Markdown when meaning does not change

Bad normalization:

- rewrite a paragraph into a cleaner summary
- flatten metaphor into literal explanation
- convert first person into generic business prose
- remove repetition that may be rhetorically intentional
- replace a poetic passage with a paraphrase

## What Improves RAG Quality In This Repo

The current `analects/` tree suggests a few clear optimization rules:

1. Keep one analect responsible for one retrieval job.
2. Separate author-voice notes from source-heavy research dossiers.
3. Treat literary and poetic passages as artifacts, not as raw material for summary.
4. Make titles and slugs explicit enough that retrieval does not rely on tags alone.
5. Use `Boundaries` to stop claims from being stretched beyond what the text supports.
6. Keep dated recaps separate from timeless positions.
7. When one note contains both reflection and reusable external phrasing, create a sibling `fragment` rather than rewriting the reflection.
8. Only store source-only entries as `fact` when the source itself is an addressable fact worth retrieving.

Repo-specific implications:

- Legacy kinds such as `slug`, `literary`, `business`, `boundary`, `source`, `control`, and `company_approach` obscure retrieval intent.
- Long question/answer operator dossiers often mix fact, interpretation, competitive analysis, and durable claim in one file.
- The old starter template encouraged empty arrays, which creates metadata noise instead of useful structure.

## Preservation Classes

Assign a preservation class before editing.

### Class A: Frozen Literary / Poetic

Use for literary, poetic, aphoristic, or rhythm-dependent writing.

Rules:

- Do not rewrite the body.
- Do not normalize line breaks.
- Do not replace unusual wording.
- Add retrieval scaffolding only before or after the text.
- If chunking is required, split only at natural stanza, paragraph, scene, or section boundaries.

Likely kind:

- `reflection`
- `fragment` only when the passage is clearly meant for reuse as wording

### Class B: Voice-Preserved Reflective / Philosophical

Use for personal essays, worldview notes, and metaphor-heavy reflections.

Rules:

- Preserve original sentences wherever possible.
- Add headings around the text instead of rewriting it.
- Put clarification in `Interpretive Note` or `Boundaries`, not inside the body.

Likely kind:

- `reflection`
- `claim`
- `approach`

### Class C: Reusable Prose / Application Fragment

Use for bios, founder language, proposal wording, scholarship statements, and other reusable passages.

Rules:

- Preserve the reusable wording verbatim.
- Add `Use When`.
- Add `Do Not Use When` when the wording could be misapplied.

Likely kind:

- `fragment`

### Class D: Technical / Factual / Procedural

Use for facts, definitions, processes, and operational instructions.

Rules:

- Light clarification is acceptable only when it improves precision.
- Separate facts from claims.
- Keep date context or limitations when material can drift over time.

Likely kind:

- `fact`
- `description`
- `procedure`

### Class E: Recap / Conversation Synthesis

Use for meetings, interviews, correspondence, or prior model sessions.

Rules:

- Preserve event context.
- Extract durable sibling notes only when they stand on their own.
- Do not treat a recap as a timeless belief unless the author has clearly endorsed it elsewhere.

Likely kind:

- `recap`

## Assessment Workflow

### Step 1: Read Without Editing

Read the file once before touching it. Identify:

- the main job of the note
- whether wording is part of the meaning
- whether the file is one retrieval unit or several
- whether the filename matches the function
- whether old front matter is still present

### Step 2: Assign Preservation Class

Choose Class A, B, C, D, or E before editing. This does not need to become front matter unless the repo later adds a dedicated field.

### Step 3: Determine The Correct Kind

Map the file to the repository taxonomy:

- `fact` - atomic addressable data
- `claim` - argues something is true
- `description` - defines or explains what something is
- `approach` - describes posture, method, or strategy
- `reflection` - preserves personal or literary thought
- `fragment` - stores reusable wording
- `procedure` - gives step-by-step instruction
- `recap` - summarizes a specific event

Legacy mapping shortcuts:

- `literary`, `ponderence` -> usually `reflection`
- `boundary` -> usually `claim` or `approach` with a `## Boundaries` section
- `source` -> `fact` only if the note is just an addressable source locator
- `control`, `technology`, `objective`, `scope`, `problem`, `measure`, `mechanism` -> choose by actual function, not by the old label

### Step 4: Evaluate The Filename

Expected form:

```text
YYYY-MM-DD-<kind>-<slug>.md
```

Check:

- Is the date accurate?
- Is the kind valid?
- Does the slug name the actual concept?
- Are underscores used inside the slug?
- Are hyphens only separating date, kind, and slug?

Prefer specific slugs over vague buckets.

### Step 5: Clean Front Matter

Keep only fields that apply:

```yaml
---
status: draft
audience: [proposal, technical]
tags: [coordination, market_structure]
related: [0000-00-00-claim-example]
---
```

Remove:

- `title`
- `date`
- `slug_convention`
- `name`
- `classification`
- `kind`
- `source_path`
- `source_type`
- `source_ref`
- `summary`

Do not keep empty arrays.

### Step 6: Identify Protected Author Text

Make the original wording easy to distinguish from retrieval scaffolding.

Useful section labels:

- `## Protected Author Text`
- `## Text`
- `## Claim`
- `## Fragment`
- `## Approach`

The main body section should contain the author's wording, not a paraphrased substitute.

### Step 7: Add Retrieval Scaffolding

Add only the scaffolding that improves routing:

- `## Retrieval Gist`
- `## Use When`
- `## Do Not Use When`
- `## Boundaries`
- `## Interpretive Note`

Rules:

- The gist should be plain-language and searchable.
- The gist should not replace the body.
- `Boundaries` are mandatory for claims that could be overextended.
- `Interpretive Note` should clarify routing, not collapse ambiguity inside literary text.

### Step 8: Decide Whether To Split

Split only when the file contains more than one retrieval job, such as:

- reflection plus reusable prose
- fact plus philosophy
- dated recap plus timeless claim
- evidence dossier plus polished claim
- technical description plus operating instruction

Do not split merely because the file is long.

### Step 9: Split By Semantic Function

When splitting:

1. Identify natural paragraph or section boundaries.
2. Move intact passages into new files.
3. Preserve wording exactly inside each new file.
4. Add only the minimal scaffolding needed for each file.
5. Link sibling files through `related`.

If a reflection contains a sentence worth reusing in proposals, keep the reflection intact and create a sibling `fragment` with the exact wording.

### Step 10: Check For Drift

After editing, ask:

- Did any sentence become narrower?
- Did any uncertainty become certainty?
- Did any personal stance become generic?
- Did any metaphor get literalized?
- Did the retrieval gist overclaim beyond the text?

If yes, revert the prose change or move the clarification outside the protected body.

## Recommended File Shapes

### Voice-Preserved Claim

```md
---
status: draft
audience: [general]
tags: [tag1, tag2]
related: [0000-00-00-kind-related_slug]
---

# Title

## Retrieval Gist

One sentence describing the claim in searchable language.

## Claim

Original claim wording.

## Protected Author Text

Original prose remains verbatim.

## Boundaries

What the claim does not mean, or where it should not be applied.
```

### Literary Or Poetic Reflection

```md
---
status: stable
tags: [tag1, tag2]
related: [0000-00-00-kind-related_slug]
---

# Title

## Retrieval Gist

Plain-language retrieval note.

## Use When

Describe the retrieval context.

## Text

Original literary text remains exactly as written.

## Interpretive Note

Optional. Add only if needed for routing.
```

### Reusable Fragment

```md
---
status: stable
audience: [proposal, general]
tags: [tag1, tag2]
related: [0000-00-00-kind-related_slug]
---

# Title

## Retrieval Gist

One sentence explaining what this prose is for.

## Use When

Describe where the wording should be reused.

## Fragment

Original reusable prose remains verbatim.

## Do Not Use When

Optional guardrail against misuse.
```

### Fact

```md
---
status: stable
audience: [technical]
tags: [tag1, tag2]
related: [0000-00-00-kind-related_slug]
---

# Title

## Retrieval Gist

One sentence stating the fact in searchable terms.

## Fact

Atomic fact.

## Context

Optional context that prevents misuse.

## Boundaries

Optional limitation or date-sensitivity note.
```

### Approach

```md
---
status: draft
audience: [proposal, technical]
tags: [tag1, tag2]
related: [0000-00-00-kind-related_slug]
---

# Title

## Retrieval Gist

One sentence explaining the operating posture.

## Approach

Original operating principle or method.

## Use When

Describe contexts where the approach should guide output.

## Boundaries

State where this approach should not be applied.
```

## Agent Rules

Any agent editing `analects/` should follow these rules:

1. Treat original prose as protected source material.
2. Never paraphrase merely to make retrieval easier.
3. Add retrieval scaffolding around the prose.
4. Split files by retrieval function, not by length.
5. Preserve literary and poetic language exactly.
6. Normalize front matter before touching body text.
7. Use valid kinds only.
8. Do not keep empty front matter fields.
9. Use `Boundaries` to prevent overextension.
10. When uncertain, preserve wording and add an external note instead.

## Recommended Agent Prompt

```text
Assess this analect file under a preservation-first rule.

Do not rewrite author prose unless strictly necessary for broken syntax or explicit contradiction.
Keep wording, cadence, metaphor, and tone intact.
Literary or poetic sections are frozen and must not be paraphrased.

Tasks:
1. Identify the correct analect kind from: fact, claim, description, approach, reflection, fragment, procedure, recap.
2. Determine whether the file should remain one analect or be split into multiple analects.
3. Clean front matter to only: status, audience, tags, related. Omit empty fields.
4. Propose a filename using YYYY-MM-DD-<kind>-<slug>.md.
5. Add retrieval scaffolding only where helpful: Retrieval Gist, Use When, Boundaries, Do Not Use When, Interpretive Note.
6. Preserve the original author text verbatim under Protected Author Text, Text, Claim, Fragment, or equivalent section.
7. If chunking is needed, return each proposed new file separately and indicate which original passages moved into each one.
8. Provide a brief drift check explaining how the original wording was preserved.
```

## Practical Conclusion

The goal is not a cleaner version of the author's thought. The goal is a more retrievable version of the author's actual language.

For analytical notes, structure and boundaries usually improve retrieval. For literary notes, the text itself is the artifact, and retrieval support must remain external to it.
