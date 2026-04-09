# GeneralsMD/Code/GameEngine/Include/GameLogic/Armor.h

## Purpose
Defines classes for handling armor types and damage modifiers in the game.

## Responsibilities
- Define armor templates and instances
- Manage armor damage calculations
- Provide storage and lookup for armor definitions
- Parse armor data from INI files

## Key Types
- **ArmorTemplate (Class)**: Stores damage coefficients for different damage types.
- **Armor (Class)**: Represents an instance of armor with a template reference.
- **ArmorStore (Class)**: Manages a collection of armor templates with lookup functionality.
- **ArmorTemplateMap (Class)**: Typedef for a hash map storing armor templates.

## Key Functions
### ArmorTemplate::adjustDamage
- Purpose: Adjusts damage based on armor coefficients.
- Calls: None

### ArmorStore::findArmorTemplate
- Purpose: Finds an armor template by name.
- Calls: None

### ArmorStore::parseArmorDefinition
- Purpose: Parses armor definitions from INI files.
- Calls: ArmorTemplate::parseArmorCoefficients

## Globals
- **TheArmorStore (ArmorStore*)**: Global instance of the armor store.

## Dependencies
- Common/NameKeyGenerator.h
- Common/STLTypedefs.h
- GameLogic/Damage.h
- INI class (external)
