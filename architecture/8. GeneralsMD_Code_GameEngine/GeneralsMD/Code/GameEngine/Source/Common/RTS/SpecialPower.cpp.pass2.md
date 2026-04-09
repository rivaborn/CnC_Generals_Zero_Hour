# GeneralsMD/Code/GameEngine/Source/Common/RTS/SpecialPower.cpp - Enhanced Analysis

## Architectural Role
This file serves as the central registry for special power definitions in the game, acting as a bridge between the INI-based data definition system and the runtime object system. It manages the lifecycle of special power templates, including parsing, storage, and validation, while coordinating with the science system for power availability checks.

## Cross-References
### Incoming
- **INI Parser System**: Calls `parseSpecialPowerDefinition` to load power definitions from INI files
- **Special Power Modules**: Query `canUseSpecialPower` to validate power usage
- **World Builder Tools**: Use `getSpecialPowerTemplateByIndex` and `getNumSpecialPowers` for UI display

### Outgoing
- **Science System**: Calls `Player::hasScience` to check power prerequisites
- **Object System**: Calls `Object::getSpecialPowerModule` to verify power capability
- **Override System**: Manages template overrides through `Overridable` interface

## Design Patterns
- **Singleton Pattern**: Global `TheSpecialPowerStore` provides centralized access to power definitions
- **Template Method Pattern**: `parseSpecialPowerDefinition` uses a structured parsing approach with field-specific handlers
- **Flyweight Pattern**: Special power templates are reused across multiple objects, with runtime state managed separately

*Not inferable*: Exact override mechanism implementation details.
