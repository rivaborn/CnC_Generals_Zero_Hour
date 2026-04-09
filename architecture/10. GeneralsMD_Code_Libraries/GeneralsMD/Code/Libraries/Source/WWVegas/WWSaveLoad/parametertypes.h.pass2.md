# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/parametertypes.h - Enhanced Analysis

## Architectural Role
This header defines the core parameter types used by the WWSaveLoad subsystem, which is responsible for serialization/deserialization of game state. The commented-out enum suggests this was either deprecated or intended for future use in a more robust save/load system.

## Cross-References
### Incoming
- Not inferable (enum is commented out, no visible usage)

### Outgoing
- Not inferable (no visible dependencies)

## Design Patterns
- **Type System Pattern**: The commented enum defines a closed set of parameter types, suggesting a type-safe serialization approach.
- **Header-Only Pattern**: The file serves as a pure header, providing type definitions without implementation.
- **Versioning Marker**: The file contains version control metadata (Modtime, Revision), indicating this was part of a larger versioned codebase.

**Key Insight**: The commented-out enum reveals this was likely part of an early save/load system that was either abandoned or replaced with a more dynamic approach (possibly script-based). The presence of `TYPE_MODELFILENAME` and `TYPE_PRESETID` suggests tight coupling with W3D's asset system and game logic's preset system.
