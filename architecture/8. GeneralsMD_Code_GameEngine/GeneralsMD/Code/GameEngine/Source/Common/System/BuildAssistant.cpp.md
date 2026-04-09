# GeneralsMD/Code/GameEngine/Source/Common/System/BuildAssistant.cpp

## Purpose
Manages construction and deconstruction logic for game objects, including building validation, object placement, and selling structures.

## Responsibilities
- Validates if units/structures can be built (prerequisites, money, etc.)
- Handles object placement and collision resolution during construction
- Manages the selling process for structures (refunds, animations, cleanup)
- Provides utility functions for line-building and tiled object placement

## Key Types
- **BuildAssistant (Class)**: Singleton managing construction/deconstruction logic
- **ObjectSellInfo (Class)**: Tracks objects being sold (ID and sell frame)
- **TileBuildInfo (Struct)**: Contains tile usage info for line-building

## Key Functions
### `isPossibleToMakeUnit`
- Purpose: Checks if a unit can be built by a constructor object
- Calls: `canBuild`, `getCommandSet`, `isEquivalentTo`

### `canMakeUnit`
- Purpose: Checks if a unit can be built including money availability
- Calls: `canBuildMoreOfType`, `canQueueCreateUnit`, `calcCostToBuild`

### `sellObject`
- Purpose: Initiates the selling process for a structure
- Calls: `deselectObject`, `cancelAndRefundAllProduction`, `onSelling`, `aiIdle`

### `moveObjectsForConstruction`
- Purpose: Moves or removes objects in the build area
- Calls: `iteratePotentialCollisions`, `aiMoveToPositionEvenIfSleeping`

## Globals
- **TheBuildAssistant (BuildAssistant*)**: Singleton instance
- **FRAMES_TO_ALLOW_SCAFFOLD (Real)**: Time to show scaffold during selling
- **TOTAL_FRAMES_TO_SELL_OBJECT (Real)**: Total time for sell animation

## Dependencies
- Game logic systems (`GameLogic`, `PartitionManager`)
- Object management (`ThingFactory`, `ThingTemplate`)
- UI/rendering (`ControlBar`, `Drawable`)
- Player/team systems (`Player`, `Team`)
- AI modules (`AIUpdate`, `BehaviorModule`)
