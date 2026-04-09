# GeneralsMD/Code/GameEngine/Include/GameClient/GameClient.h - Enhanced Analysis

## Architectural Role
This file defines the core GameClient singleton, acting as the central hub for game object management, rendering coordination, and client-side message processing. It bridges the game logic layer with the rendering and UI subsystems, managing drawable lifecycle and spatial queries.

## Cross-References
### Incoming
- **Game Logic**: AI and game state systems query drawables via `findDrawableByID` and iterate over them using `iterateDrawablesInRegion`.
- **Rendering**: W3D subsystem uses `getRenderedObjectCount` and `incrementRenderedObjectCount` for performance metrics.
- **UI**: InGameUI accesses drawables for selection and group operations (`selectDrawablesInGroup`).

### Outgoing
- **Rendering**: Calls into `Display`, `TerrainVisual`, and `ParticleSystemManager` for visual updates.
- **Input**: Interfaces with `Keyboard` and `Mouse` for user interaction.
- **Audio**: Indirectly triggers sound events via drawable state changes.

## Design Patterns
- **Singleton**: Enforces single instance of `GameClient` for global access to game state.
- **Factory Method**: Uses pure virtual methods (`createGameDisplay`, `createTerrainVisual`) to delegate subsystem instantiation to derived classes.
- **Observer**: Manages `TextBearingDrawableList` for drawables that need post-render text updates (e.g., health bars).

*Not inferable*: Exact implementation of `DrawableTOC` usage (commented-out hash table suggests prior design iteration).
