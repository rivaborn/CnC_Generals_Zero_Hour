# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SpecialPower/CashBountyPower.cpp

## Purpose
Implements the cash bounty special power system for the game, allowing players to earn cash from destroyed units.

## Responsibilities
- Manages cash bounty values for units
- Updates player cash bounty when units are created or destroyed
- Handles science-based bounty upgrades (commented out)
- Serializes/deserializes bounty data

## Key Types
- **CashBountyPowerModuleData (Class)**: Stores bounty configuration data
- **CashBountyPower (Class)**: Implements the cash bounty special power logic

## Key Functions
### `CashBountyPower::onObjectCreated`
- Purpose: Updates player cash bounty when a unit is created
- Calls: `getObject`, `getControllingPlayer`, `hasScience`, `findBounty`, `setCashBounty`

### `CashBountyPower::findBounty`
- Purpose: Calculates the bounty value for a unit
- Calls: `getCashBountyPowerModuleData`, `getObject`, `getControllingPlayer`, `hasScience`

### `CashBountyPower::onSpecialPowerCreation`
- Purpose: Initializes cash bounty when special power is created
- Calls: `SpecialPowerModule::onSpecialPowerCreation`, `getObject`, `getControllingPlayer`, `findBounty`, `setCashBounty`

### `CashBountyPower::crc`
- Purpose: Generates CRC checksum for network synchronization
- Calls: `SpecialPowerModule::crc`

### `CashBountyPower::xfer`
- Purpose: Serializes/deserializes cash bounty data
- Calls: `SpecialPowerModule::xfer`, `xferVersion`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Player.h`, `Common/Xfer.h`, `GameLogic/Module/CashBountyPower.h`, `GameLogic/Object.h`
- `SpecialPowerModule`, `MultiIniFieldParse`, `INI`, `Thing`, `Real`, `Xfer`, `XferVersion`
