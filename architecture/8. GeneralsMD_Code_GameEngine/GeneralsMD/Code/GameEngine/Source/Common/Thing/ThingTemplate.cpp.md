# GeneralsMD/Code/GameEngine/Source/Common/Thing/ThingTemplate.cpp

## Purpose
Handles parsing and management of game object templates (units, buildings, etc.) from INI files.

## Responsibilities
- Parses object properties from INI files
- Manages module attachments (behavior, draw, client update)
- Handles prerequisites and build restrictions
- Provides access to template data during gameplay

## Key Types
- `ThingTemplate` (Class): Main template class for game objects
- `ModuleInfo` (Class): Manages attached modules
- `FieldParse` (Struct): INI field parsing definition
- `USE_EXP_VALUE_FOR_SKILL_VALUE` (Const): Special value flag

## Key Functions
### `parsePrerequisiteUnit`
- Purpose: Parses unit prerequisites from INI
- Calls: `INI::parseAsciiStringVector`

### `parsePrerequisiteScience`
- Purpose: Parses science prerequisites from INI
- Calls: `INI::parseAsciiStringVector`

### `parseArbitraryFXIntoMap`
- Purpose: Parses FX definitions into template's FX map
- Calls: `INI::parseAsciiString`, `INI::parseAsciiStringVector`

### `parseArbitrarySoundsIntoMap`
- Purpose: Parses sound definitions into template's sound map
- Calls: `INI::parseAsciiString`, `INI::parseAsciiStringVector`

## Globals
- `USE_EXP_VALUE_FOR_SKILL_VALUE` (Int): Special value indicating experience should be used for skill points

## Dependencies
- `ThingTemplate.h`, `INI.h`, `ModuleFactory.h`, `ProductionPrerequisite.h`
- `GameAudio.h`, `GameText.h`, `FXList.h`, `Shadow.h`
- `Armor.h`, `Weapon.h`, `Powers.h`, `Science.h`
