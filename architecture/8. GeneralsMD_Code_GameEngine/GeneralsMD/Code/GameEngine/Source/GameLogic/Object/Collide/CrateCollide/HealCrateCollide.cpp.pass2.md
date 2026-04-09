# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/HealCrateCollide.cpp - Enhanced Analysis

## Architectural Role
This file implements the healing crate behavior, a specific crate type in the game's power-up system. It extends the base `CrateCollide` class to provide player-specific healing functionality, integrating with the game's collision, audio, and player management systems.

## Cross-References
### Incoming
- **GameLogic/Object/Collide/CrateCollide.h**: Base class definition
- **GameLogic/Module/HealCrateCollide.h**: Module data interface
- **Common/Player.h**: Player object management
- **Common/AudioEventRTS.h**: Audio event system

### Outgoing
- **Common/Player.h**: Calls `healAllObjects()`
- **Common/AudioEventRTS.h**: Uses `TheAudio` global for sound playback
- **Common/Xfer.h**: Serialization support
- **GameLogic/Object.h**: Base object interface

## Design Patterns
- **Template Method**: Extends `CrateCollide` with specific behavior in `executeCrateBehavior`
- **Dependency Injection**: Receives `Thing` and `ModuleData` in constructor
- **Global Access**: Uses `TheAudio` singleton for audio playback (common in SAGE engine)

*Not inferable*: No clear use of Observer, Factory, or Strategy patterns in this file.
