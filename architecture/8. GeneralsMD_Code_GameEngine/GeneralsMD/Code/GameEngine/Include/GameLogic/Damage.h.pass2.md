# GeneralsMD/Code/GameEngine/Include/GameLogic/Damage.h - Enhanced Analysis

## Architectural Role
Central damage abstraction layer bridging weapon systems, object health logic, and visual effects. Serves as the contract between damage sources (weapons, hazards) and damage sinks (objects, modules).

## Cross-References
### Incoming
- Weapon systems (e.g., `BoneFXDamage`) consume damage type flags
- Object modules reference damage classification functions
- AI behavior trees use `IsSubdualDamage` for tactical decisions

### Outgoing
- Relies on `BitFlags` for damage type manipulation
- Uses `Snapshot` for network serialization
- References `ObjectStatusTypes` for status damage handling

## Design Patterns
- **Data Transfer Object**: `DamageInfo` encapsulates all damage parameters
- **Type Object**: Damage types as enumerated constants with behavior queries
- **Strategy Variant**: Damage effects vary by type (explosion vs. radiation)
