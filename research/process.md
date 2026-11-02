# How this paper was produced

This is a record of how *Algorithmic Agnosticism: Why No Theory of Everything Can Be Known to Be
Final* was written. Earlier working titles were *Indistinguishable by Observation* and *Algorithmic
Conventionalism: Computability, Simplicity, and the Underdetermination of Models*. The record
accompanies the paper's "Statement on the use of AI". All work took place in one extended Claude
Code session (Anthropic; model Claude Opus 5.5) on 2026-10-30, directed by the author. The public git history begins at version 1.0; earlier drafts are
described here but not included (see §13).

## 1. Origin and thesis (author)
The ideas came from the author's earlier reading (Hofstadter, Deutsch, Wolfram) and an earlier
conversation about formal models of the universe. The author stated the thesis:

> All systems that humans can use are formal systems. All sufficiently powerful systems are
> universal. All inputs and outputs of all systems can be reproduced by other universal systems.
> The set of all observations can be reproduced by an infinite number of formal systems.
> Therefore you cannot distinguish between the infinite number of systems that can model the
> observations and "how the universe really works". You can impose aesthetic or practical
> constraints on formal systems and find the ones that meet your imposed constraints.

The author then corrected or sharpened the AI's framings:
- **MDL:** minimum description length is a constraint one *may* impose, not a criterion of
  correctness. The existence of models that cannot be told apart is the point.
- **Truth:** the claim is not about truth. Infinitely many systems are indistinguishable from
  the observations.
- **Continuous models:** continuous quantities cannot be observed or expressed, and continuous
  models are formal systems that discrete systems implement. Discrete systems add no
  limitation beyond those of mathematics.
- **Non-computable sources:** a source that isn't computable is not expressible by any system a
  human or machine can access.
- **Quantum randomness:** it affects all formal systems equally. "Discrete computable models
  are all we have, even if we wish it to be different."
- **Compression:** a minimal-description model compresses what is known, and it may predict
  things not yet known that can then be verified.

## 2. Drafting (AI, parallel agents)
- The AI wrote the shared skeleton: notation, definitions, premises, introduction and
  bibliography keys.
- Five agents then drafted the theorem sections in parallel: discrete sufficiency;
  underdetermination (T1, Gold's theorem); constraint-relative selection (T3); prediction (T4);
  and quantum randomness.
- A sixth agent verified all 50 initial references against Crossref.

## 3. Review rounds (AI, independent agents)
Each round used reviewers started without the drafting context. Their findings were then
applied by agents, one per section.

**Round 1 (mathematics and coherence).** Three errors, plus gaps, including:
- An incorrect procedure for computing the Kt minimum.
- A wrong definition of bi-immunity.
- A mischaracterization of superdeterminism.
- A misattribution of Laudan–Leplin.
- Prediction claims that overstated convergence.

The structurally important finding was that finite records (P1) do not imply that methods are
computable. The author's claim that "all systems humans can use are formal systems" was
therefore made an explicit premise, **P2**, not a derived step.

**Fact-check.** Eight flagged claims were checked against the literature, including Chaitin's
Ω attribution, the Pour-El–Richards norm-dependence, the Solomonoff bound constant, and the
oracle characterization of Adleman–Blum. Six corrections followed.

**Round 2.** Sections 6–9 were reviewed against the realist and quantum-foundations literature.
This added objections: transient underdetermination, structural realism, Bayesian confirmation
and the no-miracles argument.

## 4. Literature research (AI, seven parallel agents)
Seven strands were searched:
- The Hofstadter, Deutsch and Wolfram lineage.
- Algorithmic induction and Occam's razor.
- Formal learning theory.
- The physical Church–Turing thesis.
- Quantum randomness.
- Structuralism and real patterns.
- A direct check for precedents.

About 120 sources were checked for existence; see `related-work.md`. The search found:
- **No prior work makes the combined argument**, but each step has close precedents: Chaitin,
  Hutter 2010, Sterkenburg, Kelly, Kukla, McAllister and Piccinini. The paper was repositioned
  as a synthesis ("algorithmic conventionalism").
- **A required correction.** Bendersky et al. (PRL 2017) show that deterministic computable
  models of Bell correlations can be exposed by suitable protocols. The paper's claim about
  discrete simulators in §7 was rewritten accordingly.

## 5. Revision and second review (AI)
- **Revision.** Seven agents revised the paper by file. A bibliography agent added 101 verified
  entries under fixed keys, so the section agents never edited the bibliography at the same
  time.
- **Second review.** Two fresh reviewers found three more errors:
  - an overstatement of Bendersky et al.;
  - a false contrast between prediction and selection on finite data;
  - a mis-credit of the dominance theorem to a single program.

  They also found about 15 misattributions and 10 passages duplicated by the parallel
  revision. P2 was restated to cover stochastic systems through a computable measure.
- **Gap check.** Prompted by the author supplying Kalai (2020), this verified the last
  unconfirmed reference (Pitowsky 1990), confirmed three 2026 preprints, and corrected the
  description of Müller's programme.

## 6. Abstract
The v1 abstract was rewritten following published guidance on writing abstracts and the venues'
requirements; see `abstract-review.md`.

## 7. Necessity, sufficiency and hostile-referee audits (AI, three independent agents)
The author asked whether everything in the ~20,000-word paper was necessary, and whether the paper
was sufficient to support its claim. Three fresh reviewers answered:

- **Necessity.** About a third of the paper served no claim in the abstract: the discrete
  sufficiency theorem, most of the Bell/Bendersky material, and about 30 repeated points.
- **Sufficiency.** The theorems were correct, but the abstract's conclusion was not what they
  proved.
- **Hostile referee.** Verdict: *major revision*. Three defects:
  - "Cannot single out the right model" equivocated across three levels: trivially true for
    programs, false for an ideal agent at the level of behaviour, and permanently true only for
    chance hypotheses that never separate.
  - The claimed asymmetry ("predictions converge, identity does not") vanished under P2, because
    no computable predictor has the guarantee.
  - "Every selection reflects an imposed constraint" was true by definition.

## 8. Comparing the claims (V0, V1, V2)
The claims were compared in three versions:
- **V0:** the author's original statements.
- **V1:** the 20k-word paper.
- **V2:** a reframing the theorems actually support. For every usable method some computable world
  defeats it; no usable constraint is truth-conducive across all worlds a user could face; and only
  formulations and chance hypotheses stay permanently underdetermined, even ideally.

V2 returned closer to V0. The author accepted it.

## 9. Reframing and naming (author's decisions)
- **Target.** The author redirected the paper at searches for a final theory of everything.
- **Claim.** It was stated as unknowability, not non-existence. "There is no final theory" was
  rejected as a metaphysical overclaim.
- **Name.** The author chose "agnosticism", in Huxley's sense, noting the parallel with
  agnosticism about God.
- **Qualifier.** "Algorithmic" was kept because it matches the field and pairs with Müller's
  "algorithmic idealism".
- **Title.** The subtitle "Why No Theory of Everything Can Be Known to Be Final" was the author's.
  "On the Undecidability of…" was rejected as technically inaccurate.
- **Terminology.** The second premise was relabelled an *assumption*, to avoid confusing it with
  the paper's thesis.

## 10. The argument spine and the v2 rewrite
The author asked that every point be traced from the premises to the conclusion, keeping only what
is necessary and sufficient.

**The spine.** `argument-spine.md` lists every definition, premise, result and necessary objection,
with its dependencies:
- premises P1 and P2;
- results T1, K1, T2, L, T3, T5 and T4;
- conclusions C1–C3 and C′.

It surfaced one structural finding: C1 (no certification) and C3 (permanence even ideally) need no
P2.

**The rewrite.** Seven agents rewrote the sections against the spine in parallel, with a
bibliography agent verifying new sources. These included Pitt 1989, Smith 1982, Pitt & Smith 1988,
Hawking 2002, Hossenfelder 2018, Weinberg 1992, Maldacena 1998, Popper 1959, Huxley and Kakutani
1948.

| Version | Main text | Cited references |
|---|---|---|
| v1 | ~20,800 words | 184 |
| v2 | ~9,100 words | 63 |
| v2.2, after the later fixes | ~11,000 words | 63 |

Removed material is not included in the published repository.

## 11. Round-3 audits and fixes
**Trace audit.** A fresh agent checked every element against the spine. It found four missing
steps:
- a stochastic version of K1;
- a precise randomized form of T2, starting from the observed record;
- a derivation of "imposed";
- definitions of the selection operator and cost.

**Proof review.** A second agent found two errors and six gaps. The errors:
- The randomized corollary overstated what Pitt/Smith give. The correct form is: for every p > 0,
  some world makes success less likely than p.
- The definition of K(ν) did not support a bound.

The gaps included measurability of the convergence event, the Fubini step for randomized methods,
"cannot be told apart" needing "with certainty", and what the method observes.

**Fixes.** All were applied by per-file agents from a shared wording file (`round3-wording.md`).

**Müller.** The author asked to address the distinction with Müller. Reading Müller's arXiv source
showed that his Postulate (iii) already anticipates machine-relativity: predictions are only those
identical for every algorithmic prior. His Postulate (ii) asserts that algorithmic probability gives
the chances. Objection 7 treats algorithmic idealism as an instance of the main claim, not a
counterexample.

## 12. Alternatives to P2 and the relativized theorem
The author asked for alternatives to P2. The ones compared:
- the bold physical Church–Turing thesis;
- Gandy-style derivations from physics;
- resource-bounded premises;
- a Penrose-style denial;
- dropping P2;
- a relativized premise.

**What changed.** The agents proved that Gold's theorem holds at every oracle level
(`thm:ud-gold-rel`). They introduced the weaker premise P2\*: every world computable at a method's
own level is possible. For deterministic methods, C2 needs only P2\*.

**Verification.** An independent reviewer confirmed the theorem and proof. It required qualifiers:
- per-method levels, with A-indices;
- P2\* stated about the worlds a method must cope with;
- hypercomputers covered only if they have oracle strength and theories share their power;
  infinite-time Turing machines are not covered;
- the oracle that suffices is a "high" oracle (Adleman–Blum);
- randomized results not claimed to relativize.

The title claim rests on C1 and needs neither premise.

## 13. Necessity pass and publication
- **Necessity pass.** At the author's instruction ("references to P2, or any other claim, should
  only be made when necessary"), every reminder of which results depend on which premise was cut.
  Each dependency is now stated once. References to the second premise fell from about 45 to 23,
  and the jargon "defeats" was replaced with plain wording.
- **Toward version 1.0.** Before version 1.0 the paper went through these stages: the ~20k-word
  v1 draft; the v2 rewrite against the argument spine; round-3 fixes and the Müller objection; the
  relativized theorem and P2\*; citation-content fixes and sanitizing; the necessity pass; and the
  two further rounds in §§14–15. The repository history was then flattened into a single commit,
  version 1.0.

## 14. Pre-release round: the Vitányi-school critique
Next the author asked for a comparison with Paul Vitányi's work, and for an adversarial
critique from that school's standpoint.

**How it was run.** Two comparison agents worked in parallel: one on model selection (ideal MDL,
algorithmic statistics, structure functions, meaningful information), the other on prediction,
compression in practice, and physics. A hostile referee trained in the same school read the
primary sources and tried to break the paper.

**Verdict.**
- **What survived.** C1–C3 stand. Algorithmic statistics is a theory of the observed record. It is
  uncomputable, accurate only up to O(log n), and justifies MDL only when the data are typical, so
  it does not reach claims about what lies off the record. The objection that the defeating
  worlds are pathological fails: they are about as simple as the method.
- **What did not.** The way C′ and T3 were worded overstated them:
  - "large enough to reverse the verdict for any comparison" overstates T3: a change of machine
    reorders only near-ties;
  - "no known principle privileges a reference machine" holds only within the class of universal
    priors;
  - §7's account of why compression predicts also applied to lookup tables;
  - the key literature was not cited.

**Fixes in that round.**
- T3 and C′ restated as a near-tie result: simplicity narrows the field but cannot decide among
  the survivors that matter.
- The dominance theorem is acknowledged to privilege universal priors as a class.
- The compression mechanism in §7 is now grounded in dominance.
- A bound on the complexity of the defeating world is added to §4.
- Vitányi–Chater 2017 and Bienvenu et al. 2018 are cited at T5(b).
- Replies on ideal MDL (Vitányi–Li 2000) and on the "objectivity" of Kolmogorov complexity are
  added to objection 5.
- About ten new references, including Gács–Tromp–Vitányi 2001, Vereshchagin–Vitányi 2004, Li et
  al. 2004, Cilibrasi–Vitányi 2005, Terwijn–Torenvliet–Vitányi 2011, and Bennett et al. 1998.

## Limitations of this process
- **No human expert has reviewed the paper.** AI reviewers caught real errors in every round, but
  they share blind spots with the AI that drafted it. Expert review is being arranged.
- **Citation content was checked by AI agents, not by people.** Every work was confirmed to exist,
  with correct bibliographic data. Two agents then checked what each citing sentence attributes to
  its source. They covered 29 learning-theory sentences and about 45 philosophy and physics keys,
  reading full texts where they were accessible. They found no outright errors in the learning
  theory. They found three wrong and four misattributed claims in philosophy and physics:
  Sterkenburg 2016, the Kukla/Leplin–Laudan chronology, and the attribution of Müller's postulates,
  among others. All were corrected before version 1.0.
  - **Read from source:** Müller 2020 (arXiv source), Kalai 2020 (reference list), Hutter 2010,
    Hawking 2002, Huxley 1889, Deutsch 2011 (excerpts), Sterkenburg 2016 (preprint), Earman–Norton
    1993, and others.
  - **Not reachable, so resting on agents' recall:** Weinberg 1992, the two *Analysis* papers from
    1993, Polchinski, GRW, and Pour-El–Richards. For Pour-El–Richards the paper now uses wording
    that holds whatever the exact smoothness condition is.
  - **Still open:** the page range of Huxley 1889, and whether the Polchinski DOI is volume 1.
- **Treat the paper as a preprint.** Its claims should be checked against the original sources
  before anyone relies on them.

## 15. Pre-release round: the readiness rubric
The author then asked for a rubric for judging readiness (`../mind-of-god/research/readiness-rubric.md`, in The Mind of God project). It covers necessity, sufficiency, correctness, structure, prose, positioning, integrity and review. Independent agents scored the paper against it (`review-readiness-prerelease.md`). Their findings were then fixed:
- a corrected complexity bound;
- T2 extended to partial methods;
- a gap form of T3;
- stochastic models defined as indices;
- the knowledge standard stated as a definition;
- refutation conditions for P1, P2 and P2\*;
- active methods covered;
- the externalist and self-application objections answered;
- engagement with Kiefer 2024, Schmidhuber 2000 and Hutter's caveat;
- a further necessity pass.

Gate re-reviews followed, and citation locators and quotations were checked (`citation-check.md`). Six locators remain unconfirmed.

