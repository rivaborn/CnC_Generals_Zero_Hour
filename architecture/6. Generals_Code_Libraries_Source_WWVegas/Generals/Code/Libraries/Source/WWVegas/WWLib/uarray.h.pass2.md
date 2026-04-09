# Generals/Code/Libraries/Source/WWVegas/WWLib/uarray.h - Enhanced Analysis

## Architectural Role
This file implements a generic hash-based unique item storage system, serving as a foundational utility for managing collections where uniqueness is critical (e.g., asset references, object registries). It bridges the low-level `hashcalc.h` and `vector.h` systems with higher-level game logic requiring deduplication.

## Cross-References
### Incoming
- Likely called by asset management systems (e.g., W3D model loading) and object registries where uniqueness is enforced
- May be used by networking code for deduplicating received object references

### Outgoing
- Depends on `HashCalculatorClass` for type-specific hashing logic
- Uses `DynamicVectorClass` for dynamic storage of unique items
- Relies on `W3DNEWARRAY` for memory allocation (SAGE engine's custom allocator)

## Design Patterns
- **Template Method Pattern**: The class is templated to work with any type that has a `HashCalculatorClass` implementation
- **Hash Table with Chaining**: Uses separate chaining (via `NextHashIndex`) to handle hash collisions
- **Resource Management**: Explicit memory management for the hash table (manual `new[]`/`delete[]`)

*Not inferable*: Exact usage patterns in game logic (e.g., which subsystems enforce uniqueness).
