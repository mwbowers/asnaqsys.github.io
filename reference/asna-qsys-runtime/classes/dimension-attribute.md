---
title: DimensionAttribute Class
---

A non-RPG class, property or field may be stamped with this attribute to indicate a consumer RPG program to consider it as an array with the specified dimension.

**Namespace:** ASNA.QSys.Runtime <br/>
**Assembly:** ASNA.QSys.Runtime

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) --> DimensionAttribute

<br>
<br>

## Remarks

A non-RPG class, property or field may be stamped with this attribute to indicate a consumer RPG program to consider it as an array with the specified dimension.

[//]: # ($$TODO: Complete the Remarks section.)

<br>
<br>

## Constructor

| Name |  Description 
| --- | --- 
| **DimensionAttribute**( [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) ) | Initializes a DimensionAttribute object. Describes the item as a fixed-size array with the specified dimensions.

<br>

### DimensionAttribute( [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) )

Initializes a DimensionAttribute object. Describes the item as a fixed-size array with the specified dimensions.

```cs
DimensionAttribute( Int32 dimNumber, Int32 count );
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | dimNumber | The dimension number. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | count | The count of elements in the dimension. 

<br>


<br>
<br>

## Properties

| Type | Name | Description | Indexer
| --- | --- | --- | --- 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Count | Gets the count of elements in the dimension. | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | DimNumber | Gets the dimension number. | 

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Equals](https://docs.microsoft.com/en-us/dotnet/api/system.object.equals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if the specified object is equal to the current object; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Finalize](https://docs.microsoft.com/en-us/dotnet/api/system.object.finalize)() | Allows an object to try to free resources and perform other cleanup operations before it is reclaimed by garbage collection.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | 
| [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) | [GetCustomAttribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute.getcustomattribute)([Assembly](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.assembly), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Retrieves a custom attribute applied to a specified assembly. Parameters specify the assembly and the type of the custom attribute to search for.<br>(Inherited from [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)) | 
| [Attribute[]](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) | [GetCustomAttributes](https://docs.microsoft.com/en-us/dotnet/api/system.attribute.getcustomattributes)([Assembly]($$TODO-Assembly.html)) | Retrieves an array of the custom attributes applied to an assembly. A parameter specifies the assembly.<br>(Inherited from [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)) | An Attribute array that contains the custom attributes applied to element, or an empty array if no such custom attributes exist.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [GetHashCode](https://docs.microsoft.com/en-us/dotnet/api/system.object.gethashcode)() | Serves as the default hash function.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A hash code for the current object.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | [GetType](https://docs.microsoft.com/en-us/dotnet/api/system.object.gettype)() | Gets the Type of the current instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | The exact runtime type of the current instance.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [IsDefined](https://docs.microsoft.com/en-us/dotnet/api/system.attribute.isdefined)([Assembly]($$TODO-Assembly.html), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Determines whether any custom attributes are applied to an assembly. Parameters specify the assembly, and the type of the custom attribute to search for.<br>(Inherited from [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)) | true if a custom attribute of type attributeType is applied to element; otherwise, false.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Match](https://docs.microsoft.com/en-us/dotnet/api/system.attribute.match)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | When overridden in a derived class, returns a value that indicates whether this instance equals a specified object.<br>(Inherited from [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)) | An Object to compare with this instance of Attribute.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | [MemberwiseClone](https://docs.microsoft.com/en-us/dotnet/api/system.object.memberwiseclone)() | Creates a shallow copy of the current Object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A shallow copy of the current Object.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ReferenceEquals](https://docs.microsoft.com/en-us/dotnet/api/system.object.referenceequals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified Object instances are the same instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if objA is the same instance as objB or if both are null; otherwise, false.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ToString](https://docs.microsoft.com/en-us/dotnet/api/system.object.tostring)() | Returns a string that represents the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A string that represents the current object.

<br>
<br>
