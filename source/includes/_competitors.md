# Competitors

## Get Competitors

```json
{
   "countries":[
      {
         "id":12,
         "name":"Spain"
      },
      {
         "id":112,
         "name":"Israel"
      }
   ],
   "sports":[
      {
         "id":1,
         "name":"Football"
      }
   ],
   "competitions":[{
                    "id": 595,
                    "name": "Copa America",
                    "hasStanding": true,
                    "sportId": 1,
                    "countryId": 1,
                    "liveGames": 2,
                    "totalGames": 5
               },
               {
                    "id": 11,
                    "name": "LaLiga",
                    "hasStanding": true,
                    "sportId": 1,
                    "countryId": 12,
                    "liveGames": 2,
                    "totalGames": 5
               }
   
   ],
   "competitors":[
      {
         "id":132,
         "name":"Barcelona",
         "sportId":1,
         "countryId":1,
         "competitions":[1, 12]
      },
      {
         "id":562,
         "name":"Maccabi Haifa",
         "sportId":1,
         "countryId":112,
         "competitions":[42]
         
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
