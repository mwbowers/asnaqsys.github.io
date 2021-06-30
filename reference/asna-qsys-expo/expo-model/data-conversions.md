---
title: DataConversions class
---

Provides Data Conversion support

**Assembly:** ASNA.QSys.Expo.Model

<br>
<br>

## Remarks

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=net-5.0) | DecimalToMemUnits | Gets a string value representing the given numeric value after formatting according to the field definition | the converted value as string
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=net-5.0) | DecimalToMemUnitsSigned | Gets a string value the given numeric value after formating according to the signed field definition | the units signed value as a string
| Decimal | MemUnitsToDecimal | Gets a decimal value given a numeric value in a string after formating according to field definition | the units converted to decimal
| Decimal | FixateDecimal | Gets a decimal value given the input value after rounding or truncating according to field definition. | the decimal value as fixed number
| Decimal | MapToPacked | Gets a decimal value representing a Packed value as defined by IBM i | the packed value
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=net-5.0) | MapFromPacked | Gets a string value from a Packed numeric value | the un-packed value as a string

<br>
<br>
