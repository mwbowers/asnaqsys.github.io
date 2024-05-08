---
title: ISourceProvider interface
---

Defines a contract for a source provider.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** [ICancelerProvider](https://learn.microsoft.com/en-us/dotnet/api/), [IDisposable](https://learn.microsoft.com/en-us/dotnet/api/system.idisposable?view=net-8.0)
<br>
<br>

## Remarks
A source provider is responsible for managing the connection to a data source.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [IChannelSecurity](/reference/datagate/datagate-client/i-channel-security.html) | ChannelSecurity | Gets the channel security for the connection. |
| [DatabaseAttributes](/reference/datagate/datagate-providers/database-attributes.html) | DatabaseAttributes | Gets the database attributes. |
| [Decoder](https://learn.microsoft.com/en-us/dotnet/api/system.text.decoder?view=net-8.0) | Decoder | Gets the decoder for the connection. |
| [Encoder](https://learn.microsoft.com/en-us/dotnet/api/system.text.encoder?view=net-8.0) | Encoder | Gets the encoder for the connection. |
| [TimeSpan](https://learn.microsoft.com/en-us/dotnet/api/system.timespan?view=net-8.0) | IdleTime | Gets or sets the idle time. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsOpen | Gets a value indicating whether the connection is open. |
| [OpenOptions](/reference/datagate/datagate-providers/open-options.html) | OpenOptions | Gets the open options for the connection. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ServerUser | Gets the server user of the connection. |
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | SourceProfile | Gets the source profile of the connection. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | SupportsMultiMember | Gets a value indicating whether the source provider supports multi-member files. |

## Methods

| Signature | Description |
| --- | --- |
| [ChangeCurrentLibl](#changecurrentlibl-string-)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Changes the current library list.
| [Close()](#close-) | Closes the connection.
| [Commit](#commit-string-)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Commits the transaction.
| [EndTransaction()](#endtransaction-) | Ends the transaction.
| [MakeFileDataProvider](#makefiledataprovider-ifileobject-string-accessmode-fileopenattr-adgdataset-)([IFileObject](/reference/datagate/datagate-client/i-file-object.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AccessMode](/reference/datagate/datagate-common/access-mode.html), [FileOpenAttr](/reference/datagate/datagate-providers/file-open-attr.html), [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)) | Makes a file data provider.
| [Open](#open-sourceprofile-cancellationtoken-)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0)) | Opens a connection to the specified database.
| [Open](#open-sourceprofile-iexchange5250-openaccessrpg-openoptions-string-cancellationtoken-)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [IExchange5250](/reference/datagate/datagate-providers/i-exchange5250.html), [OpenAccessRpg](/reference/datagate/datagate-data-link/open-access-rpg.html), [OpenOptions](/reference/datagate/datagate-providers/open-options.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0)) | Opens a connection to the specified database with additional options.
| [PostOpenInit](#postopeninit-adgconnection-)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Performs post-open initialization.
| [ResetConnection()](#resetconnection-) | Resets the connection.
| [Rollback()](#rollback-) | Rolls back the transaction.
| [SetCanceler](#setcanceler-cancellationtoken-)([CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0)) | Sets the cancellation token.
| [StartTransaction](#starttransaction-transactionlevel-transactionattributes-string-string-)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html), [TransactionAttributes](/reference/datagate/datagate-providers/transaction-attributes.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Starts a transaction.

### void ChangeCurrentLibl([String\[\] newLibl](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Changes the current library list.

```cs
void ChangeCurrentLibl(String[] newLibl)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newLibl | 

### void Close()

Closes the connection.

```cs
void Close()
```

### void Commit([string transactionName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Commits the transaction.

```cs
void Commit(string transactionName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | transactionName | 

### void EndTransaction()

Ends the transaction.

```cs
void EndTransaction()
```

### IFileData MakeFileDataProvider([IFileObject file](/reference/datagate/datagate-client/i-file-object.html), [string memberName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AccessMode mode](/reference/datagate/datagate-common/access-mode.html), [FileOpenAttr openAttr](/reference/datagate/datagate-providers/file-open-attr.html), [AdgDataSet& ds](/reference/datagate/datagate-client/adg-data-set.html))

Makes a file data provider.

```cs
IFileData MakeFileDataProvider(IFileObject file, string memberName, AccessMode mode, FileOpenAttr openAttr, AdgDataSet& ds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IFileObject](/reference/datagate/datagate-client/i-file-object.html) | file | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | memberName | 
| [AccessMode](/reference/datagate/datagate-common/access-mode.html) | mode | 
| [FileOpenAttr](/reference/datagate/datagate-providers/file-open-attr.html) | openAttr | 
| [AdgDataSet&](/reference/datagate/datagate-client/adg-data-set.html) | ds | 

#### Returns

| Type | Description
| --- | ---
| [IFileData](https://learn.microsoft.com/en-us/dotnet/api/) | The file data provider.

### void Open([SourceProfile dbName](/reference/datagate/datagate-providers/source-profile.html), [CancellationToken ct](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0))

Opens a connection to the specified database.

```cs
void Open(SourceProfile dbName, CancellationToken ct)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | dbName | 
| [CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0) | ct | 

### void Open([SourceProfile dbName](/reference/datagate/datagate-providers/source-profile.html), [CancellationToken ct](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0))

Opens a connection to the specified database with additional options.

```cs
void Open(SourceProfile dbName, CancellationToken ct)
```

### void PostOpenInit([AdgConnection cn](/reference/datagate/datagate-client/adg-connection.html))

Performs post-open initialization.

```cs
void PostOpenInit(AdgConnection cn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | 

### bool ResetConnection()

Resets the connection.

```cs
bool ResetConnection()
```

### void Rollback()

Rolls back the transaction.

```cs
void Rollback()
```

### void SetCanceler([CancellationToken token](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0))

Sets the cancellation token.

```cs
void SetCanceler(CancellationToken token)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0) | token | 

### void StartTransaction([TransactionLevel level](/reference/datagate/datagate-common/transaction-level.html), [TransactionAttributes attr](/reference/datagate/datagate-providers/transaction-attributes.html), [string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string options](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Starts a transaction.

```cs
void StartTransaction(TransactionLevel level, TransactionAttributes attr, string name, string options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TransactionLevel](/reference/datagate/datagate-common/transaction-level.html) | level | 
| [TransactionAttributes](/reference/datagate/datagate-providers/transaction-attributes.html) | attr | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | options | 