# Simavokab Grammar Reference (v0.5)

> **Status:** Working draft. Vocabulary in `LEXICON.md`. Design rationale in
> `DESIGN.md`. This file covers phonology, morphology, syntax, and the
> closed-class particle inventory.
>
> **Changes from v0.4:**
> - *zan* (indeterminate) expanded to a full class-specific paradigm; *h-* series
>   added for class-specified unknowns; *zan* retained for fully unknown-class causer
> - Intransitive verb alternation (*-in* / *-an* pairs) made an explicit principle
> - Topic construction added: particle *tev*
> - Optional post-nominal case markers *sav* (subject) and *dob* (direct object)
>   added for SOV disambiguation
> - *bel* (from/source) disentangled from temporal "before"; new temporal
>   prepositions *bef* (before) and *naf* (after)
> - Resumptive pronouns required in all formal relative clauses (including
>   intransitive); informal gap allowed for intransitives only
> - Predicate adjective rule strengthened

---

## 0. The Name

**Simavokab** — *sim* (precise/clear) + *-a-* (linker) + *vok* (voice/language)
+ *-ab* (abstract suffix) = "language of precision."

CVC check: S-i-m-a-v-o-k-a-b = C-V-C-V-C-V-C-V-C ✓

---

## 1. Phonology

### 1.1 Consonants (17 + optional glottal stop)

| Symbol | IPA   | Notes                                          |
|--------|-------|------------------------------------------------|
| b      | /b/   |                                                |
| c      | /tʃ/  | as in *ch*urch                                 |
| d      | /d/   |                                                |
| f      | /f/   |                                                |
| g      | /g/   | always hard, as in *g*et                       |
| h      | /h/   |                                                |
| j      | /ʒ/   | as in mea*s*ure                                |
| k      | /k/   |                                                |
| l      | /l/   |                                                |
| m      | /m/   |                                                |
| n      | /n/   |                                                |
| p      | /p/   |                                                |
| r      | /r/   | any non-lateral rhotic; tapping/trilling optional |
| s      | /s/   |                                                |
| t      | /t/   |                                                |
| v      | /v/   |                                                |
| x      | /ʃ/   | as in *sh*oe                                   |
| z      | /z/   |                                                |
| '      | /ʔ/   | glottal stop; **interjections only** (§1.5)    |

*r* may be realised as tap [ɾ], trill [r], or approximant [ɹ] — no meaning
distinction between realisations.

### 1.2 Vowels (5)

**a e i o u** — as in Italian; full, consistent, never reduced. No diphthongs.

### 1.3 Word Structure

Every content or function word follows **CVC(VC)***: begins with a consonant,
alternates consonant and vowel, ends with a consonant.

**The word-boundary rule (absolute):** Any CC sequence with no intervening vowel
is a word boundary. Within a single word, every pair of consonants is separated
by a vowel. No exceptions for content and function words.

```
perasun magal   →  peras·un | mag·al   (n·m = word break)
domaperasup     →  one word; no internal CC
```

**Prefixes** (*pi-*, *su-*) are CV- forms; they attach without creating CC.
**Linker in compounds:** *-a-* (full /a/) joins roots: *dom-a-peras-up*.

### 1.4 Stress

**Stress falls on the first vowel of the lexical root.** Prefixes, infixes, and
suffixes are all unstressed.

| Form       | Root  | Pronunciation  |
|------------|-------|----------------|
| *bukek*    | buk   | **BU**kek      |
| *sapal*    | sap   | **SA**pal      |
| *perasun*  | peras | **PE**rasun    |
| *pimagal*  | mag   | pi**MA**gal    |
| *bevirun*  | bev   | **BE**virun    |

Compounds: primary stress on first root, secondary on subsequent roots:
*domaperasup* → **DO**ma·pe·ra·sup.
Monosyllabic particles stress their only syllable automatically.

### 1.5 Interjections

Closed class, exempt from the CVC rule:

| Form  | IPA   | Meaning                            |
|-------|-------|------------------------------------|
| *'o*  | /ʔo/  | oh! (surprise, realization)        |
| *'e*  | /ʔe/  | hey! (getting attention)           |
| *'i*  | /ʔi/  | yes!/yay! (affirmation, joy)       |
| *'a*  | /ʔa/  | ah! (understanding, satisfaction)  |
| *hah* | /hah/ | hah! (laughter) — CVC ✓           |
| *bas* | /bas/ | stop!/enough! — CVC ✓             |
| *vas* | /vas/ | well done!/bravo! — CVC ✓         |
| *zas* | /zas/ | ugh!/alas! — CVC ✓                |

---

## 2. Phonotactic Compliance Checklist

1. Starts with a consonant ✓
2. Ends with a consonant ✓
3. No CC sequence within the word ✓
4. All phonemes in the inventory ✓

**Cumulative corrections (all versions):**

| Bad form    | Problem                    | Replacement |
|-------------|----------------------------|-------------|
| *pardin*    | **rd** = CC inside word    | *patin*     |
| *simbin*    | **mb** = CC inside word    | *simin*     |
| *kontin*    | **nt** = CC inside word    | *kotin*     |
| *simtan*    | **mt** = CC inside word    | *sinan*     |
| *trubin*    | **tr** = CC at word start  | *tubin*     |
| *detrin*    | **tr** = CC inside word    | *derin*     |
| *intenin*   | starts with vowel + **nt** | *temin*     |
| *uzon*      | starts with vowel          | *vazon*     |
| *mutun*     | irregular deletion of *n*  | *munatun*   |

---

## 3. Noun Classes and Ontology

Every noun carries a mandatory **class suffix**:

```
entity
├── concrete
│   ├── living
│   │   ├── animate / sentient              → -em
│   │   │   └── sapient                    → -un
│   │   └── (living, non-animate)           → -iv
│   ├── natural (non-living, non-made)      → -ar
│   └── artificial / constructed            → -ek
├── abstract                                → -ab
├── group / collection                      → -up
└── process / gerund                        → -ag
```

| Class      | Suffix | Example               |
|------------|--------|-----------------------|
| Sapient    | *-un*  | *perasun* "person"    |
| Animate    | *-em*  | *kanem* "dog"         |
| Living     | *-iv*  | *dariv* "tree"        |
| Natural    | *-ar*  | *rokar* "rock"        |
| Artificial | *-ek*  | *bukek* "book"        |
| Abstract   | *-ab*  | *lovab* "love"        |
| Group      | *-up*  | *timup* "team"        |
| Gerund     | *-ag*  | *ronag* "running"     |

Root for "group in general": *gor* → *gorup*.

Hard cases: see DESIGN.md for the full ontological discussion including polysemous
nouns (e.g., "law" as artifact *lawek* vs. "law" as abstract proposition *lawab*).

---

## 4. Noun Morphology

### 4.1 Role Morphology

| Role    | Infix  | Meaning                              |
|---------|--------|--------------------------------------|
| Agent   | *-ir-* | the one who performs the action      |
| Patient | *-ul-* | the one/thing undergoing the action  |

```
bev  →  bevirun "drinker (sapient)" / bevulek "beverage (artifact)"
lov  →  lovirun "lover (sapient)"   / lovulun "beloved (sapient)"
```

### 4.2 The Full Noun Template

```
ROOT  +  (ROLE)  +  CLASS  +  (PLURAL)  +  (OWNERSHIP)
```

**Plural (*-es*):** used for bare plurals without a quantifier. Any quantifier
(*jat, sol, mul, dol, nol*, numbers) suppresses *-es*:
```
perasunes   "people" (bare plural)
sol perasun "some people" (quantifier present → no -es)
```

**Ownership (*-os*):** marks alienable ownership only. All other associative
relations use prepositions (§4.5).

### 4.3 Adjectives, Adverbs, and Degree

| Category     | Form                  | Example                  |
|--------------|-----------------------|--------------------------|
| Adjective    | ROOT + *-al*          | *magal* "big"            |
| Adverb       | ROOT + *-il*          | *magil* "greatly"        |
| Comp. adj    | *pi-* + ROOT + *-al*  | *pimagal* "bigger"       |
| Sup. adj     | *su-* + ROOT + *-al*  | *sumagal* "biggest"      |

Standard of comparison: *tam* ("than"):
```
tal pasem pimagal tam tal kanem   "the bird bigger than the dog"
```

**Degree modifiers** (precede the adjective or adverb they modify):
*vel* (very), *pok* (somewhat), *tes* (barely), *nep* (almost), *top* (too much).

### 4.4 Adjective Ordering

Three-level post-nominal hierarchy (most inherent nearest the noun):

```
NOUN  →  CLASSIFICATORY  →  DESCRIPTIVE  →  EVALUATIVE
```

| Level          | Encodes                                  |
|----------------|------------------------------------------|
| Classificatory | type, purpose, material, origin          |
| Descriptive    | observable properties: size, shape, color|
| Evaluative     | subjective judgment                      |

Within a level, order is free. Example:
```
tal kursekel tobonal situal magal bonal
"the beautiful big wooden rocking chair"
```

### 4.5 Adverb Ordering

```
FREQUENCY  →  TIME/PLACE adjuncts  →  MANNER  →  [particle cluster]  →  VERB
```

Time and place adjuncts may appear sentence-initially for emphasis.

### 4.6 Associative Relations (Replacing the Unitary Possessive)

English's single possessive encodes many distinct relations. Simavokab uses
explicit constructions for each:

| Relation                      | Construction             | Example                                |
|-------------------------------|--------------------------|----------------------------------------|
| **Alienable ownership**       | OWNER*-os* + THING       | *perasunos karak* "person's car"       |
| **Part-whole / attribute**    | THING *pes* WHOLE        | *menak pes karak* "engine of the car"  |
| **Inalienable (body part)**   | PART *pes* PERSON        | *memar pes mun* "my arm"               |
| **Kinship / social relation** | ROLE *rel* PERSON        | *buvun rel mun* "my father"            |
| **Origin / authorship**       | THING *bel* SOURCE       | *vokab bel Bobanom* "Bob's words"      |
| **Beneficiary**               | THING *por* RECIPIENT    | *bukek por ninun* "book for the child" |
| **Agent of event**            | GERUND *pab* AGENT       | *movanag pab Jonanom* "John's arrival" |
| **Patient of event**          | GERUND *pes* PATIENT     | *derinag pes sitak* "city's destruction"|
| **Temporal association**      | THING *den* TIME         | *novab den nalab* "today's news"       |
| **Location / origin**         | THING *bel* PLACE        | *bovab bel Ital* "food from Italy"     |
| **Experiencer**               | STATE *pes* EXPERIENCER  | *fimab pes mun* "my fear"              |

Note: *bel* covers both geographic source and origin/authorship. A dedicated
authorship particle may be introduced in a later version if overloading becomes
a problem.

---

## 5. Verb Morphology

### 5.1 Valency Suffixes

| Valency      | Suffix | Arguments | Example                               |
|--------------|--------|-----------|---------------------------------------|
| Intransitive | *-an*  | S         | *vivan* "live", *ronan* "run"         |
| Transitive   | *-in*  | S, O      | *vizin* "see", *sapin* "know"         |
| Ditransitive | *-on*  | S, O, IO  | *donon* "give (something to someone)" |

### 5.2 Transitive / Intransitive Alternation

Most action verbs have **both a transitive (*-in*) and an intransitive (*-an*)
form.** The intransitive describes the event as it affects the patient, without
asserting or implying any agent:

| Transitive (*-in*)       | Intransitive (*-an*)              |
|--------------------------|-----------------------------------|
| *derin* "destroy sth"    | *deran* "become destroyed"        |
| *brokin* "break sth"     | *brokan* "break / become broken"  |
| *klosin* "close sth"     | *klosan* "become closed"          |
| *movin* "move sth"       | *movan* "move oneself" ← existing |

This is the primary tool for expressing an event **without specifying an agent.**
It replaces the core use case of the passive in many contexts:

```
tal vasek pas brokan den tal zaran.
the vase-ART PST broke-INTR in the earthquake-NAT.
"The vase broke in the earthquake."  (no agent implied)

tal sitak pas deran pab tal surab.
the city-NAT PST was-destroyed-INTR by the storm-NAT.
"The city was destroyed by the storm."  (natural instrument, no sapient agent)
```

*pab* (by/via) marks the instrument or natural cause.

### 5.3 Copula and Classificatory Verbs

No general "to be":

| Verb     | Val.  | Meaning                    |
|----------|-------|----------------------------|
| *bidin*  | trans | be identical to            |
| *tipin*  | trans | be a type / instance of    |
| *pirin*  | trans | have property / quality    |
| *zivan*  | intr  | exist                      |
| *patin*  | trans | be part of                 |
| *mibin*  | trans | be a member of             |

### 5.4 Adjective Predication

**Formal (logical precision):** *pirin* + quality noun (ROOT + *-ab*):
```
tal dariv pirin magalab.    "The tree has the property of bigness."
```

**Informal (zero copula):** An adjective that **ends the clause** (no verb
follows in that clause) is a predicative construction:
```
tal dariv magal.            "The tree is big."     (predicative — clause-final)
tal dariv magal ronan.      "The big tree runs."   (attributive — verb follows)
```

The morphological suffix of the verb (*-an/-in/-on*) makes the verb always
identifiable; if a verb is present in the clause, any adjective preceding it
is attributive. If no verb is present, the final adjective is predicative.

For coordination of two predicates, use *kas*:
```
tal dariv magal kas ronan.  "The tree is big and runs."
```

### 5.5 "Not Permitted": Passive Voice

Passive morphology is not used. Three explicit constructions replace its functions:

| Passive function              | Simavokab replacement                       |
|-------------------------------|---------------------------------------------|
| Agency suppression            | Indeterminate pronouns (§7.3)               |
| Unknown / natural causation   | Intransitive alternation (§5.2)             |
| Patient focus / topic fronting| Topic construction with *tev* (§10.6)       |
| Result state                  | Zero-copula adjective predication (§5.4)    |

---

## 6. Particles and Function Words (Closed Class)

All particles are CVC. They form a closed class. Every particle in any example
is defined here.

### 6.1 Quantifiers

| Word  | Meaning                          |
|-------|----------------------------------|
| *nol* | no / none                        |
| *sol* | some (indefinite small quantity) |
| *mul* | many (indefinite large quantity) |
| *dol* | all / every                      |

Any quantifier (including number words, §11) suppresses *-es* on the noun.

### 6.2 Tense

| Particle | Meaning                          |
|----------|----------------------------------|
| *pas*    | past                             |
| *nun*    | present (default; often omitted) |
| *fus*    | future                           |

### 6.3 Temporal Distance (optional; follows tense particle)

| Particle | Meaning                          |
|----------|----------------------------------|
| *zip*    | near / just / soon               |
| *zap*    | moderate temporal distance       |
| *zup*    | remote / long ago / far          |

### 6.4 Aspect

| Particle | Meaning                    | Note                         |
|----------|----------------------------|------------------------------|
| *dur*    | progressive / ongoing      | from Latin *durare*          |
| *pef*    | perfective / completed     | from Latin *perfectum*       |
| *zab*    | habitual / general truth   |                              |
| *biv*    | inceptive / just beginning | from English *begin*         |

### 6.5 Modal

| Particle | Meaning                         |
|----------|---------------------------------|
| *pos*    | can / possible (epistemic)      |
| *deb*    | must / obligated (deontic)      |
| *vol*    | want / desire                   |
| *sel*    | should / advisable              |
| *nul*    | not (verbal negation)           |

### 6.6 Particle Stacking Order (Canonical)

```
MODAL  →  TENSE  →  DISTANCE  →  ASPECT  →  VERB
```

| Example                | Reading                        |
|------------------------|--------------------------------|
| *pas dur ronan*        | was running                    |
| *deb fus vokin*        | will have to say               |
| *nul pas zab vokin*    | did not habitually say         |
| *fus biv ronan*        | will begin running             |

### 6.7 Logical and Discourse Particles

| Particle | Meaning                                    |
|----------|--------------------------------------------|
| *sif*    | if (opens conditional clause)              |
| *dan*    | then / therefore (opens consequent)        |
| *nik*    | not (sentential negation)                  |
| *lev*    | end-of-embedded-clause marker              |
| *tev*    | topic marker (§10.6)                       |

Note: "for" (= because) was removed in v0.4 as redundant with *sib* and *dan*.

*nul* negates the verb phrase; *nik* negates the whole proposition.

### 6.8 Conjunctions

*kas* (and), *zor* (or), *bet* (but), *sib* (because).

### 6.9 Determiners

*tal* (the), *hal* (a/an), *nal* (this), *zal* (that), *kel* (which/what).

### 6.10 Prepositions

| Particle | Meaning                                        |
|----------|------------------------------------------------|
| *pes*    | of (part-whole, attribute, constitutive)       |
| *rel*    | in-relation-to (kinship / social)              |
| *par*    | to / toward; indirect object marker            |
| *den*    | in / at / within (location)                    |
| *bel*    | from / out of (source, origin) — **spatial and causal origin only** |
| *bef*    | before (temporal) — NEW                        |
| *naf*    | after (temporal) — NEW                         |
| *zem*    | with / accompanied by (comitative)             |
| *nob*    | without                                        |
| *por*    | for (beneficiary / intended-for)               |
| *pab*    | by / via (agent or instrument)                 |
| *tam*    | than (comparison standard)                     |
| *sub*    | under / below                                  |
| *sup*    | over / above                                   |
| *sob*    | about / concerning (propositional content)     |

**Note on *bef* and *naf*:** Previous versions incorrectly used *bel* (source)
and *par* (to/IO) as temporal prepositions. *bef* and *naf* are the correct
temporal prepositions:
```
mun pas vokin bef tal ronag.    "I spoke before the running."
xun fus movan naf tal donag.    "She will move after the giving."
```

### 6.11 Case Markers (Post-Nominal, Optional)

Case markers **follow** the noun phrase they mark, making them post-nominal.
They are optional in simple sentences where S-O-V order is unambiguous, but
recommended (and required in formal register) for complex SOV sentences.

| Marker | Meaning                   | Etymology                |
|--------|---------------------------|--------------------------|
| *sav*  | subject marker            | from *sub-agens* (Latin) |
| *dob*  | direct object marker      | from *dativus objectum*  |

The indirect object is already marked by *par* (preposition, pre-nominal).

Usage:
```
Simple SOV (order alone suffices):
perasun kanem vizin.
"The person sees the dog."

Complex SOV (case markers recommended):
tal perasun sapal tazun xun vel sapin lev  sav  tal kanem magal  dob  vizin.
the wise person who knows a lot            SUBJ the big dog      OBJ  sees.
"The wise person who knows a lot sees the big dog."
```

Case markers may also be used in SVO and VSO for emphatic role marking, but are
rarely needed in those registers since the verb's position already disambiguates.

### 6.12 Interrogative Words

All begin with *k-* (Esperanto *ki-* pattern):
*kev* (yes/no), *kel* (what/which), *kim* (who), *kaz* (when), *kos* (where),
*kiv* (why), *kom* (how).

### 6.13 Evidential Particles (Optional, Sentence-Initial)

*tid* (witnessed), *tob* (heard/told), *ged* (inferred), *set* (generally accepted).

### 6.14 Degree Particles

*vel* (very), *pok* (somewhat), *tes* (barely), *nep* (almost), *top* (too much).

### 6.15 Quotation Markers

*bok* (open quotation), *kob* (close quotation). Note: *kob* ≠ *kos* (where).

---

## 7. Pronouns

### 7.1 Personal Pronouns

**First person:**

| Form       | Gloss                                                                    |
|------------|--------------------------------------------------------------------------|
| *mun*      | I (1st singular, sapient)                                                |
| *munes*    | we — **exclusive** (does NOT include the addressee)                      |
| *munatun*  | we — **inclusive** (ALWAYS includes the addressee)                       |

*munatun* = *mun* + *-a-* + *tun*: m-u-n-a-t-u-n = CVCVCVC ✓ (standard
compound rule; no consonant is deleted).

**Second person:** *tun* (sg), *tunes* (pl). Used for any addressee regardless
of class — the entity's class is visible from its noun suffix elsewhere.

**Third person — sapient:** *xun* (sg), *xunes* (pl). Gender-neutral.

**Third person — non-sapient (all begin *r-*):**

| Form    | Class      | Form    | Class      |
|---------|------------|---------|------------|
| *rem*   | Animate    | *rek*   | Artificial |
| *remes* | Animate pl | *rekes* | Artif. pl  |
| *riv*   | Living     | *rab*   | Abstract   |
| *rives* | Living pl  | *rabes* | Abstr. pl  |
| *rar*   | Natural    | *rup*   | Group      |
| *rares* | Natural pl | *rupes* | Group pl   |

### 7.2 Reflexive and Reciprocal

*zib* (self/reflexive), *nav* (each other/reciprocal).

### 7.3 Indeterminate Pronouns

Used when the **identity** of the agent or causer is unknown. Two series:

**General indeterminate — *zan* (fully unknown class):**
Used when neither the identity nor the class of the agent/causer is known:
```
zan pas derin tal bukek.    "Something/someone destroyed the book." (class unknown)
```

**Class-specific indeterminates — *h-* series:**
Used when the class of the unknown agent/causer is known. These follow the same
class-suffix pattern as the 3rd-person pronouns:

| Form   | Class      | Meaning / typical use                  |
|--------|------------|----------------------------------------|
| *hun*  | Sapient    | "someone" (unknown sapient)            |
| *hem*  | Animate    | "some animal" (unknown animate)        |
| *hiv*  | Living     | "some organism" (unknown living thing) |
| *har*  | Natural    | "some natural force" (storm, quake, …) |
| *hek*  | Artificial | "some system/artifact" (unknown machine/program) |
| *hab*  | Abstract   | "some principle/rule" (abstract cause) |
| *hup*  | Group      | "some group" (unknown collective)      |

```
hun pas makin tal berabes.       "Some person made mistakes."
har pas derin tal sitak.         "Some natural force destroyed the city."
hek pas nokin tal ronag.         "Some artifact/system prevented the running."
```

**Choosing between *zan* and *h-* forms:**

| Situation                                   | Form                |
|---------------------------------------------|---------------------|
| Agent exists but class is truly unknown     | *zan*               |
| Agent class known, identity unknown         | appropriate *h-* form |
| Event occurred with no agent implied        | intransitive *-an* (§5.2) |
| Focus on resulting state (not on event)     | zero-copula adj (§5.4) |

### 7.4 Mixed Noun-Class Coordination

- **Speaker among the referents:** *munes* for subsequent pronoun reference.
- **Speaker not involved:** use pronoun of the highest shared supertype.
- **Ambiguous:** repeat the noun or use *nal/zal*.

---

## 8. Relative Clauses

### 8.1 The Relative Marker

*taz-* + class suffix of the antecedent:

| Class      | Marker   | Class      | Marker   |
|------------|----------|------------|----------|
| Sapient    | *tazun*  | Artificial | *tazek*  |
| Animate    | *tazem*  | Abstract   | *tazab*  |
| Living     | *taziv*  | Group      | *tazup*  |
| Natural    | *tazar*  | Gerund     | *tazag*  |

### 8.2 Resumptive Pronoun Strategy

Simavokab uses **resumptive pronouns** to make the antecedent's role inside
the relative clause explicit. The 3rd-person pronoun matching the antecedent's
class occupies the exact syntactic position the antecedent fills.

Word order inside the clause is **SVO** (default for clarity and consistency).

**Requirement:**
- **Formal / written register:** resumptive pronoun **always required**, including
  for intransitive verbs.
- **Informal / spoken:** resumptive may be omitted for intransitive verbs only
  (where the antecedent can only be subject — no ambiguity).

**Template:**
```
[ANTECEDENT NP]  [taz-CLASS]  [CLAUSE, SVO, with resumptive pronoun]  lev
```

**Transitive — object relativization ("the dog that I saw"):**
```
tal kanem  tazem  mun vizin rem  lev
the dog-ANIM  REL-ANIM  I see-TRANS it-ANIM(RESUM)  CE
```

**Transitive — subject relativization ("the dog that saw me"):**
```
tal kanem  tazem  rem vizin mun  lev
the dog-ANIM  REL-ANIM  it-ANIM(RESUM) see-TRANS I  CE
```

**Intransitive ("the dog that runs"):**
```
tal kanem  tazem  rem ronan  lev     (formal — resumptive required)
tal kanem  tazem  ronan  lev         (informal — gap permitted)
```

**Ditransitive ("the child to whom I gave the book"):**
```
tal ninun  tazun  mun donon tal bukek par xun  lev
the child-SAP  REL-SAP  I give-DITR the book-ART to he-SAP(RESUM)  CE
```

### 8.3 *lev* — Clause Boundary Marker

Required when the relative clause is embedded in a complex sentence.
May be omitted in short, unambiguous standalone relative clauses in speech.

### 8.4 Stacked Relative Clauses

```
tal kanem  tazem rem ronan lev  tazem rem vizin mun lev
"the dog that was running and that saw me"
```

---

## 9. Proper Nouns

Proper nouns receive *-anom* after phonological adaptation. Guidelines (not
rigid algorithm); personal preference in adaptation is permitted if phonotactics
are satisfied.

| Original | Adapted | Final form      |
|----------|---------|-----------------|
| Mary     | Marir   | *Mariranom*     |
| John     | Jon     | *Jonanom*       |
| Paris    | Paris   | *Parisanom*     |
| Frank    | Faran   | *Farananom*     |

---

## 10. Syntax

### 10.1 Word Order and Self-Disambiguation

Three word orders, distinguished by verb position (identifiable via valency suffix):

| Verb position | Order | Register        |
|---------------|-------|-----------------|
| Final         | SOV   | formal, written |
| Medial        | SVO   | everyday speech |
| Initial       | VSO   | commands        |

The parser locates the verb by its *-an/-in/-on* suffix, reads its position, and
assigns S/O roles accordingly. *kev* (yes/no marker) and post-nominal case
markers (*sav, dob*) are excluded from this position calculation.

### 10.2 Argument Order Conventions

**Transitive (SOV):** S precedes O precedes V. If both NPs are of the same class
or ambiguity arises, add case markers:
```
perasun kanem vizin.             (order alone: person = S, dog = O)
perasun sav kanem dob vizin.     (explicit: same meaning, unambiguous)
kanem sav perasun dob vizin.     (dog = S, person = O — reversed with markers)
```

**Ditransitive (SOV):** S IO O V (indirect object precedes direct object):
```
mun ninun bukek donon.           S IO O V
```

**Ditransitive (SVO):** S V O *par* IO:
```
mun donon bukek par ninun.       S V O par IO
```

### 10.3 Commands (VSO)

No tense particle. Subject is usually *tun* (you) and may be omitted when clear:
```
donon tun tal bukekes par tal ninun!    "Give the books to the child!"
donon tal bukekes par tal ninun!        (subject omitted — implicit *tun*)
```

### 10.4 Adjective and Adverb Placement

Post-nominal adjectives (§4.4). Adverbs precede the particle cluster (§4.5).
Degree modifiers precede their target.

### 10.5 Negation

```
mun nul vizin tun.         "I do not see you."       (verbal negation)
nik mun vizin tun.         "It is not the case that I see you."  (sentential)
```

### 10.6 Topic Construction

The particle *tev* marks a **topicalized noun phrase**, placed before the main
clause. The topic's role in the clause is filled by the appropriate 3rd-person
pronoun (resumptive strategy):

```
[TOPIC NP]  tev,  [MAIN CLAUSE with resumptive]
```

This foregrounds the patient or any other argument without passive morphology:

```
tal bukek tev, Jonanom pas makin rek.
the book-ART TOP, John-PROP past make-TRANS it-ART.
"As for the book, John made it."  (focus on the book)

Jonanom pas makin tal bukek.
"John made the book."  (focus on John's action)
```

The topic construction separates discourse-focus from syntactic role — it is
the primary replacement for the discourse-focusing function of passive voice.

### 10.7 Conditional Sentences

```
sif [condition]  dan  [consequent]

sif tun sapin tal rabin, dan mun vokin tun.
"If you know the truth, then I will speak to you."
```

### 10.8 Yes/No Questions

*kev* is always **sentence-final**, regardless of word order, excluded from
parsing calculation:

```
SVO:  tun vizin tal kanem kev?    "Do you see the dog?"
SOV:  tun tal kanem vizin kev?    (formal)
```

### 10.9 Content Questions

Questioned element replaced by interrogative in its normal position:

```
kim pas vizin tal kanem?      "Who saw the dog?"
tun vizin kel?                "What do you see?"
kaz tun ronan?                "When do you run?"
kos tal kanem zivan?          "Where does the dog live?"
kiv tun pas movan?            "Why did you move?"
kom tun pas makin nal masek?  "How did you make this machine?"
```

---

## 11. Numbers

| Value | Root  | Value | Root  | Source              |
|-------|-------|-------|-------|---------------------|
| 1     | *jat* | 7     | *sem* | Russian *семь*      |
| 2     | *tus* | 8     | *nok* |                     |
| 3     | *san* | 9     | *nov* | Latin *novem*       |
| 4     | *kar* | 10    | *dek* | Greek *deka*        |
| 5     | *kin* | 100   | *cen* | Latin *centum*      |
| 6     | *luk* | 1000  | *mil* | Latin *mille*       |

*luk* (6) from Cantonese 六 (Jyutping *luk6*). Composition: multiplicative-
additive, largest first: *san cen tus dek jat* = 321.

**Number nouns:** ROOT + *-ab* → *jatab* "the number one."
**Ordinals:** ROOT + *-al* → *jatal* "first", *tusal* "second."

---

## 12. Core Verb Inventory

All forms pass the CVC(VC)* check.

### Taxonomic / Classificatory
*tipin* (be a type of), *bidin* (be identical to), *pirin* (have property),
*zivan* (exist), *patin* (be part of), *mibin* (be a member of), *simin* (be similar to).

### Causal / Functional
*kazon* (cause), *gadin* (enable), *nokin* (prevent), *rekin* (require), *vazon* (use X for Y).

### Mereological / Spatial
*patin* (be part of), *kotin* (contain), *lokan* (be located).

### Temporal
*tibin* (occur before), *tapin* (occur after), *durin* (occur during), *sinan* (be simultaneous).

### Epistemic / Mental
*sapin* (know), *tubin* (believe), *vizin* (see/perceive), *vokan* (speak intrans.),
*vokin* (say trans.), *temin* (intend).

### Physical / Agentive (with intransitive alternates)

| Transitive (*-in*)    | Intransitive (*-an*)    | Meaning               |
|-----------------------|-------------------------|-----------------------|
| *derin*               | *deran*                 | destroy / be destroyed|
| *movin*               | *movan*                 | move sth / move self  |
| *makin*               | *makan*                 | make / come to be made|
| *lokin*               | —                       | find / seek           |
| —                     | *ronan*                 | run (intr. only)      |
| —                     | *vivan*                 | live (intr. only)     |
| *lubin*               | —                       | like / love           |
| *donon* (ditr.)       | —                       | give                  |

---

## 13. Morphological Slot Summary

| Category       | Template                                              |
|----------------|-------------------------------------------------------|
| Noun           | ROOT + (ROLE) + CLASS + (*-es*)? + (*-os*)?           |
| Verb           | ROOT + VALENCY (*-an / -in / -on*)                    |
| Adjective      | ROOT + *-al*; *pi-* … *-al*; *su-* … *-al*           |
| Adverb         | ROOT + *-il*; *pi-* … *-il*; *su-* … *-il*           |
| Particle chain | MODAL + TENSE + DISTANCE + ASPECT + VERB              |
| Compound noun  | ROOT + *-a-* + ROOT + … + CLASS                       |
| Number noun    | NUMBER-ROOT + *-ab*                                   |
| Ordinal adj    | NUMBER-ROOT + *-al*                                   |
| Proper noun    | ADAPTED-ROOT + *-anom*                                |

---

## 14. Generating Valid Word Forms

CVC: 1,445 forms. CVCVC: 123,505 forms. Check all new roots against:
(1) the particle inventory (§6), (2) the pronoun paradigm (§7), (3) the
existing verb/noun inventory. Etymology: extract consonant skeleton of source
word, choose vowels, verify no collision.

---

## 15. Glossed Examples

**Abbreviations:** SAP Sapient · ANIM Animate · LIV Living · NAT Natural ·
ART Artificial · ABST Abstract · GRP Group · GER Gerund ·
INTR Intransitive · TRANS Transitive · DITR Ditransitive ·
PL Plural · OWN Ownership suffix · AGT Agent-role · PAT Patient-role ·
PST Past · FUT Future · PRG Progressive · PFV Perfective · HAB Habitual · INCEP Inceptive ·
CMP Comparative · SUP Superlative · RESUM Resumptive pronoun · CE Clause-End ·
DEF Definite · INDEF Indefinite · TOP Topic · SUBJ Subject marker · OBJ Object marker ·
INDET Indeterminate agent

---

### Example 1 — "Wise people gave books to the child."

**SOV:** `Perasunes sapal ninun bukekes pas donon.`

**SVO:** `Perasunes sapal pas donon bukekes par ninun.`

**VSO (command, no tense, subject omitted):** `Donon tal bukekes par tal ninun!`

---

### Example 2 — Relative clauses (subject vs. object)

```
"the dog that I saw":
tal kanem  tazem  mun vizin rem  lev

"the dog that saw me":
tal kanem  tazem  rem vizin mun  lev

"the dog that runs" (formal):
tal kanem  tazem  rem ronan  lev

"the dog that runs" (informal, intransitive gap allowed):
tal kanem  tazem  ronan  lev
```

---

### Example 3 — Passive replacement strategies

```
Agency suppression (unknown sapient):
hun pas makin tal berabes.
INDET-SAP PST make-TRANS DEF mistake-ABST-PL
"Some person made mistakes."

Natural cause, no sapient agent:
tal vasek pas brokan den tal kanan.
the vase-ART PST broke-INTR in the earthquake-NAT
"The vase broke in the earthquake."

Instrument cause (natural):
tal sitak pas deran pab tal surab.
the city-NAT PST was-destroyed-INTR by the storm-NAT
"The city was destroyed by the storm."

Result state (no event implied):
tal vasek brokal.
the vase-ART broken-ADJ
"The vase is broken."

Topic fronting (replaces discourse passive):
tal bukek tev, Jonanom pas makin rek.
the book-ART TOP, John-PROP past make-TRANS it-ART
"As for the book, John made it."
```

---

### Example 4 — Case markers in complex SOV

```
Simple (order alone):
perasun kanem vizin.    "The person sees the dog."

With case markers (unambiguous regardless of NP order):
perasun sav kanem dob vizin.    same meaning, explicit

Complex SOV (markers required in formal register):
tal perasun sapal tazun xun vel sapin lev  sav
the wise person who knows a lot            SUBJ

tal kanem magal  dob  vizin.
the big dog      OBJ  sees.

"The wise person who knows a lot sees the big dog."
```

---

### Example 5 — Temporal prepositions (*bef / naf*)

```
mun pas vokin bef tal ronag.    "I spoke before the running."
xun fus movan naf tal donag.    "She will move after the giving."
```

---

### Example 6 — Full complex sentence

"If Mary knows that John made a machine, she must speak clearly to the team."

```
Sif Mariranom sapin tazab Jonanom pas makin hal masek lev,
if Mary-PROP know-TRANS REL-ABST John-PROP PST make-TRANS INDEF machine-ART CE

dan xun deb vokin simil par tal timup.
then she-SAP must speak-TRANS clearly-ADV to DEF team-GRP
```

---

### Example 7 — Indeterminate pronouns

```
zan pas derin tal bukek.        "Something/someone (class unknown) destroyed the book."
hun pas derin tal bukek.        "Some person destroyed the book."
har pas derin tal bukek.        "Some natural force destroyed the book."
hek pas derin tal bukek.        "Some system/artifact destroyed the book."
tal bukek pas deran.            "The book was destroyed." (no causer implied)
tal bukek derinal.              "The book is destroyed." (result state)
```

---

## 16. Open Questions

| # | Issue | Status |
|---|-------|--------|
| 1 | Passive voice | **Resolved:** not permitted; four explicit replacements (§5.5). |
| 2 | Reference-time tense | **Partially addressed** (*bef/naf* §6.10; *tibin/tapin* §12); narrative tense deferred. |
| 3 | Scalar degree | **Resolved:** *vel, pok, tes, nep, top* (§4.3, §6.14). |
| 4 | Mixed-class coordination | **Resolved** (§7.4). |
| 5 | Measure words | **Resolved:** optional measure nouns only. |
| 6 | Quotation markers | **Resolved:** *bok* / *kob* (§6.15). |
| 7 | Tense in narrative / reported speech | **Open.** |
| 8 | Full comparative clause syntax | **Open:** *tam* covers simple cases. |
| 9 | Formal sentence-final punctuation | **Open:** period in writing; no dedicated particle. |
| 10 | *bel* overloading (source vs. authorship) | **Flagged** (§4.6); deferred. |
| 11 | Result-state / stative aspect | **Partially addressed** via zero-copula adjective; dedicated resultative marker deferred. |
| 12 | Vocabulary for semantic domains | **In progress:** see LEXICON.md. |
