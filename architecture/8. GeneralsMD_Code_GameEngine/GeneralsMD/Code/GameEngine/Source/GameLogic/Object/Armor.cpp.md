# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Armor.cpp

## Purpose
Manages armor templates and their damage coefficients for game objects.

## Responsibilities
- Defines `ArmorTemplate` class to store damage resistance values
- Implements `ArmorStore` to manage a collection of armor templates
- Parses armor definitions from INI files
- Provides damage adjustment based on armor type

## Key Types
- **ArmorTemplate (Class)**: Stores damage coefficients for different damage types
- **ArmorStore (Class)**: Manages a collection of armor templates
- **DamageType (Enum)**: Not defined here, but used for indexing damage coefficients

## Key Functions
### ArmorTemplate::adjustDamage
- Purpose: Adjusts damage based on armor coefficients
- Calls: None

### ArmorTemplate::parseArmorCoefficients
- Purpose: Parses armor coefficients from INI file
- Calls: `INI::scanPercentToReal`, `DamageTypeFlags::getSingleBitFromName`

### ArmorStore::findArmorTemplate
- Purpose: Finds an armor template by name
- Calls: `TheNameKeyGenerator->nameToKey`

### ArmorStore::parseArmorDefinition
- Purpose: Parses armor definitions from INI file
- Calls: `TheNameKeyGenerator->nameToKey`, `ini->initFromINI`

## Globals
- **TheArmorStore (ArmorStore*)**: Global instance of the armor store

## Dependencies
- `Common/INI.h`, `Common/ThingFactory.h`, `GameLogic/Armor.h`, `GameLogic/Damage.h`
- `TheNameKeyGenerator` (external symbol)
