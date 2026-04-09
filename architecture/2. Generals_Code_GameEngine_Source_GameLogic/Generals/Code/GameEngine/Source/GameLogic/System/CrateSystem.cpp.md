# Generals/Code/GameEngine/Source/GameLogic/System/CrateSystem.cpp

## Purpose
This file implements the `CrateSystem` class, which manages crate templates and their initialization from INI files in Command & Conquer Generals.

## Responsibilities
- Manages crate template creation, deletion, and parsing.
- Handles initialization and reset of crate templates.
- Parses crate definitions from INI files.

## Key Types
- **CrateSystem (Class)**: Manages crate templates.
- **CrateTemplate (Class)**: Represents a crate template with various attributes like creation chance, veterancy level, and possible crates.

## Key Functions
### CrateSystem::init
- Purpose: Initializes the crate system.
- Calls: `reset`

### CrateSystem::reset
- Purpose: Resets the crate system by cleaning up overrides.
- Calls: `deleteOverrides`, `erase`

### CrateSystem::parseCrateTemplateDefinition
- Purpose: Parses a crate template definition from an INI file.
- Calls: `friend_findCrateTemplate`, `newCrateTemplate`, `newCrateTemplateOverride`, `initFromINI`

### CrateSystem::newCrateTemplate
- Purpose: Creates a new crate template.
- Calls: `newInstance`, `findCrateTemplate`, `setName`, `push_back`

### CrateSystem::newCrateTemplateOverride
- Purpose: Creates an override for an existing crate template.
- Calls: `newInstance`, `setNextOverride`

### CrateSystem::friend_findCrateTemplate
- Purpose: Finds a crate template by name.
- Calls: None

## Globals
- **TheCrateSystem (CrateSystem \*)**: Global instance of the crate system.

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `GameLogic/CrateSystem.h`
  - `Common/BitFlagsIO.h`
  - `INI` class
  - `AsciiString` class
  - `CrateTemplateOverride` class
