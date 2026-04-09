# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DSupplyDraw.h

## Purpose
Defines a W3D module that controls visibility of bones based on supply status.

## Responsibilities
- Manages bone visibility based on supply levels
- Provides module data for configuration
- Handles geometry change reactions

## Key Types
- **W3DSupplyDrawModuleData (Class)**: Module data containing supply bone prefix
- **W3DSupplyDraw (Class)**: Main draw module class that manages supply-based bone visibility
- **W3DSupplyDrawMagicEnum (Enum)**: Not inferable
- **W3DSupplyDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### W3DSupplyDrawModuleData::buildFieldParse
- Purpose: Parses module data fields from configuration
- Calls: Not inferable

### W3DSupplyDraw::updateDrawModuleSupplyStatus
- Purpose: Updates visual feedback based on supply levels
- Calls: Not inferable

### W3DSupplyDraw::reactToGeometryChange
- Purpose: Handles geometry change reactions
- Calls: Not inferable

## Globals
- None

## Dependencies
- W3DModelDraw.h
- MultiIniFieldParse (used in buildFieldParse)
- Thing (base class for game objects)
- ModuleData (base class for module data)
