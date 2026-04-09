# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DScienceModelDraw.cpp

## Purpose
Handles conditional rendering of 3D models based on the player's science research status.

## Responsibilities
- Checks if the local player has the required science before drawing
- Extends W3DModelDraw with science-based visibility logic
- Manages module data parsing and serialization

## Key Types
- **W3DScienceModelDrawModuleData (Class)**: Stores required science type for conditional rendering
- **W3DScienceModelDraw (Class)**: Drawable that only renders if player has specified science

## Key Functions
### `doDrawModule`
- Purpose: Conditionally renders the model based on science ownership
- Calls: `getW3DScienceModelDrawModuleData()`, `setHidden()`, `W3DModelDraw::doDrawModule()`

### `buildFieldParse`
- Purpose: Registers INI field parsing for science requirement
- Calls: `W3DModelDrawModuleData::buildFieldParse()`

### `crc`
- Purpose: Serialization checksum calculation
- Calls: `W3DModelDraw::crc()`

### `xfer`
- Purpose: Serialization/deserialization handler
- Calls: `W3DModelDraw::xfer()`

### `loadPostProcess`
- Purpose: Post-load initialization
- Calls: `W3DModelDraw::loadPostProcess()`

## Globals
- **ThePlayerList (PlayerList)**: Access to player information

## Dependencies
- `W3DScienceModelDraw.h`, `Common/Player.h`, `Common/PlayerList.h`, `Common/Science.h`, `Common/Xfer.h`
- `W3DModelDraw`, `MultiIniFieldParse`, `ScienceType`, `Xfer`, `Matrix3D`
