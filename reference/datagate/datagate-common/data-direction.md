---
title: DataDirection enum
---

Enum representing the direction of data flow.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| Input | Represents a state where data is flowing inwards. | 1 |
| InputOutput | Represents a state where data is flowing both inwards and outwards. | 3 |
| None | Represents a state where no data flow is occurring. | 0 |
| Output | Represents a state where data is flowing outwards. | 2 |

## Examples

```cs
   AdgConnection ProdDB = new AdgConnection("*Public/DG NET IBM i");
   char Quit400App = '1';
   string CustName;
   decimal TimeOfDay;

  /* We know that the first two parameters will be for
   * returning values, so we set their DataDirection
   * enumeration types to Output. The third value will
   * be sent in to tell the external program whether or not
   * to quit running, but will not return a value,
   * so we set its DataDirection type to Input. */
  ProgParm[] Parms = new ProgParm[]
  {
      new ProgParm(new ProgParmType("CustName", 0, 
          FieldType.NewChar(40)), DataDirection.Output),
      new ProgParm(new ProgParmType("TimeOfDay", 0, 
          FieldType.NewPacked(6, 0)), ASNA.DataGate.Common.DataDirection.Output),
      new ProgParm(new ProgParmType("Quit400App", 0, 
          FieldType.NewChar(1)), DataDirection.Input)
  };
  As400Program prog = new As400Program(ProdDB, "*Libl/Call400");
  prog.AppendParms(Parms); //Use our parm list defined above.
  //Here, we make sure our variables are passed as the parms in ther parm list.
  prog.ObjectToParm(Quit400App, "Quit400App", new int[]{});
  //Now we execute the call to the As400Program, "Call400".
  prog.Execute();
  //Here, we get the values from the parm list and put them back into our variables.
  CustName = Convert.ToString(prog.ParmToObject(System.Type.GetType("System.String"), 
      "CustName", new int[]{}));
  TimeOfDay = Convert.ToDecimal(prog.ParmToObject(System.Type.GetType("System.Decimal"), 
      "TimeOfDay", new int[]{}));
```