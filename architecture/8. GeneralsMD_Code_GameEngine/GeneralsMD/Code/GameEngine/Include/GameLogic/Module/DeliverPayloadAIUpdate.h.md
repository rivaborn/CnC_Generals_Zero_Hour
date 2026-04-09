# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DeliverPayloadAIUpdate.h

## Purpose
Defines the AI state machine and data structures for airborne cargo delivery in Command & Conquer Generals.

## Responsibilities
- Manages state machine for delivery aircraft behavior
- Handles payload drop logic and targeting
- Provides configuration data for delivery parameters
- Tracks delivery attempts and success conditions

## Key Types
- **DeliverPayloadStateMachine (Class)**: Controls delivery aircraft state transitions
- **DeliverPayloadData (Class)**: Contains delivery configuration parameters
- **DeliverPayloadAIUpdate (Class)**: Main AI update interface for delivery logic
- **DeliverPayloadAIUpdateModuleData (Class)**: Module-specific configuration data
- **DiveState (Enum)**: Tracks aircraft dive bombing states (pre-dive, diving, post-dive)

## Key Functions
### `deliverPayload`
- Purpose: Initiates payload delivery sequence
- Calls: State machine transitions, target position calculations

### `update`
- Purpose: Main update loop for delivery state machine
- Calls: State machine update, distance checks, decal management

### `isCloseEnoughToTarget`
- Purpose: Determines if aircraft is within delivery range
- Calls: Distance calculations

## Globals
- None

## Dependencies
- `StateMachine.h` (base state machine)
- `AIUpdate.h` (AI update interface)
- `RadiusDecal.h` (visual effects)
- `MultiIniFieldParse` (configuration parsing)
