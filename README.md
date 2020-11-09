![logo](https://github.com/victorratts13/rattsports/blob/main/asset/img/ratts.jpg?raw=true)
![api](https://img.shields.io/badge/API-v1-green) ![env](https://img.shields.io/badge/env-json-yellowgreen)

# introduction

this is a open api rest for live soccer games for bet365&copy;, betfair&copy;, 1xbet&copy; and more. You can get data in json format for your use for you personal project. 
You can access https://rattsports.online for see live games implementation and can access the api endpoint in https://api.rattsports.online/v1.

## getting games

for get all games without previous filter, access https://api.rattsports.online/v1?call=getall

- js
```js
const $.get('https://api.rattsports.online/v1', {"call": "getall"}).then((rest) => {
    console.log(rest)
})
```

- php
```php
$content = file_get_contents("https://api.rattsports.online/v1?call=getall");
$jsonData = json_decode($getObj);
var_dump($jsonData);
```
