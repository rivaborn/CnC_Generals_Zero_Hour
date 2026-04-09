# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/BodyModule.h - Enhanced Analysis

## Architectural Role
This file defines the core health/damage system for game objects, serving as the central interface between damage calculation, armor evaluation, and visual state management. It bridges the gap between combat mechanics and object rendering by exposing damage states and particle system updates.

## Cross-References
### Incoming
- Damage calculation systems (Damage.h)
- Armor evaluation (ArmorSet.h)
- AI targeting logic (uses estimateDamage)
- Veterancy systems (onVeterancyLevelChanged)
- Particle system updates (updateBodyParticleSystems)

### Outgoing
- BehaviorModule hierarchy (inherits from BehaviorModule)
- Damage effects system (DamageFX)
- Visual condition evaluation (evaluateVisualCondition)
- Module data parsing (MultiIniFieldParse)

## Design Patterns
- **Interface Segregation**: BodyModuleInterface provides a clean contract for health management
- **Template Method**: Damage state transitions use sequential enum for comparison macros
- **Strategy Pattern**: Damage calculation can be customized via armor/behavior modules

Rules followed. Output under 400 tokens.
