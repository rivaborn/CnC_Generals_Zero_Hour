# GeneralsMD/Code/GameEngine/Include/Common/KindOf.h

## Purpose
Defines an enumeration and bitmask system for categorizing game objects by their type and properties.

## Responsibilities
- Declares `KindOfType` enum with 174+ object categories
- Provides `KindOfMaskType` bitmask wrapper for testing object properties
- Defines utility functions for bitmask operations
- Declares global masks for common object groups

## Key Types
- **KindOfType (Enum)**: Enumerates all possible object categories (e.g., `KINDOF_INFANTRY`, `KINDOF_STRUCTURE`)
- **KindOfMaskType (Class)**: Bitmask wrapper for testing object properties
- **KINDOFMASK_NONE (Global)**: Empty mask (all bits clear)
- **KINDOFMASK_FS (Global)**: Pre-initialized mask for faction structures

## Key Functions
### `TEST_KINDOFMASK`
- Purpose: Tests if a mask contains a specific kind
- Calls: `m.test(t)`

### `TEST_KINDOFMASK_ANY`
- Purpose: Tests if any bits in mask intersect with another mask
- Calls: `m.anyIntersectionWith(mask)`

### `TEST_KINDOFMASK_MULTI`
- Purpose: Tests if mask has required bits set and others clear
- Calls: `m.testSetAndClear(mustBeSet, mustBeClear)`

### `KINDOFMASK_ANY_SET`
- Purpose: Checks if any bits are set in mask
- Calls: `m.any()`

### `CLEAR_KINDOFMASK`
- Purpose: Clears all bits in mask
- Calls: `m.clear()`

### `SET_ALL_KINDOFMASK_BITS`
- Purpose: Sets all bits in mask
- Calls: `m.clear()`, `m.flip()`

### `FLIP_KINDOFMASK`
- Purpose: Inverts all bits in mask
- Calls: `m.flip()`

## Globals
- **KINDOFMASK_NONE (KindOfMaskType)**: Empty mask (initialized to zero)
- **KINDOFMASK_FS (KindOfMaskType)**: Pre-initialized mask for faction structures

## Dependencies
- `Lib/BaseType.h` (for `Bool` type)
- `Common/BitFlags.h` (for `BitFlags` template)
- `Common/BitFlagsIO.h` (for bitmask I/O)
- `initKindOfMasks()` (defined in `Kindof.cpp`)
