# GeneralsMD/Code/GameEngine/Include/Common/SpecialPower.h

## Purpose
Defines special power templates and the store system for managing them in the game.

## Responsibilities
- Declares `SpecialPowerTemplate` class for defining special abilities
- Provides `SpecialPowerStore` for loading and managing special power definitions
- Defines utility functions for bitmask operations on special power types
- Exposes global store instance `TheSpecialPowerStore`

## Key Types
- **SpecialPowerTemplate (Class)**: Holds data for a special ability (name, reload time, sounds, etc.)
- **SpecialPowerStore (Class)**: Manages collection of special power templates
- **SpecialPowerType (Enum)**: Not shown, but used for power type identification
- **SpecialPowerMaskType (Enum)**: Not shown, but used for bitmask operations
- **AcademyClassificationType (Enum)**: Classifies powers for academy advice system

## Key Functions
### TEST_SPECIALPOWERMASK
- Purpose: Checks if a bit is set in a special power mask
- Calls: `m.test(t)`

### TEST_SPECIALPOWERMASK_ANY
- Purpose: Checks for any intersection between two masks
- Calls: `m.anyIntersectionWith(mask)`

### TEST_SPECIALPOWERMASK_MULTI
- Purpose: Tests if required bits are set and others are clear
- Calls: `m.testSetAndClear(mustBeSet, mustBeClear)`

## Globals
- **TheSpecialPowerStore (SpecialPowerStore*)**: Global instance of the special power store

## Dependencies
- `Common/AudioEventRTS.h`, `Common/GameMemory.h`, `Common/SubsystemInterface.h`
- `Common/BitFlags.h`, `Common/Overridable.h`, `Common/Override.h`
- `Common/SpecialPowerType.h`, `Common
