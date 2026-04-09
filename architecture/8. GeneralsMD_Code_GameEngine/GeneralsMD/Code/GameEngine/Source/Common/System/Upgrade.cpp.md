# GeneralsMD/Code/GameEngine/Source/Common/System/Upgrade.cpp

## Purpose
Manages the upgrade system for players, including upgrade templates, veterancy levels, and upgrade center functionality.

## Responsibilities
- Defines `Upgrade`, `UpgradeTemplate`, and `UpgradeCenter` classes
- Handles upgrade initialization, parsing, and management
- Manages veterancy upgrades and button image caching
- Provides upgrade lookup and affordability checks

## Key Types
- `Upgrade` (Class): Represents an instance of an upgrade with status and template reference
- `UpgradeTemplate` (Class): Defines upgrade properties (cost, build time, etc.) and parsing rules
- `UpgradeCenter` (Class): Central manager for upgrades, handles lists and initialization
- `UpgradeStatusType` (Enum): Not inferable (not shown in provided code)
- `UpgradeType` (Enum): Not inferable (not shown in provided code)

## Key Functions
### `getVetUpgradeName(VeterancyLevel v)`
- Purpose: Constructs upgrade name string for veterancy levels
- Calls: None

### `UpgradeTemplate::friend_makeVeterancyUpgrade(VeterancyLevel v)`
- Purpose: Configures an upgrade template for veterancy levels
- Calls: `getVetUpgradeName()`

### `UpgradeCenter::init()`
- Purpose: Initializes veterancy upgrades
- Calls: `newUpgrade()`, `friend_makeVeterancyUpgrade()`

### `UpgradeCenter::canAffordUpgrade(Player *player, const UpgradeTemplate *upgradeTemplate, Bool displayReason)`
- Purpose: Checks if player can afford an upgrade
- Calls: `player->getMoney()`, `upgradeTemplate->calcCostToBuild()`, `TheInGameUI->message()`

## Globals
- `TheUpgradeTypeNames` (const char*): Array of upgrade type names
- `TheUpgradeCenter` (UpgradeCenter*): Global upgrade center instance

## Dependencies
- `PreRTS.h`, `Upgrade.h`, `Player.h`, `Xfer.h`, `InGameUI.h`, `Image.h`
- `INI`, `AsciiString`, `NameKeyType`, `Money`, `Xfer`, `XferVersion` classes/types
- `TheNameKeyGenerator`, `TheMappedImageCollection` global instances
