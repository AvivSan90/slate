# Competitions

## Get All Competitions

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
     "competitions": [{
                     "id": 595,
                     "name": "Copa America",
                     "hasStandings": true,
                     "hasStandingsGroups": true,
                     "sportId": 1,
                     "countryId": 1,
                     "liveGames": 2,
                     "totalGames": 5
                },
                {
                     "id": 121,
                     "name": "LaLiga",
                     "hasStanding": true,
                     "hasStandingsGroups": true,
                     "sportId": 1,
                     "countryId": 12,
                     "liveGames": 2,
                     "totalGames": 5
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
                     "imgVer": 1
                },
                {
                     "id": 12,
                     "name": "Spain",
                     "imgVer": 1
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
                     "imgVer": 1
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
                     "imgVer": 1
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
