# Standings

## Get Standings

```json
{
    "standings": [{
                    "competitionId": 7,
                    "seasonNum": 14,
                    "stageNum": 1,
                    "displayName": "Premier League",
                    "header": [{
                                "key": "gamesPlayed",
                                "name": "P",
                                "isMajor": true
                            },
                            {
                                "key": "gamesWon",
                                "name": "W",
                                "isMajor": false
                            },
                            {
                                "key": "gamesEven",
                                "name": "D",
                                "isMajor": false
                            },
                            {
                                "key": "gamesLost",
                                "name": "L",
                                "isMajor": false
                            },
                            {
                                "key": "goals",
                                "name": "F:A",
                                "isMajor": true
                            },
                            {
                                "key": "ratio",
                                "name": "+/-",
                                "isMajor": true
                            },
                            {
                                "key": "points",
                                "name": "PTS",
                                "isMajor": true
                            },
                            {
                                "key": "form",
                                "name": "Form",
                                "isMajor": false
                            }],
                    "rows":[{
                                "competitor":{
                                                "id": 131,
                                                "name": "Real Madrid",
                                                "nameForURL": "real-madrid",
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
                                "destinationId": 1,
                                "destinationGuaranteed": true,
                                "isWinner": true
                            }]
                    }],
    
    "countries":[{
                     "id": 1,
                     "name": "Argentina",
                     "nameForURL": "argentina"
                     

                }],
    "competitions": [{
                    "id": 7,
                    "countryId": 1,
                    "sportId": 1,
                    "name": "Premier League",
                    "nameForURL": "premier-league",
                    "hasStandings": true
                }],
    "sports":[{
                    "id": 1,
                    "name": "Football",
                    "nameForURL": "football"
             }]
}
```

Return competition standings.

### Entities map 

Object | Usage | Description | Example
--------- | ------- | --------- | -----
standing | Standings | Object | object with rows, header and destinations
header | Standings | Standing's columns | [See Example](#header)
rows | Standings | Standing's rows | [See Example](#rows)
destinations | Standings | Standing's rows - position destination | [See Example](#destinations)

### HTTP Request

`GET https://ws.365scores.com/web/standings`

### Query Parameters

Parameter | required | Default | Example | Options | Description
--------- | ------- | ----------- | --- | ----- | ---------
competitions | false | '' | 12 | | Return Standing for each competition 
competitor | false | '' | 132 | | Return all Standing for specific competitor
lastUpdateId | false | '' | 848293001 | | Return only updated properties from the current lastUpdateId 

### Examples

competitions Standings

`GET https://ws.365scores.com/web/standings/?competitions=12,13,123`

competitors Standings

`GET https://ws.365scores.com/web/standings/?competitor=131`


<aside class="notice">
Don't forget general parameters.
</aside>
