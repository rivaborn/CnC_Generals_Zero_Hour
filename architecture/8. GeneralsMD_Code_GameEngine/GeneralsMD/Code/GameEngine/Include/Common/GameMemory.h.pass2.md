# GeneralsMD/Code/GameEngine/Include/Common/GameMemory.h - Enhanced Analysis

## Architectural Role
This header defines the core memory management infrastructure for the SAGE engine, providing custom allocators, memory pools, and debugging utilities that underpin all game object allocation. It serves as the foundation for the engine's memory hierarchy, supporting both fixed-size and dynamic allocations while enabling detailed memory tracking in debug builds.

## Cross-References
### Incoming
- Game object classes (e.g., units, buildings) inherit from `MemoryPoolObject`
- Subsystems like W3D rendering, AI, and networking use custom allocators
- STL containers use `STLSpecialAlloc` for memory management

### Outgoing
- Calls into `userMemoryManagerGetDmaParms` and `userMemoryManagerInitPools` (user-defined)
- Relies on `Debug.h` and `Errors.h` for assertion and error handling
- Uses `BaseType.h` for fundamental types

## Design Patterns
- **Object Pool Pattern**: `MemoryPool` implements pre-allocated object pools for performance
- **Factory Pattern**: `MemoryPoolFactory` centralizes pool creation and management
- **Singleton Pattern**: Global instances (`TheMemoryPoolFactory`, `TheDynamicMemoryAllocator`) provide system-wide access

*Not inferable*: Specific usage patterns of `DynamicMemoryAllocator` sub-pools.
