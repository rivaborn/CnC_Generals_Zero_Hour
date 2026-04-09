# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/BoneFXUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the bone-attached visual effects system, bridging the game logic layer with the rendering pipeline. It manages damage-state-dependent effects (FX, OCL, particles) tied to skeletal bones, coordinating with both client-side and server-side systems for consistent multiplayer behavior.

## Cross-References
### Incoming
- **BoneFXDamage.cpp**: Requires BoneFXDamage module (checked in `onObjectCreated`)
- **AIUpdate.cpp**: Likely called during game logic updates
- **FXList.cpp**: Uses FXList for effect management
- **ParticleSystem.cpp**: Manages particle system lifecycle

### Outgoing
- **INI.cpp**: Parses configuration data
- **Drawable.cpp**: Queries bone positions via `getPristineBonePositions`
- **Xfer.cpp**: Handles serialization for networking
- **RandomValue.cpp**: Generates random delays for effects

## Design Patterns
- **Module Pattern**: BoneFXUpdate inherits from UpdateModule, following the engine's modular architecture
- **Observer Pattern**: Effects trigger based on damage state changes (implicitly observed via `m_curBodyState`)
- **Strategy Pattern**: Different effect types (FX, OCL, particles) use similar timing/positioning logic but different execution paths

*Not inferable*: Exact timing coordination with animation system (bones may move independently of damage states).
