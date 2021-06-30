---
title: ConditionalProperty class
---

Defines a ConditionalProperty

**Assembly:** ASNA.QSys.Expo.Model

<br>
<br>

## Remarks

<br>
<br>

## Constructors

| Name |  | Description |
| --- | --- | --- |
**ConditionalProperty** | (  ) | Initializes a new instance of ConditionalProperty class


| Name |  | Description |
| --- | --- | --- |
**ConditionalProperty** | ( [Expo.Model.ConditionalValue[]](/reference/asna-qsys-expo/expo-model/conditional-value.html) Property ) | Initializes a new instance of ConditionalProperty class to the ConditionalValue collection given.


| Parameter | Type | Description
| --- | --- | ---
| Property | [Expo.Model.ConditionalValue[]](/reference/asna-qsys-expo/expo-model/conditional-value.html) | Initial ConditionalValue collection 

| Name |  | Description |
| --- | --- | --- |
**ConditionalProperty** | ( [String](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=net-5.0) propString ) | Initializes a new instance of ConditionalProperty class by de-serializing the given collection in the form of a string


| Parameter | Type | Description
| --- | --- | ---
| propString | [String](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=net-5.0) | Serializes initial ConditionalValue collection 


<br>
<br>

## Properties

| Type | Name | Description | Accesor
| --- | --- | --- | --- 
| [Expo.Model.ConditionalValue[]](/reference/asna-qsys-expo/expo-model/conditional-value.html) | Property | Gets or sets the ConditionalValue collection encapsulated by the Property | 
| Boolean | IsGiven | Gets a boolean value indicating if the ConditionalValue collection is NOT empty | 

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=net-5.0) | ToString | Serializes the ConditionalValue collection into a string. | the serialize string
| void | Reset | Clears the encapsulated ConditionalValue collection | 

<br>
<br>
