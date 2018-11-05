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
      "hasStanding": true,
      "countryId": 11,
      "sportId": 11,
      "liveGames": 2,
      "totalGames": 5
}
```

Parameter | required | type | Options  | Description
--------- | ------- | ----- | ----- | ---------
id | true | Integer |  | League's id
name | true | String | | League's name
countryId | true | Integer | | League's countryId
sportId | true | Integer | | League's sportId
hasStanding | false | Boolean | | If league has Standing data
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
                "statusGroup": 1,
                "statusText": "ET",
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
                "datetime":{
                    "timeStamp": 12334423423423,
                    "dateText": "16/07/2018",
                    "timeText": "21:00 AM"
                },
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
statusGroup | true | Integer | 1 - 'Anticipated', 2 - 'Scheduled', 3 - 'Live', 4 - 'Finished' | Game's Status
statusText | false | String | | Game's Status formatted text
showCountdown | false | Boolean | | if game card should show countdown
gameTime | false | Integer | | Game's time 
gameTimeDisplay | false | String | | Game's time formatted text
gameTimeAndStatusDisplayType | false | Integer | | Enum to present gameTimeDisplay or/and statusText
hasLineups | false | Boolean | | if game have full lineups
hasMissingPlayers | false | Boolean | | if game have only missing player lineups
hasFieldPositions | false | Boolean | | if game have positions for lineups yard
datetime | true | Object | | [Description](#datetime)
isFutureGame | false | Boolean |  | if true don't display game
description | false | String |  | Game's description
aggregatedText | false | String |  | Aggregate score formatted text
lmt | false | String |  | if exist use iframe with the lmt url
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
                         "hasStanding": true,
                         "countryId": 11
                   }],
   "games": [{
             "id": 1,
             "statusGroup": 1,
             "statusText": "ET",
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
             "hasFieldPositions": true,
             "hasLineups": true,
             "description": "Barcelona has won 5-3 after Penalties",
             "aggregatedText": "aggregated 4-2",
             "datetime":{
                 "timeStamp": 12334423423423,
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
datetime | true | Object |  | [Description](#datetime)
statusGroup | true | Integer | 1 - 'Anticipated', 2 - 'Scheduled', 3 - 'Live', 4 - 'Finished' | Game's Status
statusText | false | Integer | | Game's time
gameTimeDisplay | false | String | | Game's time formatted text
gameTime | false | Integer | | Game's time formatted text
isFutureGame | false | Boolean |  | if true don't display game
hasLineups | false | Boolean | | if game have full lineups
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
    "score": 2,
    "aggregatedScore": 4,
    "isQualified": false,
    "isWinner": false,
    "redCards": 0,
    "countryId": 11,
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
lineups | false | Array | | [Description](#lineups)

## Stage

```json
{
    "id": 7,
    "name": "Halftime",
    "shortName": "HT",
    "homeCompetitorScore": 0,
    "awayCompetitorScore": 0
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
id | true | Integer |  | stage's id
name | true | String |  | stage's name
shortName | false | String |  | stage's short name
homeCompetitorScore | true | Integer |  | stage's home competitor score
awayCompetitorScore | true | Integer |  | stage's away competitor scored


## Datetime

```json
{
    "msFromEpoch": 12334423423423,
    "dateText": "16/07/2018",
    "timeText": "21:00 AM"
}
```

Parameter | required | type | Options | Description
--------- | ------- |  ----- |  ----- | ---------
msFromEpoch | true | Integer |  | UNIX Time stamp
dateText | true | String |  | Date formatted by country and timezone
timeText | true | String |  | Time formatted by country and timezone

## Lineups

```json
{
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
members | false | Array | | array of lineups members [Description](#lineupsMember)

## gameMember

```json
[{
    "status": 1,
    "id": 6688408,
    "athleteId": 26574,
    "name": "Moshe Cohen",
    "shortName": "MoC",
    "JerseyNumber": 6,
    "statusText": "Rising star",
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
position | true | Integer |  | Position on Standing (row number)
trend | false | Integer |  | On live game if team goes up or down on Standing 
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
id | true | Integer | | Key of column use as key for Standing rows
name | true | String |  | Destination competition name
color | true | String |  | Destination display color
type | true | Integer | ??????? | Destination's type