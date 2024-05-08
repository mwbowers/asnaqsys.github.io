---
title: dgException class
---

Custom Exceptions thrown by DataGate.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)
<br>
<br>
## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.


## Constructors

| Name | Description |
| --- | --- |
| [dgException()](#dgexception-) | Default constructor.
| [dgException](#dgexception-string-)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructor that takes a message as input.
| [dgException](#dgexception-string-exception-)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Constructor that takes a message as input and inner exception.
| [dgException](#dgexception-dgerrornumber-int32-dgerrorclass-string-string-exception-)([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Create a dgException with the passed error code, system error code,error class, and text.  This dgException is constructed and thrownwhen the database server program returns an error.
| [dgException](#dgexception-dgerrornumber-int32-dgerrorclass-string-string-)([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Create a dgException with the passed error code, system error code,error class, and text.  This dgException is constructed and thrownwhen the database server program returns an error.
| [dgException](#dgexception-dgerrornumber-)([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html)) | Create a dgException with the passed error code.
| [dgException](#dgexception-dgerrornumber-exception-)([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Create a dgException with the passed error code and exception.

### dgException()

Default constructor.

```cs
dgException()
```

### dgException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructor that takes a message as input.

```cs
dgException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | 

### dgException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Constructor that takes a message as input and inner exception.

```cs
dgException(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | 
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | inner | 

### dgException([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Create a dgException with the passed error code, system error code,error class, and text.  This dgException is constructed and thrownwhen the database server program returns an error.

```cs
dgException(dgErrorNumber, Int32, dgErrorClass, String, String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html) | error | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | systemError | 
| [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html) | errorClass | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | text | 
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | inner | 

### dgException([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Create a dgException with the passed error code, system error code,error class, and text.  This dgException is constructed and thrownwhen the database server program returns an error.

```cs
dgException(dgErrorNumber, Int32, dgErrorClass, String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html) | error | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | systemError | 
| [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html) | errorClass | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | text | 

### dgException([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html))

Create a dgException with the passed error code.

```cs
dgException(dgErrorNumber)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html) | error | 

### dgException([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Create a dgException with the passed error code and exception.

```cs
dgException(dgErrorNumber, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html) | error | 
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | e | 

## Properties

| Type | Name | Description
| --- | --- | --- 
| [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html) | DefaultErrorClass | Gets the default error class. |
| [dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html) | Error | The error code for this dgException. For server side errors, thisis the error code returned by the server following a databasetransaction. |
| [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html) | ErrorClass | The class of error for this dgException. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Message | Get the error message. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | SystemError | The system error code, if any for this dgException. This memberwill contain meaningful information only with the value ofErrorClass is one of the following: |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Text | The text message of this dgException. |

## Methods

| Signature | Description |
| --- | --- |
| [FormatMessage](#formatmessage-iformatprovider-string-)([IFormatProvider](https://learn.microsoft.com/en-us/dotnet/api/system.iformatprovider?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the error message.
| [GetDefaultErrorClass](#getdefaulterrorclass-dgerrornumber-)([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html)) | Each dgErrorNumber has a default associated dgErrorClass.  Thismethod returns it.
| [GetObjectData](#getobjectdata-serializationinfo-streamingcontext-)([SerializationInfo](https://learn.microsoft.com/en-us/dotnet/api/system.runtime.serialization.serializationinfo?view=net-8.0), [StreamingContext](https://learn.microsoft.com/en-us/dotnet/api/system.runtime.serialization.streamingcontext?view=net-8.0)) | Gets the object data.
| [GetVerboseText()](#getverbosetext-) | Return a string containing a verbose description of thedgException. This string will most likely contain line separatorcharacters.  All dgException member variables are included in thestring.

### string FormatMessage([IFormatProvider provider](https://learn.microsoft.com/en-us/dotnet/api/system.iformatprovider?view=net-8.0), [string msg](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the error message.

```cs
string FormatMessage(IFormatProvider provider, string msg)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IFormatProvider](https://learn.microsoft.com/en-us/dotnet/api/system.iformatprovider?view=net-8.0) | provider | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | msg | 

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | 

### dgErrorClass GetDefaultErrorClass([dgErrorNumber err](/reference/datagate/datagate-common/dg-error-number.html))

Each dgErrorNumber has a default associated dgErrorClass.  Thismethod returns it.

```cs
dgErrorClass GetDefaultErrorClass(dgErrorNumber err)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html) |  | 

#### Returns

| Type | Description
| --- | ---
| [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html) | 

### void GetObjectData([SerializationInfo info](https://learn.microsoft.com/en-us/dotnet/api/system.runtime.serialization.serializationinfo?view=net-8.0), [StreamingContext context](https://learn.microsoft.com/en-us/dotnet/api/system.runtime.serialization.streamingcontext?view=net-8.0))

Gets the object data.

```cs
void GetObjectData(SerializationInfo info, StreamingContext context)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SerializationInfo](https://learn.microsoft.com/en-us/dotnet/api/system.runtime.serialization.serializationinfo?view=net-8.0) | info | 
| [StreamingContext](https://learn.microsoft.com/en-us/dotnet/api/system.runtime.serialization.streamingcontext?view=net-8.0) | context | 

### string GetVerboseText()

Return a string containing a verbose description of thedgException. This string will most likely contain line separatorcharacters.  All dgException member variables are included in thestring.

```cs
string GetVerboseText()
```

### Example 1. dgException ErrorClass and SystemError properties example.

```cs 
  /* This code attempts to open a file exclusively. 
  * If it fails, we print out the IBM i exception responsible.
  * "dbFile" is of type FileAdapter. */ 
  dbFile.AccessMode = AccessMode.Write;
  dbFile.OpenAttributes.ShareTypes = ShareTypes.Exclusive;
  dbFile.OpenAttributes.WaitForFile = 0;

  AdgDataSet dataSet = null;
  try
  {
      dbFile.Open(dataSet);
  }
  catch(dgException dgEx)
  {
      /* Take special action if error is due to the IBM i exception
       * "CPF1002". */
      if (dgEx.ErrorClass == dgErrorClass.dgEC_AS400CPF &amp;&amp;
          dgEx.SystemError.ToString("X") == "1002")
      {
          MessageBox.Show("iSeries threw exception CPF1002.");
          // Take alternative action here.
      }
      else
      {
          /* Throw exception otherwise. */
          throw dgEx;
      }
  }
```

### Example 2. dgException Message property example.


```cs 
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      /* This will show a somewhat specific message as to what 
       * went wrong opening the file. */
      MessageBox.Show(dgEx.Message, "Error opening file");
      //Exit procedure here.
  }
```

## Example 3. GetVerboseText method example.

```cs 
  /* Verbose text generates a large string which is a concatanation 
   * of several of dgException's properties and also shows the
   * stack trace. While not very user friendly, it can come in handy
   * developing a program. */
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read ;

  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* We retrieve the record for customer number 7800. */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");
  keyTbl.Row["CMCUSTNO"] = 7800;
  try
  {
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Write, keyTbl);
      myDS.ActiveRow["CMCUSTNO"] = 300;
      dbFile.ChangeCurrent(myDS);
  }
  catch(dgException dgEx)
  { /* Print out Verbose text to figure out why ReadRandomKey is
     * throwing an exception. */
      MessageBox.Show(dgEx.GetVerboseText(), "Datagate Exception");
  }

  dbFile.Close();
  db.Close();
```

## Example 4. dgErrorNumber property example.


```cs 
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMMASTERL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      /* There are many reasons why opening a file can fail. Here, we
       * catch some of the more general ones. */
      if (dgEx.Error == dgErrorNumber.dgEmMNOTFND)
          MessageBox.Show("Member " + dbFile.MemberName + " not found!", "Error opening file");
      else if (dgEx.Error == dgErrorNumber.dgEmFNOTFND)
          MessageBox.Show("File " + dbFile.FileName + " not found!", "Error opening file");
      else
          MessageBox.Show(dgEx.Message, "Error opening file");
          //Exit procedure here.
  }

  /* Do some action here. */

  dbFile.Close();
  db.Close();
```

