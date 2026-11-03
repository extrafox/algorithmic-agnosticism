# Algorithmic Agnosticism: Why No Theory of Everything Can Be Known to Be Final

**Christopher S. Taylor**

> **Status: version 1.0, preprint, not peer-reviewed. Comments welcome.**
> This paper was produced with substantial assistance from AI systems (Claude Code, Anthropic;
> Grok, xAI, in developing the initial idea). The author directed the work and is responsible for
> its content. See the *Statement on the use of AI* at the end of the paper and
> [`research/process.md`](research/process.md) for how it was made.

**[Read the paper (PDF)](paper/algorithmic-agnosticism.pdf)**

## In brief

Suppose physicists found a theory of everything that matched every observation ever made. This
paper argues that no one could ever know it was the final theory. Every finite body of evidence
fits infinitely many theories that disagree about what has not yet been seen. No method anyone
can actually use is even guaranteed to settle on the right one. Even an ideal agent could not
tell apart formulations that make the same predictions. Preferences for simplicity or beauty
are choices we impose, not facts the data deliver. Compact, unified theories are still worth
seeking, because they make new, testable predictions. What is misguided is the goal of a final
theory known to be final. The position is called *algorithmic agnosticism*: it neither affirms
nor denies that a final theory exists, only that one could never be known to be final.

## Abstract

Physicists have long hoped for a final theory of everything describing how the world really is. We argue that no such theory could be known to be final. We assume nothing about what the world is, only that every observation is a finite record and every usable method for choosing theories is computable. From learning theory and algorithmic information theory, we show three things. First, no method of any kind can certify a theory as final: every finite record fits infinitely many computable theories that disagree about the unobserved. Second, no usable method is guaranteed to settle on a final theory: whatever has been observed, some possible world fits it in which the method never settles on the right theory, or, if it uses chance, settles with arbitrarily small probability. Third, even an agent with unlimited data and computing power cannot separate formulations with identical predictions, or tell apart with certainty chance hypotheses that agree on which events have probability zero. What remains is choice. Simplicity narrows the field: up to a margin set by the reference machine, the data fix which models fit, and universal priors predict best as a class. But candidates that fit almost as well and disagree about the unobserved always survive; choosing among them, by simplicity, beauty or unification, is a constraint we impose. The search for compact, unified theories remains worthwhile, because they make testable predictions. What cannot succeed is the search for one known to be final. We call this position algorithmic agnosticism.

## Repository layout

- `paper/` — LaTeX source (`main.tex`, `sections/`, `refs.bib`) and the compiled PDF
  (`algorithmic-agnosticism.pdf`).
- `research/process.md` — how the paper was produced, including the review rounds and their
  limitations.
- `research/argument-spine.md` — the argument map: every premise, definition and result, with
  its dependencies, from the premises to the conclusion.
- `research/related-work.md` — the literature map from the related-work search.
- `research/abstract-review.md` — the review of the abstract against published guidance and
  venue requirements.

The public history begins at version 1.0. Drafts written before that, including a first draft of about 20,000 words, are not included; `research/process.md` describes how the paper developed through them.

## Building the PDF

```sh
brew install tectonic   # or any LaTeX distribution with natbib, cleveref, booktabs
cd paper
tectonic main.tex
```

## Comments and corrections

Comments, corrections and objections are welcome. Please open an issue on this repository. Reports
of errors in the proofs or in how other authors' work is described are especially useful.

## How to cite

DOI: [10.5281/zenodo.23900493](https://doi.org/10.5281/zenodo.23900493) (all versions; version 1.0 is [10.5281/zenodo.23900494](https://doi.org/10.5281/zenodo.23900494)).

```bibtex
@misc{taylor2026agnosticism,
  author       = {Taylor, Christopher S.},
  title        = {Algorithmic Agnosticism: Why No Theory of Everything Can Be Known to Be Final},
  year         = {2026},
  note         = {Version 1.0, preprint; not peer-reviewed},
  doi          = {10.5281/zenodo.23900493},
  howpublished = {\url{https://github.com/extrafox/algorithmic-agnosticism}}
}
```

## License

The text of this work is licensed under the
[Creative Commons Attribution 4.0 International License](LICENSE) (CC BY 4.0).
