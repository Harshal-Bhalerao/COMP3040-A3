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

Response: A JSON object containing restaurants that support the delivery method specified.
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
- List all **kinds of food** they serve. *(e.g:- Chinese, Japanese, Continental, Indian, Halal, etc. )*
- All the restaurants in a **particular city**. *(e.g:- Brandon, Winnipeg, etc.)*
