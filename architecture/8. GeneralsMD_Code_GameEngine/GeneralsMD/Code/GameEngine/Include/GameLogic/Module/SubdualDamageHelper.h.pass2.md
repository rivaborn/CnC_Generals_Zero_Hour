# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SubdualDamageHelper.h - Enhanced Analysis

## Architectural Role
This file defines a module that handles subdual damage state management for game objects, bridging the gap between body modules (which can't have updates) and the game's damage/healing systems. It's part of the modular game logic architecture, specifically the ObjectHelper subsystem.

## Cross-References
### Incoming
- Damage calculation systems (likely in `DamageSystem` or similar)
- Object creation/initialization code (where modules are attached to Things)
- Healing effects or abilities that trigger subdual recovery

### Outgoing
- `ObjectHelper` base class methods
- `Thing` object methods for state modification
- Timer/sleep mechanisms for periodic healing updates

## Design Patterns
- **Module Pattern**: Implements a self-contained module that can be attached to game objects
- **Observer Pattern**: `notifySubdualDamage` suggests it reacts to damage events
- **State Management**: Tracks healing state via `m_healingStepCountdown` for gradual recovery

*Not inferable: Specific healing algorithm or interaction with other damage systems*
