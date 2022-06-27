##  Question 2

```

function myFunction() {
  var url1 = 'https://covid19.ddc.moph.go.th/api/Cases/today-cases-all';
  var response1 = UrlFetchApp.fetch(url1, { 'muteHttpExceptions': true });
  var json = response1.getContentText();
  const data = JSON.parse(json)[0]
  Logger.log(data);

  var Data1 = data.total_case; 
  var Data2 = data.new_case_excludeabroad;
  var Data3 = data.new_death;
  var Data4 = data.update_date;
  var Data5 = data.txn_date;
  var Data6 = data.new_case;
  var Data7 = data.total_recovered;
  var Data8 = data.total_death;
  var Data9 = data.total_case_excludeabroad;
  var Data10 = data.new_recovered;
  console.log();
}
```
