# Generals/Code/GameEngine/Source/GameClient/RadiusDecal.cpp - Enhanced Analysis

## Architectural Role
This file implements the decal system for visual effects, bridging the game logic layer with the rendering subsystem (ProjectedShadowManager). It handles dynamic decals like explosion marks or area-of-effect indicators, with visibility rules tied to player ownership.

## Cross-References
### Incoming
- **GameLogic**: Calls `RadiusDecal::update` during frame processing
- **INI Parser**: Invokes `parseRadiusDecalTemplate` for modding/configuration
- **Effect/Weapon Systems**: Likely call `createRadiusDecal` on template instances

### Outgoing
- **ProjectedShadowManager**: Uses `addDecal` and shadow manipulation methods
- **PlayerList**: Checks local player visibility for ownership rules
- **GameLogic**: Queries frame count and UI state for timing/visibility

## Design Patterns
- **Template-Method**: `RadiusDecalTemplate` defines decal properties, while `RadiusDecal` handles runtime behavior
- **Dependency Injection**: Shadow configuration injected via `ShadowTypeInfo` struct
- **Observer (Implicit)**: Decals update themselves based on game time (frame count)

*Not inferable*: No clear Factory, Strategy, or Visitor patterns evident in this file.
