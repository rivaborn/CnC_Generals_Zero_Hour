# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/WorkerAIUpdate.cpp

## Purpose
Implements AI logic for worker units that can act as both dozers (builders) and supply trucks.

## Responsibilities
- Manages worker state transitions between dozer and supply truck modes
- Handles construction, repair, and supply delivery tasks
- Controls worker behavior via state machines (dozer, supply truck, worker master)
- Manages bridge scaffolding for bridge towers

## Key Types
- **WorkerAIUpdate (Class)**: Main AI update interface for worker units
- **WorkerStateMachine (Class)**: Master state machine controlling dozer/supply truck modes
- **ActAsDozerState (Class)**: State for dozer behavior
- **ActAsSupplyTruckState (Class)**: State for supply truck behavior
- **DozerTask (Enum)**: Worker task types (invalid, build, repair, etc.)

## Key Functions
### WorkerAIUpdate::update
- Purpose: Main update loop for worker AI
- Calls: AIUpdateInterface::update, m_workerMachine->updateStateMachine, m_dozerMachine->updateStateMachine

### WorkerAIUpdate::construct
- Purpose: Handles construction commands for the worker
- Calls: TheBuildAssistant->isLocationLegalToBuild, TheThingFactory->newObject

### WorkerAIUpdate::isCurrentlyFerryingSupplies
- Purpose: Checks if worker is actively transporting supplies
- Calls: m_supplyTruckStateMachine->getCurrentStateID

### WorkerAIUpdate::createMachines
- Purpose: Initializes state machines for worker behavior
- Calls: newInstance(WorkerStateMachine), newInstance(DozerPrimaryStateMachine), newInstance(SupplyTruckStateMachine)

## Globals
- **m_suppliesDepletedVoice (AudioEventRTS)**: Voice event for low supplies
- **m_buildingSound (AudioEventRTS)**: Sound played during construction

## Dependencies
- Common: ActionManager, Team, StateMachine, BuildAssistant, GameState, ThingTemplate, ThingFactory, Player, Money, Radar, RandomValue, GlobalData, ResourceGatheringManager, Upgrade
- GameClient: Drawable, GameText, InGameUI
- GameLogic: AIPathfind, Locomotor, PartitionManager, BodyModule, BridgeBehavior, BridgeTowerBehavior, CreateModule, SupplyTruckAIUpdate, SupplyCenterDockUpdate, SupplyWarehouseDockUpdate, WorkerAIUpdate
