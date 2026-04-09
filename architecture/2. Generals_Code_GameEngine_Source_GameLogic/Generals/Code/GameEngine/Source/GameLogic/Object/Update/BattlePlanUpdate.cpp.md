# Generals/Code/GameEngine/Source/GameLogic/Object/Update/BattlePlanUpdate.cpp

## Purpose
Handles battle plan execution and changes for game objects, including animations, sounds, and bonuses.

## Responsibilities
- Manages different battle plans (bombardment, hold the line, search and destroy).
- Updates object states based on current battle plan.
- Handles transitions between battle plans with animations and sound effects.
- Applies bonuses to player units based on active battle plan.
- Paralyzes enemy troops during certain conditions.

## Key Types
- **BattlePlanUpdateModuleData (struct)**: Stores configuration data for battle plans.
- **BattlePlanBonuses (struct)**: Holds bonus values applied to units under a battle plan.

## Key Functions
### update()
- Purpose: Updates the battle plan status and applies changes.
- Calls:
  - `setStatus()`
  - `enableTurret()`
  - `recenterTurret()`
  - `isTurretInNaturalPosition()`

### setBattlePlan(BattlePlanStatus plan)
- Purpose: Sets a new battle plan, applying bonuses and removing previous ones.
- Calls:
  - `player->changeBattlePlan()`
  - `obj->getBodyModule()->setMaxHealth()`
  - `obj->setVisionRange()`
  - `update->setSDEnabled()`

### paralyzeTroop(Object *obj, void *userData)
- Purpose: Paralyzes enemy troops based on battle plan settings.
- Calls:
  - `obj->isAnyKindOf()`
  - `obj->setDisabledUntil()`

## Globals
- None

## Dependencies
- **Headers**:
  - "Common/BitFlagsIO.h"
  - "Common/Radar.h"
  - "Common/PlayerList.h"
  - "Common/ThingTemplate.h"
  - "Common/ThingFactory.h"
  - "Common/Player.h"
  - "Common/Xfer.h"
  - "GameClient/GameClient.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/SpecialPowerModule.h"
  - "GameLogic/Module/BattlePlanUpdate.h"

- **External Symbols**:
  - `TheAudio`
  - `TheGameLogic`
  - `TheInGameUI`
  - `TheGameText`
