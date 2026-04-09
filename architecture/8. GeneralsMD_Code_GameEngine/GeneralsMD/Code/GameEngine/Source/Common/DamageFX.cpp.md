# GeneralsMD/Code/GameEngine/Source/Common/DamageFX.cpp

## Purpose
Handles damage effects (FX) definitions, parsing, and application in the game.

## Responsibilities
- Manages damage FX data storage and retrieval
- Parses damage FX configurations from INI files
- Applies damage FX to objects based on damage type and amount
- Supports veterancy-level specific FX

## Key Types
- **DamageFX (Class)**: Stores damage FX definitions per damage type and veterancy level
- **DamageFXStore (Class)**: Global store for damage FX definitions
- **DFX (Struct)**: Internal structure holding FX lists and thresholds

## Key Functions
### `parseCommonStuff`
- Purpose: Parses common INI parameters for veterancy and damage type ranges
- Calls: `INI::scanIndexList`, `DamageTypeFlags::getSingleBitFromName`

### `parseAmount`
- Purpose: Parses damage amount thresholds for major/minor FX
- Calls: `parseCommonStuff`, `INI::scanReal`

### `parseMajorFXList`
- Purpose: Parses major damage FX list definitions
- Calls: `parseCommonStuff`, `INI::parseFXList`

### `parseMinorFXList`
- Purpose: Parses minor damage FX list definitions
- Calls: `parseCommonStuff`, `INI::parseFXList`

### `parseTime`
- Purpose: Parses damage FX throttle time values
- Calls: `parseCommonStuff`, `INI::parseDurationUnsignedInt`

### `doDamageFX`
- Purpose: Applies damage FX to victim object
- Calls: `getDamageFXList`, `FXList::doFXObj`

## Globals
- **TheDamageFXStore (DamageFXStore*)**: Global instance of damage FX store

## Dependencies
- INI parsing utilities (`INI.h`)
- Game object system (`Object.h`)
- FX system (`FXList.h`)
- Damage system (`Damage.h`)
- Audio system (`GameAudio.h`)
- Name key generation (`NameKeyGenerator`)
