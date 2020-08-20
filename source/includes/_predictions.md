# Predictions

## Get Games Predictions

```json
{
  "lastUpdateId": 987654321,
   "ttl": 10,
    "bookmakers": [{
                        "id": 1,
                        "name": "winner",
                        "link": "https://www.winner.co.il"
                }],
   "sport":[{
               "id": 1,
               "name": "Football",
               "nameForUrl": "football"
           }],
   "countries":[{
                    "id": 1,
                    "name": "Argentina",
                    "nameForURL": "argentina",
                    "liveGames": 2,
                    "totalGames": 5,
                    "sportTypes": [1, 2, 8, 12, 13]
                },
                {
                     "id": 2,
                    "name": "Brazil",
                    "nameForURL": "brazil",
                    "liveGames": 2,
                    "totalGames": 6,
                    "sportTypes": [1, 2, 8, 12, 13]
                }],
   "competitions":[{
                         "id": 1,
                         "name": "World Cup",
                         "nameForUrl": "world-cup",
                         "hasStanding": true,
                         "hasStandingGroups": true,
                         "countryId": 11,
                         "sportId": 1,
                         "liveGames": 2,
                         "totalGames": 5
                   }],                           
   "games": [{
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
             },
                    "predictions": [
                    {
                        "id": 123456789,
                        "title": "Who will win?",
                        "insight": {
                            "statisticalAnalsys": "Beitar",
                            "text": "Beitar won last 5 matches at home",
                            "odds": {
                                "num": 1,
                                "rate": {
                                    "decimal": 1.15,
                                    "fractional": "3/20",
                                    "american": "-667"
                                },
                                "oldRate": {
                                    "decimal": 1.30,
                                    "fractional": "5/20",
                                    "american": "-444"
                                },
                                "trend": 2
                            },
                            "showVotes": true,
                            "totalVotes": 14118,
                            "odds": {
                                "lineId": 51046073,
                                "gameId": 2098432,
                                "bookmakerId": 7,
                                "lineTypeId": 1,
                                "trackingUrl": "http://www.365365.com",
                                "bookmaker": {
                                    "id": 7,
                                    "name": "1xBet",
                                    "link": "http://refpavdjhx.top/L?tag=d_241617m_5437c_&site=241617&ad=5437",
                                    "nameForURL": "1xbet",
                                    "actionButton": {
                                        "link": "http://refpavdjhx.top/L?tag=d_241617m_5437c_&site=241617&ad=5437",
                                        "label": "Bet Now"
                                    }
                                },
                                "options": [{
                                            "num": 1,
                                            "rate": {
                                                "decimal": 1.15,
                                                "fractional": "3/20",
                                                "american": "-667"
                                            },
                                            "oldRate": {
                                                "decimal": 1.30,
                                                "fractional": "5/20",
                                                "american": "-444"
                                            },
                                            "trend": 2
                                        },{
                                            "num": 2,
                                            "rate": {
                                                "decimal": 1.15,
                                                "fractional": "3/20",
                                                "american": "-667"
                                            },
                                            "oldRate": {
                                                "decimal": 1.30,
                                                "fractional": "5/20",
                                                "american": "-444"
                                            },
                                            "trend": 2
                                        },{
                                            "num": 3,
                                            "rate": {
                                                "decimal": 1.15,
                                                "fractional": "3/20",
                                                "american": "-667"
                                            },
                                            "oldRate": {
                                                "decimal": 1.30,
                                                "fractional": "5/20",
                                                "american": "-444"
                                            },
                                            "trend": 2
                                        }
                                ],
                            },
                            "options": [{
                                "num": 1,
                                "name": "Beitar",
                                "symbol": 0,
                                "vote": {
                                    "count": 9306,
                                    "key": "http://www.365scores.com/Objects/Game/WWW/?GameID=2098432",
                                    "percentage": 65
                                },
                                "num": 2,
                                "name": "Draw",
                                "symbol": 0,
                                "vote": {
                                    "count": 3061,
                                    "key": "http://www.365scores.com/Objects/Game/WWW/?GameID=2098432",
                                    "percentage": 21
                                },
                                "num": 3,
                                "name": "Hapoel",
                                "symbol": 0,
                                "vote": {
                                    "count": 2010,
                                    "key": "http://www.365scores.com/Objects/Game/WWW/?GameID=2098432",
                                    "percentage": 14
                                }
                            }],
                        }
                    }
                ]
       }]
}
```

### Entities map 

Object | Usage | Description | Example
--------- | ------- | ----------- | ---------
game | dashboard, competition scores, team scores (game card) | Game's partial data | [See Example](#full-game)
competitor | team at game card | Competitor critical data | [See Example](#competitor)
predictions | main prediction for current game | Array | | [See Example](#prediction)

Partial object of game with main prediction

This endpoint retrieves only 5 relevant games.

### HTTP Request

`GET https://webws.365scores.com/web/games/predictions`

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

####predictions for football

`GET https://webws.365scores.com/web/games/predictions/?sports=1`

####competition's predictions

`GET https://webws.365scores.com/web/games/predictions/?competitions=7`

####competitor's predictions 

`GET https://webws.365scores.com/web/games/predictions/?competitors=132`

<aside class="notice">
Don't forget general parameters.
</aside>