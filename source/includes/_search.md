# Search

## Search Entities

```json
[
    "competitions" : [{
                           "id": 595,
                           "name": "Copa America",
                           "nameForURL": "copa-america",
                           "hasStanding": true,
                           "hasStandingGroups": true,
                           "sportId": 1,
                           "countryId": 11
                      },
                      {
                           "id": 121,
                           "name": "LaLiga",
                           "nameForURL": "laliga",
                           "hasStanding": true,
                           "hasStandingGroups": true,
                           "sportId": 1,
                           "countryId": 12
                      }],
    "competitors" : [{
                         "id": 1,
                         "name": "Argentina",
                         "nameForURL": "argentina",
                         "countryId": 11,
                         "sportId": 1,
                    }]
    "athletes" : [],
    "sport":[{
               "id": 1,
               "name": "Football",
               "nameForURL": "football"
           }],
    "countries":[{
                     "id": 11,
                     "name": "Argentina",
                     "nameForURL": "argentina"
               },
               {
                     "id": 12,
                     "name": "Brazil",
                     "nameForURL": "brazil"
                 }],
]
```

### HTTP Request

`GET https://ws.365scores.com/web/search`

### Query Parameters

Parameter | required | Default | Example | Options | Description
--------- | ------- | ----------- | --- | ----- | ---------
query | true | '' | 'Barce' | | Return all entities that include the query
filter | false | all | 'competitions' | 'all' 'competitions' 'competitors' 'athletes' | Filter the results

### Examples

`GET https://ws.365scores.com/web/search?query=Barcelona&filter=competitors`

<aside class="notice">
Don't forget general parameters.
</aside>
