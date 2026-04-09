# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/HealContain.cpp

## Purpose
Implements healing functionality for objects contained within a healing container in the game.

## Responsibilities
- Manages healing of contained objects over time
- Handles object exit when healing is complete
- Provides INI field parsing for healing parameters
- Serializes/deserializes healing container state

## Key Types
- `HealContainModuleData` (Class): Stores healing configuration (time for full heal)
- `HealContain` (Class): Implements the healing container behavior
- `DamageInfo` (Struct): Used to pass healing parameters to objects

## Key Functions
### `HealContain::update`
- Purpose: Updates healing state for all contained objects each frame
- Calls: `OpenContain::update`, `doHeal`, `reserveDoorForExit`, `exitObjectViaDoor`

### `HealContain::doHeal`
- Purpose: Applies healing to a single object based on time spent in container
- Calls: `getBodyModule`, `attemptHealing`

### `HealContainModuleData::buildFieldParse`
- Purpose: Registers INI field parsing for healing container parameters
- Calls: `OpenContainModuleData::buildFieldParse`

## Globals
None

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameLogic/Damage.h`, `GameLogic/GameLogic.h`, `GameLogic/Object.h`
- `GameLogic/Module/BodyModule.h`, `GameLogic/Module/HealContain.h`, `GameLogic/Module/UpdateModule.h`
- `MultiIniFieldParse`, `INI`, `Xfer`, `Thing`, `ModuleData`, `ContainedItemsList`, `BodyModuleInterface`
