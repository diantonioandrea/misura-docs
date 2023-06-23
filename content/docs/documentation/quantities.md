---
weight: 2
bookFlatSection: false
title: "Quantities"
type: docs
---

# Quantities

Quantities are defined as `quantities.quantity(value: any, unit: str = "", uncertainty: any = 0)` objects.

`values` stands for the value of the quantity itself, while `unit` represents its unit of measure.  
`quantity(2, "kg")` is a well-defined quantity.

`unit` is a string in which the different units of measure must be _separated by a space_ and _followed by their exponent_, if different from `1`.  
`quantity(3, "m s-1")` is a well-defined quantity.

`uncertainty` stands for the quantity's uncertainty.  
`quantity(3, "s", 0.5)` is a well-defined quantity.

## Methods

`quantities.quantity` objects implement the following methods:

```python
def unit(self, print: bool = False) -> str
def dimension(self) -> str
```

which:

- `unit()`: Returns the units string of the quantity. It returns it in a fancier way if `print = True`.
- `dimension()`: Returns the dimension string of the quantity if it is convertible.

## Operations

`quantities.quantity` objects implement the following dunder methods:

```python
def __str__(self) -> str
def __repr__(self) -> str
def __format__(self, string) -> str

def __int__(self) -> int
def __float__(self) -> float
def __complex__(self) -> complex
def __bool__(self) -> bool

def __abs__(self) -> any
def __pos__(self) -> any
def __neg__(self) -> any
def __round__(self, number: int) -> any
def __floor__(self, number: int) -> any
def __ceil__(self, number: int) -> any
def __trunc__(self, number: int) -> any

def __add__(self, other: any) -> any
def __sub__(self, other: any) -> any
def __mul__(self, other: any) -> any
def __truediv__(self, other: any) -> any
def __floordiv__(self, other: any) -> any
def __pow__(self, other: any) -> any
def __mod__(self, other: any) -> any

def __lt__(self, other: any) -> any
def __le__(self, other: any) -> any
def __gt__(self, other: any) -> any
def __ge__(self, other: any) -> any
def __eq__(self, other: any) -> any
def __ne__(self, other: any) -> any
```

For a quantity to be well-defined, `value` should implement all of the methods in this list which will be called during the execution of the program.