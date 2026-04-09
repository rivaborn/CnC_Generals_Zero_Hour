# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/BridgeBehavior.h

## Purpose
Defines the bridge behavior module for the game, handling bridge-specific logic like scaffolding, damage, and tower connections.

## Responsibilities
- Manages bridge scaffolding creation/removal
- Handles bridge damage and healing effects
- Connects bridge towers and tracks their IDs
- Processes bridge-related FX and OCL (Object Creation Lists)
- Implements update and die module interfaces

## Key Types
- **BridgeTowerType (Enum)**: Not inferable.
- **BridgeBehaviorInterface (Class)**: Interface for bridge-specific operations.
- **BridgeBehaviorModuleData (Class)**: Module data for bridge behavior configuration.
- **BridgeBehavior (Class)**: Main bridge behavior module class.
- **BridgeFXInfo (Struct)**: Contains FX and timing/location data.
- **BridgeOCLInfo (Struct)**: Contains OCL and timing/location data.
- **TimeAndLocationInfo (Struct)**: Stores delay and bone name for execution.

## Key Functions
### BridgeBehavior::createScaffolding
- Purpose: Creates scaffolding around the bridge.
- Calls: Not inferable.

### BridgeBehavior::removeScaffolding
- Purpose: Removes scaffolding from the bridge.
- Calls: Not inferable.

### BridgeBehavior::onDamage
- Purpose: Handles damage events on the bridge.
- Calls: Not inferable.

### BridgeBehavior::onDie
- Purpose: Handles bridge destruction.
- Calls: Not inferable.

### BridgeBehavior::update
- Purpose: Updates bridge state each frame.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- Common/AudioEventRTS.h
- GameClient/TerrainRoads.h
- GameLogic/Module/BehaviorModule.h
- GameLogic/Module/DamageModule.h
- GameLogic/Module/Diemodule.h
- GameLogic/Module/UpdateModule.h
