---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - response

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the 365Scores Web API documentation! 

# General usage

### General root

`GET https://api.365scores.com/`

### General Query Parameters

Parameter | required | Default | Example | Description
--------- | ------- | ----------- | --- |  ---------
langId | false | 1 | Translate all strings to requested language.
timezone | false | '' | Set date and time by the timezone.
userCountryId | false | 31 | Modify data by requested country.
appType | false | ''  | Modify data by app type

<aside class="notice">
Attach all parameters to all API requests.
</aside>

# Countries

## Get All Countries

```json
[
    {
        "id": 1,
        "name": "Argentina",
        "liveGames": 2,
        "totalGames": 5
    },
    {
        "id": 2,
        "name": "Brazil",
        "liveGames": 2,
        "totalGames": 5
    }
]
```

This endpoint retrieves all countries.

### HTTP Request

`GET https://api.365scores.com/countries`

<aside class="notice">
Don't forget general parameters.
</aside>


# Games

## Get All Games

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
             "date": "16/07/2018", 
             "status": "started",
             "statusText": "ET 109'",
             "time": "21:00",
             "timePostfix": "AM",
             "isFutureGame": false,
             "lineupsStatus": 1,
             "hasTVNetworks": false,
             "hasMissingPlayers": false,
             "hasBetsTeaser": false,
             "description": "Barcelona has won 5-3 after Penalties",
             "aggregatedText": "aggregated",
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

This endpoint retrieves all games.

Return only partial game data.

### HTTP Request

`GET https://api.365scores.com/games`

### Query Parameters

Parameter | required | Default | Example | Options | Description
--------- | ------- | ----------- | --- | ----- | ---------
sports | false | '' | 1,2 | 1-9 | Return games from specific sports
countryId | false | 1 | 6 | | Sort competition priority by country
lastUpdateId | false | '' | 848293001 | | Return only updated properties from the current lastUpdateId 
startDate | false |  current date | 07/08/2018 |  | Return games from specific date(included)
endDate | false |  current date | 09/08/2018 |  |  Return games until specific date(included)
leagues | false | '' | 5930,11 | | Return games for specific leagues
competitors | false | '' | 131,132 | | Return games for specific competitors
gameIds | false | '' | 131132 | | Return specific games by ids
filter | false | '' | 'fixtures' | 'fixtures' 'recent' 'results' | Filter games

### Examples

####dashboard

`GET https://api.365scores.com/games?sport=1,2&countryId=12&lastUpdateId=848293001&startDate=07/08/2018&endDate=07/08/2018`

####competition dashboard

`GET https://api.365scores.com/games?leagues=5930&countryId=12&lastUpdateId=848293001&filter=results`

####competitor dashboard

`GET https://api.365scores.com/games?competitors=131&leagues=12&countryId=12&lastUpdateId=848293001`

####partial games

`GET https://api.365scores.com/games?gameIds=123123,123456,165432`

<aside class="notice">
Don't forget general parameters.
</aside>

## Get Game Center

```json
{
    "game": {
                "id": 1,
                "status": "started",
                "statusText": "טרם החל",
                "date": "16/07.2018",
                "time": "21:00",
                "timePostfix": "AM",
                "isFutureGame": false,
                "description": "Barcelona has won 5-3 after Penalties",
                "aggregatedText": "aggregated",
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
                                    "statusText": "כוכב עולה",
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
                                    "statusText": "כוכב עולה",
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
                "recentMatches": ["gameIds"],
                "events": [{
                    "index": 1,
                    "time": "30",
                    "playerId": 6688408,
                    "event": {
                                "id": 1,
                                "name": "גול - שער שדה"
                             }
                }],
                "eventsCategories": 2,
                "watchOnline": {},
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

Return full game data.

### HTTP Request

`GET https://api.365scores.com/game/:gameId`


### Query Parameters

Parameter | required | Default | Example | Options | Description
--------- | ------- | ----------- | --- | ----- | ---------
lastUpdateId | false | '' | 848293001 | | Return only updated properties from the current lastUpdateId 

### Examples

`GET https://api.365scores.com/game/123123?lastUpdateId=848293001`

<aside class="notice">
Don't forget general parameters.
</aside>

# Leagues

## Get All Leagues

```json
{
    "countries":[{
                     "id": 1,
                     "name": "Argentina"
                },
                {
                     "id": 12,
                     "name": "Spain"
                }],
    "sports":[{
                    "id": 1,
                    "name": "Football"
             }],
     "leagues": [{
                     "id": 595,
                     "name": "Copa America",
                     "hasTable": true,
                     "sportId": 1,
                     "countryId": 1
                },
                {
                     "id": 121,
                     "name": "LaLiga",
                     "hasTable": true,
                     "sportId": 1,
                     "countryId": 12
                }]
}
```

This endpoint retrieves all leagues.

### HTTP Request

`GET https://api.365scores.com/leagues`

### Query Parameters

Parameter | required | Default | Example | Options | Description
--------- | ------- | ----------- | --- | ----- | ---------
leagueIds | false | '' | 12 | | Return specific leagues
lastUpdateId | false | '' | 848293001 | | Return only updated properties from the current lastUpdateId 

### Examples

`GET https://api.365scores.com/leagues?leagueIds=12,13,123`


<aside class="notice">
Don't forget general parameters.
</aside>

## Get Top Leagues

```json
{
    "countries":[{
                     "id": 1,
                     "name": "Argentina"
                },
                {
                     "id": 12,
                     "name": "Spain"
                }],
    "sports":[{
                    "id": 1,
                    "name": "Football"
             }],
     "leagues": [{
                     "id": 595,
                     "name": "Copa America",
                     "hasTable": true,
                     "sportId": 1,
                     "countryId": 1
                },
                {
                     "id": 121,
                     "name": "LaLiga",
                     "hasTable": true,
                     "sportId": 1,
                     "countryId": 12
                }]
}
```

This endpoint retrieves top leagues.

### HTTP Request

`GET https://api.365scores.com/leagues/top`

<aside class="notice">
Don't forget general parameters.
</aside>


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

