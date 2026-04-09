# GeneralsMD/Code/GameEngine/Include/GameLogic/TurretAI.h

## Purpose
Defines the TurretAI system, including state machines and behaviors for turret control in the game.

## Responsibilities
- Declares turret state machine and state classes
- Defines turret behavior states (idle, aim, fire, recenter, hold)
- Provides turret configuration data structure
- Declares TurretAI class for turret control logic

## Key Types
- TurretStateType (Enum): turret state identifiers
- TurretStateMachine (Class): base state machine for turret AI
- TurretState (Class): base state class for turret behaviors
- TurretAIIdleState (Class): idle turret behavior
- TurretAIAimTurretState (Class): turret aiming behavior
- TurretAIRecenterTurretState (Class): turret recentering behavior
- TurretAIHoldTurretState (Class): turret hold behavior
- TurretAIData (Class): turret configuration data
- TurretTargetType (Enum): target type identifiers
- TurretAI (Class): main turret AI controller

## Key Functions
### updateTurretAI
- Purpose: implements turret behavior updates
- Calls: Not inferable

### setTurretTargetObject
- Purpose: sets turret target to track an object
- Calls: Not inferable

### setTurretTargetPosition
- Purpose: sets turret target to track a position
- Calls: Not inferable

### recenterTurret
- Purpose: recenters turret to default position
- Calls: Not inferable

### notifyFired
- Purpose: handles weapon fire notification
- Calls: Not inferable

### friend_turnTowardsAngle
- Purpose: turns turret toward desired angle
- Calls: Not inferable

### friend_turnTowardsPitch
- Purpose: adjusts turret pitch
- Calls: Not inferable

## Globals
- DEFAULT_TURN_RATE (Real): default turret turn rate
- DEFAULT_PITCH_RATE (Real): default turret pitch rate

## Dependencies
- Common/StateMachine.h
- Common/GameMemory.h
- MemoryPoolObject, Snapshot, NotifyWeaponFiredInterface
- Weapon, Object, Team, Coord3D, INI, MultiIniFieldParse classes
