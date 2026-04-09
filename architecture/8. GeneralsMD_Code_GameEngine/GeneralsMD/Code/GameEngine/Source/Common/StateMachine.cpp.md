# GeneralsMD/Code/GameEngine/Source/Common/StateMachine.cpp

## Purpose
Implements a finite state machine system for game objects, handling state transitions, sleep states, and debugging.

## Responsibilities
- Manages state transitions and execution flow
- Handles sleep/wake logic for states
- Provides debugging output for state machines
- Supports serialization (Xfer) for save/load
- Tracks goal objects and positions

## Key Types
- **State (Class)**: Represents a single state in the state machine
- **StateMachine (Class)**: Manages a collection of states and their transitions
- **StIncrementer (Class)**: RAII helper for tracking recursion depth
- **TransitionInfo (Struct)**: Stores transition conditions and targets

## Key Functions
### State::friend_checkForTransitions
- Purpose: Handles state transitions based on return status
- Calls: getMachine(), internalSetState()

### StateMachine::internalSetState
- Purpose: Changes current state with proper exit/enter handling
- Calls: internalGetState(), onExit(), onEnter(), friend_checkForTransitions()

### StateMachine::xfer
- Purpose: Serializes/deserializes state machine data
- Calls: xferVersion(), xferUnsignedInt(), xferBool(), xferObjectID(), xferCoord3D()

## Globals
- **TheGameLogic (External)**: Accesses game frame and object lookup
- **TheGlobalData (External)**: Contains debug flags

## Dependencies
- Common/Errors.h, Common/StateMachine.h, Common/ThingTemplate.h
- Common/GameState.h, Common/GlobalData.h, Common/Xfer.h
- GameLogic/GameLogic.h, GameLogic/Object.h
