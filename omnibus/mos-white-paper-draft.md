# Mycelial Ontological Schema (MOS): Toward a Datum-Native Semantic Grammar for Interoperable Socio-Technical Systems

## Abstract

Interoperability problems in socio-technical networks are often misidentified as failures of transmission rather than failures of operational meaning. Independent systems can exchange files, messages, and records while still remaining inoperable when recipients cannot interpret structure, preserve meaning under change, or compose foreign data without bespoke adapters. This paper presents a bounded conceptual draft of the Mycelial Ontological Schema (MOS) as a response to that problem. MOS is not presented here as another database model, nor as a replacement for linked data, property graphs, schema registries, or content-addressed systems in general. Instead, it is framed as a datum-native semantic grammar intended for settings in which information form cannot be fully pre-limited by a single centralized schema. The paper argues that the relevant research gap is not the absence of self-description, graph structure, canonicalization, or decentralized identifiers in isolation, but the absence of a unified formal core that treats canonically reproducible abstraction paths, self-describing structure, reversible mapping, and semantic interoperability as coequal requirements. Concretely, the MOS model distinguishes two canonical forms - a full ordered structure (MSS) and a minimal abstraction identity (hyphae) - and generates addressable structural namespaces (SAMRAS) from the structure encoding itself rather than from an externally declared schema. On that basis, MOS is presented as a synthetic proposal: a formalism in which abstractions rather than records or nodes are primary, in which structure is explicitly delimited and addressable, and in which cross-system coordination proceeds through shared grammar, mapping, semantic difference, and provenance rather than through repeated file shipping and ad hoc translation. The result is a more bounded and academically defensible novelty claim: MOS may be distinct not because it introduces any one isolated mechanism, but because it attempts to unify several previously separated concerns into a single abstraction-centered model for interoperable computation.

## Introduction

The central problem addressed in this paper is not whether systems can exchange data, but whether they can remain meaningfully interoperable under conditions of independent evolution. In many multi-party networks, participants can transmit bytes, files, or structured payloads without being able to interpret each other's data natively, preserve meaning when models change, or coordinate actions without recurring integration work. This condition may be described as **inoperability**: the exchange of information without reliable shared operational meaning.

That problem is especially pronounced in socio-technical settings. Software systems, organizations, devices, and human operators evolve on different timelines, adopt local conventions, and create new distinctions as their tasks change. Under those conditions, agreement on a single fixed schema or frozen interface contract becomes increasingly brittle. The issue is not simply that systems use different formats. The deeper issue is that the network cannot fully pre-limit the form of information in advance. New entities, new relationships, new constraints, and new interpretive requirements arise over time, and any rigid standard eventually encounters cases it did not anticipate.

This paper develops a bounded draft of the **Mycelial Ontological Schema (MOS)** as a response to that problem. The paper does not claim that MOS solves interoperability in the absolute, nor that it supersedes established paradigms such as linked data, property graphs, schema registries, or content-addressed systems. Instead, it advances a narrower thesis: **MOS is best understood as a datum-native semantic grammar for interoperable socio-technical systems, intended for domains in which information form cannot be fully pre-limited by a single authoritative schema.** In that framing, the relevant question is not whether related technical ingredients already exist. They do. The relevant question is whether there is an established formal model that unifies structural self-description, path-native abstraction, reversible mapping, explicit semantic difference, and canonical reproducibility as a single formal core. The claim of this paper is that MOS is most plausibly distinct at that point of synthesis.

## The Interoperability Problem

Many contemporary integration strategies treat interoperability as a problem of transport. Two systems exchange a CSV file, a JSON payload, an API response, or an event stream, and the existence of a parseable artifact is taken as evidence that interoperability has been achieved. In practice, that assumption is weak. A receiving system may be able to parse a file without being able to interpret its structure, reconcile its meanings with local concepts, or incorporate it into ongoing computation without custom glue code.

This distinction can be stated more precisely. A fixed format typically solves **transmission agreement**: it tells participants how a sequence of bits should be segmented and read into a finite set of fields. It does not necessarily solve **operational interoperability**: the capacity of independent systems to query, validate, transform, compose, and evolve those structures without bespoke bilateral work. This gap grows over time because even when syntax remains stable, meaning does not. A field name may persist while the business rule attached to it changes. A status flag may retain its label while its operational threshold shifts. A shared schema may remain nominally standard while its participating implementations drift apart.

Several familiar failure modes follow. The first is **schema drift**, where field names, types, nesting, and invariants change over time across local implementations. The second is **semantic drift**, where similar-looking symbols or fields no longer carry the same operational meaning. The third is **adapter explosion**, in which the number of translators, ETL jobs, and local patches grows faster than the number of systems because each participant must continually reconcile local change with every external dependency. Format-first integration tends to obscure these problems temporarily rather than remove them. It permits exchange while pushing interpretation cost onto every receiver.

The interoperability literature supports this diagnosis precisely. The Levels of Conceptual Interoperability Model (LCIM) was explicit that meaningful interoperability extends beyond implementation standards and exchange formats, identifying semantic and conceptual levels as qualitatively different from syntactic ones (Tolk & Muguira, 2003). The schema-matching literature treated matching as a basic, ongoing problem in data integration and later retrospectives demonstrated that even well-studied alignment approaches remained active research areas rather than solved infrastructure. Ontology and semantic-integration research reinforced the same conclusion: different applications can use the same terms while attaching different semantics to them, and ontology-based alignment remains an open problem rather than a completed layer (Euzenat & Shvaiko, 2013). This is why the strongest form of the interoperability problem is not "how do we make a file portable?" but rather "how do independently evolving systems remain operable with each other when the network cannot pre-limit the forms of meaningful information?" Once posed in that way, the problem no longer looks like a narrow matter of serialization. It becomes a question of formal representation, mapping, versioning, provenance, and shared interpretive structure.

## Research Context and Adjacent Paradigms

A bounded presentation of MOS requires careful placement among adjacent research traditions. The goal is not to deny prior art, but to identify the exact point at which MOS claims a different center of gravity.

### Semistructured and Self-Describing Data

The oldest and closest formal lineage is the semistructured-data literature. The Object Exchange Model (OEM) and related work described semistructured data as self-describing, with schema embedded in the data and no a priori regular structure assumed; data was treated as heterogeneous, incomplete, and path-addressable rather than uniformly tabular (Abiteboul et al., 1997). This is an important scholarly base for the MOS proposal because it legitimizes the claim that "schema-agnostic" does not mean "structureless." Structure may travel with the data rather than exist only as a separately governed table design. MOS builds directly on this precedent - but extends it in the direction of ordered composition, dual canonicality, and abstraction identity as formal properties rather than incidental features of a flexible format.

### Linked Data and Semantic-Web Work

The linked-data lineage, including RDF, JSON-LD, OWL, and RDF Schema, took a different route (W3C, 2014; Sporny et al., 2020). These paradigms are essential precedents for machine-readable semantics, globally referenceable identifiers, and extensible meaning across distributed authorship. They show that interoperable semantics require more than syntax, and that independently authored datasets can converge through shared vocabulary and formal semantic structure. At the same time, **order is not primitive in the core RDF graph model**: ordered collections must be represented explicitly through list vocabularies and encoding conventions layered on top of the underlying triple graph. That makes linked data a close precedent for extensible semantics but only a partial precedent for a model in which forward and backward logical ordering is intrinsic to the primary representation unit. JSON-LD demonstrates a related limitation: contexts can shape how the same JSON data is interpreted at different scales or for different audiences, which provides a useful technical precedent for the claim that interoperable convention can remain partly decentralized - but it does not address ordered abstraction or minimal reconstructive identity.

### Property Graphs and Path-Centric Graph Theory

Property-graph systems form the second major comparison class. Their formal model centers on nodes, edges, labels, and property-value pairs. Recent graph-language research is especially revealing. The G-CORE language introduced the **Path Property Graph** model precisely because paths needed to become first-class citizens for closure and compositionality (Angles et al., 2018). Newer algebraic work on graph query languages continues to identify first-class path treatment as an active research frontier rather than a settled standard. This is the strongest academic baseline for MOS because it shows that the path-native intuition is recognized as a genuine gap in current graph-database paradigms, not a redundant elaboration. The distinction between that lineage and MOS is that property-graph work typically still treats the graph object as the central frame of reference, with paths as derived or augmented features. MOS proposes to make the **canonically reproducible abstraction** - not the graph object or the node - the primary carrier of identity and reproducibility.

### Content-Addressed and Traversable DAG Systems

IPLD (InterPlanetary Linked Data) and related content-addressed DAG approaches are the closest established lineage for structural pathing without centralized schemas (Protocol Labs, 2021). IPLD explicitly presents itself as serial-format agnostic, provides generic pathing and traversal over a common data model, and relies on content-addressed hash-based links. Content Identifiers (CIDs) and multiformat prefixes provide self-describing identifiers. Selectors describe traversals over a DAG. This is highly relevant to the MOS "abstraction path" intuition - particularly the claim that pathing and identity can be formalized independently of a single application format. The key distinction is that IPLD standardizes traversable structure and content identity rather than community-level semantic agreement about what a newly coined abstraction should mean. **IPLD gives content-addressed structure and traversal; it does not give a grammar for reconciling meaning under heterogeneous evolution.** That semantic reconciliation layer remains outside the IPLD core.

### Binary Self-Description and Canonicalization

For the binary representation layer, the most relevant precedent is the family of self-delimiting binary encodings. CBOR (RFC 8949) uses major-type headers that encode type and length information together, supports indefinite-length arrays, maps, and strings terminated by an explicit break code, and specifies a deterministic encoding profile. Critically, CBOR's specification documents the **self-delimiting property** that no well-formed CBOR item is a prefix of another - making CBOR parsing possible without out-of-band size declarations (Bormann & Hoffman, 2020). That property maps closely to MOS's requirement that meaningful units be self-delimiting.

Existing binary formats differ sharply in how much they self-describe. **Protocol Buffers (Protobuf)** is compact and supports length-delimited records, but bytes are interpreted against an externally known message definition - they do not carry semantic cues in the stream. **Apache Avro** is more explicit about this tradeoff: binary Avro intentionally omits field names and type information from the payload, requiring the writer's schema or a schema with a compatible parsing canonical form to be available separately (Apache Software Foundation, 2023). Avro defines both a parsing canonical form and schema fingerprints precisely so schema equivalence can be tested without embedding full schema text in each message. **CBOR with tags and CDDL** moves further toward self-description because structural typing, delimiters, and some semantic cues can travel with the data itself. The literature therefore already establishes an important distinction: syntactic self-description, structural self-delimitation, and semantic interpretability are related but not equivalent conditions.

Canonicalization is likewise an adjacent lineage, not an empty space. Avro schema fingerprints enable schema comparison and safe evolution. RDF now has a W3C recommendation-level canonicalization algorithm for datasets (Longley & Sporny, 2023). Content-addressed DAG systems use hash-consistent representations and self-describing identifiers. These are the nearest established relatives to MOS's distinction between a full canonical form and a minimal abstraction identity. The novelty question is therefore narrower and stronger: not whether canonicalization exists, but whether a model can formally justify **two non-redundant canonical forms** - one for total ordered structure (MSS) and one for minimal reconstructive identity (hyphae) - and explain why interoperable systems need both.

### Socio-Technical Interoperability Research

Finally, there is the lineage of socio-technical interoperability research, including schema matching, ontology alignment, conceptual interoperability, and standardization studies. Star and Griesemer's concept of **boundary objects** - shared artifacts that are adaptable to different local viewpoints while remaining robust enough to maintain identity across them - provides a conceptual bridge to MOS's claim that interoperable convention can remain decentralized even when the substrate is standardized (Star & Griesemer, 1989). The socio-technical literature also demonstrates that interoperability failures are not reducible to syntax. They persist because meaning is contextual, evolving, and governed as much by institutions and incentives as by file formats. This body of work provides the most rigorous basis for MOS's claim that generalized interoperability cannot be secured merely by expanding the number of exchange formats or interface contracts.

### What Existing Systems Still Do Not Solve

Across the sources surveyed, the gap is not the absence of individual ingredients. Semistructured data handles open form. RDF and JSON-LD handle globally referenceable semantics. Property and path graph research handles navigability and path-centric query. IPLD handles content-addressed traversal. CBOR handles self-delimiting binary structure. Avro and RDF canonicalization handle major forms of canonical equivalence. What is missing from any single widely adopted paradigm is a formal core that makes **order-bearing abstraction paths, schema-agnostic structure, deterministic binary framing, reversible cross-system mappings, and decentralized semantic convention all first-class within the same model**.

The clearest technical absences are fourfold. Core graph models still privilege nodes, edges, and triples over path identity, which is why first-class path extensions keep reappearing as active research problems. Compact binary formats either depend on external schemas or stop at structural typing and lightweight tags without providing a grammar for semantic interpretation. Canonicalization systems usually canonicalize schemas, datasets, or content blocks, not a separately defined minimal abstraction identity layered over a full ordered structure. And semantic agreement still requires governance, mapping, and alignment work that lies outside the parser in every existing system. None of this means the MOS target is impossible. It means the combination is not already available as a mature, standard, generally agreed package.

One maximally defensible sentence for what is not yet possible across this landscape is: current systems can make data portable, queryable, canonical, content-addressable, or semantically annotated, but they do not yet offer a broadly standardized way to make arbitrarily extensible information simultaneously path-native, self-delimiting, reversibly canonical, and semantically interoperable without substantial external convention management.

## Defining MOS

The strongest public definition of MOS is neither "a new database" nor "a graph database with extra features." Those classifications mislocate the conceptual ambition of the model by making storage the primary category. A more precise layered classification is as follows:

- **Most precise:** a datum-native semantic grammar and abstraction calculus for interoperable systems.
- **Second-best:** a canonical ontology and serialization layer for reproducible, reversible cross-schema coordination.
- **Third-best:** a vector-native interoperability fabric rather than a database proper.

The underlying reason for this classification is that **MOS stores the rules of abstraction themselves, so that different systems can preserve their own local structure while still computing on shared meaning.** Most data systems store records, documents, or graph objects. MOS stores the compositional relationships that allow meaning to be derived, reproduced, and reconciled.

The more precise description is that **MOS is a datum-native semantic grammar in which abstractions are represented as recursively composable relationship vectors whose structure, boundaries, and references are made reproducible within a shared formal framework.** This definition matters because it relocates the primary object of the system. In a relational system, the row and its schema are primary. In document stores, the document or object is primary. In graph systems, nodes and edges or triples are primary. In MOS, meaning is built from rudimentary datum classes and compounded through reference, ordering, and abstraction operators. The system is therefore **datum-first and abstraction-first** rather than record-first, document-first, or node-first.

### Concrete Datum Model

To make this more than a definitional claim, the MOS model grounds itself in a concrete datum logic. Each datum is addressed by a three-segment coordinate: **layer - value\_group - iteration**. This addressing is ordered, non-skippable, and cascading: inserting or removing a datum requires shifting the iteration values of all following datums and propagating reference updates from the highest abstraction downward. The constraint ensures that every datum's position within the namespace is both canonical and deterministically derivable - not an arbitrary assignment, but a positional identity that follows from the structure itself.

From this base, MOS defines the **SAMRAS address space** (shape-addressed mixed-radix address space): a structural namespace derived canonically from the structure encoding rather than from a pre-declared external schema. SAMRAS stores child counts in breadth-first order and derives node addresses from ordinal positions, so the full addressable hierarchy is generated from the bitstream without separate schema declaration. This is the concrete realization of the claim made in Section 3.7 - that the combination of structure-native addressing and schema-agnosticism is not yet present in a single widely adopted standard.

### Dual Canonicality: MSS and Hyphae

MOS relies on two distinct canonical forms, and the distinction between them is central to its novelty claim.

The first is **MSS (Monotonic Structured Serialization)**: the canonical full-state representation of an information structure, comprising the complete ordered and composed datum set. MSS gives a total canonical form for the entire structure, enabling deterministic identity at the structure level.

The second is **hyphae**: the canonical minimal abstraction identity needed to reconstruct or recognize a specific datum. The hyphae value of a datum is the minimal collection of preceding datums required to abstract to it, always including all preceding rudi datums even if not used directly. For example, if a datum uses address `0-0-5`, its hyphae value includes `0-0-1` through `0-0-5`. This is not simply a schema fingerprint or a dataset hash. It is a minimal reconstructive identity: the smallest canonical basis from which the datum can be reproduced forward and backward.

This **dual canonicality** distinguishes MOS from neighboring canonicalization approaches. Avro's canonical form and schema fingerprints concern schema-level equivalence. RDF dataset normalization concerns the canonical form of a dataset as a whole. Content-addressed DAG systems give block-level identity via hashing. None of these separately formalize a minimal abstraction identity layered over a full ordered representation. MOS claims that interoperable systems need both: one canonical form to confirm total structural identity, and one to confirm the minimal basis for reconstructing a specific abstraction.

### Abstraction Operators

Beyond the datum model and the two canonical forms, MOS defines a family of abstraction operators by which complex meaning is built from simpler datums. By referring to prior defined datums in lower layers, a new datum expands an existing abstraction by:

- **Iterative duplication**: notating the magnitude of repetition within a defined space.
- **Fractal expansion**: notating the magnitude of recursive structural growth.
- **Point selection**: selecting specific positions within defined spaces rather than continuous ranges.
- **Simultaneous selection**: maintaining multiple selections of datums at the same time.
- **Selection set creation**: treating sets of simultaneous selections as first-class objects.

These operators are not simple query predicates. They are part of the ontology of how abstractions are formed, making selection a compositional primitive rather than a retrieval behavior. The closest analogues in adjacent systems - IPLD selectors, XPath, property-graph traversal - treat selection as query behavior over an existing model. MOS treats selection as constitutive of the abstraction itself.

The most defensible one-sentence formulation of MOS is therefore: **MOS is a datum-native semantic grammar in which complex meaning is constructed through recursively composable abstractions, with canonical full-state representation (MSS) and canonical minimal abstraction identity (hyphae) enabling reproducible structure, reversible mapping, and cross-system coordination without forcing all participants into a single centralized application schema.**

## Self-Describing Semantic Grammar

The conceptual core of MOS depends on the idea of a **self-describing semantic grammar**. This does not mean that every datum is self-sufficient in the strongest possible sense, nor that no shared convention is required. It means that a representation framework carries enough structural and semantic boundary information for an independent system to identify meaningful units and understand how those units relate without relying on a bespoke contract for every partner.

A self-describing semantic grammar requires at least four conditions.

First, it requires **self-delimitation** or equivalent explicit boundary rules. A receiver must be able to determine where meaningful units begin and end without guessing sizes out of band. CBOR demonstrates one realization of this requirement at the binary level: the self-delimiting property ensures no well-formed item is a prefix of another. MOS extends this requirement from the binary encoding layer to the abstraction layer - boundaries must be explicit not only for parseable bytes but for meaningful compositional units.

Second, it requires **hierarchy and grouping**. Independent systems do not exchange only flat values. They exchange collections, nested structures, scoped subobjects, and compound constraints. A grammar that cannot represent grouping and nesting without external schemas cannot function as a general interoperability substrate. The HOPS profile chain - coordinate rings (`4-*`), polygon members (`5-*`), collections (`6-*`), and filament bindings (`7-*`) - illustrates how MOS expresses hierarchical composition through explicit ordered chaining rather than assumed nesting conventions.

Third, it requires **composable addressing**. A receiver must be able to refer not only to whole artifacts, but to deterministically identified substructures. SAMRAS-derived addresses provide this within MOS. Stable structural coordinates allow systems to point to the relevant abstraction rather than repeatedly re-exporting complete snapshots.

Fourth, it requires **explicit semantic cues**. A receiver must not only see that some values are grouped, but also have machine-readable cues about the roles those values play, the relationships between them, and the constraints under which they are meant to be interpreted. Without explicit semantic cues, a system may be structurally parseable while remaining operationally ambiguous. CBOR with CDDL schemas and JSON-LD contexts represent different partial solutions to this requirement; MOS addresses it through the rudimentary datum taxonomy (chronological, spatial, nominal) and the explicit abstraction-operator grammar.

These conditions explain why self-description is stronger than ordinary serialization. A conventional payload may be syntactically valid while still depending on surrounding tribal knowledge, documentation, or bilateral assumption in order to be used correctly. A self-describing semantic grammar attempts to reduce that dependence by making structural and semantic interpretability part of the formal representation rather than a separate social layer concealed outside the artifact.

In the MOS framework, this requirement connects directly to the claim that information form cannot always be pre-limited. If the network cannot assume a fixed schema, then structure and meaning must be carried in a way that supports open-ended growth. The point is not to abolish convention, but to relocate convention from countless bespoke interface contracts toward a smaller shared grammar of structurally and semantically meaningful primitives.

## From File Shipping to Reference-Based Coordination

A major practical distinction in the project materials is the difference between **file shipping** and **reference-based resolution**. This distinction clarifies what kind of interoperability MOS is trying to support.

In a file-shipping model, one node sends another node a file, export, or payload that is only meaningful in the receiver's context if the receiver already knows how to parse and interpret it. The burden of operability lies with every receiving system. Each participant must recognize the format, infer or import the relevant semantics, map the data into its local structures, and reconcile the incoming artifact with existing records or workflows. Such systems can scale as exchange networks, but they scale poorly as operable networks because each new participant imposes recurring interpretation work on every other participant.

Reference-based coordination aims at a different ideal. Instead of treating the payload as an opaque artifact that must be reverse-engineered, it treats the exchange as a reference into a shared interpretive space. The communicated object is closer to "this abstraction, under this grammar, with this provenance, subject to these policies" than to "this file; infer what it means." Coordination becomes a matter of resolving meaningful objects and subscribing to interpretable changes rather than repeatedly importing and reinterpreting foreign snapshots.

This is not equivalent to saying that files disappear. Rather, it says that files cease to be the primary unit of coordination. The important unit becomes the addressable abstraction and the rules by which that abstraction is resolved. In this sense, MOS attempts to bring network communication closer to database-style references: not because all nodes share one physical database, but because they share a grammar within which references, mappings, and transformations become explicit and machine-auditable.

The relevance of this shift is most obvious in heterogeneous multi-party environments. If local systems can project their own internal models into a shared grammar and if receivers can interpret those projections through explicit mappings, then the network can coordinate through references and semantic differences rather than through endless bilateral adapter work. The result is not uniformity. It is structured heterogeneity.

## Mapping, Semantic Difference, and Provenance

Once MOS is defined as a self-describing semantic grammar, interoperability can no longer be imagined as sameness alone. Independent systems will continue to have different local structures, units, vocabularies, and operational assumptions. A workable model therefore requires mechanisms for **mapping**, **semantic difference**, and **provenance**.

Mapping is the bridge between a node's local model and the shared grammar. Every participant retains its own internal representation - tables, documents, graphs, spreadsheets, or application objects - but expresses those structures in the shared semantic grammar through explicit, inspectable mappings. This reduces the cost of integration because the work of translation becomes formalized and reusable rather than improvised afresh for every exchange.

Semantic difference is equally necessary. Even when two nodes refer to closely related concepts, they will often differ in units, nesting, vocabulary, timing, or interpretive rules. A coordination system that assumes away these differences will either collapse into forced standardization or degenerate into hidden divergence. MOS therefore implies a model in which differences are represented explicitly and resolved by policy or mapping logic rather than denied.

Provenance provides the third layer. If structures are mapped, transformed, and recomposed across nodes, other participants need to know where those abstractions came from and how they were produced. Provenance does not create trust by itself, but it makes trust inspectable. It enables systems to reason about source, derivation, timing, policy, and version rather than accepting foreign data as unqualified fact.

Taken together, mapping, semantic difference, and provenance push MOS beyond the claim of a mere serialization format. They locate it instead as a coordination formalism: a way of making structures interoperable not because all parties agree completely, but because disagreement, variation, and derivation become visible and addressable within the model.

## The Novelty Claim and Prior-Art Matrix

The strongest novelty claim for MOS is synthetic rather than absolute. It would be academically weak to claim novelty because MOS is relationship-centric, decentralized, canonicalized, self-describing, or path-based in any isolated sense. Each of those features has clear prior art. The stronger claim is that **MOS attempts to unify these concerns around the abstraction as the primary formal object.**

The novelty claim has four parts.

First, MOS gives **abstraction paths** and canonically reproducible abstraction structures a more central role than neighboring paradigms. Although path-centric graph research and content-addressed traversal offer close precedents, MOS treats ordered abstraction and its reproducibility as a foundational concern rather than an extension or derived feature.

Second, MOS relies on **dual canonicality** (MSS and hyphae): one canonical form for full ordered structure and another for minimal abstraction identity. This is a stronger and more unusual claim than conventional canonicalization. Avro canonical form and RDF dataset normalization canonicalize schemas and datasets respectively. IPLD hashes canonicalize block content. None separately formalizes a minimal reconstructive identity distinct from the total structure. MOS asserts both are necessary for interoperable systems that must reconstruct, address, and compare abstractions independently.

Third, MOS combines **self-describing structure** with **explicit mapping and semantic difference**. Many systems either assume a fixed schema, leave semantics largely external, or treat mappings as ancillary integration logic. MOS moves those into the conceptual center of interoperability.

Fourth, MOS links technical representation to **structured heterogeneity** rather than forced schema uniformity. Its aim is not to eliminate local models, but to allow locally governed systems to coordinate through a shared grammar without collapsing them into one platform-owned ontology.

### Prior-Art Comparison Matrix

The following table maps each adjacent paradigm to what it canonicalizes and what it does not address, in order to locate MOS's distinct claim.

| Paradigm | What it canonicalizes | What it does not address |
|---|---|---|
| RDF / OWL | Triple sets; globally referenceable semantics | Ordered composition; minimal abstraction identity; path-native structure |
| JSON-LD | Linked-data interpretation of JSON; context-scoped IRIs | Ordered hierarchy as a primitive; dual canonicality; abstraction operators |
| Property graphs (Neo4j, etc.) | Node-edge-property model | First-class path identity (still an active research gap; see G-CORE) |
| Path Property Graph (G-CORE) | First-class paths as queryable objects | Canonical abstraction identity; structural self-delimitation; semantic grammar |
| IPLD | Content-addressed, format-agnostic traversal; CIDs | Community-level semantic agreement; reversible mapping; dual canonicality |
| CBOR (RFC 8949) | Self-delimiting binary structure; major-type heads; deterministic encoding | Semantic interpretability; abstraction identity; cross-system mapping |
| Apache Avro | Parsing canonical form; schema fingerprints | Path-native identity; minimal abstraction basis separate from schema; ordered composition |
| RDF Dataset Normalization | Canonical dataset serialization | Minimal per-abstraction identity; structural namespace derivation |
| Semistructured data / OEM | Schema-embedded, heterogeneous, path-addressable data | Ordered forward/backward composition; canonical abstraction identity |
| MOS (this proposal) | Full ordered structure (MSS) **and** minimal abstraction identity (hyphae); structural namespace derived from encoding (SAMRAS) | Proven formal spec; standardized implementation; established review |

The right column for MOS is honest: the claim rests on a bounded conceptual proposal, not a completed formal standard. What MOS currently lacks is a proven formal specification - parse rules, ordering semantics, canonicalization proofs, abstraction laws, and demonstrable mapping behavior. Without that formal layer, MOS remains a strong conceptual proposal and a research direction rather than a settled technical theory. But within that scope, the prior-art matrix shows the combination is not already available in any single paradigm.

## Implications for Interoperable Socio-Technical Systems

If the MOS formulation holds, its implications are practical as well as conceptual.

The first implication is a reduction in integration friction. When nodes can express their local structures within a shared grammar and attach explicit mappings, the cost of onboarding new participants no longer grows as a purely pairwise burden. Translation work remains necessary, but it becomes explicit, inspectable, and reusable.

The second implication is a change in how coordination is organized. Systems can coordinate through references to meaningful abstractions rather than through repeated shipment of opaque files. This supports more incremental, composable, and auditable forms of cooperation.

The third implication is better handling of evolution. Because the grammar is designed for settings in which information form cannot be fully pre-limited, the system can tolerate new distinctions, new substructures, and new local variants without immediately treating them as schema violations. Growth in meaning becomes an expected condition rather than a breakdown of the model.

The fourth implication is organizational rather than purely technical. A grammar-centered approach offers a way to preserve local autonomy while still enabling network-level coordination. Participants need not abandon their internal models in order to join a broader interoperable network. Instead, they expose the relevant structures through shared grammar, mapping, provenance, and policy.

For socio-technical systems, this matters because interoperability failures are rarely just software failures. They are failures of coordination under change. A model that reduces the need for hidden conventions and ad hoc translators could therefore improve not only data exchange, but also the ability of organizations to coordinate action across heterogeneous tools and institutions.

## Limits and Non-Claims

A paper of this kind requires explicit boundaries.

First, self-describing structure does not eliminate the need for **semantic agreement**. Systems may still interpret similar abstractions differently, and no grammar alone can abolish the need for domain knowledge, negotiated meaning, or institutional governance.

Second, explicit mappings do not eliminate **translation work**. They simply make that work more systematic, inspectable, and reusable. MOS should not be presented as a system in which difference disappears. It is a system in which difference is formalized.

Third, provenance and policy do not create **trust** by themselves. They create the conditions under which trust can be audited, challenged, and reasoned about. Social legitimacy remains partly external to the representation.

Fourth, the paper does not claim that MOS is already a completed formal standard. The exact force of its novelty depends on future specification work: parse rules, ordering semantics, canonicalization proofs, abstraction laws, and demonstrable mapping behavior. Without that formal layer, MOS remains a strong conceptual proposal rather than a settled technical theory.

Fifth, MOS does not claim that graph databases, RDF, IPLD, CBOR, or Avro are incorrect, incomplete, or weak in their own domains. The novelty claim is specific and comparative: MOS appears to target a combination that those paradigms do not individually or jointly deliver in a unified form. Each is a genuine and valuable precedent.

Sixth, the paper does not claim universality in the metaphysical sense. It claims a bounded relevance for heterogeneous, evolving systems in which information form cannot be completely pre-limited and in which interoperability must survive local autonomy and change.

These non-claims are not weaknesses. They are what make the argument durable.

## Conclusion

The problem that motivates MOS is not the absence of data exchange. It is the persistence of inoperability in systems that already exchange data. Format-first integration solves transmission more easily than it solves meaning, and as socio-technical networks evolve, that gap widens. Existing research traditions provide many necessary ingredients - semistructured data, linked data, path-centric graphs, content-addressed traversal, deterministic encoding, canonicalization, schema matching, and ontology alignment - but no single dominant model has made abstraction-centered reproducibility, self-describing structure, reversible mapping, and semantic interoperability the shared core of one formal system.

MOS is most defensibly understood as a response to that gap. It is not best described as another database, nor primarily as a graph store. It is better described as a datum-native semantic grammar and abstraction calculus for interoperable systems. Its potential distinctness lies in centering the reproducible abstraction rather than the record, the document, or only the graph fact; in requiring structure, boundaries, and semantic cues to be explicit; in defining two non-redundant canonical forms (MSS for full ordered structure, hyphae for minimal abstraction identity); and in treating mapping, semantic difference, provenance, and canonical reproducibility as coequal parts of interoperability.

Whether MOS ultimately succeeds as a formal contribution depends on future proof, not on rhetoric. It must demonstrate that its abstractions can be parsed, addressed, canonicalized, mapped, and resolved across heterogeneous systems in ways that existing paradigms do not already provide in combination. But framed in that bounded way, MOS has a credible and academically serious position: it is a proposal for how independently evolving systems might remain interoperable when the form of meaningful information cannot be frozen in advance.

## References

### External Technical Standards and Academic Works

Abiteboul, S., Quass, D., McHugh, J., Widom, J., & Wiener, J. L. (1997). The Lorel query language for semistructured data. *International Journal on Digital Libraries, 1*(1), 68-88.

Angles, R., Arenas, M., Barceló, P., Hogan, A., Reutter, J., & Vrgoc, D. (2018). Foundations of modern query languages for graph databases. *ACM Computing Surveys, 50*(5), 1-40.

Apache Software Foundation. (2023). *Apache Avro specification*. https://avro.apache.org/docs/current/specification/

Bormann, C., & Hoffman, P. (2020). *Concise Binary Object Representation (CBOR)* (RFC 8949). Internet Engineering Task Force. https://www.rfc-editor.org/rfc/rfc8949

Euzenat, J., & Shvaiko, P. (2013). *Ontology matching* (2nd ed.). Springer.

Longley, D., & Sporny, M. (2023). *RDF dataset canonicalization* (W3C Candidate Recommendation). World Wide Web Consortium. https://www.w3.org/TR/rdf-canon/

Protocol Labs. (2021). *IPLD: The data model of the content-addressable web*. https://ipld.io/docs/

Sporny, M., Longley, D., Kellogg, G., Lanthaler, M., Champin, P.-A., & Lindström, N. (2020). *JSON-LD 1.1* (W3C Recommendation). World Wide Web Consortium. https://www.w3.org/TR/json-ld11/

Star, S. L., & Griesemer, J. R. (1989). Institutional ecology, "translations" and boundary objects: Amateurs and professionals in Berkeley's Museum of Vertebrate Zoology, 1907-39. *Social Studies of Science, 19*(3), 387-420.

Tolk, A., & Muguira, J. A. (2003). The levels of conceptual interoperability model. In *Proceedings of the 2003 Fall Simulation Interoperability Workshop*. Simulation Interoperability Standards Organization.

W3C. (2014). *RDF 1.1 concepts and abstract syntax* (W3C Recommendation). World Wide Web Consortium. https://www.w3.org/TR/rdf11-concepts/

### Internal Project Materials

- *Research Foundations for a Schema-Agnostic Abstraction-Path Data Model* (`drr-schema_agnostic_abstraction_path_data_model.md`)
- *Defining MOS as Novel and Distinct* (`mos_novelty_definition.md`)
- *Mapping MyCite Datum Logic to a Database Schema* (`mycelial_ontological_schema.md`)
- *MOS Operating SQL-Backed Core Declaration Draft* (`mos_sql_backed_core_declaration_draft.md`)
- *Self-Describing Semantic Grammars* (`self-describing_semantic_grammars.md`)
- *Interoperability in Socio-Technical Networks* (`interoperability_in_socio-technical_networks.md`)
- *Information Technology and Social Systems* (`information_technology_social_systems.md`)
- *Shape-Addressed Mixed-Radix Address Space* (`shape_addressed_mixed_radix_address_space.md`)
