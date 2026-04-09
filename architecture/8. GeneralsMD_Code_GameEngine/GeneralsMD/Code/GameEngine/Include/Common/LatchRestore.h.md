# GeneralsMD/Code/GameEngine/Include/Common/LatchRestore.h

## Purpose
Provides a template class for temporarily overriding a variable's value within a scope, automatically restoring the original value when the object goes out of scope.

## Responsibilities
- Save and restore a variable's original value
- Allow temporary modification of a variable
- Ensure restoration even with early returns or exceptions

## Key Types
- LatchRestore (Class): RAII wrapper for temporary variable overrides

## Key Functions
### LatchRestore::LatchRestore
- Purpose: Constructor saves original value and sets new value
- Calls: None

### LatchRestore::~LatchRestore
- Purpose: Destructor restores original value
- Calls: None

## Globals
- None

## Dependencies
- None (header-only template)
