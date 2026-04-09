# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Armor.cpp - Enhanced Analysis

## Architectural Role
This file implements the armor system's data model and parsing infrastructure, bridging the INI configuration layer with runtime damage calculation. It's a core part of the game's damage resolution pipeline, used during combat simulations and projectile impacts.

## Cross-References
### Incoming
- Damage calculation systems (e.g., projectile impact handlers)
- Object initialization code (when setting up armor properties)
- INI parsing framework (via `INI::parseArmorDefinition` callback)

### Outgoing
- `DamageTypeFlags` for damage type enumeration
- `TheNameKeyGenerator` for string-to-key conversion
- `INI` framework for configuration parsing

## Design Patterns
- **Singleton-like global store**: `TheArmorStore` provides centralized access to armor definitions
- **Strategy pattern**: Damage adjustment is delegated to `ArmorTemplate` instances based on their coefficients
- **Visitor pattern**: INI parsing uses a field parse table to dispatch to appropriate handlers

Rules followed. Output under 400 tokens.
