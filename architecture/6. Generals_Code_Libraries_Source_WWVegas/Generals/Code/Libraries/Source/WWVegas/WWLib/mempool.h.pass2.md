# Generals/Code/Libraries/Source/WWVegas/WWLib/mempool.h - Enhanced Analysis

## Architectural Role
This file implements a custom memory allocator subsystem, providing object pooling to optimize frequent allocations/deallocations common in game entities (e.g., projectiles, units). It's a foundational utility used across the engine for performance-critical memory management.

## Cross-References
### Incoming
- Game entity classes (e.g., projectiles, units) that inherit from `AutoPoolClass`
- Subsystems requiring frequent object creation/destruction (e.g., particle systems, AI behavior trees)

### Outgoing
- Global `::operator new`/`delete` for block memory allocation
- `wwdebug.h` for assertion checks

## Design Patterns
- **Object Pool Pattern**: Pre-allocates memory blocks to reduce fragmentation and allocation overhead
- **Template Metaprogramming**: Uses templates for type-safe pooling of arbitrary classes
- **Operator Overloading**: Custom `new`/`delete` to enforce pool usage for derived classes

*Not inferable*: Specific usage patterns in game code (e.g., which entity types use pooling).
