# GeneralsMD/Code/GameEngine/Source/Common/RTS/SpecialPower.cpp

## Purpose
Manages special power templates and the system that holds them in the game engine.

## Responsibilities
- Defines and parses special power templates from INI files
- Manages the global store of special power templates
- Provides lookup functions for special powers by name, ID, or index
- Handles override management for special power definitions
- Validates if an object/player can use a specific special power

## Key Types
- **SpecialPowerStore (Class)**: Manages the collection of special power templates and provides access methods
- **SpecialPowerTemplate (Class)**: Represents a special power definition with properties like reload time, required science, and type
- **SpecialPowerMaskType (Enum)**: Defines the types of special powers (e.g., daisy cutter, carpet bomb, etc.)

## Key Functions
### `parseSpecialPowerDefinition`
- Purpose: Parses special power definitions from INI files and creates/updates templates
- Calls: `findSpecialPowerTemplatePrivate`, `newInstance`, `friend_getFinalOverride`, `setNextOverride`, `markAsOverride`, `friend_setNameAndID`, `getFieldParse`, `initFromINI`

### `canUseSpecialPower`
- Purpose: Checks if an object/player meets requirements to use a special power
- Calls: `getSpecialPowerModule`, `getControllingPlayer`, `hasScience`

### `reset`
- Purpose: Resets the special power store, clearing overrides
- Calls: `deleteOverrides`

## Globals
- **TheSpecialPowerStore (SpecialPowerStore*)**: Global instance of the special power store

## Dependencies
- Key includes: `PreRTS.h`, `Common/Player.h`, `Common/Science.h`, `Common/SpecialPower.h`, `GameLogic/Object.h`, `Common/BitFlagsIO.h`
- External symbols: `INI`, `AsciiString`, `ScienceType`, `Player`, `Object`, `Overridable`
