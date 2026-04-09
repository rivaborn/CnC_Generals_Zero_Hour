# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SpecialPowerModule.h - Enhanced Analysis

## Architectural Role
This file defines the core interface and implementation for special power modules, acting as a bridge between game logic and the behavior system. It manages cooldown timers, readiness states, and power execution while integrating with the scripting engine and audio systems.

## Cross-References
### Incoming
- **Scripting Engine**: Calls `doSpecialPower`, `isReady`, `markSpecialPowerTriggered`, and `startPowerRecharge` for power execution and state checks.
- **Behavior System**: Uses `SpecialPowerModuleInterface` for module registration and behavior updates.
- **Audio System**: References `AudioEventRTS` for sound playback during power activation.

### Outgoing
- **BehaviorModule**: Inherits from `BehaviorModule` and uses its data structure.
- **Science System**: Checks `ScienceType` for power prerequisites.
- **Object System**: Interacts with `Object` for target-based powers.

## Design Patterns
- **Strategy Pattern**: `SpecialPowerModuleInterface` allows different power implementations to be swapped dynamically.
- **Template Method**: `doSpecialPower` provides a base implementation while allowing subclasses to extend behavior.
- **Observer Pattern**: `onSpecialPowerCreation` and `markSpecialPowerTriggered` notify other systems of power state changes.
