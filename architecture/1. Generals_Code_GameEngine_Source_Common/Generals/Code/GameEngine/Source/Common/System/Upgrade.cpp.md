# Generals/Code/GameEngine/Source/Common/System/Upgrade.cpp

## Purpose
This file implements the upgrade system for players in Command & Conquer Generals, handling upgrade templates, creation, and management.

## Responsibilities
- Manages upgrade templates and their properties.
- Handles the creation and deletion of upgrades.
- Checks if a player can afford an upgrade.
- Parses upgrade definitions from INI files.

## Key Types
- **Upgrade (Class)**: Represents an individual upgrade instance.
- **UpgradeTemplate (Class)**: Template for creating upgrades, including build time, cost, and display properties.
- **VeterancyLevel (Enum)**: Enumerates different veterancy levels for upgrades.

## Key Functions
### getVetUpgradeName
- Purpose: Generates the name string for a veteran upgrade based on its level.
- Calls: None

### UpgradeCenter::init
- Purpose: Initializes the upgrade center with default veteran upgrades.
- Calls: newUpgrade, friend_makeVeterancyUpgrade

### UpgradeCenter::canAffordUpgrade
- Purpose: Checks if a player can afford to build an upgrade.
- Calls: getMoney, countMoney, message

## Globals
- **TheUpgradeCenter (UpgradeCenter \*)**: Global instance of the upgrade center.

## Dependencies
- Key includes:
  - "Common/Upgrade.h"
  - "Common/Player.h"
  - "Common/Xfer.h"
  - "GameClient/InGameUI.h"
  - "GameClient/Image.h"
