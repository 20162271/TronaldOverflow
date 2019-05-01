# TronaldOverflow

## Description
- The system shows a list of daily generated quotes of Donald Trump. The system allows to rate (Like / Dislike) the quote for users.

## Entity definition
- The main entity of this WEB systems is a Quote.
- Entity has these attributes:
    - ID - String
    ```
       - Joi.string().max(22);
    ```
    - Value - String, Quote main text.
    ```
       - Joi.string().max(1000);
    ```
    - Source URL - String, which defines URL to the source of the Quote.
    ```
       - No Restrictions
    ```
    - Rating - Number, which defines rating points, given by users, of the specific Quote.
    ```
       - Joi.number().min(-10000).max(10000);
    ```
    - Created At - ISO 8601 date string, which defines when the Quote was published by the Author.
    ```
       - No Restrictions
    ```
    - Appeared_At - ISO 8601 date string, which defines when the Quote was generated using API.
    ```
       - Joi.date().min(“now”).max(“now”);
    ```
    - Tags - String, which defines tags of the specific Quote.
    ```
       - No Restrictions
    ```

## API definition
- The main information that this WEB system GET from API is Random Quote and Random Meme.
- API methods (used by this WEB system):
    - GET Random Quote:
        ```
        - GET https://api.tronalddump.io/random/quote
        ```
        - 404 {"status":404,"message":"No route found"}
    - GET Random Meme:
        ```
        - GET https://api.tronalddump.io/random/meme
        ```
        - 404 {"status":404,"message":"No route found"}
    - GET Daily Quote list:
        ```
        - GET /api/quote?size=:size
        ```
        - 400 {"status":400,"message":"Invalid size"}
    - POST Rating for the specific Quote:
        ```
        - POST /api/quote/:id/rating
        ```
        - 400 {"status":400,"message":"Invalid quote ID"}
        - 403 {"status":403,"message":"Voting ended for this quote"}
    - DELETE User rating for the specific Quote:
        ```
        - DELETE /api/quote/:id/rating
        ```
        - 400 {"status":400,"message":"Ivalid quote ID"}
        - 403 {"status":403,"message":"Voting ended for this quote"}
    - GET Daily meme:
        ```
        - GET /api/quote/:id/meme
        ```
        - 400 {"status":400,"message":"Ivalid meme ID"}

## UI definition
```
- https://wireframe.cc/HECnkA
```
