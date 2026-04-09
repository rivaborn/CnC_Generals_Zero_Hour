# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/always.h - Enhanced Analysis

## Architectural Role
This file serves as the foundational memory management and utility header for the SAGE engine, providing cross-cutting memory allocation strategies, compiler abstractions, and utility macros used throughout the codebase. It bridges low-level memory operations with higher-level engine systems.

## Cross-References
### Incoming
- Memory allocation calls from W3D rendering system (e.g., mesh/animation loading)
- Game object instantiation (e.g., units, buildings inheriting from W3DMPO)
- Utility macro usage in game logic and AI systems

### Outgoing
- Debug memory tracking via `_malloc_dbg` (MSVC debug builds)
- Memory pool management (createW3DMemPool/allocateFromW3DMemPool)
- Compiler-specific headers (visualc.h, borlandc.h)

## Design Patterns
- **Object Pool Pattern**: Memory pools for W3D objects to reduce fragmentation
- **Template Method**: `min`/`max` templates for type-safe comparisons
- **Macro Abstraction**: Compiler-specific code isolation via conditional includes

*Not inferable*: Exact inheritance hierarchy of W3DMPO subclasses.
