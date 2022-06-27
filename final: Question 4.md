## Question 4
```

var ACCESS_TOKEN = "8K0Egq1m+jhO+GAy85YS7HIz1HLuYyK5XEyGGHwazgjcHvPDZ4sv9m9fNWKy6WiP0c9YIWVCCRfZCvDGB+tgNjBrd7yyzJXVP2fGiBOtmSZo0URRxPb3+R0txWkW/J6c4ugBUTktAVc/MGGo7ArgfgdB04t89/1O/w1cDnyilFU=";

function broadcast() {
  UrlFetchApp.fetch('https://api.line.me/v2/bot/message/broadcast', {
    method: 'post',
    headers: {
      'Content-Type': 'application/json',
      'Authorization': 'Bearer ' + ACCESS_TOKEN,
    },
    payload: JSON.stringify({
      messages: [

        {
          "type": "flex",
          "altText": "ประกาศ",
          "contents": {
            "type": "carousel",
            "contents": [


              //ใส่ JSON ข้อความที่ออกแบบ

              {
                "type": "bubble",
                "direction": "ltr",
                "header": {
                  "type": "box",
                  "layout": "vertical",
                  "backgroundColor": "#325CACFF",
                  "contents": [
                    {
                      "type": "text",
                      "text": "Header",
                      "align": "center",
                      "color": "#FFFFFFFF",
                      "contents": []
                    }
                  ]
                },
                "body": {
                  "type": "box",
                  "layout": "vertical",
                  "contents": [
                    {
                      "type": "text",
                      "text": "Body",
                      "align": "center",
                      "contents": []
                    },
                    {
                      "type": "text",
                      "text": "Body",
                      "align": "center",
                      "contents": []
                    }
                  ]
                }
              }

              //วางถึงตรงนี้   
            ]
          }
        }

      ]
    }),
  });
}

```
