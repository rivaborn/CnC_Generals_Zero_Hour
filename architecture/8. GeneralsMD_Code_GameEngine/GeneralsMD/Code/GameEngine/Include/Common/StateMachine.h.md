# GeneralsMD/Code/GameEngine/Include/Common/StateMachine.h

## Purpose
Defines a finite state machine framework for game object behavior management.

## Responsibilities
- Provides core state machine classes (State, StateMachine)
- Supports state transitions, conditions, and utility states
- Manages state machine lifecycle (init, reset, update)
- Handles sleep/continue/failure/success states
- Supports debugging and memory management

## Key Types
- **State (Class)**: Base class for individual states in a state machine
- **StateMachine (Class)**: Manages a collection of states and transitions
- **StateID (Type)**: Unique identifier for states
- **StateReturnType (Enum)**: Return codes for state operations (continue/success/failure/sleep)
- **StateConditionInfo (Struct)**: Contains transition condition data
- **SuccessState/FailureState/ContinueState/SleepState (Classes)**: Utility states with predefined behavior

## Key Functions
### CONVERT_SLEEP_TO_CONTINUE
- Purpose: Converts sleep states to continue for enclosing machines
- Calls: IS_STATE_SLEEP

### MIN_SLEEP
- Purpose: Determines minimum sleep time between enclosing and enclosed machines
- Calls: IS_STATE_SLEEP, GET_STATE_SLEEP_FRAMES

## Globals
- **MACHINE_DONE_STATE_ID (const)**: Special state ID for completion
- **INVALID_STATE_ID (const)**: Invalid state ID marker

## Dependencies
- Common/GameMemory.h, GameType.h, ModelState.h, Snapshot.h, Xfer.h
- MemoryPoolObject, Snapshot, Xfer classes
- std::vector, std::map containers
- Object class (forward declared)
