# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SpectreGunshipUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the update module for the Spectre Gunship special power, integrating with the SAGE engine's special power system. It handles the gunship's orbital mechanics, weapon firing logic, and state management, bridging the game logic layer with rendering and audio subsystems.

## Cross-References
### Incoming
- **SpecialPowerModule**: Likely instantiates this module for the Spectre Gunship power.
- **GameLogic/Module/SpecialPowerUpdateModule.h**: Base class interface implementation.
- **W3D Rendering System**: For decal and particle system management (implied by `RadiusDecal` and `ParticleSystem` usage).

### Outgoing
- **AudioEventRTS**: For sound effects (afterburner, howitzer fire).
- **ParticleSystem/FXList**: For visual effects during strafing.
- **GameLogic/Module/SpecialPowerModuleInterface**: For power state coordination.

## Design Patterns
- **State Pattern**: Uses `GunshipStatus` enum to manage discrete states (inserting, orbiting, etc.), with `update()` handling transitions.
- **Template Method**: Inherits from `SpecialPowerUpdateModule`, overriding key methods like `initiateIntentToDoSpecialPower`.
- **Dependency Injection**: Module data (`SpectreGunshipUpdateModuleData`) is injected via `ModuleData`, decoupling configuration from behavior.
