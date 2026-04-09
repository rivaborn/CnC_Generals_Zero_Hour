# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SpecialAbility.h - Enhanced Analysis

## Architectural Role
This file defines the core interface for unit special abilities in the game's module system. It extends the `SpecialPowerModule` hierarchy, enabling units to execute targeted or untargeted special attacks (e.g., nuke strikes, EMP pulses). The class serves as a bridge between unit behavior and the game's power system, with memory management handled via SAGE's module macros.

## Cross-References
### Incoming
- **Unit classes** (e.g., `Nuke`, `EMPTower`) likely instantiate `SpecialAbility` via the module system.
- **Command processing** (e.g., `PlayerCommand`) may call `doSpecialPower*` methods when handling ability triggers.
- **AI behavior trees** could reference this for scripted ability usage.

### Outgoing
- **`SpecialPowerModule`** (parent class) for base power logic.
- **`Thing`** (via constructor) for unit attachment.
- **`Object`** (targeting) for location-based abilities.
- **Memory pool macros** for object lifecycle management.

## Design Patterns
- **Template Method**: The virtual `doSpecialPower*` methods enforce a structure for ability execution while allowing subclasses to define behavior.
- **Module Pattern**: Uses SAGE's module system (`MAKE_STANDARD_MODULE_MACRO`) for dynamic ability attachment to units.
- **Dependency Injection**: Constructor injects `Thing` and `ModuleData`, decoupling ability logic from unit implementation.
