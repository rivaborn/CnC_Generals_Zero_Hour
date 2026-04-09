# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DPropDraw.cpp

## Purpose
Handles drawing of 3D props (models) in the game world via the W3D rendering system.

## Responsibilities
- Manages prop model rendering through the terrain render object
- Handles prop transformation changes (position/orientation)
- Provides INI field parsing for prop module data
- Implements serialization (Xfer) and CRC for network sync

## Key Types
- **W3DPropDrawModuleData (Class)**: Stores prop drawing configuration (model name)
- **W3DPropDraw (Class)**: Draw module for rendering 3D props

## Key Functions
### `W3DPropDraw::reactToTransformChange`
- Purpose: Adds prop to terrain when position changes
- Calls: `getDrawable()`, `getW3DPropDrawModuleData()`, `TheTerrainRenderObject->addProp()`

### `W3DPropDraw::doDrawModule`
- Purpose: Placeholder for prop drawing (currently empty)
- Calls: None

### `W3DPropDraw::xfer`
- Purpose: Serializes prop draw module state
- Calls: `DrawModule::xfer()`

### `W3DPropDrawModuleData::buildFieldParse`
- Purpose: Registers INI field parsing for module data
- Calls: `ModuleData::buildFieldParse()`

## Globals
- **TheTerrainRenderObject (External)**: Used to add props to the world

## Dependencies
- `Common/Thing.h`, `Common/ThingTemplate.h`, `Common/Xfer.h`
- `GameLogic/Object.h`, `GameClient/Drawable.h`
- `W3DDevice/GameClient/Module/W3DPropDraw.h`
- `W3DDevice/GameClient/BaseHeightMap.h`
