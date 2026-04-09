# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DozerAIUpdate.h

## Purpose
Defines the AI behavior for Dozer units in Command & Conquer Generals, including building, repairing, and fortifying structures.

## Responsibilities
- Manages Dozer task states (build, repair, fortify)
- Handles dock point management for construction
- Implements state machine for Dozer behavior
- Provides interface for task assignment and cancellation
- Manages construction sounds and scaffolding

## Key Types
- **DozerPrimaryStateMachine (Class)**: Manages Dozer state transitions
- **DozerTask (Enum)**: Defines Dozer task types (build, repair, fortify)
- **DozerDockPoint (Enum)**: Defines dock points for construction
- **DozerBuildSubTask (Enum)**: Defines sub-tasks for building
- **DozerAIInterface (Class)**: Abstract interface for Dozer AI functionality
- **DozerAIUpdateModuleData (Class)**: Module data for Dozer AI configuration
- **DozerAIUpdate (Class)**: Main Dozer AI update implementation
- **DozerTaskInfo (Struct)**: Stores task target and order frame
- **DozerDockPointInfo (Struct)**: Stores dock point validity and location

## Key Functions
### findGoodBuildOrRepairPosition
- Purpose: Finds a valid position for building or repairing
- Calls: Not inferable

### findGoodBuildOrRepairPositionAndTarget
- Purpose: Finds a valid position and target for building or repairing
- Calls: Not inferable

### construct
- Purpose: Constructs an object at a specified position
- Calls: Not inferable

### newTask
- Purpose: Sets a desire to perform a specific task
- Calls: Not inferable

### cancelTask
- Purpose: Cancels a pending task
- Calls: Not inferable

### update
- Purpose: Main update entry point for Dozer AI
- Calls: Not inferable

### aiDoCommand
- Purpose: Handles AI commands for the Dozer
- Calls: Not inferable

## Globals
- None

## Dependencies
- `GameLogic/Module/AIUpdate.h`
- `AudioEventRTS` (forward reference)
- `StateMachine` (inherited)
- `AIUpdateInterface` (inherited)
- `AIUpdateModuleData` (inherited)
- `ThingTemplate`, `Coord3D`, `Player`, `ObjectID`, `Xfer`, `MultiIniFieldParse` (external types)
