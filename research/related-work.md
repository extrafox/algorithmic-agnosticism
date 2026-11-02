# Related work: deep research pass (2026-10-30)

> **Note (added at v2.2).** This file records the literature research as of the v1 stage. The
> paper's position was later renamed **algorithmic agnosticism** and reframed around theories of
> everything. The paper is now *Algorithmic Agnosticism: Why No Theory of Everything Can Be Known
> to Be Final*. References below to "algorithmic conventionalism", and the suggested Contributions
> text in §5, are superseded. The current argument is in `argument-spine.md`, and the paper's own
> introduction gives the current positioning.

Seven parallel literature searches, one per strand: the Hofstadter/Deutsch/Wolfram lineage;
algorithmic induction and Occam; formal learning theory and underdetermination; the physical
Church–Turing thesis and hypercomputation; quantum randomness and computability; structuralism,
simulation and informational realism; and a direct novelty check. Each source was checked for
existence via arXiv, Crossref, Semantic Scholar or SEP unless marked *(unverified)*.

---

## 1. Verdict

**The ideas are old; the specific combination is new.** No single work makes the paper's whole
argument, but every step has a close precedent:

| Paper's step | Closest prior art | What's actually new here |
|---|---|---|
| P1: finite records | Wheeler "it from bit" (1990); Hutter 2010; Müller 2020; Lloyd 2002 (finite bound) | Nothing; folklore |
| **P2: usable ⇒ computable** | **Piccinini 2011/2015 "Modest physical CTT" + usability constraint** (near-verbatim, including "refuted only by a *usable* hypercomputer" and dismissing randomness/arbitrary reals as unusable); Deutsch 1985; Pitowsky 1990; Shagrir–Pitowsky 2003; Button 2009 | Applying it to **methods of induction and model selection**, not just to function computation |
| D: discrete sufficiency | Kreisel 1974 (theory-relative recursiveness); Davis 2004 ("non-computable in, non-computable out"); Gorard 2020; Bournez et al. 2007 | A clean general statement, plus the naming-vs-determining distinction |
| T1: infinitely many rivals | Leibniz *Discours* §VI → Weyl → **Chaitin 2005** ("there is always a law"); **Kukla 1993/1996/1998** (algorithms that generate a rival for any theory); McAllister 2003/2011 | Theorem-level statement for *arbitrary* records, whatever generated them |
| T2: Gold non-identifiability | Putnam 1963 (the same diagonal argument); Gold 1967; **Kelly 1996, 2004** ("uncomputability: the problem of induction internalized") | Bridging into the underdetermination literature, which (including SEP) largely ignores learning theory |
| T3: MDL is machine-relative | Folklore (Li–Vitányi; Hutter 2009 open problems); Müller 2010; Leike–Hutter 2015 (agents, not selection); **Sterkenburg 2016**; Neth 2022 | The explicit **≈K(e) price on finite data**, and the contrast between invariant prediction and machine-relative identity |
| T4: Solomonoff dominance | Solomonoff 1978; Rathmanner–Hutter 2011; Schmidhuber 2000/2002; **Sterkenburg 2016/2018/2019** (who argues the guarantee rests on assuming effectiveness, i.e. P2) | Framing it as a prediction-only guarantee alongside non-identifiability; Lattimore–Hutter 2013 already did the NFL reconciliation |
| "Predict, don't identify" conclusion | Mach (economy of thought), Pearson, **Poincaré** (conventionalism), van Fraassen, **McAllister 2011**, Martins 2017 ("Don't choose theories"), Wolfram 2023 (observer theory) | Reaching it with no metaphysical premise and with every step a theorem or explicit thesis |
| Quantum case study | Calude–Svozil, Landsman 2020, Svozil 2018, Yurtsever 2000, **Bendersky et al. 2016/2017** | Running all three lenses (power, certifiability, underdetermination) together |

**Defensible originality:** an assumption-light *assembly*. Every neighbour adds a commitment the
paper refuses:

- Deutsch: realism about explanations.
- Wolfram: a unique, necessary ruliad.
- Hutter 2010: assumes an objective, computable world.
- Schmidhuber: the prior as physics.
- Müller: idealism.
- McAllister and Ladyman–Ross: ontological pluralism or realism.
- Tegmark, Fredkin and Zuse: metaphysics.

Positioned as a synthesis and sharpening, the paper is publishable. Positioned as a discovery,
philosophy-of-science referees will reject it as rediscovering Sterkenburg, Kelly and Piccinini.

**Suggested self-label (superseded; the paper now uses *algorithmic agnosticism*):** *algorithmic conventionalism*. That is, a formalized Mach–Poincaré
conventionalism, McAllister without the pluralism, and the anti-realist counterpart of Dennett's
and Ladyman–Ross's "real patterns" (the same compression facts, without the step to existence).

---

## 2. The closest precedents (read these first)

1. **Hutter, M. (2010). "A Complete Theory of Everything (will be subjective)."** *Algorithms*
   3(4):329–350. doi:10.3390/a3040329. About 40% overlap: finite record, theory as program,
   shortest-total-length selection, continuous vs. discrete, quantum randomness. *Opposite
   premises*: "there exists an objective world… the world is computable"; dismisses machine
   dependence.
2. **Sterkenburg, T. F. (2016).** "Solomonoff Prediction and Occam's Razor." *Phil. Sci.*
   83(4):459–479. doi:10.1086/687257. Also his 2018 thesis *Universal Prediction* (Groningen) and
   2019 "Putnam's Diagonal Argument and the Impossibility of a Universal Learning Machine,"
   *Erkenntnis* 84:633–656. doi:10.1007/s10670-018-9975-x. The sharpest prior statement of T3/T4,
   and he turns it against the paper's "assumption-free" wording.
3. **Chaitin, G. J. (2005).** "Epistemology as Information Theory: From Leibniz to Ω."
   arXiv:math/0506552. Theory = program; understanding = compression; with arbitrary complexity
   there is always a law; minimality cannot be proved.
4. **Piccinini, G. (2011).** "The Physical Church–Turing Thesis: Modest or Bold?" *BJPS*
   62:733–769. Also *Physical Computation* (OUP 2015), chs. 15–16. This is P2.
5. **McAllister, J. W. (2003).** "Algorithmic Randomness in Empirical Data," *SHPS A* 34(3).
   doi:10.1016/s0039-3681(03)00047-5. Also (2011) "What Do Patterns in Empirical Data Tell Us
   about the Structure of the World?" *Synthese* 182:73–87. doi:10.1007/s11229-009-9613-x. Data
   admit infinitely many pattern-plus-noise decompositions that the data don't choose between.
   He concludes the world contains all of them. Reply: Twardy, Gardner & Dowe (2005), *SHPS A*
   36(2), doi:10.1016/j.shpsa.2005.04.004, argue that MML picks one in a principled way.
6. **Kelly, K. T. (1996).** *The Logic of Reliable Inquiry* (OUP). Also (2004) "Uncomputability:
   the problem of induction internalized," *TCS* 317:227–249. Underdetermination recast as
   learning-theoretic unsolvability; computability limits recast as induction.
7. **Müller, M. P. (2020).** "Law without law." *Quantum* 4:301. doi:10.22331/q-2020-07-20-301.
   Record-first, Solomonoff-centred, with an emergent external world. Leads to idealism.
8. **Wolfram, S.** "The Concept of the Ruliad" (2021) and "Observer Theory" (2023),
   writings.stephenwolfram.com. Laws depend on bounded observers and on the description language
   ("a different description language → different laws"). Then he asserts that the ruliad is
   unique and necessary.
9. **Kukla, A. (1996).** "Does every theory have empirically equivalent rivals?" *Erkenntnis*
   44:137–166. Also *Studies in Scientific Realism* (1998). His rival T″ ("the world obeys T when
   observed, T* otherwise") is the informal form of T1(a). Replies: Leplin & Laudan 1993
   (*Analysis* 53); Stanford 2001 ("Refusing the devil's bargain").
10. **Martins, A. C. R. (2017).** "Don't choose theories." arXiv:1701.00213. Uses Solomonoff
    induction on string theory vs. the Standard Model and argues against choosing a single theory.

---

## 3. Challenges the paper must answer (not yet addressed)

### A. Correction required: Bendersky et al. and §7's Bell paragraph
- **Bendersky, de la Torre, Senno, Figueira & Acín (2017).** "Non-signaling deterministic models
  for nonlocal correlations have to be uncomputable." *PRL* 118:130401. arXiv:1606.08403.
  Consider a deterministic, computable box model with hidden signalling, a known computable time
  bound, and externally chosen settings. Observers who choose settings by a hard-enough computable
  sequence can learn the model and signal through it. So the "global deterministic simulator" in
  §7 is **not** empirically equivalent to QM under those conditions.
- **Bendersky et al. (2016).** "Algorithmic pseudorandomness in quantum setups." *PRL*
  116:230402. If the settings are computable, even *local* deterministic boxes can fake
  nonlocality in the long run (the "computability loophole"). Mixtures with the same density
  matrix built from computable sequences can be told apart from a finite prefix with arbitrarily
  small error.
- **Verdict:** the main claim survives, but the paragraph needs qualifying. A computable model of
  quantum records that respects no-signalling for external settings must *sample stochastically*
  from the computable Born measure, or else not treat the settings as external. Item (iii) in
  §7.5 ("not what any finite observer can check") is too strong given a promise.
- Related: Wood & Spekkens (2015), *NJP* 17:033002 (Bell explanations need fine-tuning).

### B. Deutsch: "good explanations are hard to vary"
*The Beginning of Infinity* (2011), *The Fabric of Reality* (1997), and "The logic of experimental
tests" (arXiv:1508.02048) deny that selection is merely imposed: explanations that vary freely are
bad on rational grounds. Suggested reply:
- informal "hard to vary" is one more constraint;
- formalized (fewer free parameters, brittleness), it is a description-length measure and inherits
  T3's machine-relativity;
- either way it doesn't identify the model in the limit (T2).

Deutsch–Marletto (2015) constructor theory of information makes P2 a contingent physical claim,
which is worth noting.

### C. Kelly–Genin: a non-aesthetic justification of Ockham
Kelly 2007 and Genin & Kelly 2019 (*Studia Logica* 107:949–989): Ockham minimizes retractions on
the way to the truth, with simplicity defined *topologically*, so not machine-relative. Vitányi &
Li 2000 (*IEEE TIT* 46(2)) give MDL a conditional correctness justification. Suggested reply:
Kelly's efficiency is relative to a chosen problem topology or hypothesis partition, which is
another imposed constraint, and it is about how efficiently a method converges, not about access
to the true model.

### D. Sterkenburg, Neth, Belot: the T4 guarantee is neither assumption-free nor usable
- Sterkenburg: Solomonoff's justification reduces to the assumption of effectiveness. Change
  "assumption-free" to "free of assumptions about the source, *given* P2".
- Sterkenburg 2019 and Neth 2022 (*Phil. Sci.* 90(2), doi:10.1017/psa.2022.72): M is
  uncomputable, so by P2 nobody can use it, and computable approximations need not converge. The
  paper already concedes M is ideal; it should cite them.
- Belot 2013 ("Bayesian orgulity"): separate the sequence-wise K(ν) regret bound, which holds on
  every sequence, from *convergence*, which is μ-a.s. only (Hutter–Muchnik 2007).
- Also: the constant K(ν) is itself machine-relative, so T3 reaches into prediction *rates*.

### E. Real-patterns realism uses the same facts
Dennett 1991 ("Real Patterns," *J. Phil.* 88), Ross 2000, Ladyman & Ross 2007 (*Every Thing Must
Go*, ch. 4: real patterns defined by compressibility relative to a physically possible computer),
and Wallace 2003/2012 (Everett worlds as real patterns). Suggested reply: granting existence to
whatever compresses is an imposed constraint, and Ladyman–Ross's relativity to a reference
computer is T3 under another name. Floridi 2008 (levels of abstraction, *Synthese* 161) is the
closest existing term for "constraint".

### F. Newman's objection hits the structural-realism reply
Newman 1928 (*Mind* 37) and Demopoulos & Friedman 1985 (*Phil. Sci.* 52(4)): Ramsey-sentence
structure collapses into empirical adequacy plus a cardinality condition. The paper equates
"structure" with "what records reach", so concede this. It *helps*: structural realism's surplus
is untestable. Use Quine 1975 ("On empirically equivalent systems of the world," *Erkenntnis* 9)
for when two programs count as the same theory.

### G. Hypercomputer candidates the paper skips
§2 and §7 say quantum randomness is "the most often proposed candidate". The literature's leading
candidates are **Malament–Hogarth / Kerr relativistic computers** (Hogarth 1992; Etesi & Németi
2002; Németi & Dávid 2006, who address usability explicitly) and real-weight analog nets
(Siegelmann). Add a paragraph citing Earman & Norton 1993 ("Forever is a day"), Shagrir &
Pitowsky 2003, Button 2009 (SAD computers fail a usability condition) and Davis 2004 ("The myth
of hypercomputation"). Also drop "in the tradition of Gandy": Copeland & Shagrir 2007 argue that
Gandy's principles are about mechanisms and don't cover relativistic or analog machines.

### H. Gisin: same premise, opposite conclusion
Gisin (2021), *Erkenntnis* 86:1469 ("are real numbers really real?"); Del Santo & Gisin (2019),
*PRA* 100:062107; Gisin (2020), *Nat. Phys.* 16:114. Finite information density leads to an
empirically equivalent but *indeterministic* classical physics. This fits T1/§7 exactly, as one
more underdetermined rival, and should be engaged.

### I. Landsman: deterministic interpretations vs. the Born rule
Landsman (2020), "Randomness? What randomness?", *Found. Phys.* 50:61–104: Bohm and 't Hooft are
strictly incompatible with the Born rule. Reply: finite records can't tell the difference (Prop.
q-records-uncertifiable). Say so explicitly.

---

## 4. Supporting work worth citing

**Limits that complement P2:**
- Wolpert 2008, "Physical limits of inference," *Physica D* 237:1257. Diagonalization over
  physical devices, independent of P2.
- Wolpert & Kinney 2024, *Found. Phys.* 54.
- Breuer 1995, *Phil. Sci.* 62:197.

**Undecidability from universality (support, not counterexamples):**
- Moore 1990, *PRL* 64:2354.
- da Costa & Doria 1991, *IJTP* 30.
- Svozil 1993, *Randomness and Undecidability in Physics*.
- Cubitt et al. 2015, and Bausch et al. 2020 (*PRX* 10).

**Gandy-style derivations of the physical Church–Turing thesis:**
- Arrighi & Dowek 2012, *IJFCS* 23.
- Dowek 2013 (bounded information density).
- Sieg 2008 (an axiomatic model for P2).

**Quantum randomness and certification:**
- Abbott, Calude & Svozil 2015, *J. Math. Phys.* 56:102201 (localized value indefiniteness).
- Abbott et al. 2019, *Phys. Scr.* 94 (experiments).
- Kovalsky et al. 2018, *PRA* 98:042131 (Kolmogorov complexity of Bell data).
- Paterek et al. 2010, *NJP* 12:013019 (logical independence and quantum randomness).
- Svozil 2018, *Physical (A)Causality* (neither determinism nor chance provable from finite data).

**Algorithmic induction:**
- Rathmanner & Hutter 2011, *Entropy* 13:1076.
- Hutter 2009, "Open problems in universal induction & intelligence," *Algorithms* 2:879.
- Leike & Hutter 2015, "Bad universal priors" (COLT; supports T3 by analogy).
- Lattimore & Hutter 2013, "No free lunch versus Occam's razor" (LNCS 7070).
- Domingos 1999, *DMKD* 3:409.
- Zenil et al. 2019, *Nat. Mach. Intell.* 1:58 (a foil: simplicity as a guide to true mechanism).

**Formal learning theory:**
- Kelly & Schulte 1995, *Erkenntnis* 43:29.
- Kelly & Glymour 1989, *Phil. Sci.* 56:185.
- Juhl & Kelly 1994 (PSA; countable additivity builds in realism).
- Earman 1992, *Bayes or Bust?*
- Genin & Kelly 2017, "The topology of statistical verifiability" (check the paper's
  claim that probabilistic underdetermination is permanent against this).
- Baltag, Gierasimczuk & Smets 2016/2019.

**Wolfram critiques:**
- Aaronson 2002, review of NKS, arXiv:quant-ph/0206089 (his model can't satisfy both special
  relativity and Bell).
- Gray 2003, *Notices AMS* 50(2) *(pages unverified)*.
- Zwirn & Delahaye 2011 (formal computational irreducibility).

**Computable-universe framings (foils):**
- Tegmark 2008, *Found. Phys.* 38:101.
- Szudzik 2012/2023 (computable models; useful for making P2 precise).
- Schmidhuber 1997/2002.
- Fredkin 2003.
- Lloyd 2002, *PRL* 88:237901.

**Historical precursors to name in §1:**
- Leibniz (*Discours* §VI) and Weyl.
- Mach (economy of thought) and Pearson (*Grammar of Science*).
- Poincaré (*La Science et l'hypothèse*).
- Ramsey/Carnap (Ramsey sentences).
- Hume and Kant.
- Hofstadter (*GEB*: one formal system, many interpretations).

---

## 5. Suggested replacement for the Contributions paragraph (§1) — superseded

> Neither the individual results nor the guiding idea is new. That a finite record admits
> arbitrarily many laws, and that a theory is to be judged by how far it compresses its data, goes
> back to Leibniz and Weyl and was made precise by Chaitin; Mach and Poincaré made economy and
> convention central to science; Hutter formalized description-length selection among computable
> theories of everything; Kelly recast underdetermination as learning-theoretic unsolvability;
> Sterkenburg showed that the Occam justification of Solomonoff prediction rests on an
> effectiveness assumption and on the choice of universal machine; and our second premise is
> Piccinini's modest physical Church–Turing thesis. Unlike these works, we assume nothing about
> whether the world is computable or what it consists of—only that records are finite and usable
> methods effective—and we combine non-identifiability in the limit, machine-relative description
> length, and the source-free regret bound of universal prediction into a single theorem-level
> sharpening of empirical underdetermination, applied in turn to quantum randomness. The
> conclusion, that data force convergence of predictions but not of model identity, is a
> formalized conventionalism.

---

## 6. Gap check (2026-10-30)
- **Verified:**
  - Pitowsky 1990 is *Iyyun: A Jerusalem Philosophical Quarterly* 39:81–99. This comes from Kalai's
    2020 chapter reference list as deposited with Crossref (doi:10.1007/978-3-030-34316-3_18).
    Semantic Scholar's record for it is wrong.
  - Landsman, arXiv:2610.23355, matches the claim and is now cited in §7.
  - Sterkenburg, arXiv:2603.20274, is a book chapter with no venue listed; it isn't cited, since his
    2016–2019 papers are.
  - Müller, *Found. Phys.* 56:11 (2026), doi:10.1007/s10701-026-00913-1. Müller himself names the
    programme "algorithmic idealism", so the paper now says so, citing muller2026.
- **Added:** Kalai 2020, "The Argument Against Quantum Computers" (in Hemmo & Shenker (eds.),
  *Quantum, Probability, Logic*, Springer), pp. 399–422. Cited in §7.2 as disputing even the
  *complexity* advantage of quantum computation, in support of Pitowsky's physical Church thesis.
- **Not found, and not cited in the paper:** Senno, "A computable interpretation of quantum
  mechanics?"; a Brukner paper on "quantum randomness and undecidability"; a Miłkowski paper on
  real patterns.
- **Content not checked, not cited:** Neth 2026, "Gruesome predictions"; Kelly & Glymour 2004.
