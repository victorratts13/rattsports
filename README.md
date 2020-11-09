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

## getting time status

for get time status from all games in live, you can use https://api.rattsports.online/v1?call=getGame&method=gameStatus. 

- js
```js
const $.get('https://api.rattsports.online/v1', {"call": "getGame", "method": "gameStatus"}).then((rest) => {
    console.log(rest)
})
```

- php
```php
$content = file_get_contents("https://api.rattsports.online/v1?call=getGame&method=gameStatus");
$jsonData = json_decode($getObj);
var_dump($jsonData);
```

## getting resumed information 
for get a little information of all games you can use https://api.rattsports.online/v1?call=getGame&method=gameInfo.

- js
```js
const $.get('https://api.rattsports.online/v1', {"call": "getGame", "method": "gameInfo"}).then((rest) => {
    console.log(rest)
})
```

- php
```php
$content = file_get_contents("https://api.rattsports.online/v1?call=getGame&method=gameInfo");
$jsonData = json_decode($getObj);
var_dump($jsonData);
```

## getting complete information

for get all information of games, you can use https://api.rattsports.online/v1?call=getGame&method=completeInfo

- js
```js
const $.get('https://api.rattsports.online/v1', {"call": "getGame", "method": "completeInfo"}).then((rest) => {
    console.log(rest)
})
```

- php
```php
$content = file_get_contents("https://api.rattsports.online/v1?call=getGame&method=completeInfo");
$jsonData = json_decode($getObj);
var_dump($jsonData);
```

## getting event information

for get all event from games, you can use https://api.rattsports.online/v1?call=getGame&method=events

- js
```js
const $.get('https://api.rattsports.online/v1', {"call": "getGame", "method": "events"}).then((rest) => {
    console.log(rest)
})
```

- php
```php
$content = file_get_contents("https://api.rattsports.online/v1?call=getGame&method=events");
$jsonData = json_decode($getObj);
var_dump($jsonData);
```

## complementation

all data returns a json in apiRest with solicited information, if you like more details, you can send email for suporte@rattsports.online or can contact me on telegram: @victorRatts


