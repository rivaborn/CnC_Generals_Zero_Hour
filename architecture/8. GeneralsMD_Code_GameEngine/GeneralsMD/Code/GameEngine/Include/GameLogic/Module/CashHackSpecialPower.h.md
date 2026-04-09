# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CashHackSpecialPower.h

## Purpose
Defines the Cash Hack special power module for stealing money from enemies.

## Responsibilities
- Declares `CashHackSpecialPowerModuleData` for configuration
- Declares `CashHackSpecialPower` class implementing the power logic
- Defines upgrade system for science-based money theft amounts
- Provides virtual methods for object/location targeting

## Key Types
- **CashHackSpecialPowerModuleData (Class)**: Holds module configuration including upgrade list and default theft amount
- **Upgrades (Struct)**: Stores science type and amount to steal per upgrade level
- **CashHackSpecialPower (Class)**: Implements the special power behavior
- **CashHackSpecialPowerMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **ScienceType (Enum)**: External enum for science types

## Key Functions
### CashHackSpecialPower::doSpecialPowerAtObject
- Purpose: Applies cash hack to a target object
- Calls: `findAmountToSteal()`

### CashHackSpecialPower::doSpecialPowerAtLocation
- Purpose: Applies cash hack at a map location
- Calls: `findAmountToSteal()`

### CashHackSpecialPower::findAmountToSteal
- Purpose: Calculates money amount to steal based on upgrades
- Calls: None visible

## Globals
- None

## Dependencies
- `SpecialPowerModule.h` (base class)
- `Object`, `SpecialPowerTemplate`, `FieldParse`, `ScienceType` (forward declarations)
- Memory pool macros and module macros (internal framework)
