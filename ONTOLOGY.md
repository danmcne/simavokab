# Simavokab Ontology Reference

> **Status:** Working draft, v0.1. Companion to `GRAMMAR.md` §3 and `DESIGN.md` §2.1.
> This document gives the full rationale for the noun class system, treats contested
> classifications, and specifies the rules for semantic coercion.

---

## 0. Why a Noun Class System

Simavokab assigns every noun a mandatory class suffix. This is not grammatical gender in the traditional sense — the classes do not sort nouns arbitrarily, as Latin's *nauta* (sailor, masculine, because men sailed) or German's *das Mädchen* (girl, neuter, because diminutives are neuter). The classes are motivated by ontological distinctions the language regards as real and important.

The practical payoffs are:

1. **Type-safe pronoun agreement.** A noun's class determines which third-person pronoun refers to it. A mismatch is a detectable error — the language equivalent of a type error in a programming language.
2. **Unambiguous relative clause resumption.** The relative marker *taz-* takes the antecedent's class suffix, making relativisation explicit regardless of word order.
3. **Forced ontological commitment.** Assigning a noun a class is a claim about what kind of thing it is. That claim can be contested, refined, or coerced — but it cannot be avoided.

The cost is real: contested cases require decisions, and decisions can be wrong or conventionally varied. This document attempts to make those decisions principled and consistent.

---

## 1. The Ontological Tree

```
entity
├── concrete
│   ├── living
│   │   ├── animate (capable of self-directed movement, goal-directed behaviour)
│   │   │   ├── sapient (capable of purposeful rational action, language-use)  → -un
│   │   │   └── non-sapient animate                                            → -em
│   │   └── non-animate living (grows, reproduces; no goal-directed movement)  → -iv
│   ├── natural (non-living, non-made, occurring independently of sapient agency) → -ar
│   └── artificial (made, constructed, or substantially shaped by sapient agency) → -ek
├── abstract (no spatiotemporal location; exists as a conceptual object)         → -ab
├── group / collective (composed of members; has internal structure)             → -up
└── process / gerund (nominalised event or activity)                             → -ag
```

The tree has three levels of decision:

- **Living vs. non-living:** does the entity metabolise, reproduce, respond to its environment through biological processes?
- **Animate vs. non-animate living:** does the living entity exhibit goal-directed movement (locomotion toward goals, not merely growth toward light)?
- **Sapient vs. non-sapient animate:** does the animate entity exhibit purposeful rational action — the capacity to form intentions, select means, and act toward consciously held ends?
- **Natural vs. artificial non-living:** is the entity's existence and form independent of sapient agency, or the result of it?

---

## 2. The Eight Classes

### 2.1 Sapient (*-un*)

Entities capable of purposeful rational action: forming intentions, choosing means, acting toward consciously held ends. Language-use is the canonical marker, but the category is not defined by it.

**Canonical members:** humans, human persons in all roles.

**Edge cases:**

| Entity | Classification | Reasoning |
|---|---|---|
| Human infant | *-un* | Potential sapience; full membership by convention |
| Human in permanent unconscious state | *-un* | Legal, moral, and social personhood maintained |
| Fictional sapient (in narrative context) | *-un* | Narrative truth; the fictional frame doesn't demote the entity's in-world classification |
| Non-human great ape | *-em* default; *-un* by explicit coercion | Strong evidence of goal-directed behaviour; current convention reserves *-un* for entities with full communicative and intentional capacity. Coercion (*-un*) is available where the speaker judges it applicable |
| Cetaceans (dolphins, whales) | *-em* default | As above |
| AI system | *-ek* default; *-un* by explicit coercion | See §3.4 |
| Deity (in theological discourse) | *-un* | The theological claim is that deities act purposefully; *-un* reflects this without endorsing it |

**Note on sapience as attribution:** The *-un* class encodes the speaker's attribution of sapience, not a metaphysical fact. Saying *remun* (animal-as-sapient) is a coercion, not an error. It expresses a position.

---

### 2.2 Animate (*-em*)

Living entities with goal-directed movement and behavioural responses but not attributed full sapience.

**Canonical members:** mammals (excluding humans), birds, fish, reptiles, insects, most invertebrates.

**Edge cases:**

| Entity | Classification | Reasoning |
|---|---|---|
| Sponge | *-iv* | No goal-directed movement; sessile |
| Jellyfish | *-em* | Exhibits movement responses to stimuli; borderline |
| Bee colony as a whole | *-up* | The colony as collective; individual bees are *-em* |
| Domesticated animal with extensive human-shaped behaviour | *-em* | Construction does not reclassify; origin does not override class |

---

### 2.3 Living non-animate (*-iv*)

Living entities that grow, reproduce, and respond biologically to their environment but do not exhibit goal-directed locomotion.

**Canonical members:** plants, trees, ferns, mosses.

**Edge cases:**

| Entity | Classification | Reasoning |
|---|---|---|
| Fungus | *-iv* | Living, non-animate; classification holds despite phylogenetic distance from plants |
| Lichen | *-iv* | Composite organism; treated as living non-animate entity |
| Bacterium | *-iv* | Living, non-animate; unicellular does not change the category |
| Virus | *-iv* default | Disputed: metabolises only within host cells; some biologists deny full living status. *-iv* is the conservative choice; *-ar* is available for speakers who treat viruses as non-living chemical entities |
| Prion | *-ar* | Non-living; misfolded protein; no metabolism or reproduction independent of host processes |
| Cultured cell line | *-iv* | Living tissue; classification holds even outside an organism |

---

### 2.4 Natural (*-ar*)

Non-living, non-made concrete objects whose existence and form are independent of sapient agency.

**Canonical members:** rocks, rivers, mountains, weather events, celestial bodies, minerals, geological formations.

**Edge cases:**

| Entity | Classification | Reasoning |
|---|---|---|
| River in a heavily managed watershed | *-ar* | Natural origin dominates; *-ek* available by coercion if the speaker wishes to foreground the engineering |
| Artificial lake | *-ek* | Made; sapient agency is constitutive of its existence |
| Diamond (natural) | *-ar* | Natural formation |
| Diamond (lab-grown) | *-ek* | Made; same chemical substance, different origin |
| Storm | *-ar* | Natural process; use *-ag* if nominalising the event ("the storming") |
| Earthquake | *-ar* | *kanan* is the standard root; see also §4 note on *zaran* (deprecated) |
| Human body (as physical object) | *-ar* for the body-as-matter; but body-as-person is *-un* | The coercion is contextually determined |

---

### 2.5 Artificial (*-ek*)

Concrete objects made or substantially shaped by sapient agency.

**Canonical members:** tools, buildings, machines, written texts, manufactured goods, vehicles, clothing.

**Edge cases:**

| Entity | Classification | Reasoning |
|---|---|---|
| Book as physical object | *-ek* | Manufactured artifact |
| City (physical infrastructure) | *-ek* | Built; *sitek* is the correct form (not *sitak*) |
| City (as social/political entity) | *-up* | Coercion; see §3.1 |
| Software (installed program) | *-ek* | Constructed artifact |
| Running process (executing instance) | *-ag* | Nominalised event; the execution is a process |
| Law (written statute) | *-ek* | Constructed text artifact |
| Ship of Theseus | *-ek* throughout | Class does not change with gradual material replacement; the artifact identity is conventional |
| Genetically modified organism | *-iv* with *-ek* coercion available | Living entity; the modification is a property, not a reclassification. Coercion to *-ek* available where the speaker wishes to foreground the construction |

---

### 2.6 Abstract (*-ab*)

Entities without spatiotemporal location that exist as conceptual or relational objects.

**Canonical members:** numbers, properties, relations, laws-as-principles, emotions (as types), theories, languages (as systems), norms, values.

**Notes:**

Abstract does not mean *subjective*. The number 7 and the property of being red are both abstract in the relevant sense — they are not located anywhere, cannot be touched, and do not interact causally with the physical world. This is a metaphysical claim, not a claim about certainty or importance.

**Edge cases:**

| Entity | Classification | Reasoning |
|---|---|---|
| Love (the emotion-type) | *-ab* | Abstract property/state type; a particular instance of love (*mun-os lovab*) is also abstract |
| Fear (an individual's current fear) | *-ab* | Mental state; experiencer expressed with *pes* (*fimab pes mun* = "my fear") |
| Law (principle, e.g. "the law of gravity") | *-ab* | Abstract relation/regularity |
| Language as a system | *-ab* | *vokab bel Simavokab* = "the language of Simavokab" |
| Money as institution | *-ab* | The monetary system; contrast *-ek* for a physical coin |
| Mathematical proof | *-ab* | Abstract object |
| A dream | *-ab* | Mental/abstract; the event of dreaming is *-ag* |

---

### 2.7 Group (*-up*)

Entities constituted by members with some form of internal structure, coordination, or shared identity. Crucially, the group is not merely a plurality (more than one member); it is a structured collective.

**Canonical members:** teams, organisations, populations, communities, species (as a collective), families (as units), institutions.

**Critical distinction: *-up* vs. plural (*-es*):**

| Form | Meaning | Example |
|---|---|---|
| *perasunes* | multiple persons (mere plurality) | "there were people in the room" |
| *perasup* | a people, a community (structured collective) | "the people voted as a body" |
| *kanemes* | multiple dogs | "three dogs entered" |
| *kanup* | a pack of dogs (coordinated group) | "the pack hunted together" |

A forest is *-ar* (natural object), not *-up* (the trees are not a structured collective). A wolf pack exhibiting coordinated hunting behaviour is *-up*. This distinction matters because *-up* nouns do not inherit *-un* (sapient) properties — groups act only through their individual members.

**Edge cases:**

| Entity | Classification | Reasoning |
|---|---|---|
| Corporation | *-up* | Structured collective of individuals; acts through its members |
| Nation-state | *-up* | Political collective; the territory is *-ar*, the state as polity is *-up* |
| Family (as social unit) | *-up* | Structured collective |
| Species (biological) | *-up* | Collective of individual organisms |
| Jury | *-up* | Structured collective with formal membership and role |
| Crowd (temporary, unstructured) | *perasunes* (plural) | No internal structure; not a collective in the relevant sense. If coordination emerges, coercion to *-up* is available |
| File system (computers) | *-ek* or *-up* | If treated as structured container of artifacts: *-ek*; if treated as a community of files with relations: *-up*. Speaker's framing determines the class |

---

### 2.8 Gerund / Process (*-ag*)

Nominalised events, activities, or processes. These are the noun forms of verbs.

**Canonical members:** running (*ronag*), speaking (*vokag*), giving (*donag*), destruction (*derinag*).

**Notes:**

The *-ag* class is the nominal form of an event, not a description of an ongoing state. "The running" refers to an event of running; "the runner" is *-ir-un* (agent-infix + sapient class). The gerund class is frequently used with associative prepositions: *derinag pes sitek* = "the destruction of the city" (patient of event), *movanag pab Jonanom* = "John's arrival" (agent of event).

---

## 3. Semantic Coercion

Natural languages routinely use the same noun in ontologically distinct ways:

> "France invaded Belgium." *(France as political agent — *-up*)*
> "France is hexagonal." *(France as geographic territory — *-ar*)*
> "France won the World Cup." *(France as national team — *-up*)*

In Simavokab, this is **explicit coercion**: the same lexical root appears with a different class suffix to foreground a different ontological aspect of the referent. Coercion is not an error; it is a deliberate communicative choice that reveals the speaker's framing.

### 3.1 How Coercion Works

A noun's **canonical class** is its default classification — the class that most naturally applies given the entity's primary nature. Coercion substitutes a different class suffix on the same root, signalling that the speaker is foregrounding a non-default aspect.

Example: *sitek* (city as artifact, canonical) vs. *situp* (city as political community, coercion) vs. *sitar* (city as geographic location, coercion):

```
tal sitek pas deran.         "The city [as built structure] was destroyed."
tal situp pas vokin.         "The city [as community] spoke."
tal sitar magal.             "The city [as place] is large."
```

### 3.2 Coercion Table for Contested Entities

| Entity | Canonical | Coercions available | Notes |
|---|---|---|---|
| City | *-ek* (built artifact) | *-up* (polity), *-ar* (geographic place) | All three are common |
| Law | *-ek* (statute text) | *-ab* (principle) | Distinct roots recommended: *lawek* vs. *lawab* |
| Money | *-ek* (coin/note) | *-ab* (institution), *-up* (economic community) | |
| Nation | *-up* (polity) | *-ar* (territory) | |
| Software | *-ek* (program) | *-ag* (running process) | |
| AI system | *-ek* (artifact) | *-un* (if sapience attributed) | Coercion to *-un* is a strong claim |
| Disease | *-iv* (biological entity) | *-ag* (as process/event) | |
| Language | *-ab* (abstract system) | *-ek* (as written artifact, e.g., a text) | |

### 3.3 Limits of Coercion

Coercion to *-un* (sapient) is the strongest available claim and should be used deliberately. Attributing sapience to an artifact, a group, or a natural force is a substantive assertion, not a casual figure of speech. In formal register, the speaker commits to the attributed property.

Coercion does not change pronoun agreement: once a noun is used with a coerced class in a sentence, pronouns in that sentence must agree with the coerced class, not the canonical class.

---

## 4. Polysemous Nouns and Recommended Roots

Some concepts naturally span classes in a way that justifies separate roots rather than coercion of a single root. The difference: **coercion** is used when the same referent is being viewed through different ontological lenses. **Separate roots** are used when the senses are genuinely distinct referents that happen to share an English gloss.

| Concept | Distinct roots recommended | Notes |
|---|---|---|
| "Law" as statute vs. "law" as principle | *lawek* / *lawab* | Different referents |
| "Court" as building vs. "court" as institution | *kurek* / *kurup* | Different referents |
| "Book" as physical object vs. "book" as text | *bukek* / *bukab* | Often conflated; distinction sometimes useful |
| "Mind" as brain vs. "mind" as mental life | *minar* (natural organ) / *minab* (abstract mental system) | |
| "Time" as duration vs. "time" as moment | *timab* (abstract duration) / *tipar* (point in time, natural) | |

Where both roots are needed, LEXICON.md will list them as separate entries with cross-references.

---

## 5. The Plural/Collective Distinction: Formal Statement

Let *N* be a noun root and *C* a class suffix.

- **Plural** (*N + C + -es*): asserts the existence of multiple tokens of type *N-C*. No internal structure, coordination, or collective identity is implied.
- **Collective** (*N + -up*): asserts the existence of a structured collective whose members are of type *N-C*. Internal structure, shared identity, or coordinated function is implied.

These are not interchangeable:

```
tal perasunes pas vokin.     "The people (many individuals) spoke."  (possibly not in concert)
tal perasup pas vokin.       "The people (as a body) spoke."         (collective speech act)
```

A sentence like "the people elected a president" nearly always requires *-up*, since election is a coordinated collective act. A sentence like "people were standing in the rain" nearly always uses *perasunes*, since no collective structure is implied.

When uncertain, use the plural (*-es*) for safety in informal register; use the collective (*-up*) only when the collective structure is relevant to the meaning.

---

## 6. Open Ontological Questions

These are not resolved in v0.5 and are flagged for future treatment:

| Question | Status |
|---|---|
| Moral status and class: do moral patients automatically get *-un*? | Open. Recommendation: *-un* encodes attributed sapience, not moral status. Moral status is a separate predicate (*pirin* + relevant abstract). |
| Digital persons and legal personhood | Open. Default: *-ek*; coercion to *-un* by explicit assertion. |
| Collective intentionality: can *-up* entities have intentions? | Partially addressed: groups act through members. A *-up* entity cannot take *temin* (intend) without coercion commentary. |
| Emergent phenomena (e.g. markets, ecosystems) | Open. Current default: *-ar* for natural emergent systems; *-ab* for abstract emergent patterns; *-up* for participant-constituted emergent systems. |
| Class assignment for untranslatable cultural concepts | Open. Policy: classify by the ontological structure of the concept, not by surface grammar of the source language. |
