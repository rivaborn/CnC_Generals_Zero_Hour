# GeneralsMD/Code/GameEngine/Source/Common/RTS/PlayerTemplate.cpp

## Purpose
Handles player template data, including faction properties, starting units, and production modifiers.

## Responsibilities
- Defines player template fields and parsing logic
- Manages player template storage and retrieval
- Handles special production cost/time/veterancy rules
- Provides image references for UI elements

## Key Types
- **PlayerTemplate (Class)**: Stores player faction data (side, starting units, production modifiers)
- **PlayerTemplateStore (Class)**: Manages collection of player templates
- **FieldParse (Struct)**: INI field parsing configuration

## Key Functions
### `getFieldParse`
- Purpose: Returns INI field parsing configuration for PlayerTemplate
- Calls: None

### `parseProductionCostChange`
- Purpose: Parses production cost percentage changes from INI
- Calls: `INI::scanPercentToReal`

### `parseProductionTimeChange`
- Purpose: Parses production time percentage changes from INI
- Calls: `INI::scanPercentToReal`

### `parseProductionVeterancyLevel`
- Purpose: Parses starting veterancy levels for production
- Calls: `INI::scanIndexList`

### `parseStartMoney`
- Purpose: Parses initial money value and deposits it
- Calls: `INI::parseInt`, `Money::init`, `Money::deposit`

### `findPlayerTemplate`
- Purpose: Finds player template by name key with backward compatibility
- Calls: None

### `parsePlayerTemplateDefinition`
- Purpose: Parses player template definitions from INI
- Calls: `INI::initFromINI`

## Globals
- **ThePlayerTemplateStore (PlayerTemplateStore*)**: Global store for player templates

## Dependencies
- `Common/GameCommon.h`, `Common/PlayerTemplate.h`, `Common/Player.h`, `Common/INI.h`, `Common/Science.h`, `GameClient/Image.h`
- `INI` class methods, `Money` class, `Image` collection, `NameKeyType` system
