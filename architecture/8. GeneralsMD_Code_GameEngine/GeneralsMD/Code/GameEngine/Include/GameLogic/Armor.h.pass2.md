# GeneralsMD/Code/GameEngine/Include/GameLogic/Armor.h - Enhanced Analysis

## Architectural Role
This file defines the core damage modification system, bridging the damage calculation pipeline (Damage.h) with entity behavior. It provides a data-driven approach to armor types, enabling balance adjustments via INI files.

## Cross-References
### Incoming
- **GameLogic/Entity.h**: Uses Armor instances for damage resistance
- **GameLogic/Weapon.h**: Applies armor adjustments during damage calculation
- **GameLogic/INIParser.cpp**: Calls parseArmorDefinition during initialization

### Outgoing
- **GameLogic/Damage.h**: Uses DamageType enum for coefficient indexing
- **Common/INI.h**: Relies on INI parsing infrastructure
- **Common/NameKeyGenerator.h**: Uses NameKeyType for template lookup

## Design Patterns
- **Template Method**: parseArmorCoefficients uses INI parsing callback pattern
- **Flyweight**: ArmorStore centralizes armor template instances
- **Strategy**: ArmorTemplate encapsulates damage adjustment logic

*Not inferable*: Exact INI parsing implementation details.
