# Generals/Code/GameEngine/Source/GameLogic/Object/Upgrade/RadarUpgrade.cpp

## Purpose
This file implements the logic for radar upgrades in Command & Conquer Generals, handling the addition and removal of radar capabilities for game objects.

## Responsibilities
- Manage radar upgrade functionality.
- Handle object deletion and capture events related to radar upgrades.
- Implement the actual upgrade process for radar facilities.

## Key Types
- `RadarUpgradeModuleData (struct)`: Stores data specific to radar upgrades, such as disable proof status.
- `RadarUpgrade (class)`: Manages the lifecycle of radar upgrades for game objects.

## Key Functions
### buildFieldParse
- Purpose: Initializes field parsing for radar upgrade module data.
- Calls: `UpgradeModuleData::buildFieldParse`

### RadarUpgrade
- Purpose: Constructor for the `RadarUpgrade` class.
- Calls: None

### ~RadarUpgrade
- Purpose: Destructor for the `RadarUpgrade` class.
- Calls: None

### onDelete
- Purpose: Handles cleanup when a radar upgrade is deleted.
- Calls: `Player::removeRadar`, `setUpgradeExecuted`

### onCapture
- Purpose: Manages radar upgrades when an object changes ownership.
- Calls: `Player::removeRadar`, `Player::addRadar`, `setUpgradeExecuted`

### upgradeImplementation
- Purpose: Implements the actual radar upgrade process.
- Calls: `Player::addRadar`, `findUpdateModule`, `extendRadar`

### crc
- Purpose: Calculates the CRC for the radar upgrade module.
- Calls: `UpgradeModule::crc`

### xfer
- Purpose: Handles data transfer (serialization) for radar upgrades.
- Calls: `xferVersion`, `UpgradeModule::xfer`

### loadPostProcess
- Purpose: Performs post-processing after loading radar upgrades.
- Calls: `UpgradeModule::loadPostProcess`

## Globals
-
