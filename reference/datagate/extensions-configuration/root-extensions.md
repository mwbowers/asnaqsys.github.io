---
title: RootExtensions class
---

Provides extension methods for accessing ASNA and DataGate configuration sections.

**Namespace:** ASNA.Extensions.Configuration
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
|  | SECTION_ASNA | Constant for the ASNA configuration section. |
|  | SECTION_ASNA_DG | Constant for the DataGate configuration section within the ASNA section. |

## Methods

| Signature | Description |
| --- | --- |
| [GetAsnaConfig](#getasnaconfig-iconfiguration-)([IConfiguration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0)) | Gets the ASNA configuration section from the provided configuration.
| [GetDataGateConfig](#getdatagateconfig-iconfiguration-)([IConfiguration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0)) | Gets the DataGate configuration section from the provided configuration.

### IConfigurationSection GetAsnaConfig([IConfiguration This](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0))

Gets the ASNA configuration section from the provided configuration.

```cs
IConfigurationSection GetAsnaConfig(IConfiguration This)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IConfiguration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0) | This | 

#### Returns

| Type | Description
| --- | ---
| [IConfigurationSection](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfigurationsection?view=net-8.0) | The ASNA configuration section.

### IConfigurationSection GetDataGateConfig([IConfiguration This](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0))

Gets the DataGate configuration section from the provided configuration.

```cs
IConfigurationSection GetDataGateConfig(IConfiguration This)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IConfiguration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0) | This | 

#### Returns

| Type | Description
| --- | ---
| [IConfigurationSection](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfigurationsection?view=net-8.0) | The DataGate configuration section.