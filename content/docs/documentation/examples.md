---
weight: 8
bookFlatSection: false
title: "Examples"
type: docs
---

# Examples

## Quantities

```python
from misura.quantities import quantity
import math
import numpy

num1 = quantity(7, "m s-1", 1)
num2 = quantity(4, "km")
num3 = numpy.array([quantity(2, "m", .5), quantity(4, "km", .1)])
num4 = quantity(numpy.array([1, 2, 3]), "T")

print(num1.unit(print=True))
print(num1.dimension())
print(num1 * 3)
print(num2 ** 2 < 16)
print(math.trunc(numpy.sum(num3)))
print(num4)
```

The output is:

```
m / s
[length / time]
21 ± 3 m / s
False
4002 ± 100 m
[1 2 3] T
```

## Units of measure

```python
from misura.quantities import quantity, convert
fromm misura.tables import addUnit

addUnit("volume", {"L": 1, "daL": 10, "hL": 100, "kL": 1000, "dL": 0.1, "cL": 0.01, "mL": 0.001}, "dm3")

num1 = quantity(3, "L")

print(convert(num1, "cm3"))
```

The output is:

```
3000.0 cm(3)
```

## Currencies

```python
from misura.currencies import currency

cur1 = currency(3, "USD")

print(convert(cur1, "EUR"))
```

The output is:

```
2.74 EUR
```

## Conversions, unpacking and packing

```python
from misura.quantities import quantity, convert, unpack, pack

num1 = quantity(2, "m2")
num2 = quantity(4, "kg")
num3 = quantity(2, "J2")
num4 = quantity(4, "C H")
num5 = quantity(7, "N m")
num6 = quantity(9, "J")
num7 = quantity(45, "A2 s2")

print(convert(num1, "cm2"))
print(num2 + quantity(5, "g"))
print(unpack(num3))
print(unpack(num4, "H"))
print(num5 + num6)
print(pack(num7, "C", full=True))
```

The output is:

```
20000.0 cm(2)
4.005 kg
2.0 kg(2) m(4) / s(4)
4.0 C kg m(2) / A(2) s(2)
16.0 J
45.0 C(2)
```

## Global options

```python
from misura.quantities import quantity
from misura.globals import style

style.quantityHighlighting = False
style.quantityPlusMinus = " +- "

num1 = quantity(2, "m s-1")
num2 = quantity(5, "s", 1)

print(num1)
print(num2)
```

The output is:

```
2 [m / s]
5 +- 1 [s]
```
