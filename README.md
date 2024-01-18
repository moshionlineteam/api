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
