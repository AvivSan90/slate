# Games

## Get All Games

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
                     "id": 11,
                     "name": "Argentina",
                     "nameForUrl": "argentina"
               },
               {
                     "id": 12,
                     "name": "Brazil",
                     "nameForUrl": "brazil"
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
    "paging":{
        "nextPage": "/web/games/?langId=1&timezoneId=15&userCountryId=31&startDate=07/08/2018&endDate=07/08/2018&aftergame=1703516&direction=1"
            },                                 
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
             "odds": {
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
                                                "num": 1,
                                                "trend": 2
                                            },{
                                                "rateOptions":{
                                                                    "american": "+100",
                                                                    "fractional": "100/150",
                                                                    "decimal": "1.25"
                                                                },
                                                "oldRate": "1.10",
                                                "kickOffRate": "1.25",
                                                "num": 2,
                                                "trend": 1
                                            },{
                                                "rateOptions":{
                                                                    "american": "+100",
                                                                    "fractional": "100/150",
                                                                    "decimal": "1.25"
                                                                },
                                                "oldRate": "1.10",
                                                "kickOffRate": "1.25",
                                                "num": 3,
                                                "trend": 3
                                            }]
                                }]
                    },
       }]
}
```

### Entities map 

Object | Usage | Description | Example
--------- | ------- | ----------- | ---------
game | dashboard, competition scores, team scores (game card) | Game's partial data | [See Example](#full-game)
competitor | team at game card | Competitor critical data | [See Example](#competitor)
odds | Odds | Array of odds | [See Example](#odds)

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
pageSize | false |  all games | 100 |  |  Return amount of games each page
predictions | array of predictions | Array | | [See Example](#prediction)

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
                "statusText": "Extra time",
                "shortStatusText": "ET",
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
                "startTime": "2018-12-06T17:15:00+02:00",
                "widgets": [{
                                "provider": "OPTA_LAW",
                                "partnerId": "football|68zplepppndhl8bfdvgy9vgu1|2ip4f1aefabczfkw80hj7uz8p|eok1bv6y79ugi4480fnh7qtey",
                                "url": "http://optawidgets.365scores.com/api/OptaLAW/GetWidget?partnerId=football%7C68zplepppndhl8bfdvgy9vgu1%7C2ip4f1aefabczfkw80hj7uz8p%7Ceok1bv6y79ugi4480fnh7qtey&lang=1&tz=",
                                "ratio": 1.777
                }],
                "venue": {
                    "id": 1,
                    "name": "Saint-Petersburg Stadium",
                    "nameForURL": "saint-petersburg-stadium",
                    "capacity": "20,000",
                    "attendance": "19,999",
                    "googlePlaceId": 1,
                },
                "stages": [{
                               "id": 7,
                               "name": "Halftime",
                               "shortName": "HT",
                               "homeCompetitorScore": 0,
                               "awayCompetitorScore": 0,
                               "isCurrent": true,
                               "isEnded": true
                           },
                            {
                                "id": 8,
                                "name": "End Of 90 Min",
                                "shortName": "FT",
                                "homeCompetitorScore": 0,
                                "awayCompetitorScore": 0,
                                "homeCompetitorExtraScore": 2,
                                "awayCompetitorExtraScore": 3,
                                "isCurrent": true,
                                "isLive": false,
                                "isEnded": false
                            }],
                "members": [{
                                "status": 1,
                                "playerId": 6688408,
                                "athleteId": 26574,
                                "name": "Moshe Cohen",
                                "nameForURL": "moshe-cohen",
                                "shortName": "MoC",
                                "JerseyNumber": 6,
                                "statusText": "Rising star",
                                "imgVer": 1
                            }],
                "homeCompetitor": {
                     "id": 1,
                     "name": "Argentina",
                     "score": 2,
                     "aggregatedScore": 4,
                     "isQualified": false,
                     "inPosition": true,
                     "isWinner": false,
                     "countryid": 1,
                     "imgVer": 1,
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
                     "imgVer": 1,
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
                "bestOdds": [{
                            "bookmakerId": 1,
                            "lines":[{
                                        "link": "https://www.winner.co.il",
                                        "bookmakerId": 1,
                                        "options":[{
                                                    "rate":{
                                                                        "american": "+100",
                                                                        "fractional": "100/150",
                                                                        "decimal": "1.25"
                                                                    },
                                                    "oldRate": {
                                                                        "american": "+100",
                                                                        "fractional": "100/150",
                                                                        "decimal": "1.25"
                                                                    },
                                                    "kickOffRate": "1.25",
                                                    "num": 1
                                                },{
                                                    "rateOptions":{
                                                                        "american": "+100",
                                                                        "fractional": "100/150",
                                                                        "decimal": "1.25"
                                                                    },
                                                    "oldRate": {
                                                                        "american": "+100",
                                                                        "fractional": "100/150",
                                                                        "decimal": "1.25"
                                                                    },
                                                    "kickOffRate": "1.25",
                                                    "num": 2
                                                },{
                                                    "rateOptions":{
                                                                        "american": "+100",
                                                                        "fractional": "100/150",
                                                                        "decimal": "1.25"
                                                                    },
                                                    "oldRate": {
                                                                        "american": "+100",
                                                                        "fractional": "100/150",
                                                                        "decimal": "1.25"
                                                                    },
                                                    "kickOffRate": "1.25",
                                                }]
                                    }]
                        }],
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
                              }],
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
            },
    "countries": [{
                    "id": 1,
                    "name": "Argentina",
                    "nameForURL": "argentina",
                    "imgVer": 1
                    
                },{
                    "id": 2,
                    "name": "Brazil",
                    "nameForURL": "brazil",
                    "imgVer": 2
                }],
    "competitions": [{
                      "id": 1,
                      "name": "World Cup",
                      "nameForURL": "world-cup",
                      "countryId": 1,
                      "imgVer": 1
                 }],
    "sports":[{
                 "id": 1,
                 "name": "Football",
                 "nameForURL": "football"
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
widgets | false | Array | | [See Example](#gameWidget)
predictions | false | Array | | [See Example](#prediction)


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
