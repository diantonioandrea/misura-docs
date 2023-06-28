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

- **AED**	United Arab Emirates Dirham
- **AFN**	Afghan Afghani
- **ALL**	Albanian Lek
- **AMD**	Armenian Dram
- **ANG**	NL Antillean Guilder
- **AOA**	Angolan Kwanza
- **ARS**	Argentine Peso
- **AUD**	Australian Dollar
- **AWG**	Aruban Florin
- **AZN**	Azerbaijani Manat
- **BAM**	Bosnia-Herzegovina Convertible Mark
- **BBD**	Barbadian Dollar
- **BDT**	Bangladeshi Taka
- **BGN**	Bulgarian Lev
- **BHD**	Bahraini Dinar
- **BIF**	Burundian Franc
- **BMD**	Bermudan Dollar
- **BND**	Brunei Dollar
- **BOB**	Bolivian Boliviano
- **BRL**	Brazilian Real
- **BSD**	Bahamian Dollar
- **BTN**	Bhutanese Ngultrum
- **BWP**	Botswanan Pula
- **BYN**	Belarusian ruble
- **BYR**	Belarusian Ruble
- **BZD**	Belize Dollar
- **CAD**	Canadian Dollar
- **CDF**	Congolese Franc
- **CHF**	Swiss Franc
- **CLF**	Unidad de Fomento
- **CLP**	Chilean Peso
- **CNY**	Chinese Yuan
- **COP**	Coombian Peso
- **CRC**	Costa Rican Colón
- **CUC**	Cuban Convertible Peso
- **CUP**	Cuban Peso
- **CVE**	Cape Verdean Escudo
- **CZK**	Czech Republic Koruna
- **DJF**	Djiboutian Franc
- **DKK**	Danish Krone
- **DOP**	Dominican Peso
- **DZD**	Algerian Dinar
- **EGP**	Egyptian Pound
- **ERN**	Eritrean Nakfa
- **ETB**	Ethiopian Birr
- **EUR**	Euro
- **FJD**	Fijian Dollar
- **FKP**	Falkland Islands Pound
- **GBP**	British Pound Sterling
- **GEL**	Georgian Lari
- **GGP**	Guernsey pound
- **GHS**	Ghanaian Cedi
- **GIP**	Gibraltar Pound
- **GMD**	Gambian Dalasi
- **GNF**	Guinean Franc
- **GTQ**	Guatemalan Quetzal
- **GYD**	Guyanaese Dollar
- **HKD**	Hong Kong Dollar
- **HNL**	Honduran Lempira
- **HRK**	Croatian Kuna
- **HTG**	Haitian Gourde
- **HUF**	Hungarian Forint
- **IDR**	Indonesian Rupiah
- **ILS**	Israeli New Sheqel
- **IMP**	Manx pound
- **INR**	Indian Rupee
- **IQD**	Iraqi Dinar
- **IRR**	Iranian Rial
- **ISK**	Icelandic Króna
- **JEP**	Jersey pound
- **JMD**	Jamaican Dollar
- **JOD**	Jordanian Dinar
- **JPY**	Japanese Yen
- **KES**	Kenyan Shilling
- **KGS**	Kyrgystani Som
- **KHR**	Cambodian Riel
- **KMF**	Comorian Franc
- **KPW**	North Korean Won
- **KRW**	South Korean Won
- **KWD**	Kuwaiti Dinar
- **KYD**	Cayman Islands Dollar
- **KZT**	Kazakhstani Tenge
- **LAK**	Laotian Kip
- **LBP**	Lebanese Pound
- **LKR**	Sri Lankan Rupee
- **LRD**	Liberian Dollar
- **LSL**	Lesotho Loti
- **LTL**	Lithuanian Litas
- **LVL**	Latvian Lats
- **LYD**	Libyan Dinar
- **MAD**	Moroccan Dirham
- **MDL**	Moldovan Leu
- **MGA**	Malagasy Ariary
- **MKD**	Macedonian Denar
- **MMK**	Myanma Kyat
- **MNT**	Mongolian Tugrik
- **MOP**	Macanese Pataca
- **MRO**	Mauritanian ouguiya
- **MUR**	Mauritian Rupee
- **MVR**	Maldivian Rufiyaa
- **MWK**	Malawian Kwacha
- **MXN**	Mexican Peso
- **MYR**	Malaysian Ringgit
- **MZN**	Mozambican Metical
- **NAD**	Namibian Dollar
- **NGN**	Nigerian Naira
- **NIO**	Nicaraguan Córdoba
- **NOK**	Norwegian Krone
- **NPR**	Nepalese Rupee
- **NZD**	New Zealand Dollar
- **OMR**	Omani Rial
- **PAB**	Panamanian Balboa
- **PEN**	Peruvian Nuevo Sol
- **PGK**	Papua New Guinean Kina
- **PHP**	Philippine Peso
- **PKR**	Pakistani Rupee
- **PLN**	Polish Zloty
- **PYG**	Paraguayan Guarani
- **QAR**	Qatari Rial
- **RON**	Romanian Leu
- **RSD**	Serbian Dinar
- **RUB**	Russian Ruble
- **RWF**	Rwandan Franc
- **SAR**	Saudi Riyal
- **SBD**	Solomon Islands Dollar
- **SCR**	Seychellois Rupee
- **SDG**	Sudanese Pound
- **SEK**	Swedish Krona
- **SGD**	Singapore Dollar
- **SHP**	Saint Helena Pound
- **SLL**	Sierra Leonean Leone
- **SOS**	Somali Shilling
- **SRD**	Surinamese Dollar
- **STD**	São Tomé and Príncipe dobra
- **SVC**	Salvadoran Colón
- **SYP**	Syrian Pound
- **SZL**	Swazi Lilangeni
- **THB**	Thai Baht
- **TJS**	Tajikistani Somoni
- **TMT**	Turkmenistani Manat
- **TND**	Tunisian Dinar
- **TOP**	Tongan Paʻanga
- **TRY**	Turkish Lira
- **TTD**	Trinidad and Tobago Dollar
- **TWD**	New Taiwan Dollar
- **TZS**	Tanzanian Shilling
- **UAH**	Ukrainian Hryvnia
- **UGX**	Ugandan Shilling
- **USD**	US Dollar
- **UYU**	Uruguayan Peso
- **UZS**	Uzbekistan Som
- **VEF**	Venezuelan Bolívar
- **VND**	Vietnamese Dong
- **VUV**	Vanuatu Vatu
- **WST**	Samoan Tala
- **XAF**	CFA Franc BEAC
- **XAG**	Silver Ounce
- **XAU**	Gold Ounce
- **XCD**	East Caribbean Dollar
- **XDR**	Special drawing rights
- **XOF**	CFA Franc BCEAO
- **XPF**	CFP Franc
- **YER**	Yemeni Rial
- **ZAR**	South African Rand
- **ZMK**	Zambian Kwacha
- **ZMW**	Zambian Kwacha
- **ZWL**	Zimbabwean dollar
- **XPT**	Platinum Ounce
- **XPD**	Palladium Ounce
- **BTC**	Bitcoin
- **ETH**	Ethereum
- **BNB**	Binance
- **XRP**	Ripple
- **SOL**	Solana
- **DOT**	Polkadot
- **AVAX** Avalanche
- **MATIC** Matic Token
- **LTC**	Litecoin
- **ADA**	Cardano

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