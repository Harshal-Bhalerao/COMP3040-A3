# COMP 3040 Assignment 3 
## Part 1: Group General Description of API

### API descriptions
Group 9 will be working on Restaurant APIs, our main focus would be to list all the restaurants in Manitoba by the kind of food they serve. 

### Endpoints:
#### List all the restaurants which provide delivery through a certain method.
> https://manitoba.restaurants/api/delivery/?method=ubereats

Parameter:
- `method`: The type of delivery method you want to search for.
  - Examples: `ubereats`, `skipthedishes`, `doordash`, `inhouse`

Response: 

This endpoint returns a list of restaurants that support the given delivery method.

```json
{
  "result": [
    {
      "name": "McDonalds",
      "city": "Winnipeg",
      "delivery_methods": ["ubereats", "skipthedishes", "doordash", "inhouse"]
    },
    ...
  ]
}
```
### List all kinds of food they serve.

> https://manitoba.restaurants/api/food/?category=Chinese


Parameter:
- `category`: The kind of food you want to search for.
  - Examples: `Chinese`, `Japanese`, `Continental`, `Indian`

Response:

This endpoint returns a list of restaurants that serve the given kind of food.

```json
{
  "result": [
    {
      "name": "McDonalds",
      "city": "Winnipeg",
      "category": ["chinese", "japanese", "continental", "indian"]
    },
    ...
  ]
}
```
- All the restaurants in a **particular city**. *(e.g:- Brandon, Winnipeg, etc.)*
> https://manitoba.restaurants/api/city/?name=winnipeg

Parameter: 
- `name` : The name of the city which will return all the restaurants located in that city.
- Examples: `winnipeg`, `brandon`

Response: 
A JSON object that will contain all the restaurant names in a particular city.

```json
{
  "result": [
    {
      "name": "winnipeg",
      "restaurants": ["mcdonalds", "burger king", "shwarma khan", "clay oven"]
    },
    ...
  ]
}
```