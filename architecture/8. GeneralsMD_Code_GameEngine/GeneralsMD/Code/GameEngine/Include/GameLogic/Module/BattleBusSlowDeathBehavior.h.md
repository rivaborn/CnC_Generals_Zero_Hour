# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/BattleBusSlowDeathBehavior.h

## Purpose
Defines behavior for the Battle Bus's slow death animation and destruction logic.

## Responsibilities
- Manages two-stage death sequence (throw + impact)
- Handles passenger damage during throw
- Controls empty hulk destruction delay
- Triggers FX and object creation lists at key moments

## Key Types
- **BattleBusSlowDeathBehaviorModuleData (Class)**: Contains configuration data for the death behavior (FX lists, damage values, timers).
- **BattleBusSlowDeathBehavior (Class)**: Implements the actual death behavior logic.
- **BattleBusSlowDeathBehaviorMagicEnum (Enum)**: Not inferable (likely internal macro enum).
- **FXList (Class)**: Reference to FX lists used during death sequence.

## Key Functions
### BattleBusSlowDeathBehavior::onDie
- Purpose: Handles the initial death event.
- Calls: Not inferable.

### BattleBusSlowDeathBehavior::beginSlowDeath
- Purpose: Initiates the slow death animation sequence.
- Calls: Not inferable.

### BattleBusSlowDeathBehavior::update
- Purpose: Updates the death animation state each frame.
- Calls: Not inferable.

## Globals
None.

## Dependencies
- `BehaviorModule.h`
- `SlowDeathBehavior.h`
- `FXList` (forward reference)
- `ObjectCreationList` (forward reference)
- `MultiIniFieldParse` (used in `buildFieldParse`)
- Memory pool and module macros (internal SAGE framework).
