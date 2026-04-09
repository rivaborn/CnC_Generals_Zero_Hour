# Generals/Code/GameEngine/Source/Common/RTS/PlayerTemplate.cpp

## Purpose
This file defines the `PlayerTemplate` class and its associated functions, which manage player templates in the game. It handles parsing of player data from INI files and provides methods to access various attributes of a player template.

## Responsibilities
- Parse player template data from INI files.
- Manage player template attributes such as starting units, money, and images.
- Provide methods to retrieve player template information.
- Store and manage multiple player templates in a `PlayerTemplateStore`.

## Key Types
- **PlayerTemplate (Class)**: Represents a player template with various attributes like side, starting units, and colors.
- **PlayerTemplateStore (Class)**: Manages a collection of `PlayerTemplate` objects.

## Key Functions
### getFieldParse
- Purpose: Returns a table of field parsing functions for player templates.
- Calls: None

### parseStartMoney
- Purpose: Parses the starting money from an INI file and initializes the `Money` object.
- Calls: `INI::parseInt`, `Money::init`, `Money::deposit`

### parseProductionCostChange
- Purpose: Parses production cost changes for specific build templates.
- Calls: `INI::getNextToken`, `INI::scanPercentToReal`

### parseProductionTimeChange
- Purpose: Parses production time changes for specific build templates.
- Calls: `INI::getNextToken`, `INI::scanPercentToReal`

### parseProductionVeterancyLevel
- Purpose: Parses veterancy levels for specific build templates.
- Calls: `INI::getNextToken`, `INI::scanIndexList`

### getHeadWaterMarkImage
- Purpose: Retrieves the head watermark image associated with a player template.
- Calls: `TheMappedImageCollection->findImageByName`

### findPlayerTemplate
- Purpose: Finds a player template by its name key, handling legacy map names.
- Calls: None

### parsePlayerTemplateDefinition
- Purpose: Parses a player template definition from an INI file and adds it to the store.
- Calls: `ini->getNextToken`, `ThePlayerTemplateStore->findPlayerTemplate`, `ini->initFromINI`

## Globals
- **ThePlayerTemplateStore (PlayerTemplateStore*)**: Global instance of the player template store.

## Dependencies
- Key includes:
  - "Common/GameCommon.h"
  - "Common/PlayerTemplate.h"
  - "Common/Player.h"
  - "Common/INI.h"
  - "Common/Science.h"
  - "GameClient/Image.h"
