# GeneralsMD/Code/GameEngine/Source/Common/System/Radar.cpp - Enhanced Analysis

## Architectural Role
This file implements the radar subsystem, acting as a bridge between game logic and UI rendering. It manages object visibility, event notifications, and terrain visualization, with tight coupling to the W3D rendering system and game state management.

## Cross-References
### Incoming
- **GameClient/ControlBar.cpp**: Calls radar event triggers
- **GameClient/InGameUI.cpp**: Uses radar messages for UI notifications
- **GameLogic/GameLogic.cpp**: Registers objects with radar system
- **GameLogic/Object.cpp**: Sets/updates radar data for objects

### Outgoing
- **GameClient/Drawable.cpp**: Queries stealth/invisibility states
- **GameLogic/PartitionManager.cpp**: Spatial queries for object visibility
- **GameLogic/TerrainLogic.cpp**: Terrain sampling for radar visualization
- **Common/Xfer.cpp**: Serialization for save/load

## Design Patterns
- **Singleton**: `TheRadar` global instance ensures single radar system
- **Observer**: Radar objects notify UI of events (e.g., attacks)
- **Flyweight**: `RadarColorLookup` caches color data for performance

*Not inferable*: Exact event handling pattern (e.g., Command) not visible in truncated content.
