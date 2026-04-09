# GeneralsMD/Code/GameEngine/Source/Common/System/CDManager.cpp - Enhanced Analysis

## Architectural Role
This file implements the CD management subsystem, which handles CD drive detection and disk verification. It operates as a singleton service that periodically checks CD presence, critical for anti-piracy measures in the original release.

## Cross-References
### Incoming
- Likely called by anti-piracy/DRM systems (not shown in code)
- Game initialization code (implied by `init()` method)

### Outgoing
- Uses `TheGameLogic` for frame counting (game timing)
- Relies on `LListNode` for drive storage (memory management)
- Depends on abstract `CDDriveInterface` for drive operations

## Design Patterns
- **Singleton**: Global `TheCDManager` instance provides system-wide access
- **Factory Method**: `createDrive()` (implied) for drive object creation
- **Observer**: Periodic updates suggest a polling-based observation pattern

*Not inferable*: Concrete implementation of `refreshInfo()` or disk verification logic.
