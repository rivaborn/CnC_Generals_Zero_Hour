# Generals/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/SalvageCrateCollide.cpp

## Purpose
This file implements the collision logic for salvage crates in Command & Conquer Generals, handling interactions with salvager units to provide bonuses like weapon sets, levels, or money.

## Responsibilities
- Handle collisions between salvage crates and salvager units.
- Determine eligibility criteria for different types of bonuses.
- Execute random chance checks for each bonus type.
- Apply the selected bonus to the unit (weapon set, level, or money).
- Play appropriate audio feedback for each action.

## Key Types
- None

## Key Functions
### isValidToExecute
- Purpose: Check if a collision with another object should be processed.
- Calls:
  - `CrateCollide::isValidToExecute`
  - `other->getTemplate()->isKindOf`

### executeCrateBehavior
- Purpose: Execute the crate's behavior based on the type of bonus and random chance.
- Calls:
  - `eligibleForWeaponSet`, `testWeaponChance`, `doWeaponSet`
  - `eligibleForLevel`, `testLevelChance`, `doLevelGain`
  - `doMoney`

### eligibleForWeaponSet
- Purpose: Determine if a unit is eligible for a weapon set bonus.
- Calls:
  - `other->isKindOf`
  - `other->testWeaponSetFlag`

### eligibleForLevel
- Purpose: Determine if a unit is eligible for a level gain.
- Calls:
  - `other->getExperienceTracker()->getVeterancyLevel`
  - `other->getExperienceTracker()->isTrainable`

### testWeaponChance
- Purpose: Check if the random chance for a weapon set bonus is met.
- Calls:
  - `GameLogicRandomValueReal`

### testLevelChance
- Purpose: Check if the random chance for a level gain is met.
- Calls:
  - `GameLogicRandomValueReal`

### doWeaponSet
- Purpose: Apply a weapon set upgrade to the unit.
- Calls:
  - `other->clearWeaponSetFlag`, `other->setWeaponSetFlag`

### doLevelGain
- Purpose: Increase the unit's level by one.
- Calls:
  - `other->getExperienceTracker()->gainExpForLevel`

### doMoney
- Purpose: Give money to the player controlling the unit and display a floating text message.
- Calls:
  - `GameLogicRandomValue`
  - `other->getControllingPlayer()->getMoney()->deposit`
  - `other->getControllingPlayer()->getScoreKeeper()->addMoneyEarned`
  - `TheInGameUI->addFloatingText`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "GameLogic/Module/SalvageCrateCollide.h"
  - "
