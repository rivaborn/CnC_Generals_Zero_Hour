# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/RebuildHoleBehavior.h

## Purpose
Defines behavior for GLA "hole" objects that reconstruct buildings after destruction.

## Responsibilities
- Manages worker respawn timing and spawning
- Handles building reconstruction process
- Tracks reconstruction state and templates
- Implements damage/health regeneration logic

## Key Types
- **RebuildHoleBehaviorModuleData (Class)**: Configuration data for hole behavior (timing, templates)
- **RebuildHoleBehaviorInterface (Class)**: Interface for reconstruction control
- **RebuildHoleBehavior (Class)**: Main behavior module implementing reconstruction logic
- **RebuildHoleBehaviorMagicEnum (Enum)**: Not inferable
- **RebuildHoleBehavior_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### RebuildHoleBehavior::update
- Purpose: Handles periodic updates for worker respawn and health regeneration
- Calls: Not inferable

### RebuildHoleBehavior::onDie
- Purpose: Initiates reconstruction process when object dies
- Calls: Not inferable

### RebuildHoleBehavior::startRebuildProcess
- Purpose: Starts the building reconstruction process
- Calls: Not inferable

### RebuildHoleBehavior::transferBombs
- Purpose: Transfers bombs from destroyed building to reconstruction
- Calls: Not inferable

## Globals
- None

## Dependencies
- `BehaviorModule.h`, `DieModule.h`, `UpdateModule.h`
- `MultiIniFieldParse`, `ThingTemplate`, `ObjectID`, `AsciiString`, `Real` types
- Memory pool and module macro systems
