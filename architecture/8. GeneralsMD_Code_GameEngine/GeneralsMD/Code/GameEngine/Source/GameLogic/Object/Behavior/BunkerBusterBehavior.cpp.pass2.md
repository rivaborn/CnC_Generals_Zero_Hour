# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/BunkerBusterBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements the Bunker Buster behavior module, which is part of the game's weapon behavior system. It handles the logic for missiles/bombs that target and damage garrisoned objects, integrating with the AI targeting system, containment system, and visual/audio effects.

## Cross-References
### Incoming
- **AIUpdateInterface**: Calls `getCurrentVictim()` to determine the target.
- **ContainModuleInterface**: Interacts with `isBustable()`, `harmAndForceExitAllContained()`, and `killAllContained()` to damage occupants.
- **FXList**: Uses `doFXObj()` for visual effects.
- **SeismicSimulationNode**: Used for seismic effects via `TheTerrainVisual`.

### Outgoing
- **GameLogic**: Uses `findObjectByID()` to locate the target.
- **UpgradeCenter**: Checks for required upgrades via `hasUpgradeComplete()`.
- **WeaponStore**: Creates and fires shockwave weapons via `createAndFireTempWeapon()`.

## Design Patterns
- **Strategy Pattern**: The behavior is encapsulated in a module that can be attached to different objects, allowing for flexible weapon behavior.
- **Observer Pattern**: The `onDie` callback acts as an observer for the object's death event, triggering the bunker-busting logic.
- **Template Method**: The `update` method follows a template for periodic updates, with specific logic for crash-through effects.
