# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/MobNexusContain.cpp - Enhanced Analysis

## Architectural Role
This file implements the containment system for transport vehicles (MobNexus units) in the game, extending the base `OpenContain` class. It handles loading/unloading mechanics, health regeneration for contained units, and special exit behaviors like scattering or velocity inheritance.

## Cross-References
### Incoming
- Called by AI systems when units need to be loaded/unloaded
- Used by game logic when checking containment validity
- Referenced during unit update cycles for health regeneration

### Outgoing
- Extends `OpenContain` functionality
- Interacts with `AIUpdate`, `StealthUpdate`, and `BodyModule` interfaces
- Uses `Locomotor` and `AIPathfind` for movement validation

## Design Patterns
- **Template Method Pattern**: Extends base class methods while preserving core containment logic
- **Strategy Pattern**: Configurable exit behaviors (scatter, orientation, velocity) via module data
- **Observer Pattern**: Health regeneration updates are applied during the game loop

Rules followed. Output under 400 tokens.
