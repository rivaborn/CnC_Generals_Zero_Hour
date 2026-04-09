# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CashBountyPower.h

## Purpose
Defines the CashBountyPower module for the game's special power system, handling cash bounty rewards.

## Responsibilities
- Manages cash bounty rewards for special powers
- Handles object creation and special power activation
- Calculates bounty amounts based on module data
- Integrates with the game's module and special power systems

## Key Types
- **CashBountyPowerModuleData (Class)**: Contains module configuration including default bounty value
- **CashBountyPower (Class)**: Implements the cash bounty power module logic
- **CashBountyPowerMagicEnum (Enum)**: Not inferable (empty enum)
- **CashBountyPower_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty enum)

## Key Functions
### CashBountyPowerModuleData::buildFieldParse
- Purpose: Parses configuration data for the module
- Calls: Not inferable

### CashBountyPower::onObjectCreated
- Purpose: Handles object creation events
- Calls: Not inferable

### CashBountyPower::onSpecialPowerCreation
- Purpose: Called when the special power is created
- Calls: Not inferable

### CashBountyPower::findBounty
- Purpose: Calculates the bounty amount
- Calls: Not inferable

## Globals
- None

## Dependencies
- SpecialPowerModule.h
- Common/Science.h
- Thing (forward reference)
- Player (forward reference)
- MultiIniFieldParse (used in buildFieldParse)
- ScienceType (from Common/Science.h)
