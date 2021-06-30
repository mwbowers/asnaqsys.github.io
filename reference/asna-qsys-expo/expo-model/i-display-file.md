---
title: IDisplayFile interface
---

Exposes DisplayFile properties and methods

**Assembly:** ASNA.QSys.Expo.Model

<br>
<br>

## Remarks

<br>
<br>

## Properties

| Type | Name | Description | Accesor
| --- | --- | --- | --- 
| void | DataSet | Gets the DisplayFile DataSet | 
| void | FeedbackAID | Gets a value that indicates the AID code sent in last user request | 
| void | FeedbackCursor | Gets a value that indicates Cursor (row, column) corresponding to the last location last user input (Hi byte is the row, Lo-byte is the column) | 
| void | FeedbackField | Gets a value that indicates the name of the last Field where the Cursor was positioned, corresponding to the last location last user input | 
| void | FeedbackFlags | Gets a value that indicates Miscelaneous feedback flags. Bit 1: Cancel-read indicator. Bit 2: Data-returned indicator. Bit 3: Command key indicator. Bits 4-16: Reserved. | 
| void | FeedbackLowestSubfile | Gets a value that indicates the indicates the lowest subfile relative record number currently displayed in the uppermost subfile display area if the last write operation was done to the subfile control record with 'Subfile Display' specified. Updated for roll up and roll down operations. Reset to 0 on a write operation to another record. Not set for message subfiles | 
| void | LastFormatNameWritten | Gets a value that indicates the name of the last Record Format written | 
| void | DisplayErrorMessages | Gets a boolean value that indicates if the Error Messages should be displayed | 
| void | PageName | Gets a value that indicates the Name of the Page (URL) | 
| void | InstanceId | Gets a value that indicates the Unique Page instance ID | 
| void | FeedbackActiveWindowCursor | If a Window Record is active, this property gets or sets a value that indicates Cursor (row, column) corresponding to the last location last user input (Hi byte is the row, Lo-byte is the column) | 
| void | FeedbackSubfileCursorRRN | Gets or sets a value that indicates Relative Record Number of a subfile record.  For input operations, updated only if data is returned to the program. If multiple subfiles are on the display, this offset will contain the relative record number for the last subfile updated. | 

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32?view=net-5.0) | GetTopRecordOnInput | Gets the Subfile Top Relative Record Number in the last input operation | the relative record number at the top
| void | SetTopRecordOnInput | Sets the Subfile Top Relative Record Number for the last input operation | 
| Boolean | SetOneTimeDefaultValue | Marks a field as one that has had a Default value (internal use) | true the field was not marked as having a Default value
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32?view=net-5.0) | AddCallHostSpecs | Will throw NonImplemented exception | throws exception

<br>
<br>
