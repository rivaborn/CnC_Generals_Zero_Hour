# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Helper/StatusDamageHelper.cpp

## Purpose
Manages timed status effects on game objects, clearing them after a specified duration.

## Responsibilities
- Tracks status conditions and their expiration times
- Clears status effects when timers expire
- Handles network synchronization via Xfer
- Manages wake/sleep cycles for efficient updates

## Key Types
- **StatusDamageHelper (Class)**: Helper for managing timed status effects on objects
- **ObjectStatusTypes (Enum)**: Status effect types (external)

## Key Functions
### `update()`
- Purpose: Handles timer expiration and clears status effects
- Calls: `clearStatusCondition()`

### `clearStatusCondition()`
- Purpose: Removes the tracked status effect from the object
- Calls: `getObject()->clearStatus()`

### `doStatusDamage(ObjectStatusTypes status, Real duration)`
- Purpose: Applies a status effect with a timed duration
- Calls: `clearStatusCondition()`, `getObject()->setStatus()`, `setWakeFrame()`

### `xfer(Xfer *xfer)`
- Purpose: Serializes object state for network synchronization
- Calls: `ObjectHelper::xfer()`

## Globals
- **TheGameLogic (External)**: Provides game frame timing

## Dependencies
- `StatusDamageHelper.h` (header)
- `ObjectHelper` (base class)
- `Xfer` (serialization)
- `Object` (game entity)
- `GameLogic` (game state)
