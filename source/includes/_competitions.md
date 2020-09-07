# Competitions

## Get All Competitions

```json
{
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
    "sports":[{
                    "id": 1,
                    "name": "Football"
             }],
     "competitions": [{
                     "id": 595,
                     "name": "Copa America",
                     "hasStandings": true,
                     "hasStandingsGroups": true,
                     "sportId": 1,
                     "countryId": 1,
                     "liveGames": 2,
                     "totalGames": 5,
                     "isTop": true
                },
                {
                     "id": 121,
                     "name": "LaLiga",
                     "hasStanding": true,
                     "hasStandingsGroups": true,
                     "sportId": 1,
                     "countryId": 12,
                     "liveGames": 2,
                     "totalGames": 5,
                     "isTop": true

                }]
}
```

This endpoint retrieves all competitions.

### HTTP Request

`GET https://ws.365scores.com/web/competitions`

### Query Parameters

Parameter | required | Default | Example | Options | Description
--------- | ------- | ----------- | --- | ----- | ---------
competitions | false | '' | 12 | | Return specific competitions
sports | false | '' | 1 | | Filter competitions by sport 
countries | false | '' | 12 | | Filter competitions by country  

### Examples

get Standings by id

`GET https://ws.365scores.com/web/competitions/?competitions=12,13,123`

get Standings for specific countries

`GET https://ws.365scores.com/web/competitions/?countryId=12,13`


<aside class="notice">
Don't forget general parameters.
</aside>

## Get Top Competitions

```json
{
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
    "sports":[{
                    "id": 1,
                    "name": "Football"
             }],
     "competitions": [{
                     "id": 595,
                     "name": "Copa America",
                     "hasStanding": true,
                     "hasStandingGroups": true,
                     "sportId": 1,
                     "countryId": 1,
                     "liveGames": 2,
                     "totalGames": 5,
                     "imgVer": 1,
                     "isTop": true
                },
                {
                     "id": 121,
                     "name": "LaLiga",
                     "hasStanding": true,
                     "hasStandingGroups": true,
                     "sportId": 1,
                     "countryId": 12,
                     "liveGames": 2,
                     "totalGames": 5,
                     "imgVer": 1,
                     "isTop": true
                }]
}
```

This endpoint retrieves top competitions.

### HTTP Request

`GET https://ws.365scores.com/web/competitions/top?limit=10`

### Query Parameters

Parameter | required | Default | Example | Options | Description
--------- | ------- | ----------- | --- | ----- | ---------
limit | false | '' | 10 | | Return limited size of competitions

<aside class="notice">
Don't forget general parameters.
</aside>
