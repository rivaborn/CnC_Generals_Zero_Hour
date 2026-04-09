# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/WorkerAIUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the core AI logic for worker units, bridging the gap between high-level player commands and low-level game mechanics. It manages state transitions between construction (dozer) and supply delivery modes, coordinating with multiple subsystems including pathfinding, resource management, and audio.

## Cross-References
### Incoming
- **GameLogic/Object/Update/AIUpdate**: Calls `WorkerAIUpdate::update` as part of the object update cycle
- **GameLogic/Module**: Uses `SupplyTruckAIUpdate`, `SupplyCenterDockUpdate`, and `SupplyWarehouseDockUpdate` for specialized behaviors
- **Common/ActionManager**: Likely dispatches construction/repair commands to this module

### Outgoing
- **Common/BuildAssistant**: Validates build locations
- **Common/ResourceGatheringManager**: Manages supply delivery logic
- **GameLogic/AIPathfind**: Handles movement to targets
- **GameClient/GameText**: For UI feedback (e.g., build errors)
- **Audio System**: Plays construction/supply sounds

## Design Patterns
- **State Machine**: Uses nested state machines (`WorkerStateMachine`, `DozerPrimaryStateMachine`, `SupplyTruckStateMachine`) to handle worker behaviors, allowing clean separation of dozer/supply truck logic.
- **Strategy Pattern**: Different worker roles (dozer/supply truck) are encapsulated in separate state machines, enabling runtime behavior switching.
- **Observer Pattern**: Listens for player commands (e.g., construction orders) via `ActionManager`, reacting dynamically to game events.
