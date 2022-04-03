# COMP 3040 Assignment 3 

## API descriptions
Our group will be working on Restaurant APIs, our main focus would be to create API endpoints related to restaurants that are located in Manitoba. Here is a list of 3 API endpoints that our API would serve:


## 1. List all the restaurants which provide delivery through a certain method.
### Endpoint
> https://manitoba.restaurants/api/delivery/?delivery_method=ubereats

### Parameter
- `delivery_method`: The type of delivery method you want to search for.
  - Examples: `ubereats`, `skipthedishes`, `doordash`, `inhouse`

### Description of Resources
```js
{
  "result": [
    {
      "name": "<String>", // The name of the restaurant
      "city": "<String>", // City where restaurant is located
      "delivery_methods": "<List[<String>]>", // Supported delivery methods
      "category": "<List[<String>]>" // Food categories served at this restaurant
    },
    ...
  ]
}
```

### Sample Response

This endpoint returns a list of restaurants that support the given delivery method.

```js
{
  "result": [
    {
      "name": "McDonalds",
      "city": "Winnipeg",
      "delivery_methods": ["ubereats", "skipthedishes", "doordash", "inhouse"],
      "category": ["chinese", "japanese", "continental", "indian"]
    },
    ...
  ]
}
```
## 2. List all kinds of food they serve.

### Endpoint
> https://manitoba.restaurants/api/food/?category=Chinese


### Parameter
- `category`: The kind of food you want to search for.
  - Examples: `Chinese`, `Japanese`, `Continental`, `Indian`

### Description of Resources
```js
{
  "result": [
    {
      "name": "<String>", // The name of the restaurant
      "city": "<String>", // City where restaurant is located
      "delivery_methods": "<List[<String>]>", // Supported delivery methods
      "category": "<List[<String>]>" // Food categories served at this restaurant
    },
    ...
  ]
}
```

### Response

This endpoint returns a list of restaurants that serve the given kind of food.

```js
{
  "result": [
    {
      "name": "McDonalds",
      "city": "Winnipeg",
      "category": ["chinese", "japanese", "continental", "indian"],
      "delivery_methods": ["ubereats", "skipthedishes", "doordash", "inhouse"]
    },
    ...
  ]
}
```
## 3. All the restaurants in a **particular city**. *(e.g:- Brandon, Winnipeg, etc.)*

### Endpoint
> https://manitoba.restaurants/api/city/?name=winnipeg

### Parameter
- `name` : The name of the city which will return all the restaurants located in that city.
  - Examples: `winnipeg`, `brandon`, `selkirk`

### Description of Resources
```js
{
  "result": [
    {
      "name": <String>, // The name of the city
      "restaurants": <String>, // The name of the restaurant 
    },
    ...
  ]
}
```
### Sample Response
A JSON object that will contain all the restaurant names in a particular city.
```js
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
