# Generals/Code/GameEngine/Source/GameLogic/Object/SpecialPower/CashBountyPower.cpp

## Purpose
This file implements the `CashBountyPower` class, which manages a special power related to cash bounties in the game. It handles the logic for setting and finding bounties based on player science.

## Responsibilities
- Manages cash bounty logic for objects.
- Parses bounty data from configuration files.
- Updates player's cash bounty when conditions are met.

## Key Types
- `CashBountyPowerModuleData (struct)`: Stores bounty data, including default and upgrade bounties.
- `CashBountyPower (class)`: Implements the special power logic for cash bounties.

## Key Functions
### CashBountyPowerModuleData::buildFieldParse
- Purpose: Sets up field parsing for bounty data.
- Calls: `SpecialPowerModuleData::buildFieldParse`, `INI::parsePercentToReal`.

### CashBountyPower::onObjectCreated
- Purpose: Updates the player's cash bounty when an object is created.
- Calls: `getObject()->getControllingPlayer()`, `controller->hasScience()`, `findBounty()`, `controller->setCashBounty()`.

### CashBountyPower::findBounty
- Purpose: Determines the bounty value based on player science.
- Calls: `getCashBountyPowerModuleData()`, `controller->hasScience()`.

### CashBountyPower::onSpecialPowerCreation
- Purpose: Handles special power creation and updates cash bounty.
- Calls: `SpecialPowerModule::onSpecialPowerCreation()`, `findBounty()`, `controller->setCashBounty()`.

## Globals
None

## Dependencies
- Key includes:
  - "Common/Player.h"
  - "Common/Xfer.h"
  - "GameLogic/Module/CashBountyPower.h"
  - "GameLogic/Object.h"

- External symbols used:
  - `INI::parseScience`
  - `INI::parsePercentToReal`
  - `SpecialPowerModuleData::buildFieldParse`
  - `XferVersion`
