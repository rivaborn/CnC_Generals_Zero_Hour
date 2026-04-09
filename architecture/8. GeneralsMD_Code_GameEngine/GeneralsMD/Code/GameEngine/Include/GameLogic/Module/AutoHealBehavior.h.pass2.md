# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/AutoHealBehavior.h - Enhanced Analysis

## Architectural Role
This file defines the `AutoHealBehavior` module, which is part of the game's behavior system. It handles automatic healing logic for objects, integrating with the damage system, upgrade system, and particle effects. The module is designed to be attached to game objects and provides configurable healing behavior, including radius-based healing and particle effects.

## Cross-References
### Incoming
- **Damage System**: Calls `onDamage` when objects take damage.
- **Update System**: Invokes `update` for periodic healing checks.
- **Upgrade System**: Uses `UpgradeMux` for upgrade management.
- **Particle System**: References `ParticleSystem` and `ParticleSystemTemplate` for visual effects.

### Outgoing
- **Damage Module**: Implements `DamageModuleInterface` for damage/healing interactions.
- **Update Module**: Inherits from `UpdateModule` for periodic updates.
- **Upgrade Module**: Inherits from `UpgradeMux` for upgrade handling.
- **Particle System**: Creates and manages particle effects for healing visuals.

## Design Patterns
- **Module Pattern**: Encapsulates healing behavior as a reusable module.
- **Strategy Pattern**: Configurable healing logic via `AutoHealBehaviorModuleData`.
- **Observer Pattern**: Reacts to damage events via `onDamage`.
