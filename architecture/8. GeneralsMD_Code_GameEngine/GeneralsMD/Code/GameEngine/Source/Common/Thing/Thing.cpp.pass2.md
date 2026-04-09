# GeneralsMD/Code/GameEngine/Source/Common/Thing/Thing.cpp - Enhanced Analysis

## Architectural Role
This file implements the core `Thing` class, serving as the foundational abstraction for all spatial entities in the SAGE engine. It bridges the gap between game logic (Objects) and rendering (Drawables) by centralizing transformation, caching, and terrain interaction logic.

## Cross-References
### Incoming
- **GameLogic**: Object and Drawable subclasses inherit from `Thing`
- **Rendering**: W3D drawables use `Thing` for spatial queries
- **AI**: Pathfinding systems query `Thing` for position/orientation

### Outgoing
- **TerrainLogic**: For height queries and slope alignment
- **GlobalData**: For physics constants (e.g., gravity)
- **Math Library**: Matrix/Vector operations

## Design Patterns
- **Template Method**: `reactToTransformChange()` hook for subclasses
- **Lazy Evaluation**: Caches derived values (height, direction vectors)
- **Composite**: `Thing` aggregates `ThingTemplate` for type information

*Not inferable*: Exact inheritance hierarchy or factory usage patterns.
