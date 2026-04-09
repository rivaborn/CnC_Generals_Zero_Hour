# GeneralsMD/Code/GameEngine/Source/Common/SkirmishBattleHonors.cpp

## Purpose
Handles saving and loading of skirmish battle honors and statistics.

## Responsibilities
- Manages skirmish game statistics (wins, losses, streaks)
- Tracks campaign completions and challenge medals
- Stores special achievements (SCUD, PPC, Nuke builds)
- Handles endurance medal tracking per map/difficulty
- Persists data via INI file

## Key Types
- SkirmishBattleHonors (Class): manages skirmish statistics and honors

## Key Functions
### SkirmishBattleHonors()
- Purpose: Constructor that loads data from "SkirmishStats.ini"
- Calls: load()

### setWins(), getWins()
- Purpose: Sets/gets the number of wins
- Calls: setInt(), getInt()

### setLosses(), getLosses()
- Purpose: Sets/gets the number of losses
- Calls: setInt(), getInt()

### setWinStreak(), getWinStreak()
- Purpose: Sets/gets current win streak
- Calls: setInt(), getInt()

### setBestWinStreak(), getBestWinStreak()
- Purpose: Sets/gets best win streak achieved
- Calls: setInt(), getInt()

### setChallengeMedals(), getChallengeMedals()
- Purpose: Sets/gets challenge medal count
- Calls: setInt(), getInt()

### setBuiltSCUD(), builtSCUD()
- Purpose: Tracks if SCUD launcher was built
- Calls: setBool(), getBool()

### setBuiltParticleCannon(), builtParticleCannon()
- Purpose: Tracks if Particle Cannon was built
- Calls: setBool(), getBool()

### setBuiltNuke(), builtNuke()
- Purpose: Tracks if Nuke was built
- Calls: setBool(), getBool()

### setHonors(), getHonors()
- Purpose: Manages bitfield of honors achievements
- Calls: setInt(), getInt()

### setEnduranceMedal(), getEnduranceMedal()
- Purpose: Tracks endurance medals per map/difficulty
- Calls: setInt(), getInt()

### setLastGeneral(), getLastGeneral()
- Purpose: Stores/recalls last used general
- Calls: setAsciiString(), getAsciiString()

### setNumGamesLoyal(), getNumGamesLoyal()
- Purpose: Tracks number of loyal games played
- Calls: setInt(), getInt()

### setUSACampaignComplete(), getUSACampaignComplete()
- Purpose: Marks USA campaign completion per difficulty
- Calls: setInt(), getInt()

### setCHINACampaignComplete(), getCHINACampaignComplete()
- Purpose: Marks China campaign completion per difficulty
