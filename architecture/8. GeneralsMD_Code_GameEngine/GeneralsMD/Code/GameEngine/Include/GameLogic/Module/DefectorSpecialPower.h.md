# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DefectorSpecialPower.h

## Purpose
Defines the Defector special power module, allowing a player to click on an enemy unit to defect it.

## Responsibilities
- Declares `DefectorSpecialPowerModuleData` for configuration.
- Declares `DefectorSpecialPower` class implementing the defect logic.
- Provides memory management macros for the module.
- Exposes methods to trigger the defect effect on objects or locations.

## Key Types
- **DefectorSpecialPowerModuleData (Class)**: Holds module-specific data (e.g., reveal radius).
- **DefectorSpecialPower (Class)**: Implements the defect special power logic.
- **DefectorSpecialPowerMagicEnum (Enum)**: Not inferable (likely internal macro enum).
- **DefectorSpecialPower_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum).

## Key Functions
### `DefectorSpecialPower::doSpecialPowerAtObject`
- Purpose: Applies the defect effect to a target object.
- Calls: Not inferable (implementation in .cpp).

### `DefectorSpecialPower::doSpecialPowerAtLocation`
- Purpose: Applies the defect effect at a world location.
- Calls: Not inferable (implementation in .cpp).

## Globals
- None.

## Dependencies
- `SpecialPowerModule.h` (base class).
- Forward declarations: `Object`, `SpecialPowerTemplate`, `FieldParse`, `ScienceType`.
