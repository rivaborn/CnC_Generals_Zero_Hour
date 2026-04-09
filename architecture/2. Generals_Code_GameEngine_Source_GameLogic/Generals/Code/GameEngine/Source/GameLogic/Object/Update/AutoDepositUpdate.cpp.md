# Generals/Code/GameEngine/Source/GameLogic/Object/Update/AutoDepositUpdate.cpp

## Purpose
This file implements the `AutoDepositUpdate` class, which handles automatic deposit updates for game objects, such as buildings or resources, in Command & Conquer Generals.

## Responsibilities
- Manages auto-deposit timing and logic.
- Awards initial capture bonuses to players.
- Updates object positions and displays floating text for cash income.

## Key Types
- `AutoDepositUpdate` (Class): Handles automatic deposit updates for game objects.
- None

## Key Functions
### AutoDepositUpdate::awardInitialCaptureBonus
- Purpose: Awards an initial capture bonus to a player if conditions are met.
- Calls:
  - `player->getMoney()->deposit`
  - `player->getScoreKeeper()->addMoneyEarned`
  - `TheInGameUI->addFloatingText`

### AutoDepositUpdate::update
- Purpose: Updates the auto-deposit logic for game objects.
- Calls:
  - `TheGameLogic->getFrame`
  - `getObject()->isNeutralControlled`
  - `getObject()->getConstructionPercent`
  - `getObject()->getControllingPlayer()->getMoney()->deposit`
  - `getObject()->getControllingPlayer()->getScoreKeeper()->addMoneyEarned`
  - `TheInGameUI->addFloatingText`

### AutoDepositUpdate::crc
- Purpose: Handles CRC (Cyclic Redundancy Check) for the update module.
- Calls:
  - `UpdateModule::crc`

### AutoDepositUpdate::xfer
- Purpose: Handles data transfer for the update module.
- Calls:
  - `xfer->xferVersion`
  - `xfer->xferUnsignedInt`
  - `xfer->xferBool`
  - `UpdateModule::xfer`

### AutoDepositUpdate::loadPostProcess
- Purpose: Performs post-processing after loading the update module.
- Calls:
  - `UpdateModule::loadPostProcess`

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `BuildAssistant.h`
  - `Thing.h`
  - `ThingTemplate.h`
  - `INI.h`
  - `RandomValue.h`
  - `Player.h`
  - `Xfer.h`
  - `GameLogic.h`
  - `AutoDepositUpdate.h`
  - `AIUpdate.h`
  - `Object.h`
  - `InGameUI.h`
  - `Color.h`
  - `GameText.h`
