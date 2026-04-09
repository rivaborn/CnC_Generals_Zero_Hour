# GeneralsMD/Code/GameEngine/Include/Common/ScoreKeeper.h - Enhanced Analysis

## Architectural Role
This file defines the `ScoreKeeper` class, which is part of the game's statistics and scoring subsystem. It tracks player performance metrics (e.g., money, units, buildings) and calculates scores, critical for both single-player and multiplayer (especially online) gameplay. The class inherits from `Snapshot`, indicating its role in network synchronization.

## Cross-References
### Incoming
- **Game Logic**: Likely called by `Player` or `Game` classes to update scores during gameplay.
- **Object Management**: Called when objects are built/destroyed (e.g., `Building`, `Unit` classes).
- **Networking**: Used by `Xfer` (serialization) for syncing scores in multiplayer.

### Outgoing
- **Serialization**: Calls `Snapshot` methods (`crc`, `xfer`, `loadPostProcess`) for network sync.
- **Template System**: Uses `ThingTemplate` to categorize objects for counting.

## Design Patterns
- **Observer**: Implicitly observes game events (e.g., object creation/destruction) to update stats.
- **Composite**: Uses `ObjectCountMap` to aggregate counts by `ThingTemplate`, allowing hierarchical tracking.
- **Memento**: Via `Snapshot`, saves/restores state for network replay or rollback.
