---
title: IndicatorExpression class
---

A condition is an ANDed grouping of two through nine indicators that
must all be in effect (set off if N or ! is specified; set on if N
or ! is not specified) before the field or keyword is selected. You can
specify a maximum of nine indicators for each condition and nine
conditions for each field or keyword. You can also specify several
conditions for a field or keyword so that if any one of them is
satisfied, the field or the keyword is selected. This is called an OR
relationship
example: 1 & 2 & !3 | 44 & 55 | 60

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [IndicatorExpression](#indicatorexpression-string-)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the indicator expression.

### IndicatorExpression([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Sets the indicator expression.

```cs
IndicatorExpression(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | expressionString | 

## Methods

| Signature | Description |
| --- | --- |
| [Eval](#eval-char-)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Evaluates the expression using the indicator values passed in.

### bool Eval([Char\[\] indicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Evaluates the expression using the indicator values passed in.

```cs
bool Eval(Char[] indicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | indicators | 

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | The result after evaluaating the expression.