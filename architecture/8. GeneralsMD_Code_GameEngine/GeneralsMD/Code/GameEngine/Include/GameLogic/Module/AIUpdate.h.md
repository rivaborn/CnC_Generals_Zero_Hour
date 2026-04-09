# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/AIUpdate.h

## Purpose
Defines the AIUpdateInterface class and related types for game entity AI behavior in Command & Conquer Generals.

## Responsibilities
- Declares AI state machine and behavior interfaces
- Defines locomotion control and pathfinding systems
- Provides attack/guard/movement command implementations
- Manages AI mood and attitude systems
- Handles turret and weapon targeting logic

## Key Types
- AIUpdateInterface (Class): Main AI behavior interface for game entities
- AIUpdateModuleData (Class): Module data containing AI configuration
- LocomotorSetType (Enum): Types of movement behaviors
- GuardTargetType (Enum): Types of guard targets
- MoodMatrixParameters (Enum): AI mood and behavior parameters

## Key Functions
### privateMoveToPosition
- Purpose: Move to given position tightening formation
- Calls: Not inferable

### privateAttackObject
- Purpose: Attack given object
- Calls: Not inferable

### privateGuardPosition
- Purpose: Guard given position
- Calls: Not inferable

### update
- Purpose: Main AI update loop
- Calls: doLocomotor, getNextMoodTarget, etc.

### computePath
- Purpose: Compute path to destination
- Calls: PathfindServicesInterface methods

## Globals
- FAST_AS_POSSIBLE (Real): Constant for maximum speed value

## Dependencies
- GameLogic/Module/UpdateModule.h
- GameLogic/AI.h
- GameLogic/AIStateMachine.h
- GameLogic/GameLogic.h
- GameLogic/LocomotorSet.h
- Various AI interface classes (DozerAIInterface, etc.)
