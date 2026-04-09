# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/HiveStructureBody.h

## Purpose
Defines a structure body module that propagates damage to slave units when available, or absorbs damage if no slaves exist.

## Responsibilities
- Propagate specified damage types to slave units
- Absorb damage if no slaves are present
- Parse configuration for damage propagation rules

## Key Types
- **HiveStructureBodyModuleData (Class)**: Holds damage propagation/swallowing flags.
- **HiveStructureBody (Class)**: Structure body that handles damage propagation logic.
- **HiveStructureBodyMagicEnum (Enum)**: Not inferable (likely internal macro enum).
- **HiveStructureBody_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum).

## Key Functions
### `HiveStructureBodyModuleData::buildFieldParse`
- Purpose: Registers INI field parsers for damage propagation flags.
- Calls: `StructureBodyModuleData::buildFieldParse`

### `HiveStructureBody::attemptDamage`
- Purpose: Handles damage logic (propagation or absorption).
- Calls: Not inferable (implementation in .cpp).

## Globals
- None

## Dependencies
- `StructureBody.h`, `Damage.h`
- `MultiIniFieldParse`, `INI` namespace (for parsing)
- `Thing`, `DamageInfo` (forward references)
