# Search

## Search Entities

```json
[
    "leagues" : [{
                           "id": 595,
                           "name": "Copa America",
                           "hasTable": true,
                           "sportId": 1,
                           "countryId": 11
                      },
                      {
                           "id": 121,
                           "name": "LaLiga",
                           "hasTable": true,
                           "sportId": 1,
                           "countryId": 12
                      }],
    "competitors" : [{
                         "id": 1,
                         "name": "Argentina",
                         "countryId": 11,
                         "sportId": 1,
                    }]
    "athletes" : [],
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
]
```

### HTTP Request

`GET https://api.365scores.com/search`

### Query Parameters

Parameter | required | Default | Example | Options | Description
--------- | ------- | ----------- | --- | ----- | ---------
query | true | '' | 'Barce' | | Return all entities that include the query
filter | false | all | 'leagues' | 'all' 'leagues' 'competitors' 'athletes' | Filter the results

### Examples

`GET https://api.365scores.com/search?query=Barcelona&filter=competitors`

<aside class="notice">
Don't forget general parameters.
</aside>
