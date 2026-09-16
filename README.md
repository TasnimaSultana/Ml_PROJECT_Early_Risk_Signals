# Ml-Early-Risk-Signals

---

## Team members

* Tasnima Sultana
* Student ID: 20245103058

---

## Problem idea

Many students who go on to fail a course show warning signs weeks before the final
examination — falling attendance, shrinking study time, late submissions. This project
investigates whether those early signals can be used to flag a student as *at risk* while
there is still time for an academic adviser to intervene.

The intended output is a support decision ("who should be contacted for extra help"), not
a grading or gatekeeping decision. The predicted label is binary: pass or fail.

---

## Current dataset status

**Status: teaching sample only. Not research data.**

The notebook in this repository uses a six-row demonstration table (`student`,
`study_hours`, `sleep_hours`, `attendance`, `snacks`, `passed`) that is written inline in
Activity C. It exists to practise Pandas operations and nothing else.

Six samples cannot support any claim about real students. A usable dataset would need:

- several hundred anonymised records across more than one intake and section
- collection with student consent and institutional approval
- a written data dictionary and a stated retention period
- no column that leaks the final result

The `data/` directory is currently empty by design — see `data/README.md`.

---

## How to run the notebook

### Option 1 — Google Colab (recommended)

1. Open <https://colab.research.google.com>.
2. Choose **File → Upload notebook** and select `notebooks/lab01_setup.ipynb`.
3. Choose **Runtime → Run all**.

NumPy and Pandas are pre-installed on Colab, so no setup step is required.

### Option 2 — Local Jupyter

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook notebooks/lab01_setup.ipynb
```

Then choose **Kernel → Restart & Run All**.

### Before submitting

- The notebook is already named `ML_Lab01_20245103058_Tasnima.ipynb` in the submission copy.
- Fill in intake and section in the header table (name and ID are already set).
- Confirm **Run all** completes from a clean kernel with no errors.
- Do not delete output cells to hide errors.

---

## Reproducibility notes

- All imports are kept in one labelled cell near the top.
- The global seed is set once: `SEED = 42`, applied to both `random` and `numpy.random`.
- Package versions are printed by the first code cell so results can be traced later.

One caution documented in Activity D: because a seed is set early in the notebook, calls
that *look* unseeded further down may still be reproducible, since they inherit the
generator state. Reproducibility is a property of the whole notebook, not of one line.

---

## What the notebook covers

| Activity | Content |
|---|---|
| A | Notebook set-up, a deliberate syntax error, its repair and a written explanation |
| B | NumPy: mean, min, standard deviation, non-mutating bonus marks, pass count, 2 × 3 reshape |
| C | Pandas: DataFrame construction, features vs. label, filtering, grouped statistics, sorting, correlation vs. causation |
| D | Reproducibility: seeded vs. unseeded generation and why a fixed split matters for fair comparison |
| E | The seven-stage ML workflow mapped onto this problem |

---

## Limitations

**All results in this repository are preliminary.**

The notebook demonstrates tooling and workflow discipline. It does not contain a trained
model, a held-out evaluation or any validated finding. The correlations visible in the
six-row sample are illustrative only and must not be read as evidence about real students.
No causal claim is made or supported anywhere in this work.
