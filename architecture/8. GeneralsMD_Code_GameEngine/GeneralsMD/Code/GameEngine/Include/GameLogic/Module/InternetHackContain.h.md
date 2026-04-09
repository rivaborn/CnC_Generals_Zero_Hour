# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/InternetHackContain.h

## Purpose
Defines a module for containing units that grants the "aiHackInternet" command to passengers.

## Responsibilities
- Inherits from `TransportContain` to handle passenger containment logic
- Provides module data parsing for configuration
- Implements `onContaining` to apply effects when units are contained
- Uses memory pool management for object allocation

## Key Types
- **InternetHackContainModuleData (Class)**: Module data for configuration parsing
- **InternetHackContain (Class)**: Main containment module class
- **InternetHackContainMagicEnum (Enum)**: Not inferable (empty)
- **InternetHackContain_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty)

## Key Functions
### InternetHackContainModuleData::buildFieldParse
- Purpose: Registers field parsing callbacks for module data
- Calls: Not inferable

### InternetHackContainModuleData::parseRiderInfo
- Purpose: Parses rider-specific configuration from INI files
- Calls: Not inferable

### InternetHackContain::onContaining
- Purpose: Applies containment effects (grants aiHackInternet command)
- Calls: Not inferable

## Globals
- None

## Dependencies
- `TransportContain.h` (base class)
- `MultiIniFieldParse`, `INI` (for configuration parsing)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module macro (`MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
