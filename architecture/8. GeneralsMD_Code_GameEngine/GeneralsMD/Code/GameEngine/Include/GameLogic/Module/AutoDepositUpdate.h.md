# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/AutoDepositUpdate.h

## Purpose
Defines the AutoDepositUpdate module for handling periodic resource deposits and capture bonuses in the game.

## Responsibilities
- Manages timed resource deposits for players
- Handles initial capture bonuses
- Processes upgrade-based supply boosts
- Parses configuration data for deposit timing and amounts

## Key Types
- **Player (Class)**: Game player entity.
- **Thing (Class)**: Game object entity.
- **upgradePair (Struct)**: Stores type and amount of upgrade boosts.
- **AutoDepositUpdateModuleData (Class)**: Holds configuration data for deposit timing, amounts, and bonuses.
- **AutoDepositUpdate (Class)**: Module implementing the deposit update logic.
- **AutoDepositUpdateMagicEnum (Enum)**: Not inferable.
- **AutoDepositUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable.

## Key Functions
### parseUpgradePair
- Purpose: Parses upgrade pair data from INI files.
- Calls: Not inferable.

### AutoDepositUpdateModuleData::buildFieldParse
- Purpose: Registers INI field parsers for module data.
- Calls: UpdateModuleData::buildFieldParse.

### AutoDepositUpdate::awardInitialCaptureBonus
- Purpose: Awards the initial capture bonus to a player.
- Calls: Not inferable.

### AutoDepositUpdate::update
- Purpose: Updates the deposit state and triggers deposits when due.
- Calls: Not inferable.

### AutoDepositUpdate::getUpgradedSupplyBoost
- Purpose: Calculates the supply boost from upgrades.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- UpdateModule.h
- INI class for parsing
- std::list, std::string
- Memory pool macros (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE
