# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DScienceModelDraw.h

## Purpose
Defines a W3D module that draws a model only if the local player has a specific science type.

## Responsibilities
- Extends `W3DModelDraw` to add science-based visibility checks
- Manages module data containing required science type
- Implements conditional drawing logic in `doDrawModule`

## Key Types
- **ScienceType (Enum)**: Not inferable (forward-declared).
- **W3DScienceModelDrawModuleData (Class)**: Holds required science type for drawing.
- **W3DScienceModelDraw (Class)**: Module that conditionally draws based on player science.
- **W3DScienceModelDrawMagicEnum (Enum)**: Not inferable (macro-generated).
- **W3DScienceModelDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (macro-generated).

## Key Functions
### `W3DScienceModelDrawModuleData::buildFieldParse`
- Purpose: Parses module data fields from configuration.
- Calls: `MultiIniFieldParse` methods.

### `W3DScienceModelDraw::doDrawModule`
- Purpose: Draws the model only if the local player has the required science.
- Calls: Parent class `doDrawModule` (conditionally).

## Globals
- None.

## Dependencies
- `W3DModelDraw.h` (parent class)
- `MultiIniFieldParse` (for config parsing)
- `Thing` (game entity base class)
- `Matrix3D` (transform data)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`, `MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
