# Generals/Code/GameEngine/Source/GameLogic/Object/Armor.cpp

## Purpose
This file contains the implementation for armor templates and their storage in the Command & Conquer Generals game engine.

## Responsibilities
- Manages armor template creation and initialization.
- Adjusts damage based on armor coefficients.
- Parses armor definitions from INI files.

## Key Types
- `ArmorTemplate`: Represents an armor template with damage coefficients.
- `ArmorStore`: Stores multiple armor templates.

## Key Functions
### ArmorTemplate::ArmorTemplate
- Purpose: Initializes a new armor template.
- Calls: `clear()`

### ArmorTemplate::clear
- Purpose: Resets all damage coefficients to 1.0f.
- Calls: None

### ArmorTemplate::adjustDamage
- Purpose: Adjusts incoming damage based on the armor's resistance.
- Calls: None

### ArmorTemplate::parseArmorCoefficients (static)
- Purpose: Parses armor coefficients from an INI file.
- Calls: `INI::scanPercentToReal`, `INI::scanIndexList`

### ArmorStore::ArmorStore
- Purpose: Initializes a new armor store.
- Calls: `clear()`

### ArmorStore::~ArmorStore
- Purpose: Cleans up the armor store.
- Calls: `clear()`

### ArmorStore::findArmorTemplate
- Purpose: Finds an armor template by name.
- Calls: `TheNameKeyGenerator->nameToKey`, `m_armorTemplates.find`

### ArmorStore::parseArmorDefinition (static)
- Purpose: Parses an armor definition from an INI file.
- Calls: `ini->getNextToken`, `TheNameKeyGenerator->nameToKey`, `ini->initFromINI`

## Globals
- `TheArmorStore` (`ArmorStore*`): The global armor store instance.

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/INI.h"
  - "Common/ThingFactory
