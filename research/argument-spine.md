# Argument spine (v2): Algorithmic Agnosticism

Title: **Algorithmic Agnosticism: Why No Theory of Everything Can Be Known to Be Final**

This document is the single source of truth for the v2 rewrite. Every element of the paper must
appear here with its dependencies. Anything not on this spine is cut. (The cut material is
not included in this repository.)

## 0. The claim

**Main claim (C).** No theory of everything (ToE) can be known to be final. The claim has
three parts:

- **C1 — No certification (unconditional).** No method of any kind, computable or not, can
  certify at a finite time that a model is final on every world consistent with what has been
  observed. Certification is possible only relative to a restriction on the worlds considered, and
  that restriction is a bias the record does not supply.
- **C2 — No reliable discovery (needs P2).** No usable method is even guaranteed to *converge* on
  a final theory, without announcing it, on every computable world. For any finite record, some
  world consistent with it defeats the method. So a user can never rule out being in such a world.
- **C3 — No fundamental formulation, even ideally (unconditional).** Even an ideal agent with
  unlimited computing power and data cannot tell apart formulations that make identical
  predictions, or chance hypotheses that agree on which events are impossible. "Which ToE is
  fundamental" is not settled even in principle.

**Corollary (C′) — what the search is good for.** Preferring one candidate ToE over its rivals is
a constraint we impose: simplicity, beauty, naturalness, unification. The most common such
constraint, simplicity, depends on the choice of machine. Seeking compact unified theories is
still worthwhile, because compression yields testable new predictions. What is misguided is the
*goal* of a final theory known to be final.

**Position: algorithmic agnosticism.** We use the word in Huxley's sense: we neither affirm nor
deny that a final theory exists; we hold that one could never be known to be final. This differs
from constructive empiricism, which is agnostic about unobservable entities. We are agnostic about
*which law generates the observations themselves*.

## 1. Setting (definitions; only what the theorems use)

- **D1 Record.** A finite sequence of (setting, outcome) pairs over a finite alphabet, encoded as
  a string; records grow by extension. A record is *functional* if no setting has two different
  outcomes.
- **D2 Model.** A deterministic model is an index e of a partial computable function φ_e. A
  stochastic model is a computable (or lower-semicomputable) measure on outcome sequences, with
  settings fixed.
- **D3 World.** Whatever produces records. A *computable world* is one whose record-generating
  behaviour is a total computable function f (deterministic) or a computable measure μ
  (stochastic). We make no claim that the actual world is computable.
- **D4 ToE / final.** A model is *final* for a world if it agrees with every record the world can
  produce: φ_e = f (extensional), or ν = μ. A *ToE* is any model offered as final.
- **D5 Method.** A function from records to models. It is *usable* if it satisfies P2 (computable,
  or a computable stochastic process).
  - *Certifies* at record R: the method outputs a model plus "final".
  - *Identifies f in the limit*: on the canonical presentation of f, its outputs are eventually
    constant at an index of f (Gold).
- **D6 Constraint / bias.** Any ordering or selection rule on models, possibly depending on the
  record. *Imposed* means the record does not determine it.
- **D7 Level of identity.** Programs (indices), extensions (behaviour), chance hypotheses
  (measures).

## 2. Premises

- **P1 Finite record (definitional).** Every use of any system yields a finite, finite-precision
  record.
- **P2 Usable systems are effective (assumption, asserted, not proved).** Every system that anyone
  can use, including every method of choosing models, is computable or a computable stochastic
  process.
  - This is Piccinini's modest physical Church–Turing thesis, extended to methods.
  - It is defended in §2, not proved.
  - **Defence (only what is needed to block the standard counterexamples):**
    - (a) *Continuous theories*: their usable consequences are computable to finite precision
      (computable analysis). Their non-computable values cannot be used (Davis; Pour-El–Richards
      as an example).
    - (b) *Relativistic hypercomputers* (Malament–Hogarth / Kerr): their output cannot be relied on
      or certified by the user (Earman–Norton).
    - (c) *Quantum randomness*: Born statistics with computable parameters form a computable
      measure, so a quantum RNG is a computable stochastic process. Randomness adds no power to
      compute functions (de Leeuw–Moore–Shannon–Shapiro; Sacks).
    - **One sentence:** refuting P2 requires a usable hypercomputer.

## 3. Results, with dependencies

| Id | Statement | Depends on | P2? | Supports | Proof source |
|---|---|---|---|---|---|
| **T1** | (a) For every finite functional record R and every e ∈ Cons(R), there are infinitely many total computable models consistent with R that differ from e, and from each other, on unobserved settings. In fact, for every unobserved x and every y, some total computable model consistent with R outputs y at x. (b) Every computable function has infinitely many indices (padding). (c) Stochastic analogue: infinitely many computable measures give R positive probability and differ in their predictions after R. | D1–D2 | no | C1, C3 | lookup-table construction (folklore; Kukla's T″); padding lemma (Rogers) |
| **K1** | *No certification.* For any method M (of any kind), any record R and any model e that M certifies at R, there is a computable world consistent with R in which e is not final. So no method certifies correctly on every computable world; certification can be correct only relative to a restricted class of worlds (a bias). | T1(a) | **no** | C1 | immediate: same record, divergent world g_y |
| **T2** | *Gold–Putnam, prefix form.* For every computable method L and every finite record R, there is a total computable world consistent with R on which L does not identify the world in the limit. Also covers randomized usable methods: none identifies every computable world with probability > ½ (*if Pitt 1989 verifies*; otherwise state as open). | D5, P2 (to cover all usable methods) | **yes** | C2 | diagonalization started from R (Putnam 1963; Gold 1967); Pitt 1989 for randomized methods |
| **L** | *Every method is a bias.* Every method that outputs consistent models is a record-indexed constraint. The class of worlds on which it succeeds is fixed by the method, not by records: by T2's prefix form, every record is consistent with worlds inside and outside that class. | T2, D6 | via T2 | C2, C′ | short proof |
| **T3** | *Simplicity is machine-relative, by a bounded amount.* For any finite record R and any e ∈ Cons(R), some universal prefix machine makes a program for φ_e the shortest program consistent with R. The shift is bounded: K_{U′} ≤ K_U + 1 and K_U ≤ K_{U′} + K(e) + O(1), so the change of machine costs about K(e) bits. Near-minimal divergent rivals exist within K(x,y)+O(1) bits of the minimum. | T1 | no | C′ | U′ construction; invariance theorem |
| **T5** | *Permanent underdetermination, even ideally.* (a) Extensionally equal models (different programs, formulations, interpretations or dualities with identical predictions) agree on every record, so no method separates them. (b) If μ and μ′ are mutually absolutely continuous, no method (any measurable function of records, computable or not) converges to the correct one with probability 1 under both. | T1(b), D2 | **no** | C3 | (a) trivial; (b) the success event has μ-measure 1, hence μ′-measure 1, a contradiction |
| **T4** | *The ideal benchmark.* The universal mixture M has log-loss within K(ν) bits of every lower-semicomputable ν on every sequence. No computable predictor has this property. So the benchmark is not a usable method (by P2). | D2 | to read it as unusable | C′ only | Solomonoff/Li–Vitányi dominance; adversarial-sequence proposition |

**What an ideal agent can do (a concession that keeps C honest).** In a deterministic computable
world, an uncomputable agent (MDL with an oracle, or a Bayesian mixture) *does* converge on the
true extension. So C2 depends on P2; C1 and C3 do not.

**T2-rel (added v2.2).** *Relativized Gold.* For every oracle A, every total
A-computable method that outputs A-indices, and every finite record R, some total A-computable
world consistent with R defeats it. This gives the weaker premise **P2\***: for some A, every
usable method is A-computable and every A-computable world is a candidate theory. P2\* suffices
for C2 for deterministic methods (`thm:ud-gold-rel`, `rem:p2star`). It is claimed only for
deterministic methods; whether Pitt/Smith relativize has not been checked.

## 4. The chain

- **C1** = T1(a) → K1. No P2 needed.
- **C2** = P2 + T2 (+ L). Every usable method is a computable bias that some world consistent with
  every record defeats.
- **C3** = T1(b) + T5. No P2 needed.
- **C′** = L + T3 (+ T4). Every preference among candidate ToEs is a constraint; simplicity is
  machine-relative. The ideal benchmark shows compression predicts, but it is unusable.

## 5. Objections that must be answered (sufficiency against a referee)

Only these (eight). Each answer is a short paragraph in §8 unless it is noted as handled in place.

1. **"This is just Hume / Popper (laws can be refuted but not verified)."** That is C1 only. The
   paper adds C2 (usable methods don't even converge: Gold), C3 (permanence even ideally), and T3
   (the main escape route, simplicity, is machine-relative).
2. **"A method need only work in *our* world, not all worlds."** Which class "ours" belongs to is
   exactly the bias; by T2's prefix form no record tells. This is the central reply and is
   handled in §4 as well.
3. **"Divergent rivals are eventually refuted, so underdetermination is transient"** (Sklar,
   Laudan–Leplin). True for each rival, but a usable method can never know the transient phase
   is over (T2, prefix form). The permanent residue is T5.
4. **"The rivals are cheap / parasitic"** (Leplin–Laudan on Kukla). Excluding them is a bias (L).
   Rivals with comparable compactness exist (T3, near-minimal), and physics supplies serious ones:
   dualities, quantum interpretations, Newtonian/Lagrangian/Hamiltonian mechanics.
5. **"Simplicity / beauty is truth-conducive"** (Occam, Deutsch's "hard to vary", Kelly–Genin
   Ockham efficiency, Hossenfelder's critique as an ally). T3 for description length.
   Hard-to-vary and naturalness are further constraints. Kelly's Ockham method converges
   retraction-efficiently relative to a chosen problem but never *certifies* finality, so it is
   consistent with C. Deutsch himself denies final knowledge; he is an ally on C and an opponent
   only on whether selection is rational.
6. **"The success of physics shows convergence on the truth"** (no-miracles). Success is
   predictive (C′, T4). Predictive success does not certify finality (K1).
7. **"Algorithmic probability is itself the law"** (Müller's algorithmic idealism). Müller
   shares the record-first starting point and accepts machine-relativity (his Postulate (iii):
   predictions are only those identical for every algorithmic prior, citing his 2010 result).
   He *postulates* that algorithmic probability gives the chances of the next observation. As a
   candidate final law, that postulate is uncertifiable (T1(c), K1), is a chosen bias (L), leaves
   finite-record predictions open (his own Postulate (iii)), and is uncomputable (T4). It is an
   instance of C, not a counterexample. The two views agree on what records settle; Müller
   affirms a law beyond them, and we remain agnostic.
8. **"P2 begs the question / hypercomputers exist."** Handled in §2's defence of P2. Here one
   sentence states what refuting P2 requires.

Targets named in the introduction: Weinberg (*Dreams of a Final Theory*), Tegmark, Wolfram's
unique ruliad, Hutter 2010.

## 6. Paper outline and word budget (~10.5k)

| § | Title | Content (only spine elements) | Words |
|---|---|---|---|
| 1 | Introduction | ToE question; C in plain English; agnosticism (Huxley); what is not claimed; precursors (Hume/Popper, Leibniz–Weyl–Chaitin, Putnam–Gold–Kelly, Hutter 2010, Hawking 2002, Hossenfelder 2018, Sterkenburg, Piccinini); contributions (synthesis; the new parts); outline | 1000 |
| 2 | Framework and premises | D1–D7; P1; P2 + defence (a)–(c); argument table (the chain in §4) | 1700 |
| 3 | No record certifies a final theory | T1(a)–(c); K1; remark that divergent rivals are refuted over time (sets up §4) | 900 |
| 4 | No usable method finds one | T2 (prefix form; randomized methods); "can't rule out a failure world"; L; the "our world" reply; the ideal-agent concession | 1500 |
| 5 | Simplicity does not single one out | T3 + near-minimal rivals; naturalness, beauty and unification as constraints; physics examples of serious rivals | 1300 |
| 6 | What even an ideal agent cannot know | T5(a) with dualities and quantum interpretations as examples; T5(b) with proof and example | 1000 |
| 7 | What the search is good for | T4 compactly; no computable predictor dominates; compression → novel prediction (Maxwell, Dirac; Vulcan as a failure) | 800 |
| 8 | Objections | the eight above | 1700 |
| 9 | Conclusion | C, C′, agnosticism | 400 |
| — | Statement on the use of AI | keep (required by norms, not by the argument) | 400 |

## 7. Removed, with reason

- **§3 discrete-sufficiency theorem, Ω remark, undecidability remark:** not needed. P2's defence
  (a) carries the continuous-models point in one paragraph.
- **§7 Bell / Bendersky / computability loophole / DI certification / Landsman / Gisin / Kalai
  material, the two kinds of limitation, the crypto section:** not needed for C. Quantum is kept
  only in P2's defence (c) and as T5(a) examples.
- **Kt / Levin search, the catalogue table, the McAllister / Twardy related-work subsection:**
  supporting only. McAllister is mentioned in one line among the precursors.
- **Weaker learning criteria (BC, BC\*, next-value) and the topology remark:** supporting only.
- **Objections on real patterns, Newman, structural realism, the simulation hypothesis, and
  constructive empiricism (except one sentence on positioning):** not among the strongest
  objections to C.
- **The Solomonoff convergence corollary and the NFL remark:** not needed. T4 dominance plus the
  no-computable-dominates result suffice for C′.

## 8. Coordination: labels and files

- **Files:** `01-intro`, `02-framework`, `03-certification`, `04-discovery`, `05-simplicity`,
  `06-ideal`, `07-prediction`, `08-objections`, `09-conclusion`, `10-ai-statement`.
- **Section labels:** `sec:intro`, `sec:framework`, `sec:certify`, `sec:discover`,
  `sec:simplicity`, `sec:ideal`, `sec:predict`, `sec:objections`, `sec:conclusion`.
- **Key labels:**
  - premises: `prem:record`, `prem:effective`
  - definitions: `def:record`, `def:model`, `def:world`, `def:final`, `def:learner`,
    `def:constraint`
  - results:
    - T1 `thm:ud-infinite`
    - K1 `thm:k1-certify`
    - T2 `thm:ud-gold`
    - L `lem:bias`
    - T3 `thm:con-machine` and near-minimal `thm:con-nearmin`
    - T5 `thm:t5-permanent`
    - T4 `thm:pred-relative`
    - no computable predictor dominates `pred:prop:no-computable`
    - randomness powerless `thm:q-powerless`
    - Born measure computable `prop:q-born-computable`
- **New bibliography keys:** `pitt1989`, `smith1982`, `hawking2002`, `hossenfelder2018`,
  `weinberg1992`, `maldacena1998`, `huxley1889`, `popper1959`, `polchinski1998`.
