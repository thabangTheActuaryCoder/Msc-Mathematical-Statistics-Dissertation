# Review of Dissertation Changes
Date: July 1, 2026

## Summary
This document reviews the changes made to the MSc dissertation based on Dr. Jan Blomerous's feedback.

---

## Files Modified

1. **References.bib**
2. **Thesis/Chapter 2/src/chapter2_litreview.tex**
3. **Thesis/Chapter 4/src/chapter4_results.tex**
4. **Thesis/Chapter 5/src/chapter5_conclusion.tex**

---

## Detailed Changes

### 1. References.bib
**Added Zhang et al. (2021) reference:**
```bibtex
@article{zhang2021understanding,
  author  = {Zhang, Chiyuan and Bengio, Samy and Hardt, Moritz and
             Recht, Benjamin and Vinyals, Oriol},
  title   = {Understanding deep learning (still) requires rethinking
             generalization},
  journal = {Communications of the ACM},
  volume  = {64},
  number  = {3},
  pages   = {107--115},
  year    = {2021},
  publisher = {ACM New York, NY, USA},
  doi     = {10.1145/3446776}
}
```

---

### 2. Chapter 2 - Literature Review
**Location:** Section 2.4 (Deep Neural Networks for Regression)

**Change:** Added citation and discussion of Zhang et al. (2021)

**Before:**
> ...as sample size and feature cardinality \citep{shwartzziv2022tabular}. In the empirical application...

**After:**
> ...as sample size and feature cardinality \citep{shwartzziv2022tabular}.
> Understanding deep learning generalization remains an active research area;
> \citet{zhang2021understanding} demonstrate that conventional statistical
> learning theory, which predicts poor generalization for overparameterized
> models, requires rethinking in the deep learning context where networks with
> more parameters than training examples can still generalize well. In the empirical application...

---

### 3. Chapter 4 - Results

#### Change 3.1: Removed unnumbered heading "Joint distribution validation"
**Location:** Around line 611

**Removed:**
```latex
\subsubsection*{Joint distribution validation}
```

**Result:** Text now flows naturally without the unnumbered heading.

---

#### Change 3.2: Added seed invariance interpretation to Figure discussion
**Location:** Around line 1281-1289

**Added text:**
> This result is invariant of the seed, indicating that the model
> converges to a consistent attribution structure in each case despite
> differences in random initialization.

---

### 4. Chapter 5 - Conclusion

#### Change 4.1: Renamed Section 5.1
**Before:** "Review of the Dissertation"
**After:** "Introduction"

---

#### Change 4.2: Converted Research Question headings
**Changed all 6 Research Questions from:**
```latex
\subsubsection*{Research Question~\ref{rq:1}}
```

**To:**
```latex
\noindent
\textbf{Research Question~\ref{rq:1}:}
```

This makes them formatted text rather than structural headings.

---

#### Change 4.3: Restructured Section 5.6 and created new Section 5.7

**Old Structure:**
- 5.6: "Implications for Actuarial Practice and Statistical Methodology"
  - Had subsubsection "Implications for actuarial practice"
  - Had subsubsection "Implications for statistical methodology"

**New Structure:**
- 5.6: "Implications for Actuarial Practice" (standalone section)
- 5.7: "Implications for Statistical Methodology" (new full section)

**Cascading changes:**
- Old 5.7 → New 5.8 (Comparison with Constrained Neural-Network Approaches)
- Old 5.8 → New 5.9 (Recommendations for Future Research)
- Old 5.9 → New 5.10 (Concluding Remark)

---

#### Change 4.4: Removed redundant subsubsection heading
**Location:** Section 5.6
**Removed:** `\subsubsection*{Implications for actuarial practice}`

The text now flows directly from the section introduction.

---

#### Change 4.5: Removed bold "Interpretability" heading
**Location:** Section 5.8 (old 5.7)
**Removed:**
```latex
\noindent
\textbf{Interpretability.}
```

The text now flows naturally without this heading.

---

#### Change 4.6: Converted subsubsection headings in Section 5.9
**Location:** Section 5.9 (Recommendations for Future Research)

**Changed from:**
```latex
\subsubsection*{Modelling and simulation extensions}
\subsubsection*{Attribution and interpretation extensions}
```

**To:**
```latex
\noindent
\textbf{Modelling and simulation extensions.}

\noindent
\textbf{Attribution and interpretation extensions.}
```

---

## Status of All Requested Changes

| # | Task | Status |
|---|------|--------|
| 1 | Remove unnumbered heading on page 134 | ✅ Completed |
| 2 | Add table descriptions below each table | ⏸️ In Progress |
| 3 | Start Chapter 5.1 with Introduction | ✅ Completed |
| 4 | Convert unnumbered headings to sentences | ✅ Completed |
| 5 | Fix duplicate "Annexure Annexure H" in section 5.4 | ✅ Not Found (may have been fixed already) |
| 6 | Remove redundant heading in section 5.6 | ✅ Completed |
| 7 | Split section 5.6 into 5.6 and 5.7 | ✅ Completed |
| 8 | Remove bold "Interpretability" in section 5.7 | ✅ Completed |
| 9 | Write out in-section headings in 5.8 | ✅ Completed |
| 10 | Add Zhang et al. (2021) reference | ✅ Completed |
| 11 | Add seed invariance result interpretation | ✅ Completed |

---

## Notes

- All changes maintain academic formatting standards
- LaTeX structure preserved throughout
- No content was removed, only reorganized or reformatted
- Table descriptions (Task 2) remains pending as it requires systematic review of all tables in the thesis

---

## Next Steps

1. Review these changes
2. Complete table descriptions if needed
3. Compile LaTeX to verify formatting
4. Submit by Friday as planned
