# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DScienceModelDraw.cpp

## Purpose
Handles drawing of 3D models only if the local player possesses the required science.

## Responsibilities
- Checks player's science ownership before rendering
- Extends W3DModelDraw functionality with science-based visibility
- Manages module data parsing and serialization

## Key Types
- W3DScienceModelDrawModuleData (Class): Stores required science type
- W3DScienceModelDraw (Class): Science-gated drawable model

## Key Functions
### W3DScienceModelDraw::doDrawModule
- Purpose: Conditionally renders model based on player's science
- Calls: `getW3DScienceModelDrawModuleData()`, `ThePlayerList->getLocalPlayer()->hasScience()`, `ThePlayerList->getLocalPlayer()->isPlayerActive()`, `setHidden()`, `W3DModelDraw::doDrawModule()`

### W3DScienceModelDraw::crc
- Purpose: Serialization CRC calculation
- Calls: `W3DModelDraw::crc()`

### W3DScienceModelDraw::xfer
- Purpose: Serialization/deserialization
- Calls: `XferVersion::xferVersion()`, `W3DModelDraw::xfer()`

### W3DScienceModelDraw::loadPostProcess
- Purpose: Post-load initialization
- Calls: `W3DModelDraw::loadPostProcess()`

## Globals
- None

## Dependencies
- `W3DDevice/GameClient/Module/W3DScienceModelDraw.h`
- `Common/Player.h`, `Common/PlayerList.h`, `Common/Science.h`, `Common/Xfer.h`
- `W3DModelDraw`, `MultiIniFieldParse`, `INI`, `Xfer`, `Matrix3
