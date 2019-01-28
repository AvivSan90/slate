# Games

## Get All Games

```json
{
  "lastUpdateId": 987654321,
   "ttl": 10,
   "sport":[{
               "id": 1,
               "name": "Football"
           }],
   "countries":[{
                     "id": 11,
                     "name": "Argentina"
               },
               {
                     "id": 12,
                     "name": "Brazil"
                 }],
   "competitions":[{
                         "id": 1,
                         "name": "World Cup",
                         "hasStanding": true,
                         "countryId": 11,
                         "sportId": 1,
                         "liveGames": 2,
                         "totalGames": 5
                   }],
                   
                                       
   "games": [{
             "id": 1,
             "statusGroup": 1,
             "statusText": "ET",
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
             "sportId": 1,
             "competitionId": 1,
             "roundNum": 3,
             "seasonNum": 6,
             "stageNum": 4,
             "datetime":{
                 "msFromEpoch": 12334423423423,
                 "dateText": "16/07/2018",
                 "timeText": "21:00 AM"
             },
             "homeCompetitor": {
                  "id": 1,
                  "name": "Argentina",
                  "score": 2,
                  "aggregatedScore": 4,
                  "isQualified": false,
                  "isWinner": false,
                  "redCards": 0,
                  "countryId": 11
             },
             "awayCompetitor": {
                  "id": 2,
                  "name": "Brazil",
                  "score": 0,
                  "aggregatedScore": 2,
                  "isQualified": false,
                  "isWinner": false,
                  "redCards": 1,
                  "countryId": 12
             }
       }]
}
```

### Entities map 

Object | Usage | Description | Example
--------- | ------- | ----------- | ---------
game | dashboard, competition scores, team scores (game card) | Game's partial data | [See Example](#full-game)
competitor | team at game card | Competitor critical data | [See Example](#competitor)

Partial object of game 

This endpoint retrieves all games.

Return only partial game data.

### HTTP Request

`GET https://ws.365scores.com/web/games`

### Query Parameters

Parameter | required | Default | Example | Options | Description
--------- | ------- | ----------- | --- | ----- | ---------
relation | false | '' | 'or' | 'or' 'and' | Relation between competition and competitor
sports | false | '' | 1,2 | 1-9 | Return games from specific sports
countries | false | 1 | 6 | | Sort competition priority by country
competitions | false | '' | 5930,11 | | Return games for specific competitions
competitor | false | '' | 131,132 | | Return games for specific competitors
games | false | '' | 131132 | | Return specific games by ids
lastUpdateId | false | '' | 848293001 | | Return only updated properties from the current lastUpdateId 
startDate | false |  current date | 07/08/2018 |  | Return games from specific date(included)
endDate | false |  current date | 09/08/2018 |  |  Return games until specific date(included)

### Examples

####dashboard

`GET https://ws.365scores.com/web/games/?sport=1,2&countries=12&lastUpdateId=848293001&startDate=07/08/2018&endDate=07/08/2018`

####competition dashboard (filter results)

`GET https://ws.365scores.com/web/games/results/?competitions=5930&countries=12&lastUpdateId=848293001`

####competition dashboard (filter fixtures)

`GET https://ws.365scores.com/web/games/fixtures/?competitions=7&countries=12&lastUpdateId=848293001`

####competitor dashboard

`GET https://ws.365scores.com/web/games/competitor=131&competitions=12&countries=12&lastUpdateId=848293001`

####partial games

`GET https://ws.365scores.com/web/games/?games=123123,123456,165432`

<aside class="notice">
Don't forget general parameters.
</aside>

## Get Game Center

```json
{
    "game": {
                "id": 1,
                "status": "started",
                "statusText": "ET",
                "gameTime": 109,
                "gameTimeDisplay": "109'",
                "gameTimeAndStatusDisplayType": 1,
                "isFutureGame": false,
                "description": "Barcelona has won 5-3 after Penalties",
                "aggregatedText": "aggregated 4-2",
                "lmt": "https://lmt.365scores.com/SportRadar?gameId=13307987&langId=1&timeZoneId=15",
                "hasLineups": false,
                "hasMissingPlayers": false,
                "hasFieldPositions": false,
                "hasTVNetworks": true,
                "countryId": 2, 
                "roundNum": 6,
                "seasonNum": 4,
                "stageNum": 3,
                "groupNum": 2,
                "competitionId": 1,
                "sportId": 1,
                 "datetime":{
                                "timeStamp": 12334423423423,
                                "dateText": "16/07/2018",
                                "timeText": "21:00 AM"
                            },
                "venue": {
                    "id": 1,
                    "name": "Saint-Petersburg Stadium",
                    "capacity": "20,000",
                    "attendance": "19,999",
                    "googlePlaceId": 1,
                },
                "stages": [{
                                "id": 7,
                                "name": "Halftime",
                                "shortName": "HT",
                                "homeCompetitorScore": 0,
                                "awayCompetitorScore": 0
                            }],
                "members": [{
                                "status": 1,
                                "playerId": 6688408,
                                "athleteId": 26574,
                                "name": "Moshe Cohen",
                                "shortName": "MoC",
                                "JerseyNumber": 6,
                                "statusText": "Rising star",
                            }],
                "homeCompetitor": {
                     "id": 1,
                     "name": "Argentina",
                     "score": 2,
                     "aggregatedScore": 4,
                     "isQualified": false,
                     "isWinner": false,
                     "countryid": 1,
                     "recentMatches": ["gameIds"],
                     "lineups": {
                                    "status": "Not Confirmed",
                                    "formation": "4-4-2",
                                    "hasFieldPositions": true,
                                    "members": [{
                                                    "playerId": 6688408,
                                                    "position": {
                                                                    "id": 1,
                                                                    "name": "striker"
                                                                },
                                                    "formation": {
                                                                    "id": 1,
                                                                    "name": "left back",
                                                                    "shortName": "LB"
                                                                },
                                                    "yardFormation": {
                                                                    "line": 2,
                                                                    "fieldPosition": 2,
                                                                    "fieldLine": 33,
                                                                    "fieldSide": 0
                                                                }
                                                }],
                                },
                     "statistics": [{
                                        "id": 1,
                                        "name": "fouls",
                                        "categoryId": 3,
                                        "categoryName": "Posessions",
                                        "value": "2",
                                        "valuePercentage": 2,
                                        "isMajor": true,
                                   }]
                },
                "awayCompetitor": {
                     "id": 2,
                     "name": "Brazil",
                     "score": 0,
                     "aggregatedScore": 2,
                     "isQualified": false,
                     "isWinner": false,
                     "countryid": 2,
                     "recentMatches": ["gameIds"],
                     "lineups": {
                                    "status": "Not Confirmed",
                                    "formation": "4-4-2",
                                    "hasFieldPositions": true,
                                    "members": [{
                                                    "playerId": 6688408,
                                                    "position": {
                                                                    "id": 1,
                                                                    "name": "striker"
                                                                },
                                                    "formation": {
                                                                    "id": 1,
                                                                    "name": "left back",
                                                                    "shortName": "LB"
                                                                },
                                                    "yardFormation": {
                                                                    "line": 2,
                                                                    "fieldPosition": 2,
                                                                    "fieldLine": 33,
                                                                    "fieldSide": 0
                                                                }
                                                }],
                                },
                     "statistics": [{
                                        "id": 1,
                                        "name": "fouls",
                                        "categoryId": 3,
                                        "categoryName": "Posessions",
                                        "value": 2,
                                        "percentage": 2,
                                        "isMajor": true,
                                   }]
                },
                "odds": {
                    "current": {
                                "bookmakerId": 1,
                                "lines":[{
                                            "link": "https://www.winner.co.il",
                                            "bookmakerId": 1,
                                            "rates":[{
                                                        "rateOptions":{
                                                                            "american": "+100",
                                                                            "fractional": "100/150",
                                                                            "decimal": "1.25"
                                                                        },
                                                        "oldRate": "1.10",
                                                        "kickOffRate": "1.25",
                                                        "num": 1
                                                    },{
                                                        "rateOptions":{
                                                                            "american": "+100",
                                                                            "fractional": "100/150",
                                                                            "decimal": "1.25"
                                                                        },
                                                        "oldRate": "1.10",
                                                        "kickOffRate": "1.25",
                                                        "num": 2
                                                    },{
                                                        "rateOptions":{
                                                                            "american": "+100",
                                                                            "fractional": "100/150",
                                                                            "decimal": "1.25"
                                                                        },
                                                        "oldRate": "1.10",
                                                        "kickOffRate": "1.25",
                                                        "num": 3
                                                    }]
                                        }]
                            },
                    "teaser": {
                                "bookmakerId": 1,
                                "games": [{
                                            "gameId": 123123,
                                            "lines":[{
                                            "link": "https://www.winner.co.il",
                                            "bookmakerId": 1,
                                            "rates":[{
                                                        "rateOptions":{
                                                                            "american": "+100",
                                                                            "fractional": "100/150",
                                                                            "decimal": "1.25"
                                                                        },
                                                        "oldRate": "1.10",
                                                        "kickOffRate": "1.25",
                                                        "num": 1
                                                    },{
                                                        "rateOptions":{
                                                                            "american": "+100",
                                                                            "fractional": "100/150",
                                                                            "decimal": "1.25"
                                                                        },
                                                        "oldRate": "1.10",
                                                        "kickOffRate": "1.25",
                                                        "num": 2
                                                    },{
                                                        "rateOptions":{
                                                                            "american": "+100",
                                                                            "fractional": "100/150",
                                                                            "decimal": "1.25"
                                                                        },
                                                        "oldRate": "1.10",
                                                        "kickOffRate": "1.25",
                                                        "num": 3
                                                    }]
                                        }]
                                         },{
                                            "gameId": 123134,
                                            "lines":[{
                                                        "link": "https://www.winner.co.il",
                                                        "bookmakerId": 1,
                                                        "rates":[{
                                                                    "rateOptions":{
                                                                                        "american": "+100",
                                                                                        "fractional": "100/150",
                                                                                        "decimal": "1.25"
                                                                                    },
                                                                    "oldRate": "1.10",
                                                                    "kickOffRate": "1.25",
                                                                    "num": 1
                                                                },{
                                                                    "rateOptions":{
                                                                                        "american": "+100",
                                                                                        "fractional": "100/150",
                                                                                        "decimal": "1.25"
                                                                                    },
                                                                    "oldRate": "1.10",
                                                                    "kickOffRate": "1.25",
                                                                    "num": 2
                                                                },{
                                                                    "rateOptions":{
                                                                                        "american": "+100",
                                                                                        "fractional": "100/150",
                                                                                        "decimal": "1.25"
                                                                                    },
                                                                    "oldRate": "1.10",
                                                                    "kickOffRate": "1.25",
                                                                    "num": 3
                                                                }]
                                                    }]
                                         }]
                            }
                },
                "previousMeetings": ["gameIds"],
                "events": [{
                    "index": 1,
                    "time": "30",
                    "playerId": 6688408,
                    "subPlayerId": 6688100,
                    "isMajor": true,
                    "event": {
                                "id": 1,
                                "name": "Goal",
                                "subTypeId": -1,
                                "subTypeName": "Own Goal",
                             }
                }],
                "eventsCategories": 2,
                "officials": [{
                                    "status": 1,
                                    "athleteId": -1,
                                    "id": 1075450,
                                    "name": "Moshe Cohen",
                                    "countryId": 2
                             }],
                "tvNetworks": [{
                                  "id": 6,
                                  "type": 1,
                                  "name": "Kan 11",
                                  "countryId": 2,
                                  "website": "https://www.iba.org.il",
                                  "bookmakerId": 0
                              }]
            },
    "countries": [{
                    "id": 1,
                    "name": "Argentina"
                },{
                    "id": 2,
                    "name": "Brazil"
                }],
    "competitions": [{
                      "id": 1,
                      "name": "World Cup",
                      "countryId": 1
                 }],
    "sports":[{
                 "id": 1,
                 "name": "Football"
            }],
    "bookmakers": [{
                        "id": 1,
                        "name": "winner",
                        "link": "https://www.winner.co.il"
                    }]
}
```

### Entities map 

Object | Usage | Description | Example
--------- | ------- | --------- | -----
game | Game center | Game's full data | [See Example](#full-game)
datetime | Game center header | Date and time data already formatted by timezone and country | [See Example](#datetime)
hasLineups | false | Boolean | | if game have full lineups
hasMissingPlayers | false | Boolean | | if game have only missing player lineups
hasFieldPositions | false | Boolean | | if game have positions for lineups yard
competitor | Team at Game center header | Competitor critical data | [See Example](#competitor)
lineups | Lineups at Game center | Competitor lineups data | [See Example](#lineups)
members | Match events | Lineups & Match events | Array of game members | [See Example](#gameMember)
stages | false | Array | | Game's stages [Description](#stage)
statistics | Stats | Array of match statistics | [See Example](#statistics)
odds | Stats | Array of match statistics | [See Example](#odds)
events | Match events | Lineups & Match events | Array of match events | [See Example](#events)
officials | Game Info | Array of officials | [See Example](#officials)
tvNetworks | Game Info | Array of TV Networks | [See Example](#tv-networks)
venue | Game Info | Data of the stadium | [See Example](#venue)

### HTTP Request

`GET https://ws.365scores.com/web/game/`


### Query Parameters

Parameter | required | Default | Example | Options | Description
--------- | ------- | ----------- | --- | ----- | ---------
gameId | true | '' | 123123 | | Return full game data by id
lastUpdateId | false | '' | 848293001 | | Return only updated properties from the current lastUpdateId 

### Examples

`GET GET https://ws.365scores.com/web/game/?gameId=123123&lastUpdateId=848293001`

<aside class="notice">
Don't forget general parameters.
</aside>
