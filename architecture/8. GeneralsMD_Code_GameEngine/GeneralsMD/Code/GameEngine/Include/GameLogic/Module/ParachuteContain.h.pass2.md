# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ParachuteContain.h - Enhanced Analysis

## Architectural Role
This file implements the parachute containment system for transport units, extending the base `OpenContain` module. It handles the physics, visual positioning, and lifecycle of objects being parachuted, bridging the gap between transport logic and in-game object behavior.

## Cross-References
### Incoming
- **Transport units**: Call `ParachuteContain` methods when deploying parachutes
- **Game logic**: Uses `update()` for frame-by-frame parachute state management
- **Collision system**: Invokes `onCollide()` during parachute descent

### Outgoing
- **OpenContain base class**: Inherits containment logic
- **Audio system**: Plays `m_parachuteOpenSound` via `AudioEventRTS`
- **Object positioning**: Calls `positionContainedObjectsRelativeToContainer()` for visual updates

## Design Patterns
- **Template Method**: Overrides virtual methods like `update()` and `onCollide()` to customize parachute behavior while reusing base `OpenContain` logic.
- **State Management**: Tracks internal state (`m_opened`, `m_isLandingOverrideSet`) to control parachute deployment and landing phases.
- **Component-Based**: Follows SAGEâs modular design, where `ParachuteContain` is a pluggable module for transport units.
