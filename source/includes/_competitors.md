# Competitors

## Get Competitors

```json
{
   "countries":[
      {
         "id":12,
         "name":"Spain",
         "imgVer": 1
      },
      {
         "id":112,
         "name":"Israel",
         "imgVer": 1
      }
   ],
   "sports":[
      {
         "id":1,
         "name":"Football",
         "imgVer": 1
      }
   ],
   "competitions":[{
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
                    "id": 11,
                    "name": "LaLiga",
                    "hasStanding": true,
                    "hasStandingGroups": true,
                    "sportId": 1,
                    "countryId": 12,
                    "liveGames": 2,
                    "totalGames": 5,
                    "imgVer": 1
               }
   
   ],
   "competitors":[
      {
         "id":132,
         "name":"Barcelona",
         "sportId":1,
         "countryId":1,
         "competitions":[1, 12],
         "imgVer": 1
      },
      {
         "id":562,
         "name":"Maccabi Haifa",
         "sportId":1,
         "countryId":112,
         "competitions":[42],
         "imgVer": 1
         
      }
   ]
}
```

This endpoint retrieves competitors based on id's.

### HTTP Request

`GET https://ws.365scores.com/web/competitors`

### Query Parameters

Parameter | required | Default | Example | Options | Description
--------- | ------- | ----------- | --- | ----- | ---------
competitors | true | '' | 12 | | Return specific competitions

### Examples

get competitors by id

`GET https://ws.365scores.com/web/competitors/?competitors=132,562`


<aside class="notice">
Don't forget general parameters.
</aside>
