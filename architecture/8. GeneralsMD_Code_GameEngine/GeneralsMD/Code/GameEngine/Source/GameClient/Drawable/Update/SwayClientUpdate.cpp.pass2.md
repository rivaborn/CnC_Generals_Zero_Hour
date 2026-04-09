# GeneralsMD/Code/GameEngine/Source/GameClient/Drawable/Update/SwayClientUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements client-side environmental animation for drawable objects (e.g., trees) affected by wind. It bridges the script-driven breeze system with the rendering pipeline, ensuring visual consistency across clients while minimizing unnecessary updates for off-screen objects.

## Cross-References
### Incoming
- **GameClient/Drawable.h**: Uses `Drawable` interface for matrix manipulation and visibility checks
- **GameLogic/ScriptEngine.h**: Consumes `BreezeInfo` for wind parameters
- **GameLogic/Object.h**: Checks `OBJECT_STATUS_BURNED` to disable sway for damaged objects

### Outgoing
- **Common/RandomValue.h**: Uses `GameClientRandomValueReal()` for parameter randomization
- **Common/Xfer.h**: Implements serialization for network sync
- **GameClient/Module/SwayClientUpdate.h**: Extends `ClientUpdateModule` base class

## Design Patterns
- **Observer Pattern**: Reacts to breeze state changes via version tracking (`m_curVersion`)
- **Lazy Update**: Only processes visible objects unless breeze parameters change
- **State Caching**: Stores current sway values to avoid redundant calculations

*Not inferable*: No clear use of Strategy or Decorator patterns despite modular design.
