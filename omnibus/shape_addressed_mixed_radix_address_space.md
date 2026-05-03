# Shape-Addressed Mixed-Radix Address Space (SAMRAS)

## Abstract

A Shape-Addressed Mixed-Radix Address Space, or SAMRAS, is not primarily a storage format, a taxonomy file, a UI navigation device, or a particular implementation artifact. It is a structural concept. More specifically, it is a conceptual model for making a variable-branching hierarchy authoritatively addressable by shape rather than by semantic labeling. In a SAMRAS, the governing authority is not a name, not a row, not a stored full path, and not a visual tree. The governing authority is the reconstructible structure itself.

This matters because most hierarchical systems silently confuse semantic attachment with structural identity. They treat titles, categories, or folders as though those are the hierarchy. They are not. Those things are overlays. A hierarchy only becomes structurally authoritative when valid addresses can be determined from the structure itself. SAMRAS exists to provide that condition. It defines an address space in which each segment is constrained by local structural reality, and in which a node is identified by its ordinal relation within a variable topology rather than by an arbitrary naming convention.

The conceptual significance of SAMRAS is therefore broader than any one implementation. It is a way of thinking about hierarchy, addressability, and structural authority in any domain where local branching may vary and where semantic attachments must remain secondary to structural form.

## The problem of hierarchical identity

A hierarchy is often treated as though its labels are its structure. That is a categorical error.

A folder name is not a hierarchy. A title is not a hierarchy. A row in a table is not a hierarchy. Even a stored path string is not, by itself, a hierarchy. Those things may express or reference structure, but they do not constitute it. The structure of a hierarchy is the ordered relation of containment and branching that makes certain positions valid and others invalid.

When this distinction is not made, systems drift. Titles become mistaken for authorities. A rendered view becomes mistaken for the source of truth. Rows are extracted and rearranged until the view appears coherent, even if the underlying structural logic no longer is. Once that happens, the system may still look organized, but it is no longer structurally authoritative. It has become semantically staged rather than structurally governed.

SAMRAS begins from the refusal of that confusion. It does not ask what the nodes are called first. It asks what structure exists first. Only after that question is settled can the system meaningfully address anything within that structure.

## What SAMRAS is

SAMRAS is a shape-addressed mixed-radix address space represented as a structural value.

Each of those terms matters.

It is shape-addressed because valid addresses are determined by the topology of the structure. The hierarchy is not imposed afterward upon a list of names. The hierarchy is already there in the structural authority, and the addresses emerge from it.

It is mixed-radix because the valid ordinal range of any address segment is not fixed globally. It depends on the local child capacity of the parent under which that segment occurs. The allowed next value is therefore context-sensitive. A segment is valid not because it belongs to a universal base, but because the parent structure authorizes it.

It is an address space because it defines a domain of possible positions. It does not merely list occupied records. It defines what positions can be validly referred to.

It is a structural value because what is stored authoritatively is not the final semantic view but the structure from which that view must be derived. In canonical form, this structural value preserves child-count information in such a way that the topology can be reconstructed and valid addresses can be derived from ordinal relation.

This is the simplest precise statement of the concept: SAMRAS is a structural authority for variable hierarchies.

## Why shape-addressed matters

The phrase shape-addressed is the conceptual center of SAMRAS.

Most systems assume that addressing begins with explicit identifiers. SAMRAS assumes the opposite. Addressing begins with shape. The structure defines the legal positions, and the address is an expression of position within that structure.

That means a node does not need to store its full address as an intrinsic property of itself. Its address is recoverable from the structure because the structure carries the branching logic that makes that address valid. The node is not first named and then placed. It is first positioned and only then may be named.

This reverses a common software habit. The usual habit is to begin from semantic tags and then arrange them. SAMRAS begins from formal position and only afterward permits semantic attachment. That is why the concept remains stable even when names change, when titles are missing, or when overlays are inconsistent. The authority has not moved, because the authority was never the overlay.

A structurally authoritative hierarchy must survive semantic incompleteness. SAMRAS is built precisely so that it can.

## Why mixed-radix matters

The phrase mixed-radix identifies the second essential property.

A uniform radix assumes that every position at a given level is governed by the same capacity rule. SAMRAS does not make that assumption. It permits local branching to vary by parent. One node may authorize three children, another eighty-one, another none. The address space is therefore locally constrained rather than globally flattened.

This is not merely a technical encoding detail. It is a conceptual claim about hierarchy itself. Real variable structures are not uniform partitions. They do not behave like a fixed decimal lattice. They behave like shaped topologies whose local possibilities differ according to their position in the whole.

SAMRAS preserves that reality. It does not force variable structure into a homogeneous frame merely for convenience. Instead, it lets the structure remain variable and derives address validity from that variation.

That is why SAMRAS is the correct conceptual class for hierarchies whose local branching is part of their truth.

## Structural authority and semantic overlay

One of the most important distinctions in SAMRAS is the distinction between structure and overlay.

The structure is authoritative. Titles, labels, classifications, and descriptive metadata are not authoritative as structure. They are attachments to structure. They may be useful, necessary, or even indispensable for human interpretation, but they do not define which addresses are valid.

This distinction is what allows SAMRAS to remain domain-agnostic. The same structure can support biological taxonomies, administrative divisions, organizational namespaces, or any other hierarchical domain. The domain changes the semantic overlay, not the structural principle.

Once this is understood, several confusions disappear. A duplicated label is not a structural duplication unless it binds to the same structural position in violation of the namespace. A missing title is not the absence of a node if the position is structurally authorized. A visually rendered hierarchy is not the structural source of truth if it is only an interpretation of node rows or labels detached from the governing structural magnitude.

The structure governs. The overlay interprets. That order must not be reversed.

## Address derivation and the rejection of arbitrary path authorship

A SAMRAS address is not arbitrary text. It is a derived ordinal path.

The root level establishes the first set of valid positions. Each later segment expresses ordinal position among siblings under a parent already authorized by the structure. A valid address is therefore not simply any hyphenated string of integers. It is a path that the structure can justify.

This is why address derivation matters conceptually. It means the system can distinguish between a string that looks like an address and a position that is actually real in the governing structure. Only the latter is authoritative.

The consequence is that SAMRAS rejects silent fabrication. A path is not made valid because a human typed it. It is valid because the structure authorizes it. Conversely, a position may be real even when no human-readable label has yet been attached to it. Structural reality is prior to semantic decoration.

This is a stricter conception of addressability than most systems adopt. That strictness is the source of its value.

## Structural potentiality, ghost positions, and existential reference

SAMRAS does not reduce reality to already materialized records.

A structurally authorized position may exist without a stored title, without a semantic profile, and without a materialized row. Such a position is structurally real even if it is semantically undefined. This is one of the most conceptually distinctive aspects of SAMRAS.

A position can therefore be addressable before it is narratively filled in. The structure makes it available as a valid site of relation. Whether the system has yet attached a name, a description, or a bound object to that site is a separate matter.

This also makes possible more careful reference semantics. A reference may designate an exact node, a grouped set under a node, or an existential but unspecified descendant below a node. These are not the same thing, and SAMRAS is strongest when those distinctions are made explicit rather than inferred carelessly from syntax alone.

What this reveals is that SAMRAS is not only a model of occupied hierarchy. It is a model of structured possibility. It governs not only what is already semantically present, but also what is structurally available for future articulation.

## Mutation, continuity, and versioned change

A structurally authoritative address space must govern mutation as strictly as it governs existence.

In SAMRAS, mutation is not conceptually the editing of a raw magnitude by hand. Mutation is the transformation of a structure under rules that preserve or deliberately revise the authoritative address space. If a change is append-only, existing addresses can remain stable because new positions are added in a way that does not reorder prior ordinal relations. If a change would alter existing ordinal relationships in a non-append manner, then the structure has become a new layout and must be treated as such.

That principle matters because it prevents silent remapping. Without it, an address may appear to remain the same while secretly changing what it denotes. A structurally serious system cannot permit that. If the layout changes in a way that alters prior meaning, a new structural version is required.

The concept here is deeper than codec behavior. SAMRAS treats structural continuity as something that must be maintained explicitly, not assumed casually. Mutation is therefore a governed act of structural authorship, not an ad hoc revision of labels or rows.

## Domain-agnostic scope

SAMRAS is not inherently geographic. It is not inherently biological. It is not inherently administrative. Those are only domains in which variable hierarchical structure appears.

The same conceptual rules apply wherever there is a need to preserve an authoritative relation between hierarchy and address. If local branching may vary by parent, and if semantic names must not be allowed to become structural substitutes, then the conceptual conditions for SAMRAS are present.

This domain-agnostic quality is essential to its uniqueness. SAMRAS is not a domain schema masquerading as a general theory. It is a general theory of structurally governed variable hierarchy that can later be instantiated in domain-specific ways.

That is why the same addressing logic can apply across taxonomic domains, administrative domains, and other hierarchical namespaces while remaining the same concept.

## Why SAMRAS exists beside HOPS

The distinction between SAMRAS and HOPS clarifies the uniqueness of SAMRAS.

HOPS defines fixed subdivision. SAMRAS reconstructs variable shape.

That contrast should be read carefully. A HOPS is appropriate where every parallel node at a given level shares the same child capacity. The structure then defines a homogeneous partition schema for an ordered continuum. A SAMRAS is appropriate where local branching differs by parent and where the system must preserve that variation as part of the structure itself.

The difference is therefore not cosmetic. It is ontological.

A HOPS says, in effect, that the space is governed by level-homogeneous denotational capacities. A SAMRAS says that the space is governed by variable local topology. One defines subdivision. The other reconstructs shape.

This contrast helps prevent misuse. If one attempts to treat a variable hierarchy as though it were a fixed partition schema, the structure is flattened and local authority is lost. If one attempts to treat a homogeneous partition as though it required variable shape reconstruction, unnecessary complexity is introduced. The two concepts should remain distinct precisely because they solve different structural problems.

## Why SAMRAS is unique

The uniqueness of SAMRAS does not lie merely in its encoding layout. It lies in the conceptual discipline it imposes.

It insists that structural validity precede semantic convenience.

It insists that address be derived from structural relation rather than authored as arbitrary text.

It insists that variable local branching be preserved as structural truth rather than normalized away.

It insists that semantically absent positions may still be structurally real.

It insists that overlays remain overlays and not be confused for the authority they interpret.

It insists that mutation be treated as structural authorship under continuity rules rather than as ungoverned revision.

Taken together, those conditions make SAMRAS more than a notation. They make it a concept for structurally authoritative hierarchy.

## Conclusion

SAMRAS should be understood as a conceptual model for addressability in variable-shape hierarchies. Its purpose is not merely to encode data more compactly or to furnish a novel syntax. Its purpose is to establish a principled relation between structure and reference.

A SAMRAS does this by making shape authoritative. The structure preserves child-capacity relations. Valid addresses are derived from ordinal position within that variable topology. Semantic titles, names, classifications, and domain narratives are then permitted to bind onto those positions without becoming the source of structural truth.

This is what makes SAMRAS both technically rigorous and conceptually important. It provides a way to preserve hierarchy as hierarchy, rather than letting it dissolve into labels, rows, or rendered views. It gives a system the ability to say, with precision, that a position is valid because the structure authorizes it, not because someone happened to name it.

SAMRAS is a structurally authoritative, shape-addressed, mixed-radix address space for variable hierarchy. It is a concept of derived positional identity. It is a separation of structural truth from semantic overlay. And it is, for that reason, not reducible to any particular implementation that happens to express it.
