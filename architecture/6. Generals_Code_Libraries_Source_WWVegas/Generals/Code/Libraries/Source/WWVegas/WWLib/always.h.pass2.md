# Generals/Code/Libraries/Source/WWVegas/WWLib/always.h - Enhanced Analysis

## Architectural Role
This file serves as the foundational memory management and utility header for the SAGE engine, providing cross-cutting concerns like custom allocators, memory pooling, and compiler abstractions that are used throughout the codebase.

## Cross-References
### Incoming
- Memory allocation calls from W3D object classes (via W3DMPO_GLUE macro)
- Game logic and rendering subsystems using min/max templates
- Debug builds leveraging custom operator new/delete overloads

### Outgoing
- Compiler-specific headers (borlandc.h, visualc.h, watcom.h)
- CRT debug functions (_malloc_dbg, _free_dbg) in debug builds
- STL components (via disabled warning 4530)

## Design Patterns
- **Object Pool Pattern**: Implemented via W3DMPO_GLUE macro for W3D object memory management
- **Template Method Pattern**: Used in min/max template functions for type safety
- **Factory Method Pattern**: createW3DMemPool acts as a factory for memory pools
