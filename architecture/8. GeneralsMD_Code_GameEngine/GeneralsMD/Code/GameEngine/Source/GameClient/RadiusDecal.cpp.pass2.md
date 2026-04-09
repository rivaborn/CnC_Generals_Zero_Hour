# GeneralsMD/Code/GameEngine/Source/GameClient/RadiusDecal.cpp - Enhanced Analysis

## Architectural Role
This file implements the decal system for visual effects, bridging the game logic layer with the rendering system. It handles the creation, updating, and serialization of circular decals projected onto the world, with visibility rules tied to player ownership.

## Cross-References
### Incoming
- **Game Logic**: Likely calls `RadiusDecal::update()` during frame processing to animate decals.
- **Effect System**: Probably invokes `RadiusDecalTemplate::createRadiusDecal()` when spawning explosion marks or area indicators.
- **INI Parser**: Uses `RadiusDecalTemplate::parseRadiusDecalTemplate()` to load decal definitions from configuration files.

### Outgoing
- **Shadow System**: Relies on `TheProjectedShadowManager` for decal rendering (`addDecal`, `setOpacity`, etc.).
- **Player System**: Checks `ThePlayerList` for local player visibility rules.
- **Game Logic**: Queries `TheGameLogic` for frame timing and UI state.

## Design Patterns
- **Template-Method**: `RadiusDecalTemplate` defines decal properties, while `RadiusDecal` handles runtime behavior (e.g., opacity animation).
- **Dependency Injection**: Decal templates are parsed from INI files and injected into runtime instances.
- **Resource Management**: Uses reference counting (`release()`) for decal cleanup, though not fully implemented in the copy constructor/assignment operator.
