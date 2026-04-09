# Generals/Code/Libraries/Source/WWVegas/WWLib/incdec.h

## Purpose
Provides template operators for incrementing and decrementing enumeration types.

## Responsibilities
- Defines `operator++` and `operator--` for enum types.
- Supports both prefix and postfix forms.
- Enables bitwise arithmetic on enums via casting to `int`.

## Key Types
None

## Key Functions
### `operator++(T & a)`
- Purpose: Prefix increment for enum types.
- Calls: None

### `operator++(T & a, int)`
- Purpose: Postfix increment for enum types.
- Calls: None

### `operator--(T & a)`
- Purpose: Prefix decrement for enum types.
- Calls: None

### `operator--(T & a, int)`
- Purpose: Postfix decrement for enum types.
- Calls: None

## Globals
None

## Dependencies
- None (header-only, no external symbols).
