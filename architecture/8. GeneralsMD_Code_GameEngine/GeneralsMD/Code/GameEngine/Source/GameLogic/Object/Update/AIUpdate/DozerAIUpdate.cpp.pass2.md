# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/DozerAIUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the specialized AI behavior for the Dozer unit, extending the base AIUpdateInterface. It manages construction, repair, and movement tasks through state machines, integrating with the game's action system, partitioning manager, and audio subsystems.

## Cross-References
### Incoming
- **AI Command System**: Calls `aiDoCommand` to handle player/AI-issued commands
- **Repair System**: Uses `findObjectToRepair` for targeting damaged objects
- **Mine Interaction**: Uses `findMine` for mine-related tasks
- **Task Completion**: Calls `internalTaskComplete` for post-task cleanup

### Outgoing
- **State Machine Framework**: Uses `StateMachine`, `ActionManager`, and custom Dozer state classes
- **Partition Manager**: Queries `ThePartitionManager` for object searches
- **Audio System**: Manages construction sounds via `TheAudio`
- **Build System**: Interacts with `BuildAssistant` for construction logic

## Design Patterns
- **State Pattern**: Uses nested state machines (`DozerPrimaryStateMachine`, `DozerActionStateMachine`) to manage complex AI behaviors
- **Command Pattern**: Encapsulates AI commands in `aiDoCommand` for centralized handling
- **Strategy Pattern**: Different `DozerActionType` states implement varying behaviors for construction/repair tasks
