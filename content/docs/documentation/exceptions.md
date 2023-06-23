---
weight: 7
bookFlatSection: false
title: "Exceptions"
type: docs
---

# Exceptions

**misura** implements the following exceptions:

- `InitError`: raised on invalid quantity definition.
- `UnitError`: raised on invalid `unit`.
- `QuantityError`: raised on operations between incompatible quantities.
- `ConversionError`: raised on errors during conversions.
- `UnpackError`: raised on errors during unpacking.
- `PackError`: raised on errors during packing.
- `UncertaintyComparisonError`: raised on comparing quantities with uncertainty.
- `DefinitionError`: raised on errors during unit definition.
- `OperationError`: raised on illegal operations with currencies.
- `CurrencyPackingError`: raised on (un)packing currencies.
- `MixingError`: raised on mixing quantities and currencies.