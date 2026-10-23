---
title: "constants"
weight: 20
description: "Planned, wave 2: the CODATA 2022 recommended values of the physical constants."
---

<!-- From go-scikit/roadmap, bib/systems-units-formats-visualization.md, sections 1b, 2c, 3b, 4, 5 and 6, and PLAN.md item 9. Change it there first. -->

**Status: planned (wave 2). No code exists.** The package name is provisional.

## What it will provide

- The CODATA 2022 recommended values: exact for h, e, k and N_A, and with their
  uncertainties, and the correlations, for the others.
- A Go table generated from NIST's ASCII file by a reproducible tool in the
  repository, which records the edition. CODATA changes every four years, so
  the edition is data, not folklore.

## References

| Subject | Reference |
| --- | --- |
| the values | Mohr, Newell, Taylor and Tiesinga, Rev. Mod. Phys. 97 (2025), the [CODATA recommended values](https://physics.nist.gov/cuu/Constants/) |
| the data source | NIST's [ASCII table of the constants](https://physics.nist.gov/cuu/Constants/Table/allascii.txt), public domain |
| the SI | BIPM, [The International System of Units (SI Brochure)](https://www.bipm.org/en/publications/si-brochure) |

## How it will be validated

| Area | Criterion |
| --- | --- |
| the table | a table diff against NIST's `allascii.txt` |
| conversion factors | within 1 ulp of the CODATA decimal |

SciPy's `scipy.constants` (BSD-3-Clause) and astropy's `astropy.constants` are
the oracles. Every item also needs unit tests at 100% coverage and a
performance table against the reference.
