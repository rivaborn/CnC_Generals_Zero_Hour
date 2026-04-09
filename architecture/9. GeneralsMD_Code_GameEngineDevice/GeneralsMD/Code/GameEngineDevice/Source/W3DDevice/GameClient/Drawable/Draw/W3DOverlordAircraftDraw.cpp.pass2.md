# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DOverlordAircraftDraw.cpp - Enhanced Analysis

## Architectural Role
This file implements a specialized draw module for aircraft units that carry portable structure upgrades (e.g., Helix, SpectreGunship). It extends the base `W3DModelDraw` to handle the unique rendering requirements of these units, particularly managing the drawing order and visibility of the contained rider (turret/upgrade).

## Cross-References
### Incoming
- Called by the rendering pipeline when drawing aircraft units with portable upgrades
- Likely invoked by the `W3DModelDraw` parent class during its draw phase

### Outgoing
- Calls into `W3DModelDraw` parent class methods (`doDrawModule`, `setHidden`, etc.)
- Uses `Drawable` methods for rider drawing and tinting
- Accesses `ContainModule` to retrieve the rider object

## Design Patterns
- **Decorator Pattern**: Extends `W3DModelDraw` to add specific behavior for overlord aircraft without modifying the base class
- **Dependency Injection**: Receives the `Thing` and `ModuleData` in constructor, allowing for flexible configuration
- **Friend Access**: Uses `friend_getRider()` to bypass encapsulation for the rider object, indicating tight coupling with `ContainModule`

Not inferable: No clear use of other patterns like Observer or Factory.
