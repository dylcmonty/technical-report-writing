## Snippet Operating Procedure

A snippet is a small, self-contained unit of reusable writing. It should preserve one stable idea from prior writing in a form that can be reused across reports, applications, proposals, and explanations.

This directory is not organized first by topic category. The topic should usually be visible from the snippet's name alone. The stronger organizing principle is the author's purpose for using the snippet.

A snippet about qualifications may be used in different ways:
- to state qualifications
- to argue why those qualifications matter
- to explain how those qualifications were formed
- to frame credibility for a specific audience

These are not the same snippet, even if they share the same subject.

## Core principle

Separate:
- subject = what the snippet is about
- purpose = why the snippet exists and what rhetorical job it performs

The subject should usually be carried by the title, slug, and filename.
The purpose should be carried by metadata.

## Recommended filename form

```text
<purpose>--<subject>.md
```

Examples:

```text
qualification-case--systems-builder.md
qualification-description--embedded-systems-background.md
motivation-framing--problem-driven-work.md
company-purpose--fruitful-network-development.md
technology-explanation--semantic-identity.md
technology-case--why-semantic-identity-matters.md
operational-position--why-semantic-identity-matters.md
```

Also use critical thinking for the additional facet of who a snippet is written for.
For example: LinkedIn professional context, scholarly context, academic context, website copy, email, partner developer communication, YC application context, or literary writing.

The filename should make the subject obvious without needing extra metadata.

## Recommended uniform form

```md
---
title: Systems Builder
slug: systems-builder
purpose: qualification-case
status: draft
audience:
  - general
tags:
  - qualifications
  - engineering
  - systems
source_type: fragment
source_ref: notes-2026-04
related:
  - qualification-description--embedded-systems-background
---

# Systems Builder

Question: Why am I qualified to work on difficult technical systems?

Answer:
I am qualified to work on difficult technical systems because my experience has consistently required me to understand incomplete environments, connect abstract ideas to implementation details, and build functioning structures across software, infrastructure, and technical communication.

Boundaries:
- This does not claim formal specialization in every subdomain.
- This does not claim that experience alone guarantees correctness.
```

## Purpose taxonomy

Use purpose as the main grouping field. Keep it small and stable.

### Qualification / credibility
- `qualification-description` — states qualifications directly
- `qualification-case` — argues why the qualifications matter
- `qualification-evidence` — gives concrete evidence of qualification
- `qualification-context` — explains the path or conditions that produced the qualification

### Identity / self-framing
- `identity-description` — states something about who I am
- `identity-framing` — frames how I should be understood
- `motivation-description` — states what drives me
- `motivation-framing` — explains why that drive matters

### Company / mission
- `company-description` — states what the company is
- `company-purpose` — states why the company exists
- `company-problem` — states the problem the company addresses
- `company-approach` — states how the company approaches the problem

### Technology / ideas
- `technology-description` — defines the technology or concept
- `technology-explanation` — explains how it works
- `technology-case` — argues why it matters
- `technology-boundary` — states what it does not claim
- `technology-comparison` — distinguishes it from alternatives

### Writing / report support
- `claim` — a reusable conclusion or assertion
- `definition` — a reusable definition
- `constraint` — a limiting condition
- `objective` — a target state
- `mechanism` — how something works
- `transition` — a bridging statement between ideas
- `boundary` — a non-claim or scope limit

## Snippet writing rules

1. One snippet should do one job.
2. Do not mix subject and purpose.
3. Prefer reuse over completeness.
4. Keep each snippet self-contained enough to quote or paste elsewhere.
5. Write the answer as a stable paragraph, not as loose notes.
6. Use boundaries when a claim could be overread.
7. Split a snippet when the same subject must serve two different purposes.

## Split test

Create separate snippets when the answer to either question is yes:

1. Is the subject the same, but the rhetorical job different?
2. Would I reuse one version in a proposal, but another in a personal explanation?

If yes, split them.

Example:

- `qualification-description--software-builder.md`
- `qualification-case--software-builder.md`

These may draw from the same source writing, but they are different snippets.

## Suggested access pattern

Use access in this order:

1. filename
2. purpose
3. tags
4. related links
5. full-text search

This keeps retrieval simple even before a larger indexing system exists.

## Voice preservation rule

Normalize structure and spelling, but do not flatten meaning.

- Preserve unusual but intentional phrasing when it carries signal.
- Keep claims specific; do not replace sharp claims with generic wording.
- Prefer clarity edits over stylistic rewriting.
- If a line expresses conviction, keep the conviction and tighten only grammar.

## Suggested future additions

Add these later as the collection grows:

- `_template.snippet.md` — starter template for new snippets
- `catalog.json` — machine-readable index of all snippets (now seeded)
- `aliases:` field — alternate names for the same subject
- `audience:` field — proposal, investor, technical, personal, academic
- `state:` field — draft, stable, deprecated, superseded

## Minimal template

```md
---
title: <subject title>
slug: <subject-slug>
purpose: <purpose>
status: draft
tags:
  - <tag>
source_type: <fragment|journal|report|proposal|conversation>
source_ref: <origin>
related: []
---

# <subject title>

Question: <what this snippet answers>

Answer:
<self-contained reusable paragraph>

Boundaries:
- <what this does not claim>
```
