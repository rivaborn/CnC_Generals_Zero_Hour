# Generals/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/SupplyTruckAIUpdate.cpp

## Purpose
This file implements the AI logic for supply trucks in Command & Conquer Generals, managing their state transitions and interactions with supply centers and warehouses.

## Responsibilities
- Manages the state machine for supply truck behavior.
- Handles supply truck docking and undocking actions.
- Updates supply status and triggers audio events when supplies are depleted.
- Processes player commands to control supply truck behavior.

## Key Types
- **SupplyTruckBusyState (Class)**: Represents the busy state of a supply truck.
- **SupplyTruckIdleState (Class)**: Represents the idle state of a supply truck.
- **SupplyTruckStateMachine (Class)**: Manages the state transitions for supply trucks.

## Key Functions
### SupplyTruckAIUpdate::makeStateMachine
- Purpose: Creates and initializes the state machine for the supply truck.
- Calls: newInstance(AIStateMachine)

### SupplyTruckAIUpdate::update
- Purpose: Updates the supply truck's state and handles AI logic.
- Calls: m_supplyTruckStateMachine->updateStateMachine(), AIUpdateInterface::update()

### SupplyTruckAIUpdate::loseOneBox
- Purpose: Decreases the number of boxes a supply truck is carrying.
- Calls: Drawable::updateDrawableSupplyStatus()

### SupplyTruckAIUpdate::gainOneBox
- Purpose: Increases the number of boxes a supply truck is carrying and checks for depleted supplies.
- Calls: ResourceGatheringManager::findBestSupplyWarehouse(), TheAudio->addAudioEvent()

### SupplyTruckBusyState::onEnter
- Purpose: Handles entering the busy state, resetting flags and logging debug information.
- Calls: SupplyTruckAIInterface::setForceBusyState()

### SupplyTruckIdleState::onEnter
- Purpose: Handles entering the idle state, updating worker interfaces and logging debug information.
- Calls: WorkerAIInterface::exitingSupplyTruckState()

## Globals
- None

## Dependencies
- **Common/Player.h**
- **Common/ResourceGatheringManager.h**
- **GameLogic/Object.h**
- **GameLogic/PartitionManager.h**
- **GameLogic/Module/SupplyTruckAIUpdate.h**
- **GameLogic/Module/SupplyCenterDockUpdate.h**
- **GameLogic/Module/SupplyWarehouseDockUpdate.h**
- **GameLogic/Module/WorkerAIUpdate.h**
- **GameClient/Drawable.h**
- **GameClient/InGameUI.h**
