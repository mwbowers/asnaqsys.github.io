---
title: RangeMode enum
---

Enum representing the mode of a range.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| First | Represents a state where the first item is selected in the range. | 5 |
| Last | Represents a state where the last item is selected in the range. | 6 |

## Examples


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
      MessageBox.Show("Error opening file! " + dgEx.Message, "Error");
      //Exit procedure or end application here.
  }

  /* We read all records with a customer number greater
   * than, but not equal to 6000 and less than or equal
   * to, 7000. */
  AdgKeyTable OneKey = myDS.NewKeyTable("RCMMastL1");
  OneKey.Row["CMCustNo"] = 10000;
  AdgKeyTable TwoKey = myDS.NewKeyTable("RCMMastL1");
  TwoKey.Row["CMCustNo"] = 40000;

  try
  {
      dbFile.ReadRange(myDS, RangeMode.First, 
      LockRequest.Read, OneKey, 
      RangeFirst.Exclude, TwoKey,
      RangeLast.Include);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error getting records 10000-40000 :" +
          dgEx.Message, "Error");
      //Exit procedure or end application here.
  }

  int totalSum = 0;
  int activeSum = 0;
  bool EOF = false;
  while(!EOF)
  {
      try
      {
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait);
          if (Convert.ToChar(myDS.ActiveRow["CMActive"]) == '1')
              activeSum ++;
          totalSum ++;
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
              EOF = true;
          else
          {
              //Exit procedure or end application here.
          }
      }
  }
  if (totalSum &gt; 0)
  {
      string percent = Convert.ToString((Convert.ToDecimal(activeSum)
          /Convert.ToDecimal(totalSum)) * 100);
      percent = percent.Substring(0, percent.IndexOf('.'));
      MessageBox.Show(percent + "% of the customers sampled are active.");
  }
  else
      MessageBox.Show("Unable to access any customers!");
  dbFile.Close();
  db.Close(); 
```
