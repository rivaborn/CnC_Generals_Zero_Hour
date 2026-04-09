# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DSupplyDraw.cpp

## Purpose
Handles dynamic visibility of supply-related bones in 3D models based on supply status.

## Responsibilities
- Manages bone visibility for supply indicators
- Updates bone display when supply changes
- Parses configuration for supply bone prefixes
- Handles serialization and CRC for supply draw module

## Key Types
- **W3DSupplyDrawModuleData (Class)**: Stores supply bone prefix configuration
- **W3DSupplyDraw (Class)**: Main supply draw module implementation

## Key Functions
### `updateDrawModuleSupplyStatus`
- Purpose: Updates bone visibility based on current supply percentage
- Calls: `getDrawable()->getPristineBonePositions`, `doHideShowSubObjs`

### `buildFieldParse`
- Purpose: Configures INI field parsing for supply draw module data
- Calls: `W3DModelDrawModuleData::buildFieldParse`

### `xfer`
- Purpose: Handles serialization of supply draw module state
- Calls: `W3DModelDraw::xfer`

## Globals
- None

## Dependencies
- `Common/Xfer.h` (Xfer)
- `GameClient/Drawable.h` (Drawable)
- `W3DDevice/GameClient/Module/W3DSupplyDraw.h` (ModuleData)
- `W3DModelDraw` (base class)
- `ModelConditionInfo::HideShowSubObjInfo` (struct)
