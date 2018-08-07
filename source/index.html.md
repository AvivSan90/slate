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

`GET http://webwidgets.365scores.com/`

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

`GET http://webwidgets.365scores.com/countries`


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
   "competitions":[{
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

### HTTP Request

`GET http://webwidgets.365scores.com/games`

### Query Parameters

Parameter | required | Default | Example | Options | Description
--------- | ------- | ----------- | --- | ----- | ---------
sports | false | '' | 1,2 | 1-9 | Return games from specific sports
countryId | false | 1 | 6 | | Sort competition priority by country
updateId | false | '' | 848293001 | | Return only updated properties from the current updateId 
startDate | false |  current date  | | 07/08/2018 | Return games from specific date(included)
endDate | false |  current date | | 09/08/2018 | Return games until specific date(included)
competitions | false | '' | 5930,11 | | Return games for specific competitions
competitors | false | '' | 131,132 | | Return games for specific competitors
filter | false | '' | 'fixtures' | 'fixtures' 'recent' 'results' | Filter games
