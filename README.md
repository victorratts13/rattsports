![logo](https://github.com/victorratts13/rattsports/blob/main/asset/img/ratts.jpg?raw=true)
![api](https://img.shields.io/badge/API-v1-green) ![env](https://img.shields.io/badge/env-json-yellowgreen)

# introduction

the ratts api was developed to meet the need for systems to consume an open sports api. It consists of fetching data from bet365 & copy; and use metrics to create simple statistics.

The complete system returns data such as:

- team information
- live matches
- pre-games
- historic
- alloys
- goals
- corners
- events in games
- statistical metrics

# api
api flames can be made through the endpoint `` https: // rattsports.online / api``, the flames are processed in real time by vercel servers, where rattsports is hosted, making a triangulation for the bet365 & copy website ;
See the main call endpoints below.
## getting all data (getall)

to obtain all data without previous formatting, the endpoint `` https: //rattsports.online/api? call = getall`` can be used.
that returns:
``` json
{
    "id": "818212",
    "league": {
        "i": "2949",
        "zc": "0",
        "jc": "0",
        "bd": "0",
        "n": "SYR D2",
        "fn": "Syria Division 2",
        "ls": "S",
        "sbn": "",
        "stn": "",
        "ci": "64",
        "cn": "Syria",
        "cs": "X"
    },
    "host": {
        "i": "34226",
        "n": "Al Tadamon Latakia",
        "sbn": "",
        "stn": ""
    },
    "guest": {
        "i": "42115",
        "n": "Efrin",
        "sbn": "",
        "stn": ""
    },
    "heh": 1,
    "lvc": 0,
    "rcn": 0,
    "zhanyi": "0",
    "sd": {
        "f": {
            "hrf": "+1.75",
            "hdx": "3.0",
            "hcb": null
        },
        "H": {
            "hrf": "+0.75",
            "hdx": "1.25",
            "hcb": null
        }
    },
    "rtime": "2021/02/18 20:00",
    "events": [],
    "events_graph": {
        "events": [],
        "ml": 0,
        "status": 0
    },
    "ss": "",
    "status": "NS",
    "f_ld": {
        "hrf": "+1.75",
        "hrfsp": "2,000",
        "grfsp": "1,800",
        "rft": "2",
        "rf": [
            {
                "hrf": "+1.75",
                "hrfsp": "2,000",
                "grfsp": "1,800",
                "rft": "2",
                "ps": "0"
            },
            {
                "hrf": "+1.75",
                "hrfsp": "1,950",
                "grfsp": "1,850",
                "rft": "100",
                "ps": "0"
            }
        ],
        "hdx": "3.0",
        "hdxsp": "1,800",
        "gdxsp": "2,000",
        "dxt": "100",
        "dx": [
            {
                "hdx": "3.0",
                "hdxsp": "1,800",
                "gdxsp": "2,000",
                "dxt": "100",
                "ps": "0"
            }
        ]
    }
}

```




## getting game status (getGameStatus)

to get basic information about game status and leagues, the endpoint `` https: //rattsports.online/api? call = getGameStatus`` can be used.
that returns:

``` json
{
    "id": "818278",
    "league": "Egypt Division 2",
    "shortname": "EGY D2",
    "game": "El Alameen v Kima Aswan",
    "timestatus": "2021/02/18 20:30",
    "timestart": "0:00",
    "country": "Egypt",
    timestamp: 1613649963143,
    "utc": "Thu, 18 Feb 2021 12:06:03 GMT",
    "callback": "success"
}
```

## getting data from a live game (getGameByEvent)

for complete information about a live game, the endpoint `` https://rattsports.online/api?call=getGameByEvent&id= [id_from_event] '' can be used. Where the `` id_from_event`` can be obtained through the `` getGameStatus`` method
that returns:

``` json
{
    "id": "818264",
    "league": {
        "id": "2465",
        "shortname": "IRN U23",
        "name": "Iran U23 League",
        "country": "Iran",
        "countryId": "74"
    },
    "game": "Sepahan Isfahan U23 v Mes Rafsanjan U23",
    "host": {
        "id": "37571",
        "name": "Sepahan Isfahan U23",
        "goals": "1",
        "redcards": "1",
        "yellowcard": "0",
        "corners": "1"
    },
    "guest": {
        "id": "30090",
        "name": "Mes Rafsanjan U23",
        "goals": "1",
        "redcards": "3",
        "yellowcard": "0",
        "corners": "1"
    },
    "handevent": 1,
    "livecorner": 0,
    "gamestats": {
        "ftime": {
            "corners": null,
            "handcap": "2.5",
            "handcapstats": "-0.75"
        },
        "htime": {
            "corners": null,
            "handcap": "1.0",
            "handcapstats": "-0.25"
        }
    },
    "allcornerstats": null,
    "events": [
        {
            "type": "gyc",
            "description": "79 '- 4th Yellow Card - (Mes Rafsanjan U23)"
        },
        {
            "type": "gc",
            "description": "78 '- 2nd Corner - Mes Rafsanjan U23"
        },
        {
            "type": "gyc",
            "description": "69 '- 3rd Yellow Card - (Mes Rafsanjan U23)"
        },
        {
            "type": "hyc",
            "description": "64 '- 2nd Yellow Card - (Sepahan Isfahan U23)"
        },
        {
            "type": "hc",
            "description": "59' - 1st Corner - Sepahan Isfahan U23"
        },
        {
            "type": "gp",
            "description": "50' - 2nd Goal -   (Mes Rafsanjan U23) - Penalty"
        },
        {
            "type": "h",
            "description": "Score After First Half - 1-0"
        },
        {
            "type": "it",
            "description": "First Half Injury Time: 2 Mins"
        },
        {
            "type": "hg",
            "description": "26' - 1st Goal -   (Sepahan Isfahan U23) "
        },
        {
            "type": "gyc",
            "description": "22' - 1st Yellow Card -  (Mes Rafsanjan U23)"
        },
        {
            "type": "cd",
            "description": "Pitch: GOOD"
        },
        {
            "type": "tq",
            "description": "Weather: GOOD"
        }
    ],
    "placegame": [
        {
            "timestatus": "26",
            "type": "hg",
            "content": "26' - 1st Goal -   (Sepahan Isfahan U23) "
        },
        {
            "timestatus": "50",
            "type": "gp",
            "content": "50' - 2nd Goal -   (Mes Rafsanjan U23) - Penalty"
        },
        {
            "timestatus": "59",
            "type": "hc",
            "content": "59' - 1st Corner - Sepahan Isfahan U23"
        },
        {
            "timestatus": "78",
            "type": "gc",
            "content": "78' - 2nd Corner - Mes Rafsanjan U23"
        }
    ],
    "endgame": "90",
    "timegame": 79
}
```

## obtendo tabela dinamica (tablematch)

para obter tabela de jogos, pode ser ultilizado o endpoint ``https://rattsports.online/api?call=tablematch``.
que retorna:

```json
{
    "id": "<a href=\"/play/818213\" class=\"btn btn-sm btn-success\">818213</a>",
    "status": "25Min",
    "game": "Al-Dumair FC v Al-Nabek",
    "league": "Syria Division 2",
    "country": "Syria",
    "lastevent": "25' - 2nd Corner - Al-Dumair FC",
    "winodd": "1.750",
    "steam": "<i class=\"fas fa-circle text-success\"></i>",
    "win": "Al-Dumair FC",
    "nextcorner": "Al-Dumair FC"
}
```

## obtendo ligas (leagues)

para obter o nome das atuais ligas, pode ser ultilizado o endpoint ``https://rattsports.online/api?call=leagues``.
que retorna:

```json
{
    "league": "Iran U23 League"
}
```

# dados e estatisticas

Em qualquer end-point dessa lista, os valores ``language`` e ``region`` podem ser definidos atraves de url-query. Caso não sejam inseridos, os padrões ``language=en`` e ``region=Europe:Berlin`` serão mantidos.

## obtendo lista de esportes (games)

para obter a lista de esportes, pode ser ultilizado o endpoint ``https://rattsports.online/api/sports?call=games``.
que retorna:

```json
{
    "type": "sport",
    "id": 1,
    "name": "Soccer",
    "skill": false
}
```

## obtendo informações de esportes (getsports)

para obter dados detalhados de esportes, pode ser ultilizado o endpoint ``https://rattsports.online/api/selectsport?call=getsports&id=[id_from_sport]``. Onde o ``id_from_sport`` pode ser obtido pelo metodo ``sports?call=games`` 

>- NOTA: caso o id do esporte seja indefinido ou nulo, o valor padrão é definido como 1

que retorna:

```json
{
    "type": "sport",
    "id": 1,
    "name": "Soccer",
    "categ": [
        {
            "type": "realcategory",
            "id": 257,
            "sid": 1,
            "name": "Albania",
            "country": {
                "type": "countrycode",
                "id": 2,
                "simple": "al",
                "full": "Albania",
                "code": "ALB",
                "codeline": "ALB",
                "continent": "Europe",
                "population": 2800000
            },
            "tournaments": [],
            "uniquetournaments": []
        }
    ]
}
```

## obtendo informações de país (bycountry)

para obter dados detalhados de esportes, pode ser ultilizado o endpoint ``https://rattsports.online/api/country?call=bycountry&id=[id_from_country]``. Onde o ``id_from_country`` pode ser obtido pelo metodo ``selectsport?call=getsports`` 

que retorna:

```json
{
  "type": "realcategory",
  "id": 1,
  "sid": 1,
  "name": "England",
  "country": {
    "type": "countrycode",
    "id": 240,
    "simple": "en",
    "full": "England",
    "code": "ENG",
    "codeline": "ENG",
    "continent": "Europe",
    "population": 51500000
  }
}
```

## obtendo informações de país (bycountry)

para obter dados detalhados de ligas, pode ser ultilizado o endpoint ``https://rattsports.online/api/selectleague?call=select&id=[id_from_sport]&placeid=[id_from_country]``. Onde o ``id_from_country`` pode ser obtido pelo metodo ``selectsport?call=getsports`` e o ``id_from_sport`` pode ser obtido pelo metodo ``sports?call=games``

>- NOTA: caso o id do esporte e id do país seja indefinido ou nulo, o valor padrão é definido como 1 

que retorna:

```json
{
    "type": "sport",
    "id": 1,
    "name": "Soccer",
    "categ": [
        {
            "type": "realcategory",
            "id": 1,"sid": 1,
            "name": "England",
            "country": {
                "type": "countrycode",
                "id": 240,
                "simple": "en",
                "full": "England",
                "code": "ENG",
                "codeline": "ENG",
                "continent": "Europe",
                "population": 51500000
            },
            "tournaments": [
                {
                    "seasonid": 77179,
                    "currentseason": 77179,
                    "name": "Premier League",
                    "roundbyround": true
                }
            ],
            "uniquetournaments": {
                "17": {
                    "_doc": "uniquetournament",
                    "_id": 17,
                    "_utid": 17,
                    "_sid": 1,
                    "_rcid": 1,
                    "name": "Premier League",
                    "currentseason": 77179,
                    "friendly": false,
                    "tournamentlevelorder": 1,
                    "_sk": false
                }
            }
        }
    ]
}
```

## complementation

all data returns a json in apiRest with solicited information, if you like more details, you can send email for suporte@rattsports.online or can contact me on telegram: @victorRatts


