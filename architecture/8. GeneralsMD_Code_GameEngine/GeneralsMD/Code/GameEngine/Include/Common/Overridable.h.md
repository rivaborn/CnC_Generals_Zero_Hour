# GeneralsMD/Code/GameEngine/Include/Common/Overridable.h

## Purpose
Defines the `Overridable` class for managing object overrides in the game engine, supporting runtime modifications via configuration files.

## Responsibilities
- Provides a linked-list mechanism for object overrides
- Supports marking objects as overrides and cleaning them up
- Enables recursive traversal to find the final override in a chain
- Integrates with memory pool management for object lifecycle

## Key Types
- **Overridable (Class)**: Base class for objects that can be overridden at runtime

## Key Functions
### `getNextOverride`
- Purpose: Returns the next override in the chain
- Calls: None

### `getFinalOverride`
- Purpose: Recursively finds the last override in the chain
- Calls: `getFinalOverride` (recursive)

### `setNextOverride`
- Purpose: Sets the next override object in the chain
- Calls: None

### `friend_getNextOverride`
- Purpose: Non-const accessor for next override (for internal use)
- Calls: None

### `friend_getFinalOverride`
- Purpose: Non-const recursive final override finder (for internal use)
- Calls: `friend_getFinalOverride` (recursive)

### `markAsOverride`
- Purpose: Marks the object as an override
- Calls: None

### `deleteOverrides`
- Purpose: Recursively deletes all overrides in the chain
- Calls: `deleteInstance`, `deleteOverrides` (recursive)

## Globals
- None

## Dependencies
- `MemoryPoolObject` (base class)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- `Bool` type
- `deleteInstance` method (inherited)
