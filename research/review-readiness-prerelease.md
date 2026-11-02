# Readiness review: AA, pre-release draft (rubric: mind-of-god/research/readiness-rubric.md)

Run 2026-11-02 by eight independent Claude agents (four per paper), read-only. Gate: FAIL (A, B, C below 3).

| Crit | Score | Key evidence / fix |
|---|---|---|
| A1–A9 | 2,1,1,1,2,3,2,2,2 → **A=1** | Overclaims: abstract/intro/conclusion C′ wording ("data fix which models fit", "fit almost as well"); 04:60 K(f)≤K(L)+O(1) should be K(L,R); 04:160 lem:bias proof wording; 06:46 "only stochastic models"; 08:14 falsificationism; 08:51 Stanford; 08:116 Hossenfelder; 08:133 "cannot be evidence" → "cannot certify". ~20 deletable sentences; duplicates (Sterkenburg ×3, Hossenfelder ×3, Popper ×3, dualities ×2, "our world" ×2, §2 chain paragraph). Rhetoric 08:24, 08:126, 08:130. |
| B1–B9 | 2,1,1,2,1,2,0,2,2 | S1: "known" standard (known ⇒ certified by record) unstated; add premise or align title/abstract. S4: premises lack "Refuted by"; no self-application of P2. S5: active (query-choosing) methods not covered. 02:234 vs 07:58 (C′ uses P2). |
| C1–C6 | 1,2,2,2,–,– | S2: near-tie claim does not follow from Thm 5.3(iii) (cost ≈ K_U(e), not the gap; log n vs constant conflated). S3: "stochastic model" = measure vs index. T2 proved for total methods only; Cor 4.3 needs dovetailing. Locators missing for several citations/quotes; putnam1975 DOI is 1979 ed.; kolmogorov1965 unchecked. |
| D1–D8 | 3,2,2,2,2,2,3,2 | Forward refs (Remark 2.7, §2.3 table); T4/T5 order; step names not in theorem titles; abstract terms undefined; Wolfram bib entry; `\today`. |
| E1–E8 | 2,3,1,2,2,1,–,2 | E3: British spellings throughout (behaviour ×9, etc.). E6: §2.3 table not a captioned float. Bibliography underfull boxes. AI statement over-discusses author. |
| F1–F5 | 1,1,2,2,1 | Missing: Kiefer 2024 (IJTP, doi:10.1007/s10773-024-05574-2) states the conclusion; Schmidhuber 2000; Hutter 2010's own finality caveat; Belot 2013, Martins 2017 (own related-work.md recommends). Contribution (v) to narrow. No research/lit record. Numeric citations (rubric: author–year). |
| G1–G6 | 2,3,2,2,2,1 | PDF AI statement still says "history of every version" is available (false since flatten); "every entry checked" overstated. No GitHub release (Zenodo needs one); repo description says v1.0. No licence line in PDF. |
| H1–H4 | 1,1,0,3(preprint) | No logic referee or trace audit after v1.1 edits; no cross-model review; raw outputs not saved. |
