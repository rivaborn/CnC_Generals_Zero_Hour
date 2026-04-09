# Generals/Code/GameEngine/Source/Common/SkirmishBattleHonors.cpp

## Purpose
This file handles the saving and loading of skirmish battle honors information, including win/loss statistics, medals earned, and other achievements.

## Responsibilities
- Manages player's battle honors data.
- Loads and saves honors data from/to an INI file.
- Provides getter and setter methods for various honors metrics.

## Key Types
- SkirmishBattleHonors (Class): Manages skirmish battle honors data.

## Key Functions
### SkirmishBattleHonors::SkirmishBattleHonors()
- Purpose: Initializes the object by loading honors data from "SkirmishStats.ini".
- Calls: load("SkirmishStats.ini")

### SkirmishBattleHonors::~SkirmishBattleHonors()
- Purpose: Destructor for the SkirmishBattleHonors class.
- Calls: None

### SkirmishBattleHonors::setWins(Int val)
- Purpose: Sets the number of wins.
- Calls: setInt("Wins", val)

### SkirmishBattleHonors::getWins(void) const
- Purpose: Retrieves the number of wins.
- Calls: getInt("Wins", 0)

### SkirmishBattleHonors::setLosses(Int val)
- Purpose: Sets the number of losses.
- Calls: setInt("Losses", val)

### SkirmishBattleHonors::getLosses(void) const
- Purpose: Retrieves the number of losses.
- Calls: getInt("Losses", 0)

### SkirmishBattleHonors::setWinStreak(Int val)
- Purpose: Sets the current win streak.
- Calls: setInt("WinStreak", val)

### SkirmishBattleHonors::getWinStreak(void) const
- Purpose: Retrieves the current win streak.
- Calls: getInt("WinStreak", 0)

### SkirmishBattleHonors::setBestWinStreak(Int val)
- Purpose: Sets the best win streak achieved.
- Calls: setInt("BestWinStreak", val)

### SkirmishBattleHonors::getBestWinStreak(void) const
- Purpose: Retrieves the best win streak achieved.
- Calls: getInt("BestWinStreak", 0)

### SkirmishBattleHonors::setChallengeMedals(Int val)
- Purpose: Sets the number of challenge medals earned.
- Calls: setInt("Challenge", val)

### SkirmishBattleHonors::getChallengeMedals(void) const
- Purpose: Retrieves the number of challenge medals earned.
- Calls: getInt("Challenge", 0)

### SkirmishBattleHonors::setBuiltSCUD(void)
- Purpose: Marks that a SCUD was built.
- Calls: setBool("SCUD", TRUE)

### SkirmishBattleHonors::builtSCUD(void) const
-
