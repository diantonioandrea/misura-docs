---
weight: 3
bookFlatSection: false
title: "Units of measure"
type: docs
---

# Units of measure

## Defaults

**misura** currently supports the following _families_ (physical quantities):

- SI base units:
	- Time, Second, **s**.
	- Length, Metre, **m**.
	- Mass, Kilogram, **kg**.
	- Electric current, Ampere, **A**.
	- Thermodynamic temperature, Kelvin, **K**.
	- Amount of substance, Mole, **mol**.
	- Luminous intensity, Candela, **cd**.
- SI derived units.
	- Plane angle, Radian, **rad**.
	- Solid angle, Steradian, **sr**.
	- Frequency, Hertz, **Hz**.
	- Force, Newton, **N**.
	- Pressure, Pascal, **Pa**.
	- Energy, Joule, **J**.
	- Power, Watt, **W**.
	- Electric charge, Coulomb, **C**.
	- Electric potential, Volt, **V**.
	- Capacitance, Farad, **F**.
	- Resistance, Ohm, **Ω**.
	- Electrical conductance, Siemens, **S**.
	- Magnetic flux, Weber, **Wb**.
	- Magentic flux density, Tesla, **T**.
	- Inductance, Henry, **H**.
	- Luminous flux, Lumen, **lm**.
	- Illuminance, Lux, **lx**.
	- Radionuclide activity, Becquerel, **Bq**.
	- Absorbed dose, Gray, **Gy**.
	- Equivalent dose, Sievert, **Sv**.
	- Catalytic activity, Katal, **kat**.

with the following orders of magnitude:

		q  =  1e-30
		r  =  1e-27
		y  =  1e-24
		z  =  1e-21
		a  =  1e-18
		f  =  1e-15
		p  =  1e-12
		n  =  1e-09
		µ  =  1e-06
		m  =  1e-03
		c  =  1e-02
		d  =  1e-01
		------------
		da =  1e+01
		h  =  1e+02
		k  =  1e+03
		M  =  1e+06
		G  =  1e+09
		T  =  1e+12
		P  =  1e+15
		E  =  1e+18
		Z  =  1e+21
		Y  =  1e+24
		R  =  1e+27
		Q  =  1e+30

## User defined units of measure

``` python
misura.addUnit(family: str, units: dict, unpacks: str = "") -> None
```

The function `addUnit` takes a string `family`, a dictionary `units` and an optional string `unpacks`.

- `family: str` is the family (physical quantity) of the to-be-defined unit of measure.
- `units: dict` is the dictionary of the available symbols for the specified family and it is structured as `{"symbol1": factor1, ..., "symbol": 1, ..., "symbolN": factorN}`.
- `unpacks: str` is the string of the units to which the new unit unpacks, if it does. In this case the new unit becomes a derived unit.

Note that the `units` dictionary must have a **reference unit**, a defining unit for that family, for which its factor is equal to `1`.