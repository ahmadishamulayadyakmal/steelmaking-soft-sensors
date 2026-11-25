# Evidence and claim boundary — C05

**Level from the authoritative case card:** A + B

| Level | What may be claimed |
|---|---|
| A | Our own numbers on public data, with our own error bars and checksums |
| B | Method reproduced on an open surrogate; journal plant numbers quoted as external literature only |
| C | Not used anywhere in this portfolio |

This case is **A + B**. Numbers produced from open datasets are our own;
plant numbers quoted from a journal are external literature only.

The exact sentence that must appear in the case report and README:

> "The plant numbers quoted here are from [citation] and were **not**
> independently reproduced. Our model was exercised on [open surrogate /
> digitised figure]; our result is [number], comparable in **method only**, not
> in plant validation."

Digitisation uncertainty must be reported separately from model error. Figures
built from synthetic data must be labelled synthetic in the caption and in
`data/SOURCES.md`.

Source policy: `CASES.md` §1 (link above). Before any figure is generated,
record the dataset and licence in `data/SOURCES.md` in this repository.
