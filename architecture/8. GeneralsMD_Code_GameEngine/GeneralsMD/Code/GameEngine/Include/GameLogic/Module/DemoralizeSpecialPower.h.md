# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DemoralizeSpecialPower.h

## Purpose
Defines the demoralize special power module for the game, allowing units to demoralize enemies within a range.

## Responsibilities
- Declares `DemoralizeSpecialPowerModuleData` to hold configuration for demoralize effects.
- Declares `DemoralizeSpecialPower` class implementing the special power logic.
- Defines range and duration calculations based on captured prisoners.
- Specifies FX (effects) to play during demoralization.

## Key Types
- `DemoralizeSpecialPowerModuleData` (Class): Holds demoralize power parameters (range, duration, FX).
- `DemoralizeSpecialPower` (Class): Implements the demoralize special power behavior.
- `FXList` (Forward reference): List of visual/audio effects to play.

## Key Functions
### `DemoralizeSpecialPowerModuleData::buildFieldParse`
- Purpose: Registers INI field parsing for demoralize module data.
- Calls: `MultiIniFieldParse::addField` (inferred).

### `DemoralizeSpecialPower::doSpecialPowerAtObject`
- Purpose: Applies demoralize effect to a target object.
- Calls: Not inferable (implementation in .cpp).

### `DemoralizeSpecialPower::doSpecialPowerAtLocation`
- Purpose: Applies demoralize effect at a world location.
- Calls: Not inferable (implementation in .cpp).

## Globals
- None.

## Dependencies
- `SpecialPowerModule.h` (base class)
- `MultiIniFieldParse` (for INI parsing)
- `Thing`, `Object`, `Coord3D` (game entity types)
- `FXList` (effects system)
- `MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE
