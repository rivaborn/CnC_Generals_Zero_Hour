# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/OCLSpecialPower.h - Enhanced Analysis

## Architectural Role
This file defines the OCLSpecialPower module, which bridges the SpecialPowerModule system with the ObjectCreationList (OCL) system. It enables special abilities that spawn objects (e.g., units, buildings) via OCLs, with configurable placement logic and science-based upgrades.

## Cross-References
### Incoming
- **SpecialPowerModule.h**: Inherits from `SpecialPowerModule` and uses `SpecialPowerModuleData`.
- **GameLogic/Module/SpecialPowerModule.h**: Parent class for special power behavior.
- **Common/Science.h**: Uses `ScienceType` for upgrade validation.
- **ObjectCreationList** (forward reference): Core dependency for object spawning logic.

### Outgoing
- **ObjectCreationList**: Used to resolve the actual objects to spawn.
- **ThingTemplate**: Referenced for placement calculations (e.g., construction sites).
- **MultiIniFieldParse**: Used in `buildFieldParse` for configuration parsing.

## Design Patterns
- **Strategy Pattern**: The `OCLCreateLocType` enum and placement logic allow dynamic selection of object creation strategies (e.g., edge placement, location-based).
- **Template Method**: `doSpecialPower` variants (`AtObject`, `AtLocation`) follow a template method structure, deferring placement logic to helper methods.
- **Composite**: `OCLSpecialPowerModuleData::Upgrades` aggregates science requirements and OCLs, enabling modular upgrades.
