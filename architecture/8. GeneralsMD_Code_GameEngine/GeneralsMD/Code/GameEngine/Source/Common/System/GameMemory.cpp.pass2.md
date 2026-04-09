# GeneralsMD/Code/GameEngine/Source/Common/System/GameMemory.cpp - Enhanced Analysis

## Architectural Role
Central memory management hub that overrides global allocation operators and provides custom memory pools. Acts as the foundation for all other subsystems' memory needs, with special handling for W3D asset loading.

## Cross-References
### Incoming
- Game logic (unit/building creation)
- W3D rendering system (texture/model loading)
- AI (pathfinding data structures)
- Network (packet buffers)
- UI (widget allocations)

### Outgoing
- System-level allocation (`sysAllocate`, `sysFree`)
- Memory pool factory (`MemoryPoolFactory`)
- Debug logging (`DEBUG_LOG`, `DEBUG_CRASH`)

## Design Patterns
- **Singleton**: Global `TheMemoryPoolFactory` and `TheDynamicMemoryAllocator` instances
- **Factory**: `MemoryPoolFactory` creates specialized allocators
- **Wrapper**: Overrides standard `new`/`delete` to inject custom behavior

*Not inferable*: Exact checkpointing mechanism for `BlockCheckpointInfo`
