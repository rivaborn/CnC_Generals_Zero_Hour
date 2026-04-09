# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/InstantDeathBehavior.h - Enhanced Analysis

## Architectural Role
This file defines a module in the game's behavior system that handles instant death effects, extending the `DieModule` base class. It bridges the game logic layer with rendering (FX) and object creation systems, enabling modular death animations and effects.

## Cross-References
### Incoming
- Likely called by `Thing` objects during their destruction lifecycle (via `DieModule` interface).
- Referenced in module registration systems (e.g., `ModuleDatabase`).

### Outgoing
- Uses `FXList` for visual effects, `ObjectCreationList` for spawnable objects, and `WeaponTemplate` for weapon-based death effects.
- Relies on `DieModuleData` for configuration inheritance.

## Design Patterns
- **Template Method**: Extends `DieModule` with `onDie`, enforcing a death behavior hook.
- **Composite**: Aggregates vectors of effect templates (`FXListVec`, `OCLVec`, `WeaponTemplateVec`) for flexible death configurations.
- **Dependency Injection**: Module data is injected via `ModuleData`, decoupling behavior from object instantiation.
