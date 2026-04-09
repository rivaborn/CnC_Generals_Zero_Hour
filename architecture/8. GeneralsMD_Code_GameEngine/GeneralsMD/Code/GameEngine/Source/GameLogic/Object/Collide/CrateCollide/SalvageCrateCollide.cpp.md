# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/SalvageCrateCollide.cpp

## Purpose
Handles collision logic for salvage crates, granting rewards like weapon/armor upgrades, experience levels, or money to eligible units.

## Responsibilities
- Validates if a unit can interact with a salvage crate
- Applies rewards based on unit type and random chances
- Plays appropriate audio cues for reward types
- Tracks salvage collection statistics

## Key Types
- **SalvageCrateCollide (Class)**: Manages salvage crate collision behavior
- **SalvageCrateCollideModuleData (Struct)**: Contains configuration data for salvage rewards (not shown in this file)

## Key Functions
### `isValidToExecute`
- Purpose: Checks if the colliding object is a valid salvager unit
- Calls: `CrateCollide::isValidToExecute`, `getTemplate()->isKindOf`

### `executeCrateBehavior`
- Purpose: Applies the appropriate reward based on unit eligibility and random chances
- Calls: `eligibleForArmorSet`, `doArmorSet`, `eligibleForWeaponSet`, `testWeaponChance`, `doWeaponSet`, `eligibleForLevel`, `testLevelChance`, `doLevelGain`, `doMoney`, `getControllingPlayer()->getAcademyStats()->recordSalvageCollected`

### `eligibleForWeaponSet`
- Purpose: Determines if a unit can receive a weapon upgrade from the crate
- Calls: `isKindOf`, `testWeaponSetFlag`

### `eligibleForArmorSet`
- Purpose: Determines if a unit can receive an armor upgrade from the crate
- Calls: `isKindOf`, `testArmorSetFlag`

### `eligibleForLevel`
- Purpose: Checks if a unit can gain an experience level from the crate
- Calls: `getExperienceTracker()->getVeterancyLevel`, `getExperienceTracker()->isTrainable`

### `doWeaponSet`
- Purpose: Applies weapon upgrade flags to the unit
- Calls: `testWeaponSetFlag`, `clearWeaponSetFlag`, `setWeaponSetFlag`

### `doArmorSet`
- Purpose: Applies armor upgrade flags and model conditions to the unit
- Calls: `testArmorSetFlag`, `clearArmorSetFlag`, `setArmorSetFlag`, `clearAndSetModelConditionState`, `setModelConditionState`

### `doMoney`
- Purpose: Grants money to the player and displays a floating text notification
- Calls: `getControllingPlayer()->getMoney()->deposit`, `getControllingPlayer()->getScoreKeeper()->addMoneyEarned`, `TheInGameUI->addFloatingText`

## Glob
