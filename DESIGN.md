# Simavokab Design Document

> **Status:** Working draft, v0.1. Companion to `GRAMMAR.md` (v0.5+).
> This document explains *why* the language is built the way it is.
> Readers who want the rules without the reasoning should read `GRAMMAR.md`.
> Readers who want to understand, critique, or extend the design should start here.

---

## 0. What Simavokab Is

Simavokab is a constructed language designed for **semantic precision under formal conditions**. It is not a replacement for natural language in everyday life, nor an attempt to capture the full expressive range of poetry, humour, or casual speech. It is a precision instrument — a register optimised for contexts where ambiguity is costly: legal drafting, technical specification, philosophical argument, cross-cultural formal communication, and machine-readable discourse.

The name encodes the goal: *sim* (precise, clear) + *vok* (voice, language) + *-ab* (abstract suffix) = language of precision.

### Non-goals

Simavokab explicitly does not aim to be:

- **Maximally naturalistic.** Natural languages are the product of evolutionary and social pressures that optimise for speed, social bonding, and ambiguity-tolerance. Those are not the pressures here.
- **Culturally neutral.** No language is. Simavokab encodes specific philosophical commitments (listed below) and anyone using it should understand them.
- **Minimal.** Toki Pona's strength — a vocabulary of ~120 words — is also its limitation. Simavokab aims for sufficient vocabulary to express technical and philosophical ideas without circumlocution.
- **Poetic-first.** The design prioritises denotation over connotation, precision over evocation. A poet could use Simavokab, but would be working against the grain.
- **A universal language for all humanity.** The phonology is learnable across language backgrounds, but the design philosophy is specific and the intended user is someone who has chosen precision as a value.

---

## 1. The Precision Principle

The foundational design claim can be stated in one sentence:

> **Ambiguity is optional in Simavokab, never mandatory.**

This requires explanation, because it is sometimes misread as a demand for maximal explicitness. That is not the claim. The claim is directional: wherever natural language *forces* ambiguity — where there is no available surface form to express a distinction you need — Simavokab provides one. The speaker then chooses whether to use it.

Examples of mandatory ambiguity in English that Simavokab resolves:

| English expression | Ambiguity | Simavokab resolution |
|---|---|---|
| "John's book" | ownership, authorship, subject, topic, relation? | eleven distinct constructions (§4.6 GRAMMAR) |
| "Mistakes were made" | who made them? was there an agent at all? | indeterminate pronoun series forces class-level commitment (§7.3) |
| "The door is open" | current state vs. completed event | zero-copula adjective vs. resultative aspect |
| "some people" | indefinite quantity vs. social collective | *perasunes* (plural) vs. *perasup* (collective) |

The speaker of Simavokab can always choose a shorter, less specified form in informal register. What they cannot do is be trapped in an ambiguity they want to resolve.

---

## 2. Philosophical Foundations

### 2.1 Ontological Realism

The noun class system (§3 GRAMMAR) rests on a commitment to **ontological realism**: the view that there are genuine distinctions in reality — between living and non-living things, between sapient agents and non-sapient organisms, between artifacts and natural objects — and that a well-designed language should reflect them rather than collapse them.

This is a substantive philosophical position. A thoroughgoing nominalist might object that the category boundaries are not sharp (where does a virus fall? is a corporation "real"?). Simavokab's response is that contested boundaries are a feature of reality, not a failure of classification. The noun class system does not pretend the categories are crisp; it provides explicit coercion mechanisms for entities that span categories (see ONTOLOGY.md §3), and it requires the speaker to commit to a classification, making the commitment visible and contestable.

The alternative — no noun classes, or purely grammatical gender — produces a language where ontological confusion is invisible in the surface form. Simavokab makes the confusion explicit so it can be addressed.

### 2.2 Agency and Causation

The most consistent design thread in Simavokab is the **primacy of agency**. Several features follow from this commitment:

**The valency suffix system** (*-an/-in/-on*) requires every verb to declare its argument structure. There is no default transitivity that could be exploited to obscure whether something was done or merely happened.

**The absence of passive morphology** is a consequence of agency-primacy, not an arbitrary restriction. When English says "mistakes were made," it achieves something philosophically important: it describes an event while leaving the causal structure unspecified. Simavokab makes this impossible without a choice. The speaker must select from:
- *hun pas makin tal berabes* — "some sapient agent made mistakes" (agent exists, class specified)
- *zan pas makin tal berabes* — "something/someone (class unknown) made mistakes" (agent exists, class unspecified)
- *tal berabes pas makan* — "the mistakes came to be made" (anticausative; event occurred; no agent implied)
- *tal berabes makal* — "the mistakes are made" (result state; no event implied)

Each of these says something different, and each one is honest about what is being said. A language that permits genuine evasion of causal structure makes accountability harder to express and easier to avoid.

**The h-series indeterminate pronouns** (*hun, hem, hiv, har, hek, hab, hup*) are the practical implementation of this principle. They allow the speaker to describe an event without knowing the identity of the agent while still committing to the agent's ontological class. "Some sapient being did this" is different from "some natural force did this," and Simavokab requires the distinction.

**The topic construction** (*tev*) allows patient-focus in discourse without the passive's causal opacity. "As for the book, John made it" foregrounds the book without concealing John.

### 2.3 The Praxeological Strand

A secondary influence on the agency-primacy commitment comes from the praxeological tradition in economics. Praxeology is the study of purposeful human action — the view that social explanation begins with individual agents, and that collective phenomena are explained by composition of individual actions rather than by irreducible collective forces.

Simavokab's design can be understood without reference to this tradition. But several features reflect it:

- **The *-un* sapient class is ontologically privileged.** Only sapients act in the full sense — with purposes, means, and ends. The pronoun system, the indeterminate series, and the topic construction all treat sapient agency as a distinct category of causation.
- **The *-up* group class does not inherit sapient properties.** Groups are coordination structures composed of individual agents. A corporation (*timup* or a relevant compound) is not itself sapient; it acts only through its members. Simavokab's morphology makes this distinction: group nouns take *-up* pronouns, not *-un* pronouns. The grammar encodes methodological individualism at the level of pronoun agreement.
- **The *vazon* verb** ("use X for Y") directly encodes the means-end structure of purposeful action. The beneficiary preposition *por* encodes the end; the instrumental *pab* encodes the means.

Other frameworks (Kantian ethics, speech act theory, any tradition that distinguishes action from event) converge on similar design decisions.

### 2.4 The Fregean Copula Decomposition

English "is" performs at least four logically distinct functions:

| English | Logical operation | Simavokab |
|---|---|---|
| "The morning star is the evening star" | Identity | *bidin* |
| "Fido is a dog" | Type/instance membership | *tipin* |
| "Fido is large" | Property predication | *pirin* (formal); zero-copula (informal) |
| "God is" | Existence | *zivan* |
| "Fido is part of the pack" | Part-whole | *patin* |
| "Fido is a member of the club" | Set membership | *mibin* |

Frege's analysis in the *Grundlagen der Arithmetik* (1884) established that these are logically distinct, and that conflating them produces the pseudo-problems that have plagued much of Western metaphysics (the ontological argument for God's existence is a famous casualty: it treats existence as a property predicate when it is not). Simavokab declines to conflate them. The zero-copula predicative adjective construction handles the most common informal case efficiently; the explicit verb forms are available when precision matters.

### 2.5 The Leibnizian Possessive Decomposition

The English possessive "'s" and the preposition "of" both collapse a wide range of relations into a single surface form. Leibniz's project of a *characteristica universalis* — a notation in which the logical structure of propositions would be visible in their surface form — motivates the eleven-way decomposition in §4.6 of the grammar. The relations encoded are genuinely distinct: ownership involves legal and social facts; authorship involves causal and intentional facts; part-whole is mereological; kinship is genealogical or social. Collapsing them is convenient; it is not precise.

This decomposition also has a practical benefit: it makes the relations falsifiable. "John's book" could be contested in any number of ways depending on which relation is intended. *bukek bel Jonanom* (book authored by John) cannot be contested as an ownership claim; *Jonanom-os bukek* (John's owned book) cannot be contested as an authorship claim.

---

## 3. Computational Design

Simavokab was designed with formal parsability as an explicit criterion. The following properties are guaranteed by the phonotactic rules:

### 3.1 Deterministic Tokenisation

**The word-boundary rule:** any sequence of two consonants with no intervening vowel marks a word boundary. This property is detectable by a finite-state automaton scanning the character stream left to right. No lexicon lookup is required for segmentation.

Formal statement: the set of valid word forms is a regular language over the phoneme alphabet, and the set of valid utterances is the concatenation of valid word forms separated by word boundaries. Both are recognisable by finite automata.

**Consequence:** a Simavokab tokeniser is O(n) in the length of the input and requires no backtracking.

### 3.2 Part-of-Speech Detection

Every word's part of speech is identifiable from its suffix, without lexicon lookup:

| Suffix | POS |
|---|---|
| *-al* | Adjective |
| *-il* | Adverb |
| *-an* | Intransitive verb |
| *-in* | Transitive verb |
| *-on* | Ditransitive verb |
| *-em, -un, -iv, -ar, -ek, -ab, -up, -ag* | Noun (class encoded) |
| *-anom* | Proper noun |

Particles are a closed class, fully enumerable. Any CVC form not in the particle inventory and not matching the above suffixes is an error.

### 3.3 Verb-Position Register Detection

The three word orders (SOV, SVO, VSO) are distinguished by verb position, which is identifiable from the valency suffix. A parser can therefore determine the syntactic register of a clause as a side effect of finding the verb — no separate register-detection step is required.

### 3.4 Clause Boundary Detection

The particle *lev* marks the end of embedded clauses (relative and complement). Combined with the clause-initial markers (*taz-CLASS* for relative clauses, *gav* for complement clauses, *sif* for conditionals), clause nesting is explicitly bracketed. A pushdown automaton suffices for clause structure; the grammar is context-free.

### 3.5 Type Checking

Noun class suffixes encode an ontological type. Pronoun agreement is type-checked: a sapient (*-un*) antecedent takes *xun* or *mun/tun*; an animate (*-em*) antecedent takes *rem*; and so on. A class mismatch between a noun and its resumptive pronoun or coordinated pronoun is a detectable error, equivalent to a type error in a programming language.

### 3.6 Validation

Given the above properties, the following checks can be automated and run as continuous integration on the repository:

```python
def is_valid_word(word):
    # 1. Starts with a consonant
    # 2. Ends with a consonant
    # 3. No CC sequence within the word
    # 4. All phonemes in the declared inventory
    # 5. Suffix is a known grammatical suffix or particle
```

This script should be run against every example in GRAMMAR.md, every entry in LEXICON.md, and every derived form generated by the morphological rules. Invalid forms should fail the build.

---

## 4. Linguistic Influences

Simavokab is not original in its individual features; it is original in the particular combination and the philosophical motivation behind it. The main borrowings are:

| Source | Feature borrowed | Reason |
|---|---|---|
| Japanese | Topic marker (*tev*, cf. *wa* は) | Clean separation of information structure from grammatical relation |
| Hebrew, Persian, Arabic | Resumptive pronouns in relative clauses | Explicit role-marking eliminates parsing ambiguity |
| Esperanto | Regular agglutinative morphology | Predictability and learnability |
| Lojban | Explicit valency, clause boundary particles | Ambiguity minimisation |
| Turkish, Quechua | Evidential system | Explicit encoding of epistemic source |
| Italian | Five-vowel system, consistent realisation | Cross-linguistic phonetic accessibility |
| Austronesian languages | Simple syllable structure (CV-based) | Parseability and pronounceability |
| Frege (*Grundlagen*) | Copula decomposition | Logical precision in predication |
| Leibniz (*Characteristica*) | Possessive decomposition | Surface visibility of logical structure |
| Aristotle | Ontological categories, causal roles | Motivated noun class and preposition systems |

Unlike Esperanto or Interlingua, Simavokab does not privilege European vocabulary. Number roots are drawn from Latin (*cen*, *mil*), Greek (*dek*), Russian (*sem*), and Cantonese (*luk*). Lexical roots will continue to be drawn from multiple language families, with phonotactic adaptation as the constraint rather than etymological origin.

### A note on orthography

The consonant symbols *j* (= /ʒ/), *x* (= /ʃ/), and *c* (= /tʃ/) are kept despite being counterintuitive for many learners of European languages. The reasons:

1. They preserve strict one-symbol-per-phoneme correspondence, which is valuable for both parser clarity and consistent transcription.
2. They maintain a compact, pure-ASCII orthography with no digraphs or diacritics.
3. The phoneme-to-symbol mapping can be learned in minutes from a reference card; the cognitive cost is front-loaded and small.
4. Changing them after vocabulary has been established would be a much larger disruption than learning the conventions initially.

The phoneme /ʒ/ is cross-linguistically rare, but one unusual phoneme in an 18-consonant inventory is an acceptable cost for the lexical space it opens. Speakers who cannot produce /ʒ/ may substitute /ʃ/ or /dʒ/ without meaning difference; the sound distinction is maintained in writing.

---

## 5. Design Decisions Log

Major design decisions are logged in `DESIGN_DECISIONS.md` with the reasoning and alternatives rejected. This document covers the foundational philosophy; the decisions log covers specific choices and their history across versions.

Key decisions logged there include:

- Passive voice: why morphological passive was excluded and what replaces it
- The *-an/-in* alternation: semantic licensing conditions
- The *bel* particle: authorship vs. spatial origin overloading (open)
- Case markers *sav/dob*: whether optional-in-practice defeats the purpose
- The *tev* topic construction: resumptive requirement in formal vs. informal register
- Number system: mixed-etymology roots and the decision not to use a constructed base

---

## 6. What Simavokab Is Not

**It is not a claim that Sapir-Whorf determinism is strong.** Simavokab does not assert that speakers of other languages cannot think precise thoughts; it asserts that having precise surface forms available makes certain kinds of communication easier and certain kinds of evasion harder.

**It is not politically neutral.** The primacy of individual agency over collective causation is a substantive commitment. The language makes it easier to ask "who did this?" than to say "it was done." Users should understand that this is a design choice, not a discovery about the nature of language.

**It is not finished.** The grammar is at v0.5; the vocabulary is incomplete; the complement clause system is being formalised; narrative tense and sequence-of-tense rules are open. This document reflects the design as it stands, not as it will eventually be.

**It is not Lojban.** Lojban pursues logical completeness at the cost of human speakability. Simavokab accepts some imprecision in the interest of remaining a language that could in principle be spoken fluently. The evidential system is optional, not mandatory; informal register permits gaps and ellipsis that formal register does not.
