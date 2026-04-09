# GeneralsMD/Code/Libraries/Source/WWVegas/WWDebug/wwhack.h

## Purpose
Defines a macro for forcing module linkage in a library to ensure inclusion in the executable.

## Responsibilities
- Provides `FORCE_LINK` macro to enforce module inclusion.
- Declares corresponding `_Force_Link_` function template.
- Prevents duplicate inclusion via header guards.

## Key Types
- None

## Key Functions
### `FORCE_LINK(module)`
- Purpose: Forces linkage of a specified module into the executable.
- Calls: `_Force_Link_ ## module()`

### `DECLARE_FORCE_LINK(module)`
- Purpose: Declares the linkage function for a module.
- Calls: None

## Globals
- None

## Dependencies
- Uses `_MSC_VER` for `#pragma once` compatibility.
- Relies on C++ preprocessor macros.
