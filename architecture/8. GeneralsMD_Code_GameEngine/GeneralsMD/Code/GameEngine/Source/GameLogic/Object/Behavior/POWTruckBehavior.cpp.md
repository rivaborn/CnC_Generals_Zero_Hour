# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/POWTruckBehavior.cpp

## Purpose
Implements behavior for the POW (Prisoner of War) Truck in the game, handling collision logic for picking up surrendered units.

## Responsibilities
- Manages collision detection with surrendered units
- Coordinates prisoner pickup via AI interface
- Handles serialization (Xfer) and CRC for network sync
- Extends OpenContain behavior for containment logic

## Key Types
- `POWTruckBehaviorModuleData` (Class): Module data container for POW Truck behavior
- `POWTruckBehavior` (Class): Main behavior class handling POW Truck logic
- `POWTruckAIUpdateInterface` (External): Interface for POW Truck AI operations

## Key Functions
### `onCollide`
- Purpose: Handles collision with other objects to pick up surrendered units
- Calls: `getAIUpdateInterface`, `isSurrendered`, `getPOWTruckAIUpdateInterface`, `loadPrisoner`

### `crc`
- Purpose: Generates CRC checksum for network synchronization
- Calls: `OpenContain::crc`

### `xfer`
- Purpose: Serializes/deserializes POW Truck behavior data
- Calls: `OpenContain::xfer`

### `loadPostProcess`
- Purpose: Post-processing after loading
- Calls: `OpenContain::loadPostProcess`

## Globals
None

## Dependencies
- `PreRTS.h`, `ThingTemplate.h`, `Xfer.h`, `InGameUI.h`, `Object.h`
- `AIUpdate.h`, `POWTruckAIUpdate.h`, `POWTruckBehavior.h`
- `OpenContainModuleData`, `OpenContain`, `MultiIniFieldParse`, `XferVersion`
