# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/JetSlowDeathBehavior.h

## Purpose
Defines behavior for jet slow death animations and effects in the game.

## Responsibilities
- Manages jet death sequence with multiple stages (initial death, secondary, hit ground, final explosion)
- Handles visual effects (FXList) and object creation lists (OCL) for each death stage
- Controls jet physics during death (roll rate, pitch rate, fall speed)
- Manages audio events for death sounds
- Provides module data structure for configuration

## Key Types
- **JetSlowDeathBehaviorModuleData (Class)**: Contains configuration data for jet death behavior (FX lists, delays, rates, sounds)
- **JetSlowDeathBehavior (Class)**: Implements the jet slow death behavior logic
- **JetSlowDeathBehaviorMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **FXList (Class)**: Reference to FXList class for visual effects (defined elsewhere)

## Key Functions
### JetSlowDeathBehavior::onDie
- Purpose: Handles the initial death event
- Calls: Not inferable

### JetSlowDeathBehavior::beginSlowDeath
- Purpose: Starts the slow death sequence
- Calls: Not inferable

### JetSlowDeathBehavior::update
- Purpose: Updates the death animation state each frame
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/AudioEventRTS.h` (AudioEventRTS)
- `GameLogic/Module/BehaviorModule.h` (BehaviorModule)
- `GameLogic/Module/SlowDeathBehavior.h` (SlowDeathBehavior)
- `FXList` (forward reference)
