# Simavokab

**sim** (precise) + **vok** (language) + **-ab** (abstract) = *language of precision*

Simavokab is a constructed language designed for semantic precision under formal conditions. It provides explicit surface forms for distinctions that natural languages routinely collapse — causal structure, ontological type, epistemic source, and relational category — while remaining learnable and, in principle, speakable.

It is not a universal language, a minimalist language, or a replacement for natural language in everyday use. It is a precision instrument: a register built for contexts where ambiguity is costly.

> **Status:** Grammar v0.5 (working draft). Vocabulary in progress. Core architecture stable; complement clause syntax and narrative tense are the main open items.

---

## A First Example

**"If Mary knows that John made a machine, she must speak clearly to the team."**

```
Sif  Mariranom  sapin   gav  Jonanom  pas   makin    hal  masek   lev,
if   Mary-PROP  know-TR COMP John-PROP PST  make-TR  INDEF mach-ART CE

dan  xun   deb    vokin   simil    par   tal   timup.
then she-SAP must  say-TR  clearly  to    DEF   team-GRP
```

Even in this single sentence the key design decisions are visible: the verb declares its own valency (*sapin* = transitive, takes two arguments; *vokin* = transitive); the complement clause is explicitly bracketed (*gav … lev*); the noun *masek* carries a mandatory ontological class suffix (*-ek* = artifact); tense is a separate preverbal particle (*pas*); and the modal (*deb*) precedes tense in a fixed stacking order.

---

## Core Design Decisions

### 1. The Precision Principle

> Ambiguity is optional in Simavokab, never mandatory.

Where natural language *forces* ambiguity, Simavokab provides a surface form to resolve it. The speaker always chooses how much precision to deploy.

### 2. Phonotactics as a Parsing Contract

Every content and function word follows a strict **CVC(VC)\*** pattern: begins with a consonant, strictly alternates consonant and vowel, ends with a consonant. One consequence is immediately useful:

> **Any sequence of two consecutive consonants is a word boundary.**

Tokenisation requires no dictionary lookup. A finite-state automaton scans the character stream and emits boundaries wherever two consonants are adjacent. Morphological category is then readable from the suffix alone.

### 3. Agency Is Explicit

Simavokab has no passive morphology. This is not an aesthetic preference — it is a consequence of treating agency as the central organising category of language about events. When something happens, the grammar requires the speaker to commit to a description of the causal structure:

| Situation | Construction | Example |
|---|---|---|
| Known sapient agent | Active transitive | *hun pas derin tal bukek* "some person destroyed the book" |
| Unknown agent class | *zan* + transitive | *zan pas derin tal bukek* "something/someone (class unknown) destroyed it" |
| Known class, unknown identity | *h-* series + transitive | *har pas derin tal sitek* "some natural force destroyed the city" |
| Event, no agent implied | Anticausative (*-an*) | *tal bukek pas deran* "the book was destroyed" (no agent) |
| Result state only | Zero-copula adjective | *tal bukek derinal* "the book is destroyed" |
| Patient focus in discourse | Topic construction | *tal bukek tev, Jonanom pas makin rek* "as for the book, John made it" |

These six constructions collectively replace passive voice while forcing the speaker to say something more specific each time.

### 4. Ontological Type System

Every noun carries a mandatory class suffix encoding its ontological category. This suffix determines pronoun agreement, relative clause marking, and coercion possibilities — functioning as a grammatical type system.

```
entity
├── concrete
│   ├── living
│   │   ├── sapient                → -un    perasun  "person"
│   │   ├── animate (non-sapient)  → -em    kanem    "dog"
│   │   └── non-animate living     → -iv    dariv    "tree"
│   ├── natural (non-made)         → -ar    rokar    "rock"
│   └── artificial (made)          → -ek    bukek    "book"
├── abstract                       → -ab    lovab    "love"
├── group / collective             → -up    timup    "team"
└── process / gerund               → -ag    ronag    "running"
```

A noun's class suffix is not an arbitrary gender. It is a claim about what kind of thing the noun refers to — and that claim can be contested, refined, or deliberately overridden (see *Semantic Coercion* below).

### 5. The Copula Is Four Verbs

English "is" performs logically distinct functions that Simavokab keeps separate:

| Simavokab verb | Logical operation | Example |
|---|---|---|
| *bidin* | Identity | "the morning star is the evening star" |
| *tipin* | Type membership | "Fido is a dog" |
| *pirin* | Property predication (formal) | "the tree has bigness" |
| *zivan* | Existence | "God exists" |
| *patin* | Part-whole | "the wheel is part of the car" |
| *mibin* | Set membership | "Fido is a member of the pack" |
| *(zero copula)* | Property predication (informal) | *tal dariv magal* "the tree is big" |

### 6. Possessive Relations Are Explicit

English "'s" collapses eleven logically distinct relations into one surface form. Simavokab uses dedicated constructions for each:

| Relation | Construction | Example |
|---|---|---|
| Alienable ownership | OWNER-*os* + THING | *perasunos karak* "person's car" |
| Part-whole | THING *pes* WHOLE | *menak pes karak* "engine of the car" |
| Inalienable (body part) | PART *pes* PERSON | *memar pes mun* "my arm" |
| Kinship | ROLE *rel* PERSON | *buvun rel mun* "my father" |
| Authorship | THING *fab* AUTHOR | *vokab fab Bobanom* "Bob's words" |
| Beneficiary | THING *por* RECIPIENT | *bukek por ninun* "book for the child" |
| Agent of event | GERUND *pab* AGENT | *movanag pab Jonanom* "John's arrival" |
| Patient of event | GERUND *pes* PATIENT | *derinag pes sitek* "the city's destruction" |
| Temporal association | THING *den* TIME | *novab den nalab* "today's news" |
| Geographic origin | THING *bel* PLACE | *bovab bel Ital* "food from Italy" |
| Experiencer | STATE *pes* EXPERIENCER | *fimab pes mun* "my fear" |

---

## The Language at a Glance

### Phonology

**Consonants (18):** b c d f g h j k l m n p r s t v x z
**Vowels (5):** a e i o u (Italian quality; never reduced; no diphthongs)

Key symbol conventions (one grapheme, one phoneme throughout):

| Symbol | Sound | As in |
|---|---|---|
| c | /tʃ/ | *ch*urch |
| j | /ʒ/ | mea*s*ure |
| x | /ʃ/ | *sh*oe |
| g | /g/ | always hard, as in *g*et |

The glottal stop *'* (/ʔ/) appears in interjections only and is the sole exception to the CVC word-structure rule.

**Stress:** always on the first vowel of the lexical root. Prefixes, infixes, and suffixes are unstressed. In compounds, primary stress falls on the first root.

### Morphology

**Noun template:** ROOT + (ROLE infix) + CLASS suffix + (*-es* plural) + (*-os* ownership)

```
lov  +  -ir-  +  -un              →  lovirun    "lover (sapient)"
lov  +  -ul-  +  -un              →  lovulun    "beloved (sapient)"
peras + -un   + -es               →  perasunes  "people (bare plural)"
```

**Adjectives:** ROOT + *-al* (post-nominal). Comparatives *pi-*ROOT*-al*; superlatives *su-*ROOT*-al*.
**Adverbs:** ROOT + *-il*. Same comparative/superlative prefixes.
**Proper nouns:** phonotactically adapted root + *-anom*. Examples: *Jonanom* (John), *Mariranom* (Mary), *Parisanom* (Paris).

**Verb valency is mandatory and suffix-marked:**

| Suffix | Valency | Arguments | Example |
|---|---|---|---|
| *-an* | Intransitive | S | *ronan* "run" |
| *-in* | Transitive | S, O | *vizin* "see" |
| *-on* | Ditransitive | S, O, IO | *donon* "give" |

### Syntax

Three word orders, distinguished by verb position (always identifiable from the valency suffix):

| Order | Register | Verb position |
|---|---|---|
| SOV | Formal / written | Final |
| SVO | Everyday speech | Medial |
| VSO | Commands | Initial |

```
SOV:  Perasunes sapal ninun bukekes pas donon.
SVO:  Perasunes sapal pas donon bukekes par ninun.
VSO:  Donon tal bukekes par tal ninun!
      "Wise people gave books to the child."
```

Optional post-nominal case markers *sav* (subject) and *dob* (direct object) resolve ambiguity in complex SOV sentences.

**Particle stacking (preverbal):**

```
MODAL → TENSE → TEMPORAL DISTANCE → ASPECT → VERB

deb   fus   zip   dur   vokin
must  FUT   soon  PRG   speak-TR
"will soon have to be speaking"
```

### Relative Clauses

Introduced by *taz-* + antecedent's class suffix. A resumptive pronoun fills the antecedent's role inside the clause. Clause is closed by *lev*.

```
tal kanem   tazem   mun vizin rem   lev
DEF dog-ANIM REL-ANIM I  see-TR it-ANIM  CE
"the dog that I saw"

tal kanem   tazem   rem vizin mun   lev
DEF dog-ANIM REL-ANIM it-ANIM see-TR I   CE
"the dog that saw me"
```

Informal register permits omission of the resumptive for intransitive verbs only, where no ambiguity arises.

### Complement Clauses

Introduced by *gav*, closed by *lev*:

```
Mariranom sapin   gav  Jonanom pas movan  lev.
Mary-PROP know-TR COMP John-PROP PST move-INTR CE
"Mary knows that John moved."
```

### Topic Construction

The particle *tev* fronts a noun phrase for discourse focus. A resumptive pronoun fills its role in the main clause. This is the primary replacement for the discourse-focusing function of passive voice.

```
tal bukek tev,   Jonanom  pas  makin   rek.
DEF book-ART TOP  John-PROP PST make-TR it-ART
"As for the book, John made it."
```

### Questions

**Yes/no:** sentence-final *kev*.
```
tun vizin tal kanem kev?    "Do you see the dog?"
```

**Content:** interrogative word in the questioned element's normal position. All interrogatives begin with *k-*:
*kim* (who), *kel* (what), *kaz* (when), *kos* (where), *kiv* (why), *kom* (how).

```
kim pas vizin tal kanem?    "Who saw the dog?"
```

### Pronouns

**First:** *mun* (I), *munes* (we, exclusive), *munatun* (we, inclusive — always includes addressee)
**Second:** *tun* (sg), *tunes* (pl) — class-neutral; class of addressee is visible from their noun elsewhere
**Third, sapient:** *xun* (sg), *xunes* (pl) — gender-neutral
**Third, non-sapient:** class-matched, all begin *r-*:

| Class | Singular | Plural |
|---|---|---|
| Animate | *rem* | *remes* |
| Living | *riv* | *rives* |
| Natural | *rar* | *rares* |
| Artificial | *rek* | *rekes* |
| Abstract | *rab* | *rabes* |
| Group | *rup* | *rupes* |

**Indeterminate (unknown identity):** *zan* (class unknown) and the *h-* series for known class: *hun* (sapient), *hem* (animate), *hiv* (living), *har* (natural force), *hek* (artifact/system), *hab* (abstract), *hup* (group).

### Evidentials (optional, sentence-initial)

| Particle | Meaning |
|---|---|
| *tid* | speaker witnessed directly |
| *tob* | heard or reported |
| *ged* | inferred |
| *set* | generally accepted |

### Numbers

Multiplicative-additive, largest first. Roots drawn from multiple language families:

*jat* 1 · *tus* 2 · *san* 3 · *kar* 4 · *kin* 5 · *luk* 6 · *sem* 7 · *nok* 8 · *nov* 9 · *dek* 10 · *cen* 100 · *mil* 1000

*san cen tus dek jat* = 321

---

## Semantic Coercion

A noun's class suffix is a commitment, not a permanent label. When the same entity is viewed through a different ontological lens, the class suffix changes to make that framing explicit:

```
tal sitek  pas  deran.       "The city [as built structure] was destroyed."
tal situp  pas  vokin.       "The city [as community] spoke."
tal sitar  magal.            "The city [as place] is large."
```

This is not an error — it is a deliberate communicative choice. The coercion is visible in the surface form, making the speaker's framing contestable.

The strongest coercion is to *-un* (sapient). Attributing sapience to an artifact or a natural force is a substantive claim. In formal register, it commits the speaker to the attribution.

---

## Philosophical Grounding

The design draws on several converging traditions:

**Frege** (*Grundlagen*, 1884): identity, predication, existence, and class membership are logically distinct. Collapsing them into a single copula produces pseudo-problems. Simavokab keeps them separate.

**Leibniz** (*Characteristica Universalis*): logical structure should be visible in surface form. The eleven-way possessive analysis is the direct application of this principle.

**Praxeology** (Mises, Austrian economics): social explanation begins with purposeful individual agents. This motivates agency-primacy in the grammar — the *-un* class is ontologically privileged, groups (*-up*) do not inherit sapient properties, and the passive suppression of agency is structurally unavailable.

**Aristotle** (Categories, Physics): the ontological tree and the causal role distinctions in the preposition system both draw on the Aristotelian tradition of motivated categorisation.

A secondary strand, not philosophical but pragmatic: the grammar is designed to be **formally parseable**. Tokenisation is O(n) with no lexicon. Part-of-speech is suffix-readable. Clause nesting is explicitly bracketed. Valency is obligatorily declared. The language could in principle be compiled to formal logic — and it is designed so that compiling it would not require heroic effort.

See `DESIGN.md` for the full treatment.

---

## Repository

```
simavokab/
├── README.md               ← you are here
├── GRAMMAR.md              ← complete reference grammar (v0.5)
├── DESIGN.md               ← philosophical and computational foundations
├── ONTOLOGY.md             ← noun class system, edge cases, coercion rules
├── GLOSSARY.md             ← grammatical terms and interlinear abbreviations
├── LEXICON.md              ← vocabulary (in progress)
├── EXAMPLES.md             ← annotated example texts (forthcoming)
├── DESIGN_DECISIONS.md     ← versioned log of major decisions and alternatives (forthcoming)
├── FORMAL_GRAMMAR.md       ← EBNF/PEG specification for parser implementers (forthcoming)
└── tools/
    └── validate.py         ← phonotactic checker (forthcoming)
```

---

## Key Open Items (v0.6 agenda)

- **Complement clause syntax** (*gav* particle introduced; full treatment of embedded tense and evidentiality in subordinate clauses pending)
- **Narrative tense / sequence of tense** — rules for how tense is anchored in extended discourse and reported speech
- **Comparative clauses** — *tam* ("than") currently covers simple NP comparisons; clausal comparisons (*faster than she swims*) need a full construction
- **Resultative aspect** — dedicated marker for the resultant-state reading, distinct from perfective *pef*
- **Anticausative licensing** — explicit list of which transitive verbs license an intransitive *-an* alternate (not all do; creation verbs, knowledge verbs, and communication verbs do not)
- **Phonotactic validator** — CI script to catch CC violations in grammar examples and lexicon before release

---

## Quick Reference Card

```
PHONEMES      b c d f g h j k l m n p r s t v x z  +  a e i o u
              c=/tʃ/  j=/ʒ/  x=/ʃ/  (one symbol, one sound throughout)

WORD SHAPE    CVC(VC)*  — starts C, ends C, no CC within word
BOUNDARY      any CC sequence = word break (no lexicon needed)
STRESS        first vowel of lexical root

NOUN          ROOT + (role infix) + CLASS + (-es plural) + (-os ownership)
CLASSES       -un sapient  -em animate  -iv living  -ar natural
              -ek artifact  -ab abstract  -up group  -ag gerund
ROLES         -ir- agent infix   -ul- patient infix

VERB          ROOT + -an (intr) / -in (trans) / -on (ditrans)
PARTICLES     MODAL → TENSE → DISTANCE → ASPECT → VERB
TENSE         pas (past)  nun (present)  fus (future)
ASPECT        dur (PRG)  pef (PFV)  zab (HAB)  biv (INCEP)
MODALS        pos (can)  deb (must)  vol (want)  sel (should)  nul (not)

WORD ORDER    SOV (formal)  SVO (everyday)  VSO (commands)
QUESTIONS     sentence-final kev (yes/no); k- words in situ (content)
RELATIVE      [NP] taz-CLASS [clause + resumptive] lev
COMPLEMENT    [V] gav [clause] lev
TOPIC         [NP] tev, [clause with resumptive]
CONDITIONAL   sif [condition] dan [consequent]

PRONOUNS      mun (I)  tun (you)  xun (he/she/they-SAP)
              rem rek riv rab rar rup  (3rd non-sapient, by class)
INDET         zan (class unknown)  hun hem hiv har hek hab hup (class known)
EVIDENTIALS   tid (witnessed)  tob (reported)  ged (inferred)  set (accepted)

DETERMINER    tal (the)  hal (a)  nal (this)  zal (that)
NEGATION      nul (verbal)  nik (sentential)
CONJUNCTIONS  kas (and)  zor (or)  bet (but)  sib (because)
CLAUSE END    lev
```
