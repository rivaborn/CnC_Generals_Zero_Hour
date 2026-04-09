# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DSupplyDraw.cpp

## Purpose
Handles dynamic visibility of supply-related bones in 3D models based on supply status.

## Responsibilities
- Manages bone visibility based on supply levels
- Parses supply bone prefix from INI data
- Updates bone visibility when supply status changes
- Serializes/deserializes module state

## Key Types
- `W3DSupplyDrawModuleData` (Class): Stores supply bone prefix configuration
- `W3DSupplyDraw` (Class): Main draw module implementing supply-based bone visibility

## Key Functions
### `updateDrawModuleSupplyStatus`
- Purpose: Updates bone visibility based on current supply levels
- Calls: `getDrawable()->getPristineBonePositions`, `doHideShowSubObjs`

### `buildFieldParse`
- Purpose: Registers INI field parsing for supply bone prefix
- Calls: `W3DModelDrawModuleData::buildFieldParse`

### `crc` / `xfer` / `loadPostProcess`
- Purpose: Standard SAGE serialization methods
- Calls: Base class versions of same methods

## Globals
None

## Dependencies
- `Common/Xfer.h` (Xfer serialization)
- `GameClient/Drawable.h` (Drawable base)
- `W3DDevice/GameClient/Module/W3DSupplyDraw.h` (Module data)
- `W3DModelDraw` (Base class)
- `ModelConditionInfo` (Bone visibility control)
