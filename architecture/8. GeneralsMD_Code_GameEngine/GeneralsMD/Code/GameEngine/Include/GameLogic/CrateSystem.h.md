# GeneralsMD/Code/GameEngine/Include/GameLogic/CrateSystem.h

## Purpose
Defines the crate system for managing supply crates in the game, including templates, creation logic, and subsystem integration.

## Responsibilities
- Manages crate templates and their creation conditions
- Handles parsing of crate definitions from INI files
- Provides lookup and creation of crate objects
- Integrates with the game's subsystem interface

## Key Types
- **ScienceType (Enum)**: Not inferable.
- **crateCreationEntry (Struct)**: Stores crate name and creation chance.
- **CrateTemplate (Class)**: Represents a crate template with conditions and creation parameters.
- **CrateTemplateOverride (Class)**: Override mechanism for CrateTemplate.
- **CrateSystem (Class)**: Subsystem for managing crate templates and creation logic.

## Key Functions
### CrateTemplate::parseCrateCreationEntry
- Purpose: Parses crate creation entries from INI files.
- Calls: Not inferable.

### CrateSystem::parseCrateTemplateDefinition
- Purpose: Parses crate template definitions from INI files.
- Calls: Not inferable.

### CrateSystem::findCrateTemplate
- Purpose: Finds a crate template by name.
- Calls: Not inferable.

### CrateSystem::newCrateTemplate
- Purpose: Creates a new crate template.
- Calls: Not inferable.

## Globals
- **TheCrateSystem (CrateSystem*)**: Global instance of the crate system.

## Dependencies
- Common/Ini.h, Common/Overridable.h, Common/Override.h
- SubsystemInterface (not defined here)
- AsciiString, Real, VeterancyLevel, KindOfMaskType (not defined here)
