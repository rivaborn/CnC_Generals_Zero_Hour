# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/HelicopterSlowDeathUpdate.h

## Purpose
Defines behavior for helicopters during slow death sequences, including spiral descent, blade ejection, and ground impact effects.

## Responsibilities
- Manages helicopter slow death animation parameters
- Handles particle effects, sound, and object creation during death sequence
- Controls spiral descent physics and timing
- Manages blade ejection and final explosion events

## Key Types
- **HelicopterSlowDeathBehaviorModuleData (Class)**: Contains configuration data for slow death behavior
- **HelicopterSlowDeathBehavior (Class)**: Implements the slow death behavior logic
- **HelicopterSlowDeathBehaviorMagicEnum (Enum)**: Not inferable
- **HelicopterSlowDeathBehavior_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### HelicopterSlowDeathBehaviorModuleData::buildFieldParse
- Purpose: Parses configuration data from INI files
- Calls: Not inferable

### HelicopterSlowDeathBehavior::beginSlowDeath
- Purpose: Initiates the slow death sequence
- Calls: Not inferable

### HelicopterSlowDeathBehavior::update
- Purpose: Updates the slow death animation state each frame
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/AudioEventRTS.h`
- `GameLogic/Module/SlowDeathBehavior.h`
- `ParticleSystemTemplate` (forward declared)
- Memory pool and module macros from SAGE engine
