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

## Available symbols

**misura** currently supports the following _symbols_:

- **EUR**	Euro
- **USD**	US Dollar
- **JPY**	Japanese Yen
- **BGN**	Bulgarian Lev
- **CZK**	Czech Republic Koruna
- **DKK**	Danish Krone
- **GBP**	British Pound Sterling
- **HUF**	Hungarian Forint
- **PLN**	Polish Zloty
- **RON**	Romanian Leu
- **SEK**	Swedish Krona
- **CHF**	Swiss Franc
- **ISK**	Icelandic Króna
- **NOK**	Norwegian Krone
- **HRK**	Croatian Kuna
- **RUB**	Russian Ruble
- **TRY**	Turkish Lira
- **AUD**	Australian Dollar
- **BRL**	Brazilian Real
- **CAD**	Canadian Dollar
- **CNY**	Chinese Yuan
- **HKD**	Hong Kong Dollar
- **IDR**	Indonesian Rupiah
- **ILS**	Israeli New Sheqel
- **INR**	Indian Rupee
- **KRW**	South Korean Won
- **MXN**	Mexican Peso
- **MYR**	Malaysian Ringgit
- **NZD**	New Zealand Dollar
- **PHP**	Philippine Peso
- **SGD**	Singapore Dollar
- **THB**	Thai Baht
- **ZAR**	South African Rand

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