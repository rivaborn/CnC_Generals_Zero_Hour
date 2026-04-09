# GeneralsMD/Code/GameEngine/Include/Common/ObjectStatusTypes.h

## Purpose
Defines object status flags used throughout the game engine for game object state management.

## Responsibilities
- Declares `ObjectStatusTypes` enum with status flags
- Provides `ObjectStatusMaskType` for bitmask operations
- Implements utility functions for status mask testing/manipulation
- Defines global `OBJECT_STATUS_MASK_NONE`

## Key Types
- **ObjectStatusTypes (Enum)**: Status flags for game objects (e.g., destroyed, stealthed, on fire)
- **ObjectStatusMaskType (Class)**: Bitmask wrapper for status flags
- **OBJECT_STATUS_MASK_NONE (Global)**: Predefined empty status mask

## Key Functions
### TEST_OBJECT_STATUS_MASK
- Purpose: Check if a specific status flag is set
- Calls: `m.test()`

### TEST_OBJECT_STATUS_MASK_ANY
- Purpose: Check if any flag in a mask is set
- Calls: `m.anyIntersectionWith()`

### TEST_OBJECT_STATUS_MASK_MULTI
- Purpose: Check multiple status conditions (some set, some clear)
- Calls: `m.testSetAndClear()`

### OBJECT_STATUS_MASK_ANY_SET
- Purpose: Check if any status flag is set
- Calls: `m.any()`

### CLEAR_OBJECT_STATUS_MASK
- Purpose: Clear all status flags
- Calls: `m.clear()`

### SET_ALL_OBJECT_STATUS_MASK_BITS
- Purpose: Set all status flags
- Calls: `m.clear()`, `m.flip()`

### FLIP_OBJECT_STATUS_MASK
- Purpose: Invert all status flags
- Calls: `m.flip()`

## Globals
- **OBJECT_STATUS_MASK_NONE (ObjectStatusMaskType)**: Predefined empty mask

## Dependencies
- `Lib/BaseType.h`
- `Common/BitFlags.h`
- `Common
