# Moshionline API Endpoints README

Welcome to the documentation for Moshi Online's API endpoints. This guide provides information on various endpoints to help you interact with our API.

## 1. Events Endpoint

### Endpoint: `https://moshionline.net/api?events` [GET]

This endpoint retrieves information about the current events on the server.

#### Response Example:
```json
{
  "lastBackup": 0,
  "globalPriceDiscount": 0,
  "globalLevelDiscount": 0,
  "gardenGrowthTime": 5400,
  "rewardBooster": 1,
  "clientSideShop": false,
  "lastGeneralShopRotation": 0,
  "lastSeedShopRotation": 0,
  "success": true
}
```

- **lastBackup:** Timestamp of the last backup.
- **globalPriceDiscount:** Global price discount of shop items.
- **globalLevelDiscount:** Global level discount of shop items.
- **gardenGrowthTime:** Current garden growth time in seconds.
- **rewardBooster:** Multiplier booster for minigames.
- **clientSideShop:** If true, there is no shop restock cooldown.
- **lastGeneralShopRotation:** Timestamp of the last general shop rotation.
- **lastSeedShopRotation:** Timestamp of the last seed shop rotation.

## 2. Codes Endpoint

### Endpoint: `https://moshionline.net/api?codes` [GET]

This endpoint fetches all the secret codes available.

#### Response Example:
```json
{
  "codes": [
    {
      "code": "DUMMYCODE123",
      "prize": "500",
      "type": "Coins",
      "status": true
    }
  ]
}
```

- **code:** Secret code.
- **prize:** Prize associated with the code.
- **type:** Type of the prize.
- **status:** If the code is active or not.

## 3. Blog Endpoint

### Endpoint: `https://moshionline.net/api?blog` [GET]

This endpoint retrieves all the blog posts from Moshi Online.

#### Response Example:
```json
{
  "data": [
    {
      "id": 1,
      "title": "Welcome to Moshionline",
      "description": "Explore the exciting world of Moshionline!",
      "thumbnail": "https://moshionline.net/blog/images/thumbnails/welcome.png",
      "category": "news",
      "date": 1634643575
    }
  ]
}
```

- **id:** Unique identifier for the blog post.
- **title:** Title of the blog post.
- **description:** Brief description of the blog post.
- **thumbnail:** URL of the blog post thumbnail image.
- **category:** Category of the blog post.
- **date:** Timestamp of the blog post creation.

## 4. FAQ Endpoint

### Endpoint: `https://moshionline.net/api?faq` [GET]

This endpoint retrieves frequently asked questions.

#### Response Example:
```json
{
  "data": [
    {
      "id": 1,
      "title": "How to Play",
      "question": "Learn how to start playing Moshionline!",
      "question_id": "getting-started",
      "date": 1634643585
    }
  ]
}
```

- **id:** Unique identifier for the FAQ.
- **title:** Title of the FAQ.
- **question:** Question and its answer.
- **question_id:** Identifier for the question.
- **date:** Timestamp of the FAQ entry.

## 5. Highscore Endpoint

### Endpoint: `https://moshionline.net/api?highscore&highscore=[GAME_ID]` [GET]

This endpoint retrieves highscores for a specific game.

#### Response Example:
```json
{
  "data": [
    {
      "user": "player1",
      "difficulty": "hard",
      "score": 9500
    },
    {
      "user": "player2",
      "difficulty": "medium",
      "score": 8000
    }
  ]
}
```

- **user:** Username of the player.
- **difficulty:** Difficulty level of the game.
- **score:** Score achieved by the player.

## 6. Statistics

To access statistics, an internal server key is required.

### Endpoint: `https://moshionline.net/api?statistics` [GET]

Gets all the game information that staff might care about.

#### Response Example:
```json
{
  "total_users": 0,
  "active_today": 0,
  "daily_users": 0,
  "yesterday_users": 0,
  "weekly_users": 0,
  "monthly_users": 0,
  "staff_users": 0,
  "banned_users": 0,
  "total_games": 0,
  "total_missions": 0,
  "total_puzzles": 0,
  "total_messages": 0,
  "total_gifts": 0,
  "total_mysterygifts": 0,
  "total_moshlings_owned": 0,
  "total_items_owned": 0,
  "total_clothing_owned": 0,
  "total_seeds_owned": 0,
  "total_codes_redeemed": 0
}
```

- **total_users:** Total number of registered users.
- **active_today:** Number of users active today.
- **daily_users:** Number of users who registered today.
- **yesterday_users:** Number of users who registered yesterday.
- **weekly_users:** Number of users registered in the last week.
- **monthly_users:** Number of users registered in the last month.
- **staff_users:** Number of staff members.
- **banned_users:** Number of banned users.
- **total_games:** Total number of games played.
- **total_missions:** Total number of missions played.
- **total_puzzles:** Total number of puzzles played.
- **total_messages:** Total number of messages sent.
- **total_gifts:** Total number of gifts given.
- **total_mysterygifts:** Total number of mystery gifts given.
- **total_moshlings_owned:** Total number of Moshlings owned.
- **total_items_owned:** Total number of items owned.
- **total_clothing_owned:** Total number of clothing items owned.
- **total_seeds_owned:** Total number of seeds owned.
- **total_codes_redeemed:** Total number of codes redeemed.

## 7. Player Lookup

To perform a player lookup, an API key is *currently* required.

### Endpoint: `https://moshionline.net/api?player&player=[USERNAME]` [GET]

This endpoint provides information about a specific player.

#### Response Example:
```json
{
  "username": "dummy_player",
  "monstar": "A",
  "monster": "furi",
  "joined": 1685163202,
  "views": 500,
  "games_played": 20,
  "banned": false,
  "rocks": 300,
  "level": 3,
  "level_progress": 30,
  "success": true
}
```
- **username:** Player's username.
- **monstar:** Monstar level.
- **monster:** Player's chosen monster.
- **joined:** Timestamp of when the player joined.
- **views:** Number of times the player has been viewed.
- **games_played:** Number of games played by the player.
- **banned:** Whether the player is banned or not.
- **rocks:** Total rox owned by the player.
- **level:** Player's level.
- **level_progress:** Player's progress towards the next level.
