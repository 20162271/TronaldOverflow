# TronaldOverflow

## Description
- The system shows a list of daily generated quotes of Donald Trump. The system allows to rate (Like / Dislike) the quote for users.

## Entity definition
- The main entity of thi WEB systems is a Quote.
- Entity has these attributes:
    - ID - String
    ```
       - No Restrictions
    ```
    - Value - String, Quote main text.
    ```
       - No Restrictions
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
- APIs methods (used by this WEB system):
    - GET Random Quote:
    ```
        - GET https://api.tronalddump.io/random/quote
    ```
    - GET Random Meme:
    ```
        - GET https://api.tronalddump.io/random/meme
    ```

## UI definition
```
- https://wireframe.cc/HECnkA
```
