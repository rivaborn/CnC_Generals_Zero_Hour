# Generals/Code/GameEngine/Source/GameLogic/Object/SpecialPower/CashHackSpecialPower.cpp

## Purpose
This file implements the logic for a special power called "Cash Hack," which allows a player to steal money from an enemy player.

## Responsibilities
- Parses configuration data for Cash Hack upgrades.
- Manages the execution of the Cash Hack special power.
- Handles the transfer of money between players when the special power is used.

## Key Types
- `CashHackSpecialPowerModuleData (struct)`: Stores configuration data for Cash Hack, including upgrade pairs and default amount to steal.
- `CashHackSpecialPower (class)`: Implements the Cash Hack special power functionality.

## Key Functions
### parseCashHackUpgradePair
- Purpose: Parses a single upgrade pair from an INI file.
- Calls:
  - `INI::parseScience`
  - `INI::parseInt`

### buildFieldParse
- Purpose: Builds field parsing for Cash Hack module data.
- Calls:
  - `SpecialPowerModuleData::buildFieldParse`

### doSpecialPowerAtLocation
- Purpose: Handles the special power action at a location (not implemented in this file).

### findAmountToSteal
- Purpose: Determines the amount of money to steal based on player's science upgrades.

### doSpecialPowerAtObject
- Purpose: Executes the Cash Hack special power on a target object.
- Calls:
  - `SpecialPowerModule::doSpecialPowerAtObject`
  - `Money::withdraw`
  - `Money::deposit`
  - `ScoreKeeper::addMoneyEarned`
  - `InGameUI::addFloatingText`

### crc
- Purpose: Implements CRC functionality for Cash Hack.
- Calls:
  - `SpecialPowerModule::crc`

### xfer
- Purpose: Handles Xfer serialization for Cash Hack.
- Calls:
  - `Xfer::xferVersion`
  - `SpecialPowerModule::xfer`

### loadPostProcess
- Purpose: Performs post-load processing for Cash Hack.
- Calls:
  - `SpecialPowerModule::loadPostProcess`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Player.h"
  - "Common/Team.h"
  - "Common/Xfer.h"
  - "GameClient/GameText.h"
  - "GameLogic/Object.h"
  - "GameLogic/PartitionManager.h"
  - "GameLogic/Module/CashHackSpecialPower.h"
  - "GameClient/InGameUI.h"

- External symbols used:
  - `INI`
  - `MultiIniFieldParse`
  - `FieldParse`
  - `Thing`
  - `ModuleData`
  - `SpecialPowerModule`
  - `Coord3D`
  - `UnsignedInt`
  - `Player`
  - `Object`
  - `Money`
  - `
