# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Body/ActiveBody.cpp - Enhanced Analysis

## Architectural Role
This file implements the core damage and health management system for game entities, bridging the gap between physical object representation (BodyModule) and game logic (damage application, healing, and state transitions). It serves as a critical middleware layer that coordinates between rendering (particle effects), gameplay mechanics (armor, veterancy), and networking (state synchronization).

## Cross-References
### Incoming
- **DamageModule.cpp**: Calls `attemptDamage` to apply damage to active bodies
- **Weapon.cpp**: Invokes damage logic through `attemptDamage` when weapons hit targets
- **AIUpdate.cpp**: Likely queries health/damage states for tactical decisions
- **ControlBar.cpp**: May poll health status for UI display

### Outgoing
- **Armor.cpp**: Uses `validateArmorAndDamageFX` for armor calculations
- **DamageFX.cpp**: Triggers visual/audio damage effects via `doDamageFX`
- **ParticleSys.cpp**: Manages damage-state particle systems
- **GameLogic.cpp**: Accesses global game state for damage thresholds
- **Xfer.cpp**: Handles serialization for networking

## Design Patterns
- **State Pattern**: Damage states (pristine/damaged/rubble) are managed through explicit state transitions
- **Observer Pattern**: Particle systems are dynamically created/destroyed based on damage state changes
- **Composite Pattern**: Health management is decomposed into sub-modules (armor, subdual, veterancy) with clear ownership hierarchy

Rules followed. Output under 400 tokens.
