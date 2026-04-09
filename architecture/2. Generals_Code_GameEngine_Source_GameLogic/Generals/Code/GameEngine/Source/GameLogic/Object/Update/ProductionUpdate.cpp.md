# Generals/Code/GameEngine/Source/GameLogic/Object/Update/ProductionUpdate.cpp

## Purpose
This file manages the production queue and update logic for buildings in Command & Conquer Generals, handling tasks like queuing units or upgrades, managing door animations, and processing production entries.

## Responsibilities
- Manage production queues for buildings.
- Handle queuing and canceling of unit and upgrade productions.
- Update door states based on production status.
- Process production entries to track progress and completion.

## Key Types
- **ProductionUpdateModuleData (struct)**: Stores configuration data for production modules, including door animation times and queue limits.
- **ProductionEntry (class)**: Represents an entry in the production queue, holding details about the item being produced.
- **ProductionUpdate (class)**: Manages the production queue and update logic for buildings.

## Key Functions
### ProductionUpdate::queueUpgrade
- Purpose: Queues an upgrade to be produced.
- Calls: `TheUpgradeCenter->canAffordUpgrade`, `player->addUpgrade`, `newInstance(ProductionEntry)`, `addToProductionQueue`.

### ProductionUpdate::cancelUpgrade
- Purpose: Cancels a queued upgrade production.
- Calls: `player->removeUpgrade`, `removeFromProductionQueue`, `deleteInstance`.

### ProductionUpdate::queueCreateUnit
- Purpose: Queues the production of a unit.
- Calls: `TheBuildAssistant->canMakeUnit`, `newInstance(ProductionEntry)`, `addToProductionQueue`.

### ProductionUpdate::cancelAndRefundAllProduction
- Purpose: Cancels all production items in the queue and refunds costs to the player.
- Calls: `cancelUnitCreate`, `cancelUpgrade`.

## Globals
- **theOpeningFlags (ModelConditionFlagType[DOOR_COUNT_MAX])**: Flags for door opening states.
- **theClosingFlags (ModelConditionFlagType[DOOR_COUNT_MAX])**: Flags for door closing states.
- **theWaitingOpenFlags (ModelConditionFlagType[DOOR_COUNT_MAX])**: Flags for doors waiting to open.
- **theWaitingToCloseFlags (ModelConditionFlagType[DOOR_COUNT_MAX])**: Flags for doors waiting to close.

## Dependencies
- Key includes:
  - `Common/BitFlagsIO.h`
  - `Common/BuildAssistant.h`
  - `Common/CRCDebug.h`
  - `Common/GameState.h`
  - `Common/Player.h`
  - `GameLogic/GameLogic.h`
  - `GameLogic/Module/CreateModule.h`
  - `GameLogic/Object.h`
- External symbols used:
  - `TheUpgradeCenter`, `TheBuildAssistant`, `TheThingFactory`, `TheInGameUI`, `TheGameLogic`
