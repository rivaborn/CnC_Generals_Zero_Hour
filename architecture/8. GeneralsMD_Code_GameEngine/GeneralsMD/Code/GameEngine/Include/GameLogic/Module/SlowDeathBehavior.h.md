# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SlowDeathBehavior.h

## Purpose
Defines the SlowDeathBehavior module for handling gradual destruction of objects over time with visual effects and phases.

## Responsibilities
- Manages timed destruction of objects with configurable phases (initial, midpoint, final)
- Handles visual effects, object creation lists, and weapons during destruction
- Provides interface for controlling slow death behavior via damage info
- Tracks destruction state with flags and timers

## Key Types
- **SlowDeathBehaviorModuleData (Class)**: Contains configuration data for slow death behavior (timers, effects, weapons).
- **SlowDeathBehaviorInterface (Class)**: Interface for controlling slow death behavior.
- **SlowDeathBehavior (Class)**: Main module implementing slow death logic, inheriting from UpdateModule and DieModuleInterface.
- **SlowDeathPhaseType (Enum)**: Defines phases of slow death (initial, midpoint, final).

## Key Functions
### SlowDeathBehavior::onDie
- Purpose: Handles object destruction logic when damage is applied.
- Calls: getSlowDeathBehaviorModuleData(), isDieApplicable(), beginSlowDeath()

### SlowDeathBehavior::beginSlowDeath
- Purpose: Initiates the slow death process with damage information.
- Calls: getSlowDeathBehaviorModuleData(), doPhaseStuff()

### SlowDeathBehavior::update
- Purpose: Updates the slow death state each frame.
- Calls: getSlowDeathBehaviorModuleData(), doPhaseStuff()

## Globals
- **TheSlowDeathPhaseNames (const char**)**: Array of phase name strings (conditionally defined).

## Dependencies
- **BehaviorModule.h, DieModule.h, UpdateModule.h**: Base module headers.
- **FXList, ObjectCreationList, WeaponTemplate, DamageInfo**: External classes used for effects and damage handling.
