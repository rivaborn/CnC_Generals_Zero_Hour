# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DTruckDraw.h - Enhanced Analysis

## Architectural Role
This file defines the rendering logic for truck-like vehicles, extending the base `W3DModelDraw` class to handle specialized visual effects (particle systems, bone animations) and segmented body parts (cab/trailer). It bridges the W3D rendering pipeline with game-specific truck behavior.

## Cross-References
### Incoming
- **GameClient/Thing.h**: Likely instantiates `W3DTruckDraw` for vehicle objects.
- **GameClient/ParticleSys.h**: Manages particle effects triggered by truck movement.
- **Common/AudioEventRTS.h**: Handles sound events (powerslide, landing).

### Outgoing
- **W3DDevice/GameClient/Module/W3DModelDraw.h**: Inherits core model rendering functionality.
- **WW3D2/HAnim.h**: Uses bone animation for wheel/tire rotations.
- **WW3D2/RendObj.h**: Interacts with render objects for bone updates.

## Design Patterns
- **Template Method**: `doDrawModule` overrides base class rendering while reusing `W3DModelDraw` infrastructure.
- **Composite**: Manages multiple particle emitters (`m_dustEffect`, `m_dirtEffect`) as part of a larger effect system.
- **Observer**: Reacts to geometry changes via `reactToGeometryChange()` (though implementation is empty here).
