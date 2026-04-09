# GeneralsMD/Code/GameEngine/Include/Common/Upgrade.h

## Purpose
Defines the upgrade system for players, including upgrade templates, instances, and management.

## Responsibilities
- Declares `Upgrade`, `UpgradeTemplate`, and `UpgradeCenter` classes
- Defines upgrade status and type enums
- Provides bitmask utilities for upgrade masks
- Manages upgrade parsing and lookup

## Key Types
- `Upgrade` (Class): Represents an upgrade instance with status and template reference
- `UpgradeTemplate` (Class): Defines upgrade properties (cost, time, sounds, etc.)
- `UpgradeCenter` (Class): Manages all upgrade templates and provides lookup
- `UpgradeStatusType` (Enum): Tracks upgrade production/completion state
- `UpgradeType` (Enum): Distinguishes player vs. object upgrades
- `UpgradeMaskType` (Class): Bitmask for upgrade identification

## Key Functions
### `TEST_UPGRADE_MASK`
- Purpose: Checks if an upgrade bit is set in a mask
- Calls: `m.test()`

### `TEST_UPGRADE_MASK_ANY`
- Purpose: Checks for intersection between two upgrade masks
- Calls: `m.anyIntersectionWith()`

### `TEST_UPGRADE_MASK_MULTI`
- Purpose: Tests if required bits are set and others are clear
- Calls: `m.testSetAndClear()`

### `canAffordUpgrade`
- Purpose: Determines if a player can afford an upgrade
- Calls: Not inferable (implementation in .cpp)

## Globals
- `TheUpgradeCenter` (UpgradeCenter*): Singleton for upgrade management
- `TheUpgradeTypeNames` (const char*): Array of upgrade type names

## Dependencies
- `Player`, `UpgradeTemplate`, `NameKeyType`, `Image`, `AcademyClassificationType` (forward references)
- `AudioEventRTS`, `INI`, `Snapshot`, `MemoryPoolObject`, `SubsystemInterface` (includes)
- `VeterancyLevel` (used but not defined here)
