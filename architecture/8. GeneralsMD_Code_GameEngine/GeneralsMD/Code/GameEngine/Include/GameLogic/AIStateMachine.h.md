# GeneralsMD/Code/GameEngine/Include/GameLogic/AIStateMachine.h

## Purpose
Defines the AI state machine system for Command & Conquer Generals, including state types, state classes, and transition conditions.

## Responsibilities
- Declares AI state types (enum AIStateType)
- Defines state machine classes (AIStateMachine, AttackStateMachine)
- Declares various AI state classes (e.g., AIIdleState, AIAttackState)
- Provides state transition condition functions
- Manages state machine ownership and memory allocation

## Key Types
- AIStateType (Enum): enumerates all possible AI states
- AIStateMachine (Class): base AI state machine implementation
- AttackStateMachine (Class): specialized attack state machine
- AIIdleState (Class): idle behavior state
- AIAttackState (Class): attack behavior state
- AIMoveToState (Class): movement state
- AIGuardState (Class): guard behavior state
- NotifyWeaponFiredInterface (Class): weapon firing notification interface

## Key Functions
### outOfWeaponRangeObject
- Purpose: checks if target is out of weapon range
- Calls: Not inferable

### outOfWeaponRangePosition
- Purpose: checks if position is out of weapon range
- Calls: Not inferable

### wantToSquishTarget
- Purpose: determines if unit wants to attack target
- Calls: Not inferable

## Globals
- None

## Dependencies
- "Lib/Basetype.h"
- "Common/AudioEventRTS.h"
- "Common/GameMemory.h"
- "Common/StateMachine.h"
- "GameLogic/TerrainLogic.h"
- Forward declarations: AIGuardMachine, Weapon, Team, etc.
