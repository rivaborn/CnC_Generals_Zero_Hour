# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/DeliverPayloadAIUpdate.cpp

## Purpose
Implements the AI logic for airborne cargo delivery, managing approach, payload deployment, and post-delivery behavior.

## Responsibilities
- Controls state machine for delivery process (approach, delivery, cleanup)
- Handles diving logic for strafing attacks
- Manages visible payload subobjects and decals
- Implements recovery from off-map situations
- Coordinates payload creation and physics

## Key Types
- `DeliverPayloadData` (struct): Configuration for delivery parameters (distances, delays, offsets)
- `DeliverPayloadAIUpdate` (class): Main AI update interface for delivery logic
- `DeliverPayloadStateMachine` (class): State machine managing delivery phases
- `DeliveringState` (class): State handling payload deployment
- `ConsiderNewApproachState` (class): State for reattempting delivery
- `RecoverFromOffMapState` (class): State for handling off-map situations
- `HeadOffMapState` (class): State for exiting map after delivery
- `CleanUpState` (class): State for post-delivery cleanup

## Key Functions
### `deliverPayload`
- Purpose: Initializes delivery process with target positions and configuration
- Calls: `deliverPayloadStateMachine` methods, `createRadiusDecal`, `showSubObject`

### `update`
- Purpose: Main update loop handling state machine and diving logic
- Calls: `updateStateMachine`, `getDistanceSquared`, `fireCurrentWeapon`, `doFXPos`

### `calcMinTurnRadius`
- Purpose: Calculates minimum turning radius based on locomotor capabilities
- Calls: `getMaxSpeedForCondition`, `getMaxTurnRate`

### `isCloseEnoughToTarget`
- Purpose: Determines if object is within delivery range
- Calls: `getDistanceSquared`

### `isOffMap`
- Purpose: Checks if object is outside map boundaries
- Calls: `getExtentIncludingBorder`

## Globals
- None

## Dependencies
- `Common/Player.h`, `Common/RandomValue.h`, `Common/ThingFactory.h`
- `GameClient/Drawable.h`, `GameClient/FXList.h`, `GameClient/InGameUI.h`
- `GameLogic/Locomotor.h`, `GameLogic/Module/SmartBombTargetHomingUpdate.h`
- `GameLogic/Module/DeliverPayloadAIUpdate.h`, `GameLogic/Object.h`
- `GameLogic/PartitionManager.h`, `GameLogic/Weapon.h`, `GameLogic/WeaponSet.h`
