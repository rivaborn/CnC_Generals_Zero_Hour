# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DTreeDraw.cpp

## Purpose
Handles tree rendering and behavior in the game world, including topping and shadow effects.

## Responsibilities
- Manages tree model rendering and positioning
- Handles tree topping physics and effects
- Processes tree transformation changes
- Serializes tree state for save/load

## Key Types
- **W3DTreeDrawModuleData (Class)**: Stores tree configuration (models, animations, physics)
- **W3DTreeDraw (Class)**: Main tree drawable module implementing rendering and behavior

## Key Functions
### `W3DTreeDrawModuleData::buildFieldParse`
- Purpose: Registers INI parsing rules for tree module data
- Calls: `ModuleData::buildFieldParse`

### `W3DTreeDraw::reactToTransformChange`
- Purpose: Handles tree positioning and terrain integration
- Calls: `TheTerrainRenderObject->addTree`

### `W3DTreeDraw::doDrawModule`
- Purpose: Placeholder for tree rendering (currently empty)
- Calls: None

### `W3DTreeDraw::xfer`
- Purpose: Serializes tree module state
- Calls: `DrawModule::xfer`

## Globals
- None

## Dependencies
- `Common/Thing.h`, `Common/ThingTemplate.h`, `GameLogic/Object.h`
- `GameClient/Drawable.h`, `W3DDevice/GameClient/BaseHeightMap.h`
- `W3DDevice/GameClient/Module/W3DTreeDraw.h`
