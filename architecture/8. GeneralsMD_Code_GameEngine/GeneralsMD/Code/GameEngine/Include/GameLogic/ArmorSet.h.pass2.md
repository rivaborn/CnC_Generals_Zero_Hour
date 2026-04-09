# GeneralsMD/Code/GameEngine/Include/GameLogic/ArmorSet.h - Enhanced Analysis

## Architectural Role
This header defines the core data structures for the game's armor/damage system, bridging between unit attributes and damage calculations. It provides the type system and matching infrastructure used by the damage resolution pipeline.

## Cross-References
### Incoming
- Damage calculation modules (e.g., `DamageFX` application)
- Unit/weapon systems (for armor template application)
- INI parsing infrastructure (for mod support)

### Outgoing
- Relies on `SparseMatchFinder` for condition-based template selection
- Uses `BitFlags` for efficient condition tracking
- Forward-declares `ArmorTemplate` and `DamageFX` for decoupled implementation

## Design Patterns
- **Strategy Pattern**: `ArmorTemplateSet` encapsulates different armor behaviors as interchangeable templates
- **Composite Pattern**: `ArmorTemplateSetVector` groups multiple armor configurations
- **Type Object Pattern**: `ArmorSetType` enum with bitflag handling enables runtime behavior variation

Rules followed. Analysis limited to 400 tokens.
