---
title: "units"
weight: 10
description: "Planned, wave 2: quantities with exact dimensions, conversion and dimensional analysis."
---

<!-- From go-scikit/roadmap, bib/systems-units-formats-visualization.md, sections 1b, 2c, 3b, 4 and 5, bib/maple.md, and PLAN.md items 9 and 21. Change it there first. -->

**Status: planned (wave 2). No code exists.** The package name is provisional.

## What it will provide

- A dimension vector of seven rational exponents, with a scale factor and an
  offset; the offset only for degC and degF.
- Quantities and conversion between compatible units.
- A parser for the UDUNITS grammar, which the CF conventions of NetCDF use, and
  a database of SI, US customary and derived units.
- Dimensional analysis: compatibility checks and Buckingham's pi theorem, from
  the null space of the exponent matrix.
- In wave 4 (item 21), user-defined unit systems such as EMU, ESU and atomic
  units, as Maple's `Units` package offers.

## References

| Subject | Reference |
| --- | --- |
| the SI | BIPM, [The International System of Units (SI Brochure)](https://www.bipm.org/en/publications/si-brochure), 9th ed., normative |
| unit grammar and database | [UDUNITS-2](https://www.unidata.ucar.edu/software/udunits/); the licence is BSD-3-Clause text plus a patent-termination clause, to be read before the database is copied |
| unified codes | [UCUM](https://ucum.org/ucum), case-sensitive, used in health data |
| dimensional analysis | Buckingham, Phys. Rev. 4 (1914) 345, [doi:10.1103/PhysRev.4.345](https://doi.org/10.1103/PhysRev.4.345) |
| representation | Hart, *Multidimensional Analysis*, Springer 1995, [doi:10.1007/978-1-4612-4208-6](https://doi.org/10.1007/978-1-4612-4208-6) |

## How it will be validated

| Area | Criterion |
| --- | --- |
| dimensions | exact rational dimension vectors |
| conversion | factors within 1 ulp of the decimal value in the references; a table diff against NIST SP 811 |

Oracles and references: [pint](https://github.com/hgrecco/pint) (its definitions
file is data that may be ported), astropy's `astropy.units`, and UDUNITS-2
itself. The corpus is NIST
[Special Publication 811](https://www.nist.gov/pml/special-publication-811) and
pint's test suite. Every item also needs unit tests at 100% coverage and a
performance table against the reference.
