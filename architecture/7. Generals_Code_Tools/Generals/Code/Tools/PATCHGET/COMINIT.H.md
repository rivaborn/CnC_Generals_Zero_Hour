# Generals/Code/Tools/PATCHGET/COMINIT.H

## Purpose
Header file declaring the `ComInit` class for automatic COM initialization in the PATCHGET tool.

## Responsibilities
- Declares the `ComInit` class for COM initialization.
- Provides constructor and destructor for COM lifecycle management.
- Serves as a header guard to prevent multiple inclusions.

## Key Types
- **ComInit (Class)**: Wrapper for COM initialization and cleanup.

## Key Functions
### ComInit()
- Purpose: Constructor that initializes COM.
- Calls: Not inferable (implementation in cominit.cpp).

### ~ComInit()
- Purpose: Destructor that uninitializes COM.
- Calls: Not inferable (implementation in cominit.cpp).

## Globals
- None.

## Dependencies
- None (header-only, no external symbols).
