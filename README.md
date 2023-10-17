# @darkside-developers/cricket-details

![Logo]([https://example.com/path/to/your/logo.png](https://i.ibb.co/mT0KR26/pngimg-com-cricket-PNG104.png) "Logo Alt Text")

[![npm](https://img.shields.io/npm/v/@darkside-developers/cricket-details)](https://www.npmjs.com/package/@darkside-developers/cricket-details)
[![npm](https://img.shields.io/npm/dt/@darkside-developers/cricket-details)](https://www.npmjs.com/package/@darkside-developers/cricket-details)
![npm](https://img.shields.io/npm/l/@darkside-developers/cricket-details)


A Node.js library for fetching cricket match details, live scores, match news, featured matches, upcoming matches, and recently concluded matches.

## Installation & Result

### Live Matches Urls
```javascript
// Get Live matches urls
const { cricket } = require('@darkside-developers/cricket-details');

const matchDetails = cricket.match_url();
console.log(matchDetails);
```
```javascript
[
  {
    "status": true,
    "creator": {
      "name": "DarkWinzo",
      "github": "@DarkWinzo"
    },
    "result": {
      "title": "Match 1",
      "link": "https://www.cricbuzz.com/match1"
    }
  },
  {
    "status": true,
    "creator": {
      "name": "DarkWinzo",
      "github": "@DarkWinzo"
    },
    "result": {
      "title": "Match 2",
      "link": "https://www.cricbuzz.com/match2"
    }
  },
  ...
]
```

### Live Matches Score
```javascript
// Get Live matches score
const { cricket } = require('@darkside-developers/cricket-details');

const liveScore = cricket.live_score('https://www.example.com/live-match');
console.log(liveScore);
```
```javascript
{
  "status": true,
  "creator": {
    "name": "DarkWinzo",
    "github": "@DarkWinzo"
  },
  "result": {
    "title": "Match Title",
    "status": "In Progress",
    "update": "Latest update here",
    "current_score": "Team A: 100/2 (Overs: 10.5)",
    "batsman": "Player 1: 50 (30 balls)",
    "batsman_run": "50",
    "balls_faced": "30",
    "fours": "6",
    "sixes": "2",
    "sr": "166.67",
    "batsman_two": "Player 2: 30 (25 balls)",
    "batsman_two_run": "30",
    "batsman_two_balls_faced": "25",
    "batsman_two_fours": "3",
    "batsman_two_sixes": "1",
    "batsman_two_sr": "120.00",
    "bowler_stats_1": "Bowler 1: 2/40",
    "bowler_over": "4.5",
    "bowler_runs": "40",
    "bowler_wickets": "2",
    "bowler_maiden": "0",
    "bowler_stats_2": "Bowler 2: 1/20",
    "batsman_stats_1": "Batsman 1: 20 (15 balls)",
    "batsman_stats_2": "Batsman 2: 10 (8 balls)",
    "highest_run_scorer": "Player 3: 60",
    "highest_wicket_taker": "Bowler 3: 3/25",
    "partnership": "Current Partnership: 80 runs (10.2 ov)",
    "recent_balls": "Recent balls: WD 4 1 6 2",
    "last_wicket": "Last wicket: Player 4 (Out: LBW, Bowler 4)",
    "currenly_run_rate": "Current Run Rate: 7.69",
    "commentary": "Latest commentary here"
  }
}
```

### Recently Match Details
```javascript
// Get Recently match details
const { cricket } = require('@darkside-developers/cricket-details');

const upcomingMatches = cricket.upcoming_match();
console.log(upcomingMatches);
```
```javascript
{
  "status": true,
  "creator": {
    "name": "DarkWinzo",
    "github": "@DarkWinzo"
  },
  "upcoming": {
    "series": "Upcoming Series",
    "match": [
      {
        "header": "Match Header 1",
        "team_a": "Team A",
        "team_b": "Team B",
        "status": "Upcoming",
        "link": "https://www.cricbuzz.com/upcoming-match1"
      },
      {
        "header": "Match Header 2",
        "team_a": "Team C",
        "team_b": "Team D",
        "status": "Upcoming",
        "link": "https://www.cricbuzz.com/upcoming-match2"
      },
      ...
    ]
  }
}
```

### Cricket Match News
```javascript
// Get Cricket Matches News
const { cricket } = require('@darkside-developers/cricket-details');

const news = cricket.match_news();
console.log(news);
```
```javascript
{
  "status": true,
  "creator": {
    "name": "DarkWinzo",
    "github": "@DarkWinzo"
  },
  "news": [
    {
      "headline": "News 1",
      "image": "https://m.cricbuzz.com/a/img/v1/595x396/news1.jpg",
      "link": "https://m.cricbuzz.com/news1"
    },
    {
      "headline": "News 2",
      "image": "https://m.cricbuzz.com/a/img/v1/595x396/news2.jpg",
      "link": "https://m.cricbuzz.com/news2"
    },
    ...
  ]
}
```

### Feature Match Details
```javascript
// Get Cricket Feature Matches Details
const { cricket } = require('@darkside-developers/cricket-details');

const featuredMatches = cricket.feature_match();
console.log(featuredMatches);
```
```javascript
{
  "status": true,
  "creator": {
    "name": "DarkWinzo",
    "github": "@DarkWinzo"
  },
  "featured": [
    {
      "header": "Match Header 1",
      "team_a": "Team A",
      "team_b": "Team B",
      "status": "In Progress",
      "link": "https://www.cricbuzz.com/feature-match1"
    },
    {
      "header": "Match Header 2",
      "team_a": "Team C",
      "team_b": "Team D",
      "status": "Upcoming",
      "link": "https://www.cricbuzz.com/feature-match2"
    },
    ...
  ]
}
```

### Upcoming Match Details
```javascript
// Get Cricket Upcoming Matches Details
const { cricket } = require('@darkside-developers/cricket-details');

const upcomingMatches = cricket.upcoming_match();
console.log(upcomingMatches);
```
```javascript
{
  "status": true,
  "creator": {
    "name": "DarkWinzo",
    "github": "@DarkWinzo"
  },
  "upcoming": {
    "series": "Upcoming Series",
    "match": [
      {
        "header": "Match Header 1",
        "team_a": "Team A",
        "team_b": "Team B",
        "status": "Upcoming",
        "link": "https://www.cricbuzz.com/upcoming-match1"
      },
      {
        "header": "Match Header 2",
        "team_a": "Team C",
        "team_b": "Team D",
        "status": "Upcoming",
        "link": "https://www.cricbuzz.com/upcoming-match2"
      },
      ...
    ]
  }
}
```

