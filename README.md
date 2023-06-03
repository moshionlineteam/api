# Moshi Online API Documentation

## Endpoint: `https://moshionline.net/api?player=[username]`

Returns information about a player in Moshi Online.

**Parameters:**
- `username` (required): The username of the player.

**Response:**
- `username` (string): The username of the player.
- `monstar` (string): The monstar associated with the player.
- `monster` (string): The monster associated with the player.
- `joined` (integer): The date when the player joined Moshi Online.
- `views` (integer): The number of views the player has.
- `rank` (string): The rank of the player.
- `rocks` (integer): The number of rocks the player has.
- `level` (integer): The level of the player.
- `level_progress` (integer): The progress towards the next level for the player.

**Example Request:**
```
GET https://moshionline.net/api?player=johndoe
```

**Example Response:**
```json
{
  "username": "johndoe",
  "monstar": "Z",
  "monster": "furi",
  "joined": 60000,
  "views": 256,
  "rank": "Member",
  "rocks": 500,
  "level": 5,
  "level_progress": 80
}
```

---

## Endpoint: `https://moshionline.net/api?highscore=[id]`

Returns the highscore information for a specific game in Moshi Online.

**Parameters:**
- `id` (required): The ID of the game. Available IDs are as follows:

| ID  | Game Name                      |
|-----|--------------------------------|
| 1   | Blutterby Field                |
| 2   | En-Gen                         |
| 4   | The undergroup disco           |
| 5   | Ice-Scream                     |
| 6   | Moshling Boshling              |
| 10  | Quack Attack                   |
| 11  | Thump Glump                    |
| 13  | Shouty Shack                   |
| 21  | The Great Moshi Beanstalk      |
| 91  | Blue Jeeper's Flight           |
| 92  | Bug's Big Bounce               |
| 93  | Downhill Dash                  |
| 94  | Octo's Eco Adventure           |
| 95  | Sea Monster Munch              |
| 96  | Ecto's Cave                    |
| 100 | The Daily Challenge            |


**Response:**
- `game` (string): The name of the game.
- `data` (array): An array of highscore objects.
  - `score` (integer): The score achieved.
  - `username` (string): The username associated with the score.
  - `difficulty` (string): The difficulty level of the game.

**Example Request:**
```
GET https://moshionline.net/api?highscore=1
```

**Example Response:**
```json
{
  "game": "Blutterby Field",
  "data": [
    {
      "score": 100,
      "username": "johndoe",
      "difficulty": "easy"
    },
    {
      "score": 200,
      "username": "janedoe",
      "difficulty": "medium"
    },
    ...
  ]
}
```


## Endpoint: `https://moshionline.net/api?codes`

Retrieves an array of codes with their associated details.

**Response**:

- (array): An array of codes objects.
  - `code` (string): The code value.
  - `prize` (string): The associated prize for the code.
  - `type` (string): The type or category of the code.
  - `status` (boolean): Indicates the status of the code. `true` represents an active code, and `false` represents an inactive code.

**Example Request:**
```
GET https://moshionline.net/api?codes
```

**Example Response:**
```json
    [
      {
        "code": "YAYABBY134",
        "prize": "150",
        "type": "ROX",
        "status": true
      },
      {
        "code": "PORT",
        "prize": "Wiggly Wallpaper",
        "type": "ACCESSORY",
        "status": true
      },
      ...
    ]
```
