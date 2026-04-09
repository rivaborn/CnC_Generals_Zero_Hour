# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/PoisonedBehavior.h

## Purpose
Defines behavior for handling poison damage effects in the game.

## Responsibilities
- Manages poison damage application over time
- Handles poison duration and intervals
- Controls poisoned state transitions
- Provides damage interface for poison effects

## Key Types
- **PoisonedBehaviorModuleData (Class)**: Stores poison damage interval and duration settings
- **PoisonedBehavior (Class)**: Implements poison behavior logic
- **PoisonedBehaviorMagicEnum (Enum)**: Not inferable
- **PoisonedBehavior_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### PoisonedBehavior::onDamage
- Purpose: Handles damage application and starts poison effects
- Calls: startPoisonedEffects

### PoisonedBehavior::update
- Purpose: Updates poison state and applies periodic damage
- Calls: calcSleepTime

### PoisonedBehavior::startPoisonedEffects
- Purpose: Initializes poison effects when damage is applied

### PoisonedBehavior::stopPoisonedEffects
- Purpose: Cleans up poison effects when duration ends

## Globals
- None

## Dependencies
- BehaviorModule.h
- DamageModule.h
- UpdateModule.h
- Memory pool macros and module creation macros
