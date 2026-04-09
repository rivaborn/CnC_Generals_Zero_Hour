# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/DozerAIUpdate.cpp

## Purpose
Implements AI behavior for the Dozer unit in Command & Conquer Generals Zero Hour, handling construction, repair, and movement tasks.

## Responsibilities
- Manages Dozer task execution (build, repair, fortify)
- Controls state machines for action selection and movement
- Handles task cancellation and completion
- Provides docking point management for construction
- Implements boredom behavior for idle Dozers

## Key Types
- **DozerActionType (Enum)**: Defines Dozer action states (pick position, move, execute)
- **DozerActionPickActionPosState (Class)**: State for selecting action positions
- **DozerActionMoveToActionPosState (Class)**: State for moving to action positions
- **DozerActionDoActionState (Class)**: State for executing actions (build/repair)
- **DozerPrimaryStateMachine (Class)**: Manages primary Dozer behaviors
- **DozerActionStateMachine (Class)**: Manages action-specific behaviors

## Key Functions
### findObjectToRepair
- Purpose: Locates objects needing repair within the Dozer's range
- Calls: ThePartitionManager queries, distance checks

### findMine
- Purpose: Finds mine objects for Dozer actions
- Calls: ThePartitionManager queries, object type checks

### aiDoCommand
- Purpose: Handles AI commands for the Dozer
- Calls: createMachines, privateRepair, privateResumeConstruction, AIUpdateInterface methods

### internalTaskComplete
- Purpose: Handles task completion cleanup
- Calls: internalTaskCompleteOrCancelled, goal object state updates

## Globals
- **MIN_ACTION_TOLERANCE (Real)**: Minimum distance tolerance for action execution (70.0f)

## Dependencies
- Common: ActionManager, Team, StateMachine, BuildAssistant, ThingTemplate, ThingFactory, Player, Money, Radar, RandomValue, GameState, GlobalData, Xfer
- GameClient: Drawable, GameText, InGameUI
- GameLogic: AIPathfind, PartitionManager, Locomotor, various Module headers
- Audio: AudioEventRTS for construction sounds
