# Entities

## Sport

```json
{
     "id": 1,
     "name": "Football"
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
    "liveGames": 2,
    "totalGames": 5
}
```

Parameter | required | type | Options  | Description
--------- | ------- |  ----- |  ----- | ---------
id | true | Integer |  | Country's id
name | true | String | | Country's name
liveGames | false | Integer |  | Live games for current country
totalGames | false | Integer |  | Total games for current country

## League

```json
{
      "id": 1,
      "name": "World Cup",
      "hasTable": true,
      "countryId": 11,
      "liveGames": 2,
      "totalGames": 5
}
```

Parameter | required | type | Options  | Description
--------- | ------- | ----- | ----- | ---------
id | true | Integer |  | League's id
name | true | String | | League's name
countryId | true | Integer | | League's countryId
hasTable | false | Boolean | | If league has table data
liveGames | false | Integer | | Live games for current competition
totalGames | false | Integer | | Total games for current competition

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
                "status": "started",
                "statusText": "ET",
                "gameTimeText": "109'",
                "datetime":{
                                "timeStamp": 12334423423423,
                                "dateText": "16/07/2018",
                                "timeText": "21:00 AM"
                            },
                "isFutureGame": false,
                "description": "Barcelona has won 5-3 after Penalties",
                "aggregatedText": "aggregated 4-2",
                "lmt": "https://lmt.365scores.com/SportRadar?gameId=13307987&langId=1&timeZoneId=15",
                "venue": {
                    "name": "Saint-Petersburg Stadium",
                    "capacity": "20,000",
                    "attendance": "19,999",
                    "googlePlaceId": 1
                },
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
                                     "hasFieldPositions": true
                                },
                     "members": [{
                                    "status": 1,
                                    "id": 6688408,
                                    "athleteId": 26574,
                                    "name": "Moshe Cohen",
                                    "shortName": "MoC",
                                    "JerseyNumber": 6,
                                    "statusText": "Rising star",
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
                                    "substitude": {
                                                     "playerId": 22,
                                                     "time": 90.0,
                                                     "type": 1,
                                                     "status": 1
                                                  }
                                }],
                     "statistics": [{
                                        "id": 1,
                                        "name": "fouls",
                                        "categoryId": 3,
                                        "categoryName": "Posessions",
                                        "value": 2,
                                        "valuePercentage": 2
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
                                     "hasFieldPositions": true
                                },
                     "members": [{
                                    "status": 1,
                                    "id": 6688408,
                                    "athleteId": 26574,
                                    "name": "Moshe Cohen",
                                    "shortName": "MoC",
                                    "JerseyNumber": 6,
                                    "statusText": "Rising star",
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
                                    "substitude": {
                                                     "playerId": 22,
                                                     "time": 90.0,
                                                     "type": 1,
                                                     "status": 1
                                                  }
                                }],
                     "statistics": [{
                                        "id": 1,
                                        "name": "fouls",
                                        "categoryId": 3,
                                        "categoryName": "Posessions",
                                        "value": 2,
                                        "valuePercentage": 2
                                   }]
                },
                "countryId": 2, 
                "season": {
                     "id": 1,
                     "name": "Season 1"
                },
                "stage": {
                     "id": 1,
                     "name": "Stage 1"
                },
                "group": {
                     "id": 1,
                     "name": "Group 1"
                },
                "competitionId": 1,
                "sportId": 1,
                "round": {
                     "id": 1,
                     "name": "Round 1"
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
                    "next": {
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
                    "subPlayerId" :6688100,
                    "event": {
                                "id": 1,
                                "name": "Goal"
                             }
                }],
                "eventsCategories": 2,
                "officials": [{
                                    "status": 1,
                                    "id": 6688408,
                                    "name": "Moshe Cohen",
                                    "shortName": "MoC",
                                    "JerseyNumber": 6,
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
    "leagues": [{
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

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
game | true | Object |  | Full game data
id | true | Integer |  | Game's id
lastUpdateId | true | Integer |  | Game's update id for delta fetching
ttl | true | Integer |  | Seconds for next game request 
status | true | String | 'scheduled' 'started' 'ended' | Game's Status
statusText | false | String | | Game's Status formatted text
gameTimeText | false | String | | Game's Status formatted text
datetime | true | Object | | [Description](#datetime)
isFutureGame | false | Boolean |  | if true don't display game
description | false | String |  | Game's description
aggregatedText | false | String |  | Aggregate score formatted text
lmt | false | String |  | if exist use iframe with the lmt url
venue | false | Object | | [Description](#venue)
homeCompetitor | true | Object | | [Description](#competitor)
awayCompetitor | true | Object | | [Description](#competitor) 
season | false | Object | | Game's season (league season)
stage | false | Object | | Game's stage (use on qualification competition)
season | false | Object | | Game's season 
group | false | Object | | Game's group of competition
round | false | Object | | season's round
competitionId | true | Integer | | Game's competition
sportId | true | Integer | | Game's sport type
odds | false | Object | | [Description](#odds)
previousMeetings | false | Array | | Array of gameIds for previous meeting between current competitors
events | false | Array | | Array of match events
eventsCategories | false | Integer | | ?????????????????????
officials | false | Array | | Array of game's officials
tvNetworks | false | Array | | Array of tv networks
bookmakers | false | Array | | Array of Bookmakers for odds -> lines
 

## Partial Game

```json
{
  "description": "Future api response for games:",
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
   "leagues":[{
                         "id": 1,
                         "name": "World Cup",
                         "hasTable": true,
                         "countryId": 11
                   }],
   "games": [{
             "id": 1,
             "datetime":{
                 "timeStamp": 12334423423423,
                 "dateText": "16/07/2018",
                 "timeText": "21:00 AM"
             },
             "status": "started",
             "statusText": "ET",
             "gameTimeText": "109'",
             "isFutureGame": false,
             "lineupsStatus": 1,
             "hasTVNetworks": false,
             "hasBetsTeaser": false,
             "description": "Barcelona has won 5-3 after Penalties",
             "aggregatedText": "aggregated 4-2",
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
             },
             "sportId": 1,
             "competitionId": 1,
             "round": {
                          "id": 1,
                          "name": "Round One"
                      }
       }]
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
lastUpdateId | true | Integer |  | Game's update id for delta fetching
ttl | true | Integer |  | Seconds for next game request 
games | true | Array |  | Array of partial games
id | true | Integer |  | Game's id
datetime | true | Object | | [Description](#datetime)
status | true | String | 'scheduled' 'started' 'ended' | Game's Status
statusText | false | String | | Game's Status formatted text
gameTimeText | false | String | | Game's Status formatted text
isFutureGame | false | Boolean |  | if true don't display game
lineupsStatus | true | Integer | 0 - none, 1 - partial, 2 - full | Game's lineups status (icon display functionality)
hasTVNetworks | false | Boolean | | if games have tv networks (icon display functionality)
hasBetsTeaser | false | Boolean | | if games have odds (icon display functionality)
description | false | String |  | Game's description
aggregatedText | false | String |  | Aggregate score formatted text
homeCompetitor | true | Object | | [Description](#competitor)
awayCompetitor | true | Object | | [Description](#competitor)
competitionId | true | Integer | | Game's competition
sportId | true | Integer | | Game's sport type
round | false | Object | | Game part of round 


## Competitor

```json
{
    "id": 1,
    "name": "Argentina",
    "score": 2,
    "aggregatedScore": 4,
    "isQualified": false,
    "isWinner": false,
    "redCards": 0,
    "countryId": 11
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
id | true | Integer |  | Competitor's id
name | true | String |  | Competitor's name
score | false | Integer |  | Competitor's score for specific game
aggregatedScore | false | Integer |  | Competitor's aggregatedScore for specific game
isQualified | false | Boolean |  | If competitor qualified to next stage
isWinner | false | Boolean |  | If competitor qualified to next stage
redCards | false | Integer |  | If competitor qualified to next stage
countryId | true | Integer |  | Competitor's country

## Datetime

```json
{
    "timeStamp": 12334423423423,
    "dateText": "16/07/2018",
    "timeText": "21:00 AM"
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
timeStamp | true | Integer |  | UNIX Time stamp
dateText | true | String |  | Date formatted by country and timezone
timeText | true | String |  | Time formatted by country and timezone

## Lineups

```json
{
     "status": "Not Confirmed",
     "formation": "4-4-2",
     "hasFieldPositions": true
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
status | true | Integer | ??? | Lineup's status
formation | false | String |  | Competitor's lineups formation
hasFieldPositions | false | Boolean |  | Flag if members has field positions

## Members

```json
[{
    "status": 1,
    "id": 6688408,
    "athleteId": 26574,
    "name": "Moshe Cohen",
    "shortName": "MoC",
    "JerseyNumber": 6,
    "statusText": "Rising star",
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
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
status | true | Integer | 0 - Not playing, 1 - Doubtful, 2 - playing | Member's status
id | true | Integer | | Member's id (id for specific game)
athleteId | true | Integer | | Member's id (athlete entity id)
name | true | String | | Member's name
shortName | false | String | | Member's nickname
JerseyNumber | false | Integer | | Member's jersey number

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

## Substitute

```json
{
   "playerId": 22,
   "time": 90.0,
   "type": 1,
   "status": 1
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
playerId | true | Integer | | Substitute player's id
time | true | String | | Substitute time
type | false | String | ?????? | Substitution type
status  | false | String | ?????? | ???????????

## Statistics

```json
[{
    "id": 1,
    "name": "fouls",
    "categoryId": 3,
    "categoryName": "Posessions",
    "value": "2",
    "valuePercentage": 2
}]
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
id | true | Integer | | Statistic's id
name | true | String | | Statistic's name
categoryId | true | Integer | | Statistics need to be group by category id 
categoryName | true | String | ?????? | Substitution type
status  | true | Integer | ?????? | ???????????
value  | true | String | ?????? | Value of current statistic
percentage  | false | Double | ?????? | Percentage from away and home current statistic


## Odds

```json
{
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
    "oldRate": "1.10",
    "kickOffRate": "1.25",
    "num": 1
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
rateOptions | true | Object | | All supported rate types
oldRate | false | Double | | if rate changes saving old rate for trend (Decimal)
kickOffRate | false | Double | | the rate when the game is startting (Decimal)
num | true | Integer | 0-2 | Rate label 0 - 'X', 1 - '1', 2 - '2'

## Events

```json
[{
    "index": 1,
    "time": "30",
    "playerId": 6688408,
    "subPlayerId" :6688100,
    "isMajor": true,
    "event": {
                "id": 1,
                "name": "Goal"
             }
}]
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
index | true | Object | | Event index on display 
time | true | String | | Event time
playerId | true | Integer | | Main player for the event
subPlayerId | false | Integer | | Sub player 
event | true | Object |  | Event Object with id and name
isMajor | false | Boolean |  | If event are major (filter top)

## Officials

```json
[{
      "status": 1,
      "id": 6688408,
      "name": "Moshe Cohen",
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
}]
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
key | true | String | | Key of column use as key for table rows
name | false | Integer |  | Column display name 
major | false | Integer |  | If show on small view

## Rows

```json
[{
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
    "destinationId": 1,
    "destinationGuaranteed": true,
    "isWinner": true
}]
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
competitor | true | Object | | [Description](#competitor)
group | false | Integer |  | Use if competition has groups, id and display name
gamesPlayed | true | Integer |  | Competitor games played on current league
gamesWon | true | Integer |  | Competitor wins on current league
gamesLost | true | Integer |  | Competitor loses on current league
gamesEven | true | Integer |  | Competitor draws on current league
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
position | true | Integer |  | Position on table (row number)
trend | false | Integer |  | On live game if team goes up or down on table 
recentForm | false | Array |  | trend for recent matches on current league
destinationId | false | Integer |  | Destination by position
destinationGuaranteed | false | Boolean |  | If Destination guaranteed for current competitor
isWinner | false | Boolean |  | If current competitor won the league title

### Destinations

```json
[{
    "id": 1,
    "name": "Champions League",
    "color": "#ff0000",
    "type": 1
}]
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
id | true | Integer | | Key of column use as key for table rows
name | true | String |  | Destination competition name
color | true | String |  | Destination display color
type | true | Integer | ??????? | Destination's type
