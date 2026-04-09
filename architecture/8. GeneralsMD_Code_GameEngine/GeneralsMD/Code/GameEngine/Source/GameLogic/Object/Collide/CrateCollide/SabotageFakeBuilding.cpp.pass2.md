# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/SabotageFakeBuilding.cpp - Enhanced Analysis

## Architectural Role
This file implements the sabotage behavior for a specialized "saboteur" crate that targets fake buildings. It extends the base `CrateCollide` class to add validation logic for enemy fake structures and executes sabotage effects (damage, visual/audio feedback, and radar events). It integrates with the AI system to ensure sabotage only occurs when the target is the AI's goal object.

## Cross-References
### Incoming
- **AIUpdateInterface**: Called to verify the target is the AI's goal object (prevents unintended sabotage).
- **Radar**: Used to trigger infiltration events via `TheRadar->tryInfiltrationEvent`.
- **EVA System**: Plays sabotage announcements via `TheEva->setShouldPlay`.

### Outgoing
- **CrateCollide**: Base class for collision logic (inherited methods like `isValidToExecute`).
- **Object**: Target validation (e.g., `isKindOf(KINDOF_FS_FAKE)`, `isLocallyControlled`).
- **Damage System**: Applies lethal damage via `attemptDamage` with `DAMAGE_UNRESISTABLE`.

## Design Patterns
- **Template Method**: Extends `CrateCollide` with specialized validation (`isValidToExecute`) and execution (`executeCrateBehavior`).
- **Strategy**: Encapsulates sabotage logic as a module, allowing dynamic behavior assignment to crates.
- **Observer**: Triggers radar/EVA events as side effects of sabotage (loose coupling via global managers).
