---
title: "go-units documentation"
linkTitle: "Home"
type: docs
cascade:
  type: docs
description: "Units and physical constants in pure Go (CGO=0). Planned, wave 2 of the go-scikit roadmap: no library exists yet."
---

**go-units is planned.** It is the organisation the
[go-scikit parity plan](https://github.com/go-scikit/roadmap/blob/main/PLAN.md)
names for what MATLAB's `symunit` and `physconst` and Mathematica's `Quantity`
offer. No library exists, no code is written and nothing is released: these
pages say what the organisation will cover, in which wave, and what each part
will be validated against.

## Scope

Quantities with exact dimensions, conversion between units (including offset
units such as degC and degF), dimensional analysis, and the CODATA physical
constants. Dates and time scales are out of scope: they belong to go-datetime.
None of the existing Go unit packages is a dimensional-analysis engine (they are
typed floats, byte-size parsers or conversion tables), so none is a dependency.

## Plan

| Item in the plan | What | Wave |
| --- | --- | --- |
| 9 | go-units, together with go-sciio (size S for go-units) | 2 |
| 21 | user-defined unit systems: EMU, ESU and atomic units (size S) | 4 |

The plan is [PLAN.md](https://github.com/go-scikit/roadmap/blob/main/PLAN.md);
where each item stands is [STATUS.md](https://github.com/go-scikit/roadmap/blob/main/STATUS.md).
The facts behind the scope, the references and the validation measures are in
the roadmap's
[bibliography](https://github.com/go-scikit/roadmap/blob/main/bib/systems-units-formats-visualization.md).

## The planned packages

The names are provisional.

| Package | Status | What it will provide |
| --- | --- | --- |
| [units]({{< relref "units" >}}) | planned (wave 2) | dimension vectors, quantities, conversion, the UDUNITS grammar, dimensional analysis |
| [constants]({{< relref "constants" >}}) | planned (wave 2) | the CODATA 2022 recommended values |

## Status

Nothing is released, so there is nothing to install. When a package is released
its page becomes the package's own documentation, and this site's version label
follows the newest release, as in the other go-scikit organisations.
