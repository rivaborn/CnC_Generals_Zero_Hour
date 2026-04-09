# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DScienceModelDraw.h

## Purpose
Defines a W3D module that renders a model only if the local player has a specific science type.

## Responsibilities
- Extends `W3DModelDraw` to add science-based visibility checks
- Manages module data containing required science type
- Implements drawing logic with science prerequisite validation

## Key Types
- **ScienceType (Enum)**: Not inferable (forward-declared).
- **W3DScienceModelDrawModuleData (Class)**: Holds required science type for drawing.
- **W3DScienceModelDraw (Class)**: Module that conditionally renders based on science.
- **W3DScienceModelDrawMagicEnum (Enum)**: Not inferable (macro-related).
- **W3DScienceModelDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (macro-related).

## Key Functions
### `W3DScienceModelDrawModuleData::buildFieldParse`
- Purpose: Parses module data fields from configuration.
- Calls: `MultiIniFieldParse` methods.

### `W3DScienceModelDraw::doDrawModule`
- Purpose: Draws the model only if the local player has the required science.
- Calls: Parent class `doDrawModule` (conditional).

## Globals
- None.

## Dependencies
- `W3DModelDraw.h` (parent class)
- `MultiIniFieldParse` (for config parsing)
- `Thing` (game entity base)
- `Matrix3D` (transform data)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module macro (`MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
