# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SupplyTruckAIUpdate.h

## Purpose
Defines the AI state machine and interface for supply trucks in the game, controlling docking behavior and supply management.

## Responsibilities
- Manages supply truck state transitions (idle, busy, wanting, regrouping, docking)
- Handles supply box inventory and docking logic
- Provides interface for external AI systems to interact with supply trucks
- Configures truck behavior via module data (delays, scan distances, etc.)

## Key Types
- **SupplyTruckStateMachine (Class)**: State machine controlling truck docking behavior
- **SupplyTruckWantsToPickUpOrDeliverBoxesState (Class)**: State for active supply delivery/pickup
- **RegroupingState (Class)**: State for truck regrouping at base when supply operations fail
- **DockingState (Class)**: State handling the actual docking process
- **SupplyTruckAIUpdateModuleData (Class)**: Configuration data for supply truck behavior
- **SupplyTruckAIInterface (Class)**: Interface for supply truck AI functionality
- **SupplyTruckAIUpdate (Class)**: Main AI update module implementing supply truck logic

## Key Functions
### `update()`
- Purpose: Main update loop for supply truck AI state machine
- Calls: State machine update methods

### `privateDock(Object *obj, CommandSourceType cmdSource)`
- Purpose: Handles docking command execution
- Calls: State machine transition methods

### `privateIdle(CommandSourceType cmdSource)`
- Purpose: Transitions truck to idle state
- Calls: State machine transition methods

## Globals
- **m_suppliesDepletedVoice (AudioEventRTS)**: Sound played when last supply box is taken

## Dependencies
- `Common/StateMachine.h`
- `GameLogic/Module/AIUpdate.h`
- `Xfer` class for serialization
- `Object`, `Thing` classes
- `AudioEventRTS` for sound events
