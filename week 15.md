1. Create a Function

```
function myFunction() {

}
```

2. Connected to google sheets 

```
  var sheetId = " your google sheets id";
  var currentSheet = SpreadsheetApp.openById(sheetId).getSheetByName("Sheet name");
```

3. Create variable and data

```
  var name = "teeraphong";
```

4. console.log

```
  console.log("Name :" + name)
```

5. Create alert box 

```
  var result = SpreadsheetApp.getUi().alert("Your name : " + name);
  
```
```
  var result = SpreadsheetApp.getUi().alert("Your name : " + name, SpreadsheetApp.getUi().ButtonSet.OK_CANCEL);
```
6. Show alert result

```
  SpreadsheetApp.getActive().toast(result);
  
```
7. if, else

```
if (result == "OK") {
do something 
}else {
do something 
  }
```

8. getLastRow

```
  var lastRow = currentSheet.getLastRow();
  
```
9. setValue

```
  currentSheet.getRange(lastRow + 1, 1).setValue(name);
```
