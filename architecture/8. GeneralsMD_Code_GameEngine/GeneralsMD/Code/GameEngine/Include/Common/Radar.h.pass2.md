# GeneralsMD/Code/GameEngine/Include/Common/Radar.h - Enhanced Analysis

## Architectural Role
This file defines the core radar subsystem, bridging game logic (object visibility, events) with rendering (coordinate transformations, shroud management). It acts as a central hub for spatial awareness, coordinating between the game world, UI, and player feedback systems.

## Cross-References
### Incoming
- **Game Logic**: Unit/structure systems call `addObject`/`removeObject` for radar representation
- **UI**: HUD/interface code uses `draw` and coordinate conversion methods (`worldToRadar`, `radarToWorld`)
- **Event System**: Game events trigger `createEvent` for visual/auditory feedback

### Outgoing
- **Rendering**: Calls into `GameWindow` for display management
- **Terrain**: Uses `TerrainLogic` for elevation/water level sampling
- **Audio**: Implicitly triggers sound playback via `RadarEvent` (soundPlayed flag)

## Design Patterns
- **Singleton**: `TheRadar` provides global access to radar state
- **Observer**: Radar objects notify the subsystem of state changes (via `examineObject`)
- **Strategy**: Virtual `draw` method enables different radar rendering implementations (e.g., minimap vs. tactical view)

*Not inferable*: Exact event handling pipeline or memory management for `RadarObject` lists.
