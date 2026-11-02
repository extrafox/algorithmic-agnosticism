# Citation locator and quotation check (AA)

Run 2026-11-02. Sources were fetched from open copies and treated as untrusted. "Applied" means a locator was inserted into the existing `\citep`/`\citet` command. refs.bib is unchanged.

## Locators

| Citation (location) | Status | Locator | Source used | URL |
|---|---|---|---|---|
| deleeuw1956 (02, thm:q-powerless) | VERIFIED, applied | Thms. 2–3 | Thm. 2: for computable p, a p-enumerable or strongly p-enumerable set (enumerated with nonzero probability) is 1-enumerable. Thm. 3: for computable p, a p-computable sequence (each output correct with probability > 1/2) is computable. Checked in the OCR of the Shannon *Collected Papers* reprint, pp. 749–752. The original pages are probably 190–193 (not verified). | https://archive.org/details/claude-shannon-collected-papers |
| pitt1989 (04, rem:randomized, p > 1/2) | VERIFIED, applied | Thm. 3.21 with n = 1 | Thm. 3.21: if 1/(n+1) < p ≤ 1 then EX_prob(p) ⊆ EX_team(n). The n = 1 case is restated after Cor. 3.30 (p. 413). Checked in the JACM PDF, Wayback copy. | https://doi.org/10.1145/62044.62053 |
| pitt1989 (04, probability ↔ teams) | VERIFIED, applied | Thm. 3.36 | Thm. 3.36: if 1/(n+1) < p ≤ 1/n then ID_prob(p) = ID_freq(p) = ID_team(n). Same source. | https://doi.org/10.1145/62044.62053 |
| smith1982 (04) | VERIFIED, applied | Thm. 3.1 | Thm. 3.1 is the team hierarchy, which generalizes the Blum–Blum nonunion theorem (p. 1149). The claim that REC is not finite-team identifiable is a consequence; Smith does not state it as a numbered result. Checked in the JACM PDF, Wayback copy. | https://doi.org/10.1145/322344.322356 |
| pitt-smith1988 (04) | NOT FOUND | none | The full text was unreachable. The zbMATH reviews give no theorem numbers. | https://doi.org/10.1016/0890-5401(88)90046-6 |
| kakutani1948 (06) | NOT FOUND | none | No open source gives a theorem number. German Wikipedia cites pp. 217–218. One arXiv paper (Mejak, 2204.02767) cites the Bernoulli case as "Corollary 1" of Kakutani. Neither was confirmed against the original. | https://doi.org/10.2307/1969123 |
| vitanyi-li2000 (08) | NOT FOUND (IEEE version) | none | In the arXiv preprint this is Thm. 4 in §2.5 "Ideal MDL and Bayesianism", which rests on Thm. 3 (§2.4). The numbering of the IEEE version was not confirmed, so no locator was added. | https://arxiv.org/abs/cs/9901014 |
| kelly2007 (08) | NOT FOUND (TCS version) | none | In the 2007 preprint, §5 has Prop. 1 (Ockham + stalwart ⇒ efficient), Prop. 2 (the converse) and Cor. 1. The published numbering was not confirmed. | https://doi.org/10.1016/j.tcs.2007.04.009 |
| genin-kelly2019 (08) | NOT FOUND (Studia Logica version) | none | Only a differently titled preprint was found; §9 there has Props. 9.1–9.3. Low confidence that this matches the published paper. | https://doi.org/10.1007/s11225-018-9809-5 |
| kolmogorov1965 (05, invariance) | VERIFIED, applied | §3 | §3, "An Algorithmic Approach", contains the unnumbered "Fundamental theorem" (K_A(y/x) ≤ K_φ(y/x) + C_φ). Checked in the English translation (Problems Inform. Transmission). | http://alexander.shen.free.fr/library/Kolmogorov65_Three-Approaches-to-Information.pdf |
| li-vitanyi2019 (05, invariance) | NOT FOUND (4th ed.) | none | The invariance theorem is Thm. 2.1.1 in the 2nd and 3rd editions. The Springer preview of the 4th edition stops before §2.1, so the number was not confirmed there. | https://doi.org/10.1007/978-3-030-11298-1 |
| li-vitanyi2019 (07, Ch. 4) | VERIFIED (existing) | Ch. 4 | Ch. 4 is "Algorithmic Probability", pp. 261–343 (Crossref). | https://doi.org/10.1007/978-3-030-11298-1_4 |
| rogers1967 (03, ch. 1 padding) | VERIFIED (existing) | ch. 1 | §1.8, Thm. 1-III: "Each partial recursive function has ℵ₀ distinct indices." Checked in archive.org full-text snippets. | https://archive.org/details/theoryofrecursiv0000hart |
| rogers1967 (04, ch. 9 relativization) | VERIFIED (existing) | ch. 9 | Ch. 9 is "Turing Reducibility; Hypersimple Sets". It contains §9.2 "Relative Recursiveness" (p. 128) and §9.3 "Relativized Theory" (p. 134). | https://archive.org/details/theoryofrecursiv0000hart |

## Quotations

| Quotation (location) | Status | Source used | URL |
|---|---|---|---|
| Deutsch, "there can be no such thing as an ultimate explanation" (08, ch. 3) | VERIFIED | *The Beginning of Infinity*, ch. 3 "The Spark" (p. 64 per Glattfelder 2019). Matches the Google Books snippet word for word: "...if only because there can be no such thing as an ultimate explanation: just as 'the gods did it' is always a bad explanation...". | https://books.google.com/books?id=jZHanN5_KPgC |
| Deutsch, hard to vary (08, ch. 1, paraphrase) | VERIFIED | Ch. 1 "The Reach of Explanations": "explanations that are hard to vary in the sense that changing the details would ruin the explanation". "Not a matter of taste" is our paraphrase and is not in quotation marks. | https://archive.org/details/the-beginning-of-infinity-explanations-that-transform-the-world-david-deutsch |
| Sklar, "transient" (08, objection 3) | VERIFIED, locator p. 380 added | Sklar himself uses "transient underdetermination" (Google Books snippet of Phil. Rev. 84). Three citing sources (Mind 1990; Seidel 2014; Voosholz 2025) place it at pp. 380–1, and SEP agrees. Page 380 was not viewed directly. | https://plato.stanford.edu/entries/scientific-underdetermination/ |
