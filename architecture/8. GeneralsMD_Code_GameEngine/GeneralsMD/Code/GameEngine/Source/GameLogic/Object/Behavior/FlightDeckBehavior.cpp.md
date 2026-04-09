# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/FlightDeckBehavior.cpp

## Purpose
Handles aircraft movement and parking behavior for aircraft carriers in Command & Conquer Generals Zero Hour.

## Responsibilities
- Manages flight deck spaces and runways for aircraft parking/takeoff
- Handles aircraft production, healing, and order propagation
- Tracks runway usage and aircraft assignments
- Manages particle effects for catapult systems
- Serializes flight deck state for save/load

## Key Types
- `FlightDeckBehaviorModuleData` (Class): Configuration data for flight decks (runways, healing rates, etc.)
- `FlightDeckBehavior` (Class): Main behavior module controlling flight deck operations
- `FlightDeckInfo` (Struct): Tracks parking space info (position, occupied object)
- `RunwayInfo` (Struct): Stores runway endpoints and usage state
- `HealingInfo` (Struct): Tracks healing progress for aircraft

## Key Functions
### `buildInfo`
- Purpose: Initializes flight deck layout and aircraft positions
- Calls: `getObject()`, `TheThingFactory->newObject()`, `getSingleLogicalBonePosition()`

### `purgeDead`
- Purpose: Removes references to destroyed aircraft
- Calls: `TheGameLogic->findObjectByID()`, `isEffectivelyDead()`

### `aiDoCommand`
- Purpose: Handles AI commands and propagates them to aircraft
- Calls: `propagateOrdersToPlanes()`, `aiGuardPosition()`, etc.

### `xfer`
- Purpose: Serializes flight deck state for save/load
- Calls: `AIUpdateInterface::xfer()`, `xferObjectID()`, `xferUnsignedInt()`

## Globals
- `HEAL_RATE_FRAMES` (line 955): Not inferable (truncated in sample)

## Dependencies
- Key includes: `PreRTS.h`, `Common/ThingFactory.h`, `GameLogic/AI.h`, `GameLogic/Module/FlightDeckBehavior.h`
- External symbols: `TheThingFactory`, `TheGameLogic`, `TheAI`, `TheNameKeyGenerator`
