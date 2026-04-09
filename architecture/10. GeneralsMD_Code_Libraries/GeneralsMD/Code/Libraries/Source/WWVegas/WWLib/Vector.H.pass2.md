# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/Vector.H - Enhanced Analysis

## Architectural Role
This file provides the foundational container abstraction for the SAGE engine, serving as the primary dynamic array implementation used throughout the codebase for game object management, resource tracking, and data structures. Its vector classes underpin many subsystems' memory management patterns.

## Cross-References
### Incoming
- Game object managers (e.g., unit, building, projectile systems)
- Resource loading pipelines
- AI behavior trees and decision structures
- Network synchronization data structures
- UI element containers

### Outgoing
- Memory allocation system (`W3DNEWARRAY`)
- Bit manipulation utilities
- Standard C++ memory management (`new`, `delete`)

## Design Patterns
- **Template Method Pattern**: Base `VectorClass` defines interface while derived classes implement specific behaviors (e.g., `DynamicVectorClass` handles growth)
- **Flyweight Pattern**: `BooleanVectorClass` uses bit-packing to minimize memory for boolean states
- **Proxy Pattern**: `operator[]` in `BooleanVectorClass` provides virtual access to packed bits

*Not inferable*: Exact usage patterns in game systems (e.g., thread safety assumptions, typical element types)
