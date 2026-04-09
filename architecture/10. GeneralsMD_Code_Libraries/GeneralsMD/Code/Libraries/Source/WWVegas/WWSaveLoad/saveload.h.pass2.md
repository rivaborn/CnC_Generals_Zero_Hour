# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/saveload.h - Enhanced Analysis

## Architectural Role
This header defines the core save/load framework, acting as the central coordinator for serialization across the engine. It bridges game state persistence with the chunk-based I/O system, handling object registration, pointer remapping, and post-load processing.

## Cross-References
### Incoming
- Game subsystems (e.g., physics, WW3D) call `SaveLoadSystemClass::Save/Load` during game state serialization
- Persistable objects use `REQUEST_POINTER_REMAP` macros during deserialization
- Post-load callbacks register via `Register_Post_Load_Callback`

### Outgoing
- Uses `PointerRemapClass` for pointer remapping during load
- Relies on `SList` for managing subsystem/factory registries
- Delegates chunk I/O to `ChunkSaveClass`/`ChunkLoadClass` implementations

## Design Patterns
- **Factory Pattern**: `PersistFactoryClass` enables runtime object creation without tight coupling
- **Observer Pattern**: Post-load callbacks use `SList` for deferred execution
- **Bridge Pattern**: `SaveLoadSubSystemClass` abstracts file format structure from concrete data

*Not inferable*: Exact chunk I/O implementation details (micro-chunks vs. standard chunks).
