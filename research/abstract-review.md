# Abstract review (2026-10-30)

## Problems with the previous abstract (234 words, 5 sentences)
1. **It opened by saying what the paper does not claim.** The reader got no context or gap first.
   Mensh & Kording call results-before-context "the most common error".
2. **Its third sentence ran to 121 words**, chaining four results with semicolons. That breaks the
   "Rule of One" (frame one contribution) and Gopen & Swan's advice to keep the subject next to the
   verb.
3. **It used jargon and symbols without defining them:** K(ν), "lower semicomputable", "effective",
   "sound formal theory". The `\K` macro breaks on arXiv, whose abstracts are plain text.
4. **It lacked key search terms:** "underdetermination" (which is in the title), "scientific
   realism", "Solomonoff", "minimum description length", "learning theory".
5. **Kept:** the honest "assembling known results", and naming the position at the end.

## Rules applied
Sources: Koopman 1997; Nature's summary-paragraph guide; Mensh & Kording 2017; Gopen & Swan 1990;
Weinberger et al. 2015; Elsevier SEO guidance; Springer and Cambridge author instructions.

- Order the moves: context, gap, "we show", results, implication.
- Frame one central contribution; the results are its facets.
- State the theses themselves, not "we discuss".
- Be self-contained: no citations, symbols or undefined acronyms.
- Put the key concept in the first one or two sentences.
- Use the exact phrases people search for.
- Use plain words, but don't over-compress.
- Exemplars in this field (Belot 2013, Neth 2023, Sterkenburg 2019, McAllister 2011) run 85–120
  words, in the first person, as plain prose with no formulas.

## Venue limits (see the venue research for sources)
- **Synthese:** abstract 150–250 words; no length cap. Best fit.
- **Journal of Philosophical Logic:** 150–250 words; no length cap.
- **Foundations of Physics, EJPS, Minds & Machines:** 150–250 words; no stated length cap.
- **Philosophy of Science:** 100-word abstract; 9,000-word cap.
- **BJPS:** 24-page cap. **Erkenntnis:** 10,000 words. **SHPS:** 12,000 words. At about 20,000
  words, the paper would have to be split for any of these.
- **arXiv:** at most 1920 characters, plain ASCII, no custom macros.

## Master abstract (now in main.tex)
207 words, 1419 characters, 9 sentences, the longest 31 words. Fits all Springer journals and arXiv.

Scientific realists hold that successful theories approximately describe how the world really is; underdetermination arguments deny that evidence can settle this, but they have remained largely informal. We make the denial precise without assuming anything about what the world is. Our premises are that every observation is a finite, finite-precision record, and that every method anyone can use to choose among models is computable, a modest physical Church-Turing thesis. Combining known results from learning theory and algorithmic information theory, we show that every finite record is reproduced by infinitely many computable models that disagree about what has not been observed. No computable method identifies the right model on every computable world, even with unlimited data. Simplicity criteria such as minimum description length depend on an arbitrary choice of reference machine, so every selection among rivals reflects a constraint we impose. Prediction is different: Solomonoff's universal predictor does nearly as well as every computable model on every data sequence. Quantum randomness, the most cited escape route, adds no computational power when its probabilities are computable and cannot be certified from finite records. We call the resulting position algorithmic conventionalism: data can force predictions to converge, but cannot single out which of the equivalent models is the right one.

## Short abstract (Philosophy of Science, ~100 words)
99 words.

Underdetermination arguments hold that evidence cannot settle how the world really is, but they have remained largely informal. Assuming only that observations are finite records and that usable methods are computable, we combine known results to make the claim precise. Every record fits infinitely many computable models that disagree about the unobserved, no computable method identifies the right one even with unlimited data, and simplicity criteria depend on an arbitrary choice of reference machine. Yet a universal predictor does nearly as well as every computable model. Data can force predictions to converge, but never single out the right model.

## Suggested keywords
underdetermination; scientific realism; Solomonoff induction; minimum description length; formal learning theory; physical Church-Turing thesis; quantum randomness; conventionalism

## Previous abstract (for reference)

We make no claim about what the universe is. We start from two premises: every use
of any system leaves a finite, finite-precision, symbolic record; and every system
that can be used---every method of turning records into predictions included---is
effective (computable, or for stochastic systems described by a computable measure),
a modest physical Church--Turing thesis extended to methods. Assembling
known results into a single argument, we show: whatever a sound formal theory,
continuous or not, effectively determines is computable, so discrete computation adds
no limitation beyond those of formal mathematics; every record is reproduced by
infinitely many computable models that disagree on what has not been observed, and no
computable method identifies the correct model on every computable world, even with
unbounded data; every selection among these models is the work of an imposed
constraint, and description length itself is relative to a choice of universal
machine; yet, given the second premise, the (uncomputable) universal predictor is
within $\K(\nu)$ bits of every lower semicomputable model $\nu$ on any data sequence,
with no assumption about the source of the data. Quantum randomness is a case study:
powerless for computing functions when its probabilities are computable,
uncertifiable from finite records, and underdetermined across interpretations. The
position, which we call algorithmic conventionalism, is that data can force
convergence of an ideal predictor's predictions but never single out which of the
observationally equivalent models is the right one.
