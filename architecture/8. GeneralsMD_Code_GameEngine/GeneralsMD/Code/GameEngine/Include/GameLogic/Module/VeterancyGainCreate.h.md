# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/VeterancyGainCreate.h

## Purpose
Defines a module that sets an object's veterancy level on creation if a required science is present.

## Responsibilities
- Sets veterancy level for objects at creation time
- Checks for presence of required science
- Provides module data structure for configuration

## Key Types
- **VeterancyGainCreateModuleData (Class)**: Contains veterancy level and required science type
- **VeterancyGainCreate (Class)**: Module implementation that handles veterancy assignment
- **VeterancyGainCreateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **VeterancyGainCreate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### VeterancyGainCreateModuleData::buildFieldParse
- Purpose: Parses module data from configuration files
- Calls: Not inferable

### VeterancyGainCreate::onCreate
- Purpose: Applies veterancy level to object during creation
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/GameCommon.h`
- `Common/Science.h`
- `GameLogic/Module/CreateModule.h`
- `Thing` class (forward reference)
- `VeterancyLevel` type
- `ScienceType` type
- `CreateModule` base class
- `CreateModuleData` base class
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module macro (`MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
