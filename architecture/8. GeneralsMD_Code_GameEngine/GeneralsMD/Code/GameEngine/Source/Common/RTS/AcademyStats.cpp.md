# GeneralsMD/Code/GameEngine/Source/Common/RTS/AcademyStats.cpp

## Purpose
Tracks player statistics to provide in-game advice for improving gameplay.

## Responsibilities
- Collects player performance metrics (buildings, units, resources)
- Evaluates advice tiers (basic/intermediate/advanced)
- Generates contextual tips for the player
- Handles serialization/deserialization of stats

## Key Types
- **AcademyStats (Class)**: Main stats tracker
- **AcademyAdviceInfo (Struct)**: Container for generated advice strings
- **TheAcademyClassificationTypeNames (Array)**: String names for academy classifications

## Key Functions
### `findDozerCommandSet`
- Purpose: Locates the dozer's command set for buildable structure analysis
- Calls: `TheControlBar->findCommandSet`

### `updateAcademyStats`
- Purpose: Updates stats for each player object during iteration
- Calls: `AcademyStats::recordProduction`

### `update`
- Purpose: Periodically updates power/money stats and triggers object iteration
- Calls: `m_player->iterateObjects`, `updateAcademyStats`

### `recordProduction`
- Purpose: Records production events (buildings/units) and calculates derived stats
- Calls: None visible

### `evaluateTier1Advice`
- Purpose: Generates basic gameplay advice based on tier 1 stats
- Calls: `TheGameText->fetch`

### `calculateAcademyAdvice`
- Purpose: Orchestrates advice generation across all tiers
- Calls: `evaluateTier1Advice`, `evaluateTier2Advice`, `evaluateTier3Advice`

## Globals
- **TheAcademyClassificationTypeNames (const char**)**: String array for academy classifications

## Dependencies
- Key includes: `AcademyStats.h`, `Energy.h`, `Player.h`, `GameLogic.h`
- External symbols: `TheGameLogic`, `TheControlBar`, `TheGameText`, `ThePlayerList`, `TheGlobalData`
