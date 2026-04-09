# Generals/Code/GameEngine/Source/Common/StatsCollector.cpp

## Purpose
This file implements a statistics collector for tracking player actions and game state in Command & Conquer Generals.

## Responsibilities
- Collects and records various player stats such as build, move, attack commands, unit counts, and scroll times.
- Manages the creation and writing to stat files based on game events and time intervals.
- Initializes and resets statistics at the start of a game session.

## Key Types
- None

## Key Functions
### StatsCollector::StatsCollector
- Purpose: Initializes the stats collector with default values.
- Calls: None

### StatsCollector::~StatsCollector
- Purpose: Destructor for the stats collector.
- Calls: None

### StatsCollector::reset
- Purpose: Resets and initializes the stat file header.
- Calls: TheFileSystem->createDirectory, createFileName, writeInitialFileInfo, zeroOutStats

### StatsCollector::collectMsgStats
- Purpose: Collects message-based statistics like build commands.
- Calls: None

### StatsCollector::collectUnitCountStats
- Purpose: Counts player and AI units in the game.
- Calls: TheGameLogic->getFirstObject, obj->getNextObject, obj->isKindOf, obj->isNeutralControlled, obj->getControllingPlayer

### StatsCollector::update
- Purpose: Updates statistics every frame based on time intervals.
- Calls: collectUnitCountStats, writeStatInfo, zeroOutStats

### StatsCollector::incrementScrollMoveCount
- Purpose: Increments the scroll map command count.
- Calls: None

### StatsCollector::incrementAttackCount
- Purpose: Increments the attack command count.
- Calls: None

### StatsCollector::incrementBuildCount
- Purpose: Increments the build command count.
- Calls: None

### StatsCollector::incrementMoveCount
- Purpose: Increments the move command count.
- Calls: None

### StatsCollector::writeFileEnd
- Purpose: Writes final statistics and metadata to the file.
- Calls: fopen, fprintf, fclose

### StatsCollector::startScrollTime
- Purpose: Starts tracking scroll time.
- Calls: None

### StatsCollector::endScrollTime
- Purpose: Ends tracking scroll time.
- Calls: None

## Globals
- TheStatsCollector (StatsCollector*): Global instance of the stats collector.
- statsDir (char[]): Directory for storing stat files.

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/StatsCollector.h"
  - "Common/FileSystem.h"
  - "Common/PlayerList.h"
  - "Common/Player.h"
  - "Common/GlobalData.h"
  - "Common/Money.h"
  - "GameLogic/Object.h"
  - "GameLogic/GameLogic.h"
  - "GameClient/MapUtil.h"
  - "GameNetwork/
