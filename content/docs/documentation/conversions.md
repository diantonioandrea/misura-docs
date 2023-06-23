---
weight: 5
bookFlatSection: false
title: "Conversions, unpacking and packing"
type: docs
---

# Conversions, unpacking and packing

## Conversion

```python
misura.convert(converted: quantity, target: str, partial: bool = False, un_pack: bool = False) -> quantity
```

The function `convert` takes a `quantity` object, converted, a string, `targets`, and two flags: `partial` and `un_pack`.

- `qnt: quantity` is the quantity that needs to be converted.
- `targets: str` is the string of target units, the units that need to be matched after conversion.
- `partial: bool` whether or not the conversion should be partial, e.g. `"m s-1" -> "km s-1"`.
- `un_pack: bool` whether or not to (un)pack derived units during conversion.

## Unpacking

```python
misura.unpack(qnt: quantity, targets: str = "") -> quantity
```

The function `unpack` takes a `quantity` object, qnt and an optional string, `targets`.

- `qnt: quantity` is the quantity that needs to be converted.
- `targets: str = ""` is the string of target units, the derived units that need to be unpacked. If empty, it unpacks every derived unit.

## Packing

```python
misura.pack(qnt: quantity, targets: str, full: bool = False) -> quantity
```

The function `pack` takes a `quantity` object, qnt, two strings, `targets` and `ignore`, and a flag, `full`.

- `qnt: quantity` is the quantity that needs to be converted.
- `targets: str` is the string of target units, the derived units that need to be matched.
- `ignore: str = ""` Due to the fact that `pack` works by first unpacking the units, some units can be manually ignored to enhance the final result.
- `full: bool = False` whether or not to fully pack a unit.

## Shortcuts

The following `quantities.quantity` methods should serve as shortcuts to the `convert`, `unpack` and `pack` functions:

``` python
class quantity:
	...

    def cto(self, targets: str, partial: bool = False, un_pack: bool = True) -> quantity:  # Convert to.
        return convert(self, targets, partial, un_pack)

    def uto(self, targets: str = "") -> quantity:  # Unpack to.
        return unpack(self, targets)

    def pto(self, targets: str, ignore: str = "", full: bool = False) -> quantity:  # Pack to.
        return pack(self, targets, ignore, full)
```