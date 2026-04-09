# GeneralsMD/Code/GameEngine/Include/Common/DisabledTypes.h

## Purpose
Defines enumeration and bitmask utilities for tracking disabled states of game objects.

## Responsibilities
- Declares `DisabledType` enum for various disabled states
- Provides `DisabledMaskType` bitmask wrapper for state tracking
- Implements utility functions for bitmask operations
- Declares global bitmask constants

## Key Types
- **DisabledType (Enum)**: Enumerates all possible disabled states (e.g., EMP, hacked, paralyzed)
- **DisabledMaskType (Class)**: Bitmask wrapper for tracking multiple disabled states
- **DISABLED_ANY (Enum)**: Special value indicating any disabled state (read-only)

## Key Functions
### TEST_DISABLEDMASK
- Purpose: Checks if a specific disabled state is set in the mask
- Calls: `m.test()`

### TEST_DISABLEDMASK_ANY
- Purpose: Checks if any disabled state from a mask is set
- Calls: `m.anyIntersectionWith()`

### TEST_DISABLEDMASK_MULTI
- Purpose: Checks if required states are set and forbidden states are clear
- Calls: `m.testSetAndClear()`

### DISABLEDMASK_ANY_SET
- Purpose: Checks if any disabled state is set in the mask
- Calls: `m.any()`

### CLEAR_DISABLEDMASK
- Purpose: Clears all disabled states from the mask
- Calls: `m.clear()`

### SET_ALL_DISABLEDMASK_BITS
- Purpose: Sets all possible disabled states in the mask
- Calls: `m.clear()`, `m.flip()`

### FLIP_DISABLEDMASK
- Purpose: Inverts all disabled states in the mask
- Calls: `m.flip()`

## Globals
- **DISABLEDMASK_NONE (DisabledMaskType)**: Pre-initialized empty mask
- **DISABLE
