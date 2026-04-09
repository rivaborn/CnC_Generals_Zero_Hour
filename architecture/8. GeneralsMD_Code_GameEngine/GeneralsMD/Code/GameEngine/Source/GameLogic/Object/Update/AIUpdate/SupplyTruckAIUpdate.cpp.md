# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/SupplyTruckAIUpdate.cpp

## Purpose
Implements the AI state machine for supply trucks, managing their behavior when ferrying supplies between warehouses and supply centers.

## Responsibilities
- Manages supply truck state transitions (idle, busy, wanting, regrouping, docking)
- Handles supply box inventory (gain/lose boxes)
- Coordinates docking with supply centers/warehouses
- Implements player command handling (forced states, preferred docks)

## Key Types
- `SupplyTruckBusyState` (Class): Handles player-controlled supply truck behavior
- `SupplyTruckIdleState` (Class): Manages idle supply truck behavior
- `SupplyTruckStateMachine` (Class): State machine controlling supply truck AI
- `SupplyTruckWantsToPickUpOrDeliverBoxesState` (Class): State for finding docks
- `RegroupingState` (Class): State for regrouping when docking fails
- `DockingState` (Class): State for managing docking operations

## Key Functions
### `SupplyTruckAIUpdate::update`
- Purpose: Updates the supply truck state machine
- Calls: `m_supplyTruckStateMachine->updateStateMachine()`, `AIUpdateInterface::update()`

### `SupplyTruckAIUpdate::gainOneBox`
- Purpose: Adds a supply box and checks if source is depleted
- Calls: `getObject()->getControllingPlayer()->getResourceGatheringManager()->findBestSupplyWarehouse()`

### `SupplyTruckAIUpdate::privateDock`
- Purpose: Handles docking commands and remembers preferred docks
- Calls: `AIUpdateInterface::privateDock()`

### `SupplyTruckStateMachine::isForcedIntoWantingState`
- Purpose: Checks if truck should enter wanting state
- Calls: `update->isForcedIntoWantingState()`

### `SupplyTruckStateMachine::isForcedIntoBusyState`
- Purpose: Checks if truck should enter busy state
- Calls: `update->isForcedIntoBusyState()`

## Globals
- `REGROUP_SUCCESS_DISTANCE_SQUARED` (Enum): Distance threshold for regrouping success

## Dependencies
- `Common/Player.h`, `Common/ResourceGatheringManager.h`
- `GameLogic/Object.h`, `GameLogic/PartitionManager.h`
- `GameLogic/Module/SupplyTruckAIUpdate.h`
- `GameClient/Drawable.h`, `GameClient/InGameUI.h`
