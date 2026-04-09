# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/uarray.h - Enhanced Analysis

## Architectural Role
This file implements a generic hash-based unique item storage system, critical for managing game entities (units, buildings) where uniqueness is required. It bridges the low-level memory management (via `DynamicVectorClass`) with the game's object identification system (via `HashCalculatorClass`).

## Cross-References
### Incoming
- Likely called by game logic systems needing unique object tracking (e.g., unit/building managers)
- Used by modding infrastructure for custom object registration

### Outgoing
- Depends on `HashCalculatorClass` for type-specific hashing
- Uses `DynamicVectorClass` for dynamic memory management
- Relies on `W3DNEWARRAY` for memory allocation

## Design Patterns
- **Template Method Pattern**: Uses `HashCalculatorClass` as a strategy for type-specific hashing
- **Hash Table with Chaining**: Implements collision resolution via linked lists in the hash table
- **RAII**: Manages memory lifecycle via constructor/destructor for the hash table

*Not inferable*: Exact usage contexts in game logic or modding systems.
