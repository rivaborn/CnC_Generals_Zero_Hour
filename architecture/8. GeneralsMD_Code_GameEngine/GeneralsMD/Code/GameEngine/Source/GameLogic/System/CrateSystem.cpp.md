# GeneralsMD/Code/GameEngine/Source/GameLogic/System/CrateSystem.cpp

## Purpose
Manages crate templates and their initialization/parsing in the game.

## Responsibilities
- Creates, stores, and deletes crate templates
- Parses crate definitions from INI files
- Handles crate overrides and inheritance
- Provides lookup for crate templates by name

## Key Types
- **CrateSystem (Class)**: Manages crate templates and system state
- **CrateTemplate (Class)**: Represents a crate type with properties and possible contents
- **crateCreationEntry (Struct)**: Stores crate name and chance for random selection

## Key Functions
### `CrateSystem::parseCrateTemplateDefinition`
- Purpose: Parses crate template definitions from INI files
- Calls: `TheCrateSystem->friend_findCrateTemplate`, `TheCrateSystem->newCrateTemplate`, `TheCrateSystem->newCrateTemplateOverride`, `ini->initFromINI`

### `CrateSystem::newCrateTemplate`
- Purpose: Creates a new crate template, optionally copying from default
- Calls: `newInstance`, `findCrateTemplate`

### `CrateSystem::newCrateTemplateOverride`
- Purpose: Creates an override version of an existing crate template
- Calls: `newInstance`

### `CrateTemplate::parseCrateCreationEntry`
- Purpose: Parses crate contents and their probabilities from INI
- Calls: `ini->getNextToken`

## Globals
- **TheCrateSystem (CrateSystem*)**: Singleton instance of the crate system

## Dependencies
- `CrateSystem.h`, `Common/BitFlagsIO.h`, `PreRTS.h`
- `INI`, `Overridable`, `KindOfMaskType`, `FieldParse`, `AsciiString`, `VeterancyNames`
