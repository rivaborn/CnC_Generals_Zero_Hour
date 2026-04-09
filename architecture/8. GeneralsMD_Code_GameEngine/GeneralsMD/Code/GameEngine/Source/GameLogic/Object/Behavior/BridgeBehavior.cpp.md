# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/BridgeBehavior.cpp

## Purpose
Implements bridge behavior in the game, including scaffolding management, damage handling, and bridge destruction effects.

## Responsibilities
- Manages bridge scaffolding creation/removal
- Handles bridge damage states and effects
- Controls bridge tower objects
- Manages bridge destruction animations and sounds
- Serializes bridge state for save/load

## Key Types
- `BridgeBehaviorModuleData` (Class): Stores bridge behavior configuration
- `BridgeBehavior` (Class): Main bridge behavior implementation
- `TimeAndLocationInfo` (Struct): Contains delay and bone location data
- `BridgeFXInfo` (Struct): Stores FX list with timing/location info
- `BridgeOCLInfo` (Struct): Stores OCL list with timing/location info

## Key Functions
### `parseTimeAndLocationInfo`
- Purpose: Parses delay and optional bone location from INI data
- Calls: `ini->getNextToken`, `ini->parseDurationUnsignedInt`, `ini->getNextAsciiString`

### `resolveFX`
- Purpose: Resolves bridge damage/repair effects from template data
- Calls: `TheTerrainLogic->findBridgeAt`, `bridge->getBridgeTemplateName`, `TheTerrainRoads->findBridge`

### `createScaffolding`
- Purpose: Creates scaffold objects when bridge is being built/repaired
- Calls: `TheThingFactory->newObject`, `setScaffoldData`, `TheAI->pathfinder()->changeBridgeState`

### `removeScaffolding`
- Purpose: Removes scaffold objects when bridge construction completes
- Calls: `BridgeScaffoldBehavior::getBridgeScaffoldBehaviorInterfaceFromObject`, `TheAI->pathfinder()->changeBridgeState`

### `xfer`
- Purpose: Serializes bridge state for save/load operations
- Calls: `UpdateModule::xfer`, `TheTerrainLogic->findBridgeAt`, `bridge->setBridgeObjectID`

## Globals
- None

## Dependencies
- Common: `Radar.h`, `ThingFactory.h`, `ThingTemplate.h`, `Xfer.h`
- GameClient: `InGameUI.h`, `FXList.h`, `Line2D.h`, `TerrainRoads.h`
- GameLogic: `AI.h`, `AIPathfind.h`, `Object.h`, `GameLogic.h`, `ObjectCreationList.h`, `Module/BodyModule.h`, `Module/BridgeBehavior.h`, `Module/BridgeScaffoldBehavior.h`, `Module/PhysicsUpdate.h`, `PartitionManager.h`, `TerrainLogic.h`
