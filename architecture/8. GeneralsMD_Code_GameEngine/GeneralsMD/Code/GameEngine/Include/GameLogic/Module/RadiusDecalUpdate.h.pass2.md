# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/RadiusDecalUpdate.h - Enhanced Analysis

## Architectural Role
This file defines a module for managing dynamic visual effects (radius decals) tied to game objects, bridging the game logic layer with the rendering system. It extends the UpdateModule framework to handle decal lifecycle in sync with game object behavior.

## Cross-References
### Incoming
- **GameObject/Thing subclasses**: Likely attach this module to objects that need visual effects (e.g., explosions, weapon impacts)
- **Weapon/Attack systems**: Probably trigger decal creation during attacks
- **INI parsing system**: Uses MultiIniFieldParse for configuration

### Outgoing
- **RadiusDecal class**: Directly creates/destroys decal instances
- **UpdateModule base class**: Inherits update timing and module infrastructure
- **Memory pool system**: Uses custom allocation macros

## Design Patterns
- **Module Pattern**: Encapsulates decal behavior as a reusable component
- **Template Method**: buildFieldParse extends base class parsing
- **Dependency Injection**: Module data injected via constructor

*Not inferable*: Exact decal rendering integration with W3D system.
