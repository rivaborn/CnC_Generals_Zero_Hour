# Generals/Code/Tools/mangler/wlib/arraylist.h - Enhanced Analysis

## Architectural Role
This file defines a core container class (`ArrayList`) used throughout the engine for dynamic array-based storage. It's part of the toolchain's utility library (`wlib`), providing a memory-efficient list implementation that's heavily used in both tools and runtime code.

## Cross-References
### Incoming
- **Tools**: Matchbot's `wlib` (duplicate file in different tool directory)
- **Runtime**: Likely used in game logic containers (e.g., unit lists, waypoints)

### Outgoing
- **Memory**: Direct `new`/`delete[]` calls with manual object construction
- **STL-like**: Mimics vector/list operations without STL dependency

## Design Patterns
- **Object Pool**: Pre-allocates slots and uses placement new for efficiency
- **Manual Memory Management**: Explicit destructor calls and raw memory handling
- **Template Metaprogramming**: Generic container with type-independent operations

*Not inferable*: Exact runtime usage patterns (e.g., threading safety, typical payload types).
