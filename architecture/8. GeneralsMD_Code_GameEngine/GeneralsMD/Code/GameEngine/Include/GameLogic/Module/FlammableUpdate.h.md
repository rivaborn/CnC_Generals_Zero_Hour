# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/FlammableUpdate.h

## Purpose
Manages flammable object states (normal, aflame, burned) and their effects in the game.

## Responsibilities
- Tracks flammability status of objects
- Handles damage and healing while aflame
- Manages burning sound effects
- Controls transitions between flammability states

## Key Types
- **FlammabilityStatusType (Enum)**: Represents object flammability states (normal, aflame, burned)
- **FlammableUpdateModuleData (Class)**: Contains configuration data for flammable behavior
- **FlammableUpdate (Class)**: Main module handling flammable object updates and damage

## Key Functions
### tryToIgnite
- Purpose: Attempts to ignite the object based on flammability rules
- Calls: Not inferable

### update
- Purpose: Updates flammability state and applies effects
- Calls: calcSleepTime, doAflameDamage, startBurningSound, stopBurningSound

### onDamage
- Purpose: Handles damage events while object is aflame
- Calls: Not inferable

## Globals
- None

## Dependencies
- Common/AudioEventRTS.h
- GameLogic/Module/DamageModule.h
- GameLogic/Module/UpdateModule.h
