# Tables

## Get Tables

```json
{
   "header": [{
                 "key": "gamesPlayed",
                 "name": "P",
                 "major": true
             },
             {
                 "key": "gamesWon",
                 "name": "W",
                 "major": false
             },
             {
                 "key": "gamesEven",
                 "name": "D",
                 "major": false
             },
             {
                 "key": "gamesLost",
                 "name": "L",
                 "major": false
             },
             {
                 "key": "goals",
                 "name": "F:A",
                 "major": true
             },
             {
                 "key": "ratio",
                 "name": "+/-",
                 "major": true
             },
             {
                 "key": "points",
                 "name": "PTS",
                 "major": true
             },
             {
                 "key": "form",
                 "name": "Form",
                 "major": false
             }],
   "data":   [{
                "rows":[{
                            "competitor":{
                                            "id": 131,
                                            "name": "Real Madrid",
                                            "countryId": 1,
                                            "sportId": 1
                                         },
                            "group": {
                                        "id":1,
                                        "name": "Group A"
                                     },
                            "gamesPlayed": 3,
                            "gamesWon": 3,
                            "gamesLost": 3,
                            "gamesEven": 1,
                            "for": 26,
                            "against": 9,
                            "ratio": 17,
                            "points": 19,
                            "strike": -1,
                            "gamesOverTime": 0,
                            "gamesWonOnOverTime": 0,
                            "gamesWonOnPenalties": 0,
                            "gamesLossOnOverTime": 0,
                            "gamesLossOnPenalties": 0,
                            "position": 1,
                            "trend": 0,
                            "recentForm": [0,1,2,2,1],
                            "destinationId": 1
                        }]
             }],
    "destinations": [{
                          "id": 1,
                          "name": "Champions League",
                          "color": "#ff0000",
                          "type": 1
                     }],
    "countries":[{
                     "id": 1,
                     "name": "Argentina"
                }],
    "sports":[{
                    "id": 1,
                    "name": "Football"
             }]
}
```

Return league standings.

### HTTP Request

`GET https://api.365scores.com/table`

### Query Parameters

Parameter | required | Default | Example | Options | Description
--------- | ------- | ----------- | --- | ----- | ---------
leagueIds | false | '' | 12 | | Return table for each league 
competitorId | false | '' | 132 | | Return all table for specific competitor
lastUpdateId | false | '' | 848293001 | | Return only updated properties from the current lastUpdateId 

### Examples

leagues tables

`GET https://api.365scores.com/table?leagueIds=12,13,123`

competitors tables

`GET https://api.365scores.com/table?competitorId=131`


<aside class="notice">
Don't forget general parameters.
</aside>
