# Generals/Code/Libraries/Source/WWVegas/WWLib/slnode.cpp

## Purpose
Defines memory pool allocation for GenericSLNode objects.

## Responsibilities
- Declares an auto-pool for GenericSLNode with 256 slots
- Likely supports linked-list node management (inferred from filename)

## Key Types
- None (only macro definition)

## Key Functions
None

## Globals
- GenericSLNodePool (AutoPool): Pre-allocated memory pool for GenericSLNode instances

## Dependencies
- "slnode.h" (header)
- DEFINE_AUTO_POOL macro (memory management utility)
