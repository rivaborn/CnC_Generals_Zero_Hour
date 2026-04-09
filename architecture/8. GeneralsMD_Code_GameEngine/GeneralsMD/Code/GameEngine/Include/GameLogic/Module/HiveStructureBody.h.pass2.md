# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/HiveStructureBody.h - Enhanced Analysis

## Architectural Role
This file defines the damage propagation logic for hive structures, a key part of the Generals' AI and unit hierarchy system. It extends the base structure body to handle damage distribution to slave units, critical for the game's asymmetric faction mechanics.

## Cross-References
### Incoming
- Damage handling systems (e.g., `DamageInfo` processing)
- Structure body initialization (likely called during object creation)
- INI parsing infrastructure (for module data configuration)

### Outgoing
- Base `StructureBody` class (inheritance)
- `Damage` subsystem (for damage type flags)
- INI parsing utilities (for module data configuration)

## Design Patterns
- **Template Method**: `buildFieldParse` extends parsing behavior via inheritance
- **Strategy**: Damage propagation logic is encapsulated as a module, allowing runtime configuration
- **Composite**: Implicitly supports the hive/slave unit hierarchy pattern

*Not inferable*: Exact damage propagation mechanism (e.g., how slaves are identified/located).
