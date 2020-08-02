# Entities


## LiveData

```json
{
     "isLive": true,
     "homeScore": 2,
     "awayScore": 1,
     "gameStatus": 2
}

```

Parameter | required | type | Options  | Description
--------- | ------- |  ----- |  ----- | ---------
isLive | true | Boolean |  | is live game
homeScore | false | Integer |  | Score of the home competitor
awayScore | false | Integer |  | Score of the away competitor
gameStatus | false | Integer |  | 1 -> Competitor is wining  ,  2 -> Competitor is losing  ,  3 -> Drew 




## Sport

```json
{
     "id": 1,
     "name": "Football",
     "nameForURL": "football"
}
```

Parameter | required | type | Options  | Description
--------- | ------- |  ----- |  ----- | ---------
id | true | Integer |  | Sport's id
name | true | String |  | Sport's name

## Country

```json
{
    "id": 1,
    "name": "Argentina",
    "nameForURL": "argentina",
    "liveGames": 2,
    "totalGames": 5,
    "imgVer": 1
}
```

Parameter | required | type | Options  | Description
--------- | ------- |  ----- |  ----- | ---------
id | true | Integer |  | Country's id
name | true | String | | Country's name
liveGames | false | Integer |  | Live games for current country
totalGames | false | Integer |  | Total games for current country
imgVer | false | Integer |  | Image version (add to image url)

## Competition

```json
{
      "id": 1,
      "name": "World Cup",
      "nameForURL": "world-cup",
      "hasStanding": true,
      "hasStandingGroups": true,
      "countryId": 11,
      "sportId": 11,
      "liveGames": 2,
      "totalGames": 5,
      "imgVer": 1
}
```

Parameter | required | type | Options  | Description
--------- | ------- | ----- | ----- | ---------
id | true | Integer |  | Competition's id
name | true | String | | Competition's name
countryId | true | Integer | | Competition's countryId
sportId | true | Integer | | Competition's sportId
hasStanding | false | Boolean | | If Competition has Standing data
hasStandingGroups | false | Boolean | | If Standing has groups
liveGames | false | Integer | | Live games for current competition
totalGames | false | Integer | | Total games for current competition
imgVer | false | Integer |  | Image version (add to image url)

## Bookmaker

```json
{
    "id": 1,
    "name": "winner",
    "link": "https://www.winner.co.il"
}
```

Parameter | required | type | Options  | Description
--------- | ------- | ----- | ----- | ---------
id | true | Integer |  | Bookmaker's id
name | true | String | | Bookmaker's name
link | true | Integer | | Bookmaker's website link

## Full Game

```json
{
    "game": {
                "id": 1,
                "statusGroup": 1,
                "statusText": "Extra time",
                "shortStatusText": "ET",
                "gameTimeDisplay": "89'",
                "gameTime": 89,
                "gameTimeAndStatusDisplayType": 1,
                "hasLineups": false,
                "hasMissingPlayers": false,
                "hasFieldPositions": false,
                "isFutureGame": false,
                "description": "Barcelona has won 5-3 after Penalties",
                "aggregatedText": "aggregated 4-2",
                "lmt": "https://lmt.365scores.com/SportRadar?gameId=13307987&langId=1&timeZoneId=15",
                "countryId": 2, 
                "competitionId": 1,
                "sportId": 1,
                "roundNum": 3,
                "seasonNum": 6,
                "stageNum": 4,
                "groupNum": 1,
                "startTime": "2018-12-06T17:15:00+02:00",
                "widgets": [{
                                "provider": "OPTA_LAW",
                                "partnerId": "football|68zplepppndhl8bfdvgy9vgu1|2ip4f1aefabczfkw80hj7uz8p|eok1bv6y79ugi4480fnh7qtey",
                                "url": "http://optawidgets.365scores.com/api/OptaLAW/GetWidget?partnerId=football%7C68zplepppndhl8bfdvgy9vgu1%7C2ip4f1aefabczfkw80hj7uz8p%7Ceok1bv6y79ugi4480fnh7qtey&lang=1&tz=",
                                "ratio": 1.777
                }],
                "venue": {
                    "name": "Saint-Petersburg Stadium",
                    "capacity": "20,000",
                    "attendance": "19,999",
                    "googlePlaceId": 1
                }, 
                "stages": [{
                               "id": 7,
                               "name": "Halftime",
                               "shortName": "HT",
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
                                "nameForURL": "world-cup",
                                "shortName": "MoC",
                                "JerseyNumber": 6,
                                "statusText": "Rising star",
                                "imgVer": 1
                            }],
                "homeCompetitor": {
                     "id": 1,
                     "name": "Argentina",
                     "imgVer": 1,
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
                                     "playersStatistics": {
                                                            "Subjects": [{
                                                                            "id": 328865,
                                                                            "name": "Pass"
                                                                        }],
                                                            "Categories": [{
                                                                                "id": 1,
                                                                                "name": "Passing",
                                                                                "shortName": "Passing",
                                                                                "subjectId": 328865
                                                                            }],
                                                            "Tables": [{
                                                                            "categoryId": 1,
                                                                            "groups": [{
                                                                                            "id": 1,
                                                                                            "name": "Starters"
                                                                                        }],
                                                                            "columns": [{
                                                                                            "num": 1,
                                                                                            "name": "C",
                                                                                            "shortName": "C",
                                                                                            "order": 147,
                                                                                            "isMajor": true
                                                                                        }],
                                                                            "rows": [{
                                                                                        "groupId": 1,
                                                                                        "playerId": 1139046,
                                                                                        "num": 1,
                                                                                        "values": [{
                                                                                                        "columnNum": 1,
                                                                                                        "value": "26"
                                                                                                    }],
                                                                                    }],
                                                                            "summary": [{
                                                                                        "title": "Team Totals",
                                                                                        "values": [{
                                                                                                        "columnNum": 1,
                                                                                                        "value": "26"
                                                                                                    }],
                                                                                        }],
                                                                            }],
                                                            "Expandable": false
                                                        },
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
                                        "value": "50%",
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
                                     "playersStatistics": {
                                                            "Subjects": [{
                                                                            "id": 328865,
                                                                            "name": "Pass"
                                                                        }],
                                                            "Categories": [{
                                                                                "id": 1,
                                                                                "name": "Passing",
                                                                                "shortName": "Passing",
                                                                                "subjectId": 328865
                                                                            }],
                                                            "Tables": [{
                                                                            "categoryId": 1,
                                                                            "groups": [{
                                                                                            "id": 1,
                                                                                            "name": "Starters"
                                                                                        }],
                                                                            "columns": [{
                                                                                            "num": 1,
                                                                                            "name": "C",
                                                                                            "shortName": "C",
                                                                                            "order": 147,
                                                                                            "isMajor": true
                                                                                        }],
                                                                            "rows": [{
                                                                                        "groupId": 1,
                                                                                        "playerId": 1139046,
                                                                                        "num": 1,
                                                                                        "values": [{
                                                                                                        "columnNum": 1,
                                                                                                        "value": "26"
                                                                                                    }],
                                                                                    }],
                                                                            "summary": [{
                                                                                        "title": "Team Totals",
                                                                                        "values": [{
                                                                                                        "columnNum": 1,
                                                                                                        "value": "26"
                                                                                                    }],
                                                                                        }],
                                                                            }],
                                                            "Expandable": false
                                                        },
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
                                        "value": "50%",
                                        "valuePercentage": 2
                                   }]
                },
                "odds": {
                    "live": {
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
                                                        "oldRate": {
                                                                        "american": "+100",
                                                                        "fractional": "100/150",
                                                                        "decimal": "1.25"
                                                                    },
                                                        "kickOffRate": "1.25",
                                                        "name": "1",
                                                        "template": "#COMPETITOR1",
                                                        "competitorId": 132
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
                                                        "name": "X",
                                                        "template": "Draw",
                                                        "competitorId": 132
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
                                                        "name": "2",
                                                        "template": "#COMPETITOR2",
                                                        "competitorId": 131
                                                    }]
                                        }]
                            },
                },
                "previousMeetings": ["gameIds"],
                "events": [{
                                    "competitorId": 562,
                                    "statusId": 6,
                                    "stageId": 7,
                                    "order": 1,
                                    "num": 1,
                                    "gameTimeDisplay": "89'",
                                    "gameTime": 89,
                                    "addedTime": 0,
                                    "gameTimeAndStatusDisplayType": 1,
                                    "playerId": 6688408,
                                    "isMajor": false,
                                    "extraPlayers" :[
                                        6688100,
                                    ],
                                    "eventType": {
                                                "id": 1,
                                                "name": "Goal",
                                                "subTypeId": -1,
                                    }
                            }],
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
                    "imgVer": 1
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

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
game | true | Object |  | Full game data
id | true | Integer |  | Game's id
lastUpdateId | true | Integer |  | Game's update id for delta fetching
ttl | true | Integer |  | Seconds for next game request 
statusGroup | true | Integer | 1 - 'Anticipated', 2 - 'Scheduled', 3 - 'Live', 4 - 'Finished' | Game's Status
statusText | false | String | | Game's Status formatted text
shortStatusText | false | String | | Game's Status short formatted text
showCountdown | false | Boolean | | if game card should show countdown
gameTime | false | Integer | | Game's time 
gameTimeDisplay | false | String | | Game's time formatted text
gameTimeAndStatusDisplayType | false | Integer | | Enum to present gameTimeDisplay or/and statusText
hasLineups | false | Boolean | | if game have full lineups
hasMissingPlayers | false | Boolean | | if game have only missing player lineups
hasFieldPositions | false | Boolean | | if game have positions for lineups yard
startTime | true | String | | ISO string game start time
isFutureGame | false | Boolean |  | if true don't display game
description | false | String |  | Game's description
aggregatedText | false | String |  | Aggregate score formatted text
lmt | false | String |  | if exist use iframe with the lmt url
widgets | false | Array | | [Description](#gameWidget)
venue | false | Object | | [Description](#venue)
members | false | Array | | Game's members (both competitors, include management) [Description](#gameMember)
stages | false | Array | | Game's stages [Description](#stage)
homeCompetitor | true | Object | | [Description](#competitor)
awayCompetitor | true | Object | | [Description](#competitor) 
competitionId | true | Integer | | Game's competition
sportId | true | Integer | | Game's sport type
odds | false | Object | | [Description](#odds)
previousMeetings | false | Array | | Array of gameIds for previous meeting between current competitors
events | false | Array | | Array of match events
officials | false | Array | | Array of game's officials
tvNetworks | false | Array | | Array of tv networks
bookmakers | false | Array | | Array of Bookmakers for odds -> lines
roundNum | false | Integer | | Game part of round 
seasonNum | false | Integer | | Game part of season 
stageNum | false | Integer | | Game part of stage 
groupNum | false | Integer | | Game part of group 

## Prediction

```json
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
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
id | true | Integer |  | Predision's id
title | true | String |  | Predision's title
insight | false | Object |  | [Description](#insight)
showVotes | true | Boolean | | if to show votes count or percentage
totalVotes | true | Integer | | total votes
odds | false |  | Object | [Description](#odds)
options | true | Object |  | [Description](#predictionOptions)


## insight

```json
{
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
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
statisticalAnalsys | true | String |  | option name that provide by insight
text | true | String |  | Description of statistical analsys
odds | false |  | Object | [Description](#rate)

## predictionOption

```json
{
    "num": 1,
    "name": "Beitar",
    "symbol": 0,
    "vote": {
        "count": 9306,
        "key": "http://www.365scores.com/Objects/Game/WWW/?GameID=2098432",
        "percentage": 65
    },
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
num | true | Integer |  | option num
name | true | String |  | option name
vote | true |  | Object | [Description](#vote)

## vote

```json
{
    "count": 9306,
    "key": "http://www.365scores.com/Objects/Game/WWW/?GameID=2098432",
    "percentage": 65
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
count | true | Integer |  | votes count per option
key | true | String |  | key for POST request
percentage | true | | String | votes percentage per option

## gameWidget

```json
{
    "provider": "OPTA_LAW",
    "partnerId": "football|68zplepppndhl8bfdvgy9vgu1|2ip4f1aefabczfkw80hj7uz8p|eok1bv6y79ugi4480fnh7qtey",
    "url": "http://optawidgets.365scores.com/api/OptaLAW/GetWidget?partnerId=football%7C68zplepppndhl8bfdvgy9vgu1%7C2ip4f1aefabczfkw80hj7uz8p%7Ceok1bv6y79ugi4480fnh7qtey&lang=1&tz=",
    "ratio": 1.777
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
provider | true | String |  | Widget's provider name
partnerId | true | Integer |  | Widget's partner id (added to url}
url | true | String |  | Widget's url (used on iframe)
ratio | true | Integer |  | Widget's ratio

## Partial Game

```json
{
  "description": "Future api response for games:",
  "lastUpdateId": 987654321,
   "ttl": 10,
   "sport":[{
               "id": 1,
               "name": "Football",
               "nameForURL": "football"
           }],
   "countries":[{
                     "id": 11,
                     "name": "Argentina",
                     "nameForURL": "argentina",
                     "imgVer": 1
               },
               {
                     "id": 12,
                     "name": "Brazil",
                     "nameForURL": "brazil",
                     "imgVer": 1
                 }],
   "competitions":[{
                         "id": 1,
                         "name": "World Cup",
                         "nameForURL": "world-cup",
                         "hasStanding": true,
                         "hasStandingGroups": true,
                         "countryId": 11,
                         "imgVer": 1
                   }],
   "games": [{
             "id": 1,
             "statusGroup": 1,
             "statusText": "Extra time",
             "shortStatusText": "ET",
             "gameTimeDisplay": "89'",
             "gameTime": 89,
             "gameTimeAndStatusDisplayType": 1,
             "isFutureGame": false,
             "hasLineups": false,
             "hasMissingPlayers": false,
             "hasFieldPositions": false,
             "showCountdown": false,
             "hasTVNetworks": false,
             "hasBetsTeaser": false,
             "displayTitle": "Semi Final",
             "description": "Barcelona has won 5-3 after Penalties",
             "aggregatedText": "aggregated 4-2",
             "startTime": "2018-12-06T17:15:00+02:00",
             "homeCompetitor": {
                  "id": 1,
                  "name": "Argentina",
                  "score": 2,
                  "imgVer": 2,
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
                  "imgVer": 1,
                  "aggregatedScore": 2,
                  "isQualified": false,
                  "isWinner": false,
                  "redCards": 1,
                  "countryId": 12
             },
             "sportId": 1,
             "competitionId": 1,
             "roundNum": 3,
             "seasonNum": 6,
             "stageNum": 4,
             "groupNum": 1,
       }]
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
lastUpdateId | true | Integer |  | Game's update id for delta fetching
ttl | true | Integer |  | Seconds for next game request 
games | true | Array |  | Array of partial games
id | true | Integer |  | Game's id
startTime | true | String |  | ISO string game start time
statusGroup | true | Integer | 1 - 'Anticipated', 2 - 'Scheduled', 3 - 'Live', 4 - 'Finished' | Game's Status
statusText | false | Integer | | Game's time
shortStatusText | false | String | | Game's Status short formatted text
gameTimeDisplay | false | String | | Game's time formatted text
gameTime | false | Integer | | Game's time formatted text
isFutureGame | false | Boolean |  | if true don't display game
hasLineups | false | Boolean | | if game have full lineups
displayTitle | false | String | 'Match Week 12' 'Semi Final' | games groups title 
hasMissingPlayers | false | Boolean | | if game have only missing player lineups
hasFieldPositions | false | Boolean | | if game have positions for lineups yard
hasTVNetworks | false | Boolean | | if game have tv networks
showCountdown | false | Boolean | | if game card should show countdown
hasBetsTeaser | false | Boolean | | if games have odds (icon display functionality)
description | false | String |  | Game's description
aggregatedText | false | String |  | Aggregate score formatted text
members | false | Array | | game's Members [Description](#gameMember)
homeCompetitor | true | Object | | [Description](#competitor)
awayCompetitor | true | Object | | [Description](#competitor)
competitionId | true | Integer | | Game's competition
sportId | true | Integer | | Game's sport type
roundNum | false | Integer | | Game part of round 
seasonNum | false | Integer | | Game part of season 
stageNum | false | Integer | | Game part of stage 
groupNum | false | Integer | | Game part of group 

## Competitor

```json
{
    "id": 1,
    "name": "Argentina",
    "imgVer": 1,
    "score": 2,
    "aggregatedScore": 4,
    "isQualified": false,
    "isWinner": false,
    "redCards": 0,
    "countryId": 11,
    "type": 2,
    "lineups": {
                "status": "Not Confirmed",
                "formation": "4-4-2",
                "hasFieldPositions": true,
                 "playersStatistics": {
                                        "Subjects": [{
                                                        "id": 328865,
                                                        "name": "Pass"
                                                    }],
                                        "Categories": [{
                                                            "id": 1,
                                                            "name": "Passing",
                                                            "shortName": "Passing",
                                                            "subjectId": 328865
                                                        }],
                                        "Tables": [{
                                                        "categoryId": 1,
                                                        "groups": [{
                                                                        "id": 1,
                                                                        "name": "Starters"
                                                                    }],
                                                        "columns": [{
                                                                        "num": 1,
                                                                        "name": "C",
                                                                        "shortName": "C",
                                                                        "order": 147,
                                                                        "isMajor": true
                                                                    }],
                                                        "rows": [{
                                                                    "groupId": 1,
                                                                    "playerId": 1139046,
                                                                    "num": 1,
                                                                    "values": [{
                                                                                    "columnNum": 1,
                                                                                    "value": "26"
                                                                                }],
                                                                }],
                                                        "summary": [{
                                                                    "title": "Team Totals",
                                                                    "values": [{
                                                                                    "columnNum": 1,
                                                                                    "value": "26"
                                                                                }],
                                                                    }],
                                                        }],
                                        "Expandable": false
                                    },
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
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
id | true | Integer |  | Competitor's id
name | true | String |  | Competitor's name
score | false | Integer |  | Competitor's score for specific game
aggregatedScore | false | Integer |  | Competitor's aggregatedScore for specific game
isQualified | false | Boolean |  | If competitor qualified to next stage
inPosition | false | Boolean |  | If competitor is in position
isWinner | false | Boolean |  | If competitor qualified to next stage
redCards | false | Integer |  | If competitor qualified to next stage
countryId | true | Integer |  | Competitor's country
lineups | false | Array | | [Description](#lineups)
imgVer | false | Integer |  | Image version (add to image url)
type | true | Integer | | Competitor type (team, nationalTeam, player, coupl)

## Stage

```json
{
    "id": 7,
    "name": "Halftime",
    "shortName": "HT",
    "homeCompetitorScore": 0,
    "awayCompetitorScore": 0,
    "homeCompetitorExtraScore": 2,
    "awayCompetitorExtraScore": 3,
    "time": "47'",
    "isCurrent": true,
    "isLive": false,
    "isEnded": false
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
id | true | Integer |  | stage's id
name | true | String |  | stage's name
shortName | false | String |  | stage's short name
homeCompetitorScore | true | Integer |  | stage's home competitor score
awayCompetitorScore | true | Integer |  | stage's away competitor scored
homeCompetitorExtraScore | false | Integer |  | stage's home competitor extra score (tie breaker)
awayCompetitorExtraScore | false | Integer |  | stage's away competitor extra score (tie breaker)
time | false | String |  | stage's time
isCurrent | false | Boolean |  | if stage is current result
isLive | false | Boolean |  | if stage is live
isEnded | false | Boolean |  | if stage is ended

## Lineups

```json
{
    "status": "Not Confirmed",
    "formation": "4-4-2",
    "hasFieldPositions": true,
    "playersStatistics": {
                            "Subjects": [{
                                            "id": 328865,
                                            "name": "Pass"
                                        }],
                            "Categories": [{
                                                "id": 1,
                                                "name": "Passing",
                                                "shortName": "Passing",
                                                "subjectId": 328865
                                            }],
                            "Tables": [{
                                            "categoryId": 1,
                                            "groups": [{
                                                            "id": 1,
                                                            "name": "Starters"
                                                        }],
                                            "columns": [{
                                                            "num": 1,
                                                            "name": "C",
                                                            "shortName": "C",
                                                            "order": 147,
                                                            "isMajor": true
                                                        }],
                                            "rows": [{
                                                        "groupId": 1
                                                        "playerId": 1139046,
                                                        "num": 1,
                                                        "values": [{
                                                                        "columnNum": 1,
                                                                        "value": "26"
                                                                    }],
                                                    }],
                                            "summary": [{
                                                        "title": "Team Totals",
                                                        "values": [{
                                                                        "columnNum": 1,
                                                                        "value": "26"
                                                                    }],
                                                        }],
                                            }],
                            "Expandable": false
                        },
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
                                },
                    "substitute": {
                                    "playerId": 22,
                                    "time": 90.0,
                                    "type": 1,
                                    "status": 1
                                }
                }]
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
status | true | Integer | ??? | Lineup's status
formation | false | String |  | Competitor's lineups formation
hasFieldPositions | false | Boolean |  | Flag if members has field positions
playersStatistics | false | Object |  | players statistics for box-score [Description](#playersStatistics)
members | false | Array | | array of lineups members [Description](#lineupsMember)

## gameMember

```json
[{
    "status": 1,
    "id": 6688408,
    "athleteId": 26574,
    "name": "Moshe Cohen",
    "nameForURL": "moshe-cohen",
    "shortName": "MoC",
    "JerseyNumber": 6,
    "statusText": "Rising star",
    "imgVer": 1
}]
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
status | true | Integer | 0 - Not playing, 1 - Doubtful, 2 - playing | Member's status
id | true | Integer | | Member's id (id for specific game)
athleteId | true | Integer | | Member's id (athlete entity id)
name | true | String | | Member's name
shortName | false | String | | Member's nickname
JerseyNumber | false | Integer | | Member's jersey number
imgVer | false | Integer |  | Image version (add to image url)

## playersStatistics

```json
{
    "Subjects": [{
                    "id": 328865,
                    "name": "Pass"
                }],
    "Categories": [{
                        "id": 1,
                        "name": "Passing",
                        "shortName": "Passing",
                        "subjectId": 328865
                    }],
    "Tables": [{
                    "categoryId": 1,
                    "groups": [{
                                    "id": 1,
                                    "name": "Starters"
                                }],
                    "columns": [{
                                    "num": 1,
                                    "name": "C",
                                    "shortName": "C",
                                    "order": 147,
                                    "isMajor": true
                                }],
                    "rows": [{
                                "groupId": 1,
                                "playerId": 1139046,
                                "num": 1,
                                "values": [{
                                                "columnNum": 1,
                                                "value": "26"
                                            }],
                            }],
                    "summary": [{
                                "title": "Team Totals",
                                "values": [{
                                                "columnNum": 1,
                                                "value": "26"
                                            }],
                                }],
                    }],
    "Expandable": false
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
Subjects | false | Array | | Array of player statistics subjects [Description](#subject)
Categories | false | Array | | Array of player statistics categories [Description](#category)
Tables | false | Array | | Array of player statistics tables [Description](#table)
Expandable | false | Boolean | | If playes statistics is expandable

## subject

```json
[{
    "id": 328865,
    "name": "Pass"
}]
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
id | false | Number | | Subject's id 
name | false | String | | Subject's name 


## category

```json
[{
    "id": 1,
    "name": "Passing",
    "shortName": "Passing",
    "subjectId": 328865
}]
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
id | false | Number | | Category's id 
name | false | String | | Category's name 
shortName | false | String | | Category's short name 
subjectId | false | Number | | Subject's id

## table

```json
[{
    "categoryId": 1,
    "groups": [{
                    "id": 1,
                    "name": "Starters"
                }],
    "columns": [{
                    "num": 1,
                    "name": "C",
                    "shortName": "C",
                    "order": 147,
                    "isMajor": true
                }],
    "rows": [{
                "groupId": 1,
                "playerId": 1139046,
                "num": 1,
                "values": [{
                                "columnNum": 1,
                                "value": "26"
                            }],
            }],
    "summary": [{
                "title": "Team Totals",
                "values": [{
                                "columnNum": 1,
                                "value": "26"
                            }],
                }],
}]
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
categoryId | false | Number | | Category's id 
groups | false | Array | | Array of statistics groups[Description](#group)
columns | false | Array | | Array of statistics table columns [Description](#column)
rows | false | Array | | Array of table rows [Description](#row)
summary | false | Array | | Array of statistics table summary [Description](#summary)

## group

```json
[{
    "id": 1,
    "name": "Starters"
}],
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
id | false | Number | | Group's id 
name | false | String | | Group's name 

## column

```json
[{
    "num": 1,
    "name": "C",
    "shortName": "C",
    "order": 147,
    "isMajor": true
}],
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
num | false | Number | | Column's id 
name | false | String | | statistic's name 
shortName | false | String | | statistic's short name 
order | false | Number | | Column's order number 
isMajor | false | Boolean | | If column it's statistics highlight

## row

```json
[{
"playerId": 1139046,
"num": 1,
"values": [{
                "columnNum": 1,
                "value": "26"
            }],
}]
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
playerId | false | Number | | Player's id 
groupId | false | Number | | Table group's id 
num | false | Number | | Row's nun 
values | false | Array | | Array of value in row [Description](#value)

## summary

```json
[{
    "title": "Team Totals",
    "values": [{
                    "columnNum": 1,
                    "value": "26"
                }],
}],
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
title | false | String | | Summary's title 
values | false | Array | | Array of value in summary [Description](#value)

## value

```json
[{
    "columnNum": 1,
    "value": "26"
}],
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
columnNum | false | String | | Column's num 
value | false | ArraNumbery | | Statistic's value 

## lineupsMember

```json
[{
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
}]
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
playerId | true | Integer | | Member's id (id for specific game)
position | true | Object | | [Description](#position)
formation | false | Object | | [Description](#formation)
yardFormation | false | Object | | [Description](#yardFormation)

## Position

```json
{
  "id": 1,
  "name": "striker"
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
id | true | Integer | | Position's id
name | true | String | | Position's name

## Formation

```json
{
  "id": 1,
  "name": "left back",
  "shortName": "LB"
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
id | true | Integer | | Formation's id
name | true | String | | Formation's name
shortName | false | String | | Formation's nickname

## Yard formation

```json
{
   "line": 2,
   "fieldPosition": 2,
   "fieldLine": 33,
   "fieldSide": 0
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
line | true | Integer | | ?????????
fieldPosition | true | String | | ???????????
fieldLine | false | String | | ????????????
fieldSide  | false | String | | ???????????

## Statistics

```json
[{
    "id": 1,
    "name": "fouls",
    "categoryId": 3,
    "categoryName": "Posessions",
    "value": "50%",
    "valuePercentage": 2,
    "isMajor": true
}]
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
id | true | Integer | | Statistic's id
name | true | String | | Statistic's name
categoryId | true | Integer | | Statistics need to be group by category id 
categoryName | true | String | ?????? | Substitution type
value  | true | String | ?????? | Value of current statistic
percentage  | false | Double | ?????? | Percentage from away and home current statistic
isMajor  | true | Boolean | ?????? | If current statistic is major

## Odds

```json
{
    "current": {
                "bookmakerId": 1,
                "lines":[{
                            "link": "https://www.winner.co.il",
                            "bookmakerId": 1,
                            "rates":[{
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
                                    "kickOffRate": {
                                        "american": "+100",
                                        "fractional": "100/150",
                                        "decimal": "1.25"
                                    },
                                    "name": "1",
                                    "template": "#COMPETITOR1",
                                    "competitorId": 132
                                    },{
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
                                    "kickOffRate": {
                                        "american": "+100",
                                        "fractional": "100/150",
                                        "decimal": "1.25"
                                    },
                                    "name": "X",
                                    "template": "Draw",
                                    "competitorId": 132
                                    },{
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
                                    "kickOffRate": {
                                        "american": "+100",
                                        "fractional": "100/150",
                                        "decimal": "1.25"
                                    },
                                    "name": "2",
                                    "template": "#COMPETITOR2",
                                    "competitorId": 131
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
                                        "kickOffRate": {
                                            "american": "+100",
                                            "fractional": "100/150",
                                            "decimal": "1.25"
                                        },
                                        "name": "1",
                                        "template": "#COMPETITOR1",
                                        "competitorId": 132
                                    },{
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
                                        "kickOffRate": {
                                            "american": "+100",
                                            "fractional": "100/150",
                                            "decimal": "1.25"
                                        },
                                        "name": "X",
                                        "template": "Draw",
                                        "competitorId": 132
                                    },{
                                        
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
                                        "kickOffRate": {
                                            "american": "+100",
                                            "fractional": "100/150",
                                            "decimal": "1.25"
                                        },
                                        "name": "2",
                                        "template": "#COMPETITOR2",
                                        "competitorId": 131
                                    }]
                         },{
                            "gameId": 123134,
                            "lines":[{
                                        "link": "https://www.winner.co.il",
                                        "bookmakerId": 1,
                                        "rates":[{
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
                                                    "kickOffRate": {
                                                        "american": "+100",
                                                        "fractional": "100/150",
                                                        "decimal": "1.25"
                                                    },
                                            "name": "1",
                                            "template": "#COMPETITOR1",
                                            "competitorId": 132
                                            },{
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
                                                    "kickOffRate": {
                                                        "american": "+100",
                                                        "fractional": "100/150",
                                                        "decimal": "1.25"
                                                    },
                                                "name": "X",
                                                "template": "Draw",
                                                "competitorId": 132
                                            },{
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
                                                "kickOffRate": {
                                                    "american": "+100",
                                                    "fractional": "100/150",
                                                    "decimal": "1.25"
                                                },
                                                "name": "2",
                                                "template": "#COMPETITOR2",
                                                "competitorId": 131
                                            }]
                                    }]
                         }]
            }
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
odds | false | Object | | Game's odds
current | false | Object | | Odds for current game
teaser | false | Object | | Odds for next game for each competitor

## Lines

```json
[{
    "link": "https://www.winner.co.il",
    "bookmakerId": 1,
    "rates":[{
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
                "name": "1",
                "template": "#COMPETITOR1",
                "competitorId": 132
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
                "name": "X",
                "template": "Draw",
                "competitorId": 132
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
                "name": "2",
                "template": "#COMPETITOR2",
                "competitorId": 131
            }]
}]

```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
link | false | Integer | | Bookmaker line link to website
bookmakerId | true | String | | Bookmaker's id
rates | true | Array | | [Description](#rate)

## Rate

```json
{
    "rateOptions":{
                        "american": "+100",
                        "fractional": "100/150",
                        "decimal": "1.25"
                    },
    "oldRate": {
                    "american": "+120",
                    "fractional": "100/230",
                    "decimal": "1.40"
                },
    "kickOffRate": "1.25",
    "num": 1
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
rateOptions | true | Object | | All supported rate types
oldRate | false | Object | | if rate changes saving old rate for trend
kickOffRate | false | Double | | the rate when the game is startting (Decimal)
name | true | String | | Rate label Ex. '1', 'x', '2', 'Under', 'Over',

## Events

```json
[{
        "competitorId": 562,
        "statusId": 6,
        "stageId": 7,
        "order": 1,
        "num": 1,
        "gameTimeDisplay": "89'",
        "gameTime": 89,
        "addedTime": 0,
        "gameTimeAndStatusDisplayType": 1,
        "playerId": 6688408,
        "isMajor": false,
        "extraPlayers" :[
            6688100,
        ],
        "eventType": {
                    "id": 1,
                    "name": "Goal",
                    "subTypeId": -1,
        }
}]
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
competitorId | true | Integer| | Event's competitior id
statusId | true | Integer | | game status at the event
stageId | true | Integer | | game stage at the event
order | true | Integer | | Event order on display 
num | true | Object | | Event num on display 
gameTime | false | Integer | | Game's time 
addedTime | false | Integer | | Game's added time 
gameTimeDisplay | false | String | | Game's time formatted text
gameTimeAndStatusDisplayType | false | Integer | | Enum to present gameTimeDisplay or/and statusText
playerId | true | Integer | | Main player for the event
extraPlayers | false | Array | | array of extra players [playerId]
eventType | true | Object |  |  [Description](#EventType)
isMajor | false | Boolean |  | If event are major (filter top)

## Event Type

```json
{
        "id": 1,
        "name": "Goal",
        "subTypeId": -1,
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
id | true | Integer |  | Enum of events
name | true | Integer | | Events desplay name
subTypeId | true | String | | Event Sub type

## Officials

```json
[{
      "status": 1,
      "id": 6688408,
      "name": "Moshe Cohen",
      "nameForURL": "moshe-cohen",
      "shortName": "MoC",
      "countryId": 2
}]
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
status | true | Integer | ????? | ???????
id | true | Integer | | Official's id for current game
name | true | String | | Official's name
shortName | false | String | | Official's name
JerseyNumber | false | Object |  | Event Object with id and name
countryId | true | Integer |  | Official's country

## TV Networks

```json
[{
    "id": 6,
    "type": 1,
    "name": "Kan 11",
    "nameForURL": "kan-11",
    "countryId": 2,
    "website": "https://www.iba.org.il",
    "bookmakerId": 0
}]
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
id | true | Integer | ????? | TVNetwork's id
type | true | Integer | | ?????????
name | true | String | | TVNetwork's name
countryId | true | Object |  | Official's country
website | false | String |  | Link to TVNetwork's website
bookmakerId | false | Integer |  | ??????????

## Venue

```json
{
    "name": "Saint-Petersburg Stadium",
    "nameForURL": "saint-petersburg-stadium",
    "capacity": "20,000",
    "attendance": "19,999",
    "googlePlaceId": 1
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
name | true | String | | Venue's name
capacity | false | Integer |  | Venue's capacity
attendance | false | Integer |  | Current game attendance
googlePlaceId | false | Integer |  | Google maps place id of the current venue

## Header 

```json
[{
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
}]
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
key | true | String | | Key of column use as key for Standing rows
name | false | Integer |  | Column display name 
isMajor | false | Integer |  | If show on small view

## Rows

```json
[{
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
    "detailedRecentForm": [{
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
    "recentForm": [0,1,2,2,1],
    "destinationNum": 1,
    "destinationGuaranteed": true,
    "isWinner": true,
    "liveGameId": 2034294,
    "liveGameStatus": 0,
    "previousPosition": 3
}]
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
competitor | true | Object | | [Description](#competitor)
group | false | Integer |  | Use if competition has groups, id and display name
gamesPlayed | true | Integer |  | Competitor games played on current competition
gamesWon | true | Integer |  | Competitor wins on current competition
gamesLost | true | Integer |  | Competitor loses on current competition
gamesEven | true | Integer |  | Competitor draws on current competition
for | true | Integer |  | Competitor goals
against | true | Integer |  | Competitor conceded goals
ratio | true | Integer |  | Competitor goals - conceded goals
points | true | Integer |  | Competitor points earned
strike | true | Integer |  | wins strike
gamesOverTime | true | Integer |  | Total games that go to over time
gamesWonOnOverTime | true | Integer |  | Total games that won after over time
gamesWonOnPenalties | true | Integer |  | Total games that won after penalties
gamesLossOnOverTime | true | Integer |  | Total games that lost after over time
gamesLossOnPenalties | true | Integer |  | Total games that lost after penalties
position | true | Integer |  | Position on Standing (row number)
trend | false | Integer |1 - up, 0 - even, -1 - down| On live game if team goes up or down on Standing 
recentForm | false | Array |  | trend for recent matches on current competition
detailedRecentForm | false | Array<PartialGame> |  | Array of last (Max) 5 games
destinationNum | false | Integer |  | Destination by position
destinationGuaranteed | false | Boolean |  | If Destination guaranteed for current competitor
isWinner | false | Boolean |  | If current competitor won the competition title
liveGameId | false | Integer |  | Live game id
liveGameStatus | false | Integer | 1 - winner, 0 - draw, -1 - lose | On live game if team winner, draw or lose 
previousPosition | false | Integer |  | Previous position on standing on live game (row number)

### Destinations

```json
[{
    "id": 1,
    "name": "Champions League",
    "nameForURL": "champions-league",
    "color": "#ff0000",
    "type": 1
}]
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
id | true | Integer | | Key of column use as key for Standing rows
name | true | String |  | Destination competition name
color | true | String |  | Destination display color
type | true | Integer | ??????? | Destination's type
