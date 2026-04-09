# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/StealthDetectorUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the stealth detection system, bridging the game logic layer with rendering, audio, and UI subsystems. It handles periodic scans for stealthed objects, manages detection state, and triggers visual/audio feedback.

## Cross-References
### Incoming
- **GameLogic/Object/Update/UpdateModule.cpp**: Likely instantiates `StealthDetectorUpdate` via factory pattern
- **GameClient/Drawable.cpp**: Called when attaching particle effects to drawables
- **GameLogic/Module/StealthUpdate.cpp**: Interacts via `markAsDetected()` calls

### Outgoing
- **PartitionManager**: Uses spatial queries to find nearby objects
- **Radar**: Updates radar with detection events
- **Audio**: Plays ping sounds for detection
- **InGameUI**: Displays detection messages
- **ParticleSystemManager**: Creates visual effects for detection

## Design Patterns
- **Observer Pattern**: Detects stealthed objects by monitoring their status bits
- **Strategy Pattern**: Uses `PartitionFilter` to encapsulate detection criteria
- **Component Pattern**: Extends `UpdateModule` base class for modular behavior

*Not inferable*: Exact factory instantiation mechanism or event-driven integration points.
