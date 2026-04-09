# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/ProductionUpdate.cpp

## Purpose
Handles production logic for buildings, including unit creation and upgrade research.

## Responsibilities
- Manages production queues for units and upgrades
- Handles door animations for production exits
- Processes production timers and completion states
- Manages refunds and cancellations of production
- Serializes production state for save/load

## Key Types
- `ProductionUpdateModuleData` (Class): Stores production configuration (queue limits, door timings)
- `ProductionEntry` (Class): Represents a single production item in the queue
- `ProductionUpdate` (Class): Main production update module handling queue management
- `DoorInfo` (Struct): Tracks door animation states and timings

## Key Functions
### `queueCreateUnit`
- Purpose: Adds a unit to the production queue
- Calls: `TheBuildAssistant->canMakeUnit`, `addToProductionQueue`

### `queueUpgrade`
- Purpose: Adds an upgrade to the production queue
- Calls: `TheUpgradeCenter->canAffordUpgrade`, `addToProductionQueue`

### `cancelAndRefundAllProduction`
- Purpose: Cancels all production items and refunds costs
- Calls: `cancelUnitCreate`, `cancelUpgrade`

### `xfer`
- Purpose: Serializes production state for save/load
- Calls: `UpdateModule::xfer`, `TheThingFactory->findTemplate`, `TheUpgradeCenter->findUpgrade`

## Globals
- `theOpeningFlags` (Array): Door opening animation flags
- `theClosingFlags` (Array): Door closing animation flags
- `theWaitingOpenFlags` (Array): Door waiting open flags
- `theWaitingToCloseFlags` (Array): Door waiting to close flags

## Dependencies
- `Common/BitFlagsIO.h`, `Common/BuildAssistant.h`, `Common/GameState.h`
- `GameLogic/Module/ProductionUpdate.h`, `GameLogic/Object.h`
- `GameClient/ControlBar.h`, `GameClient/Drawable.h`
- `TheThingFactory`, `TheUpgradeCenter`, `TheGameLogic`, `TheInGameUI`
