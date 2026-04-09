# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DSupplyDraw.h

## Purpose
Defines a W3D module for visually representing supply status by hiding/showing bones in a 3D model.

## Responsibilities
- Manages supply-related bone visibility in 3D models
- Updates visual feedback based on supply levels
- Handles geometry changes for supply bones
- Provides module data parsing for configuration

## Key Types
- **W3DSupplyDrawModuleData (Class)**: Stores module configuration including supply bone prefix
- **W3DSupplyDraw (Class)**: Main module class handling supply visualization
- **W3DSupplyDrawMagicEnum (Enum)**: Not inferable (likely unused placeholder)
- **W3DSupplyDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused placeholder)

## Key Functions
### W3DSupplyDrawModuleData::buildFieldParse
- Purpose: Parses module configuration from INI files
- Calls: Not inferable

### W3DSupplyDraw::updateDrawModuleSupplyStatus
- Purpose: Updates bone visibility based on current supply levels
- Calls: Not inferable

### W3DSupplyDraw::reactToGeometryChange
- Purpose: Handles changes to the 3D model geometry
- Calls: Not inferable

## Globals
- None

## Dependencies
- `W3DModelDraw.h` (base class)
- `AsciiString` (string type)
- `MultiIniFieldParse` (INI parsing)
- `Thing` (game entity base)
- `ModuleData` (module configuration base)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module macro (`MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
