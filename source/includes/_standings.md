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
                                "liveData": {
                                      "isLive": true,
                                      "homeScore": 2,
                                      "awayScore": 1,
                                      "gameStatus": 2
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
                                "detailedRecentForm" :[{
                                    "id": 1,
                                    "statusGroup": 1,
                                    "statusText": "Extra time",
                                    "shortStatusText": "ET",
                                    "gameTime": 109,
                                    "gameTimeDisplay": "109'",
                                    "gameTimeAndStatusDisplayType": 1,
                                    "isFutureGame": false,
                                    "lineupsStatus": 1,
                                    "hasTVNetworks": false,
                                    "hasBetsTeaser": false,
                                    "hasFieldPositions": true,
                                    "hasLineups": true,
                                    "description": "Barcelona has won 5-3 after Penalties",
                                    "aggregatedText": "aggregated 4-2",
                                    "displayTitle": "Semi Final",
                                    "sportId": 1,
                                    "competitionId": 1,
                                    "roundNum": 3,
                                    "seasonNum": 6,
                                    "stageNum": 4,
                                    "startTime": "2018-12-06T17:15:00+02:00",
                                    "homeCompetitor": {
                                        "id": 1,
                                        "name": "Argentina",
                                        "score": 2,
                                        "aggregatedScore": 4,
                                        "isQualified": false,
                                        "isWinner": false,
                                        "redCards": 0,
                                        "countryId": 11,
                                        "imgVer": 1
                                    },
                                    "awayCompetitor": {
                                        "id": 2,
                                        "name": "Brazil",
                                        "score": 0,
                                        "aggregatedScore": 2,
                                        "isQualified": false,
                                        "isWinner": false,
                                        "redCards": 1,
                                        "countryId": 12,
                                        "imgVer": 1
                                    }
                                }],
                                "recentForm": [1, 2, 0, 1, 2],
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
                    "hasStandings": true,
                    "hasStandingGroups": true,
                }],
    "sports":[{
                    "id": 1,
                    "name": "Football",
                    "nameForURL": "football"
             }],
    "games": [{
                    "id": 2034294,
                    "sportId": 1,
                    "competitionId": 4,
                    "seasonNum": 8,
                    "stageNum": 1,
                    "roundNum": 35,
                    "competitionDisplayName": "National League",
                    "startTime": "2020-02-18T21:45:00+02:00",
                    "statusGroup": 3,
                    "statusText": "Halftime",
                    "gameTimeAndStatusDisplayType": 1,
                    "gameTime": 45,
                    "gameTimeDisplay": "45'",
                    "hasLineups": true,
                    "hasFieldPositions": true,
                    "hasTVNetworks": false,
                    "homeCompetitor": {
                    "id": 69,
                    "countryId": 1,
                    "sportId": 1,
                    "name": "Barnet",
                    "score": 1,
                    "aggregatedScore": -1,
                    "isQualified": false,
                    "isWinner": false,
                    "redCards": 0,
                    "nameForURL": "barnet",
                    "type": 1
                    },
                    "awayCompetitor": {
                    "id": 10026,
                    "countryId": 1,
                    "sportId": 1,
                    "name": "Harrogate Town",
                    "score": 1,
                    "aggregatedScore": -1,
                    "isQualified": false,
                    "isWinner": false,
                    "redCards": 0,
                    "nameForURL": "harrogate-town",
                    "type": 1
                    }
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
