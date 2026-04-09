# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/BridgeScaffoldBehavior.cpp

## Purpose
Implements the behavior for bridge scaffold objects, controlling their movement between positions.

## Responsibilities
- Manages scaffold motion states (rise, build, tear down, sink)
- Handles position interpolation with speed control
- Provides interface for external control
- Serializes/deserializes state for networking

## Key Types
- **BridgeScaffoldBehavior (Class)**: Controls scaffold movement logic
- **ScaffoldTargetMotion (Enum)**: Motion state (STM_STILL, STM_RISE, STM_BUILD_ACROSS, STM_TEAR_DOWN_ACROSS, STM_SINK)

## Key Functions
### `setPositions`
- Purpose: Sets the scaffold's key positions (create, rise, build)
- Calls: None

### `setMotion`
- Purpose: Sets the current motion target
- Calls: None

### `reverseMotion`
- Purpose: Reverses current motion direction
- Calls: `setMotion`

### `update`
- Purpose: Updates scaffold position based on current motion
- Calls: `getObject`, `setPosition`, `setMotion`, `TheGameLogic->destroyObject`

### `getBridgeScaffoldBehaviorInterfaceFromObject`
- Purpose: Retrieves scaffold interface from an object
- Calls: `getBehaviorModules`, `getBridgeScaffoldBehaviorInterface`

### `xfer`
- Purpose: Serializes/deserializes scaffold state
- Calls: `UpdateModule::xfer`, `xferVersion`, `xferCoord3D`, `xferReal`

## Globals
- **TheGameLogic (GameLogic**)**: Game logic instance for object destruction

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameClient/InGameUI.h`, `GameLogic/GameLogic.h`, `GameLogic/Object.h`, `GameLogic/Module/BridgeScaffoldBehavior.h`
- `UpdateModule`, `Object`, `Coord3D`, `Xfer`, `BehaviorModule`, `BridgeScaffoldBehaviorInterface`
