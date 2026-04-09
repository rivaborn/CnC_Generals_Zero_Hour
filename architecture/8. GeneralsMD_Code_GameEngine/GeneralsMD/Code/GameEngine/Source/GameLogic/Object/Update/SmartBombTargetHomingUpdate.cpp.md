# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/SmartBombTargetHomingUpdate.cpp

## Purpose
Handles homing behavior for smart bomb projectiles by adjusting their trajectory toward a target position.

## Responsibilities
- Adjusts projectile position to improve target acquisition
- Manages target position tracking
- Applies course correction based on module data
- Ensures projectile is above terrain before applying corrections

## Key Types
- **SmartBombTargetHomingUpdate (Class)**: Manages homing behavior for smart bomb projectiles
- **SmartBombTargetHomingUpdateModuleData (Struct)**: Contains module-specific configuration (not shown in this file)

## Key Functions
### `SetTargetPosition`
- Purpose: Sets the target position for homing
- Calls: None

### `update`
- Purpose: Applies course correction to the projectile's position
- Calls: `getSmartBombTargetHomingUpdateModuleData()`, `getObject()`, `isSignificantlyAboveTerrain()`, `getPosition()`, `setPosition()`

### `crc`
- Purpose: Handles CRC serialization
- Calls: `UpdateModule::crc()`

### `xfer`
- Purpose: Handles Xfer serialization
- Calls: `UpdateModule::xfer()`

### `loadPostProcess`
- Purpose: Post-processing after loading
- Calls: `UpdateModule::loadPostProcess()`

## Globals
- **m_targetReceived (BOOL)**: Tracks whether a target has been set
- **m_target (Coord3D)**: Stores the target position

## Dependencies
- `PreRTS.h`, `Common/RandomValue.h`, `Common/Xfer.h`, `GameLogic/GameLogic.h`, `GameLogic/Object.h`, `GameLogic/Module/SmartBombTargetHomingUpdate.h`
- `UpdateModule`, `Thing`, `Coord3D`, `Xfer`, `UpdateSleepTime`
