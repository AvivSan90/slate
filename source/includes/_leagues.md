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
                     "countryId": 1,
                     "liveGames": 2,
                     "totalGames": 5
                },
                {
                     "id": 121,
                     "name": "LaLiga",
                     "hasTable": true,
                     "sportId": 1,
                     "countryId": 12,
                     "liveGames": 2,
                     "totalGames": 5
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
sportId | false | '' | 1 | | Filter leagues by sport 
countryId | false | '' | 12 | | Filter leagues by country  

### Examples

get tables by id

`GET https://api.365scores.com/leagues?leagueIds=12,13,123`

get tables for specific countries

`GET https://api.365scores.com/leagues?countryId=12,13`


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
                     "countryId": 1,
                     "liveGames": 2,
                     "totalGames": 5
                },
                {
                     "id": 121,
                     "name": "LaLiga",
                     "hasTable": true,
                     "sportId": 1,
                     "countryId": 12,
                     "liveGames": 2,
                     "totalGames": 5
                }]
}
```

This endpoint retrieves top leagues.

### HTTP Request

`GET https://api.365scores.com/leagues/top`

<aside class="notice">
Don't forget general parameters.
</aside>
