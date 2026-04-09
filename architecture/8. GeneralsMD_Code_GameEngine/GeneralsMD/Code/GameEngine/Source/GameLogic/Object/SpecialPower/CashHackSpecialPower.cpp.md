# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SpecialPower/CashHackSpecialPower.cpp

## Purpose
Implements the Cash Hack special power, which steals money from an enemy player.

## Responsibilities
- Parses configuration data for Cash Hack upgrades
- Handles money theft logic between players
- Displays floating text for stolen/lost money
- Manages special power state and serialization

## Key Types
- **CashHackSpecialPowerModuleData (Class)**: Holds configuration for Cash Hack, including upgrade amounts and default steal value
- **CashHackSpecialPower (Class)**: Implements the Cash Hack special power functionality
- **Upgrades (Struct)**: Stores science requirement and amount to steal for an upgrade

## Key Functions
### parseCashHackUpgradePair
- Purpose: Parses upgrade configuration from INI file
- Calls: `INI::parseScience`, `INI::parseInt`

### findAmountToSteal
- Purpose: Determines how much money to steal based on player's upgrades
- Calls: None

### doSpecialPowerAtObject
- Purpose: Executes the money theft when targeting an enemy object
- Calls: `SpecialPowerModule::doSpecialPowerAtObject`, `Money::withdraw`, `Money::deposit`, `TheInGameUI->addFloatingText`

## Globals
- **TheGameText (External)**: Game text resource
- **TheInGameUI (External)**: In-game UI manager

## Dependencies
- `PreRTS.h`, `Common/Player.h`, `Common/Team.h`, `Common/Xfer.h`
- `GameClient/GameText.h`, `GameLogic/Object.h`, `GameLogic/PartitionManager.h`
- `GameLogic/Module/CashHackSpecialPower.h`, `GameClient/InGameUI.h`
- `SpecialPowerModule`, `Money`, `INI`, `MultiIniFieldParse`
