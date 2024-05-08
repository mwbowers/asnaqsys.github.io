---
title: ReadSequentialMode enum
---

Enum representing the mode of reading values in a sequential manner.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| Current | Represents a state where the current value is read in the sequence. | 3 |
| First | Represents a state where the first value is read in the sequence. | 5 |
| Last | Represents a state where the last value is read in the sequence. | 6 |
| Next | Represents a state where the next value is read in the sequence. | 1 |
| Previous | Represents a state where the previous value is read in the sequence. | 2 |

## Examples

The follwing code examples demonstrate how to use the `ReadSequentialMode` enumeration.

```cs 
  AdgConnection db = new AdgConnection("*Public/DG NET iSeries");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.ReadWrite; 
  AdgDataSet myDS = null;

  dbFile.OpenNewAdgDataSet(out myDS);
  /* We read the first customer for this file (customer number 100)-
   * the record is represented in myDS's active row property. */
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read);

  /* We read the next customer for this file (customer number 200). */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);

  /* We read the last record in the file (should be customer number 100000). */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Last, LockRequest.Read);

  /* We read the previous record (which gives us customer number 99900).
   * We also lock the record. */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Previous, LockRequest.Write);

  /* We unlock the record so that other users can view or update it. */
  dbFile.ReleaseCurrent();

  /* ... Some time passes... */

  /* We lock the current record by reading it again. */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Current, LockRequest.Write);

  /* Close this file and open a different one. */
  dbFile.Close();
  dbFile.FileName = "*Libl/CSMASTERL1";
  dbFile.MemberName = "CSMASTERL1";

  dbFile.OpenNewAdgDataSet(out myDS);

  /* We read randomly to find the record for customer number 500.
   * In this file, several records may have that customer number. */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCSMastL1"); //New file, so reinstantiate key table.
  keyTbl.Row["CSCustNo"] = 500;
  keyTbl.KeyPartCount = 1;
  dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Read, keyTbl);

  /* Now we get customer number 80000 by setting the file pointer to
   * just past it and then reading backwards once. */
  keyTbl.Row["CSCUSTNO"] = 80000;
  dbFile.SeekKey(SeekMode.SetGT, keyTbl);
  dbFile.ReadSequential(myDS, ReadSequentialMode.Previous, LockRequest.Read);
  
```