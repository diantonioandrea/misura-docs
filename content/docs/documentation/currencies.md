---
weight: 4
bookFlatSection: false
title: "Currencies"
type: docs
---

# Currencies

Quantities are defined as `currencies.currency(value: any, symbol: str = "")` objects, which inherits from `quantities.quantity`.

`values` stands for the value of the currency itself, while `symbol` represents its code.  
`currency(2, "EUR")` is a well-defined currency.

## Rates

Latest currency exchange rates can be found on [misura.diantonioandrea.com](https://misura.diantonioandrea.com/currencies/rates.json).

## Operations

`currencies.currency` objects re-implement the following dunder methods, which are stricter versions:

```python
def __str__(self) -> str
def __repr__(self) -> str
def __format__(self, string) -> str

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
```

For a currency to be well-defined, `value` should implement all of the methods in this list which will be called during the execution of the program.