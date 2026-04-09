# Generals/Code/Tools/WorldBuilder/src/GroveTool.cpp

## Purpose
Handles tree/shrub placement in WorldBuilder, including grove generation and terrain validation.

## Responsibilities
- Plants individual trees/shrubs at specified positions
- Generates groves recursively from seed locations
- Validates terrain suitability (cliffs, water, slope)
- Manages undoable object placement

## Key Types
- `GroveTool` (Class): Main tool class for grove placement
- `GroveOptions` (External): Configuration for tree types and placement rules

## Key Functions
### `plantTree`
- Purpose: Places a single tree at given coordinates
- Calls: `addObj`, `TheGroveOptions->getTotalTreePerc`, `GameLogicRandomValue`

### `plantGrove`
- Purpose: Recursively generates a grove of trees from a seed location
- Calls: `plantTree`, `plantShrub`, `GameLogicRandomValueReal`, `localIsUnderwater`, `_positionIsTooCliffyForTrees`

### `_positionIsTooCliffyForTrees`
- Purpose: Checks if terrain is too steep for tree placement
- Calls: `TheTerrainRenderObject->getHeightMapHeight`

### `localIsUnderwater`
- Purpose: Determines if a position is underwater
- Calls: `PolygonTrigger::getFirstPolygonTrigger`, `pTrig->pointInTrigger`, `TheTerrainRenderObject->getHeightMapHeight`

## Globals
- `flatTolerance` (Real): Minimum surface normal Z for tree placement (0.8f)

## Dependencies
- `GroveTool.h`, `CUndoable.h`, `MainFrm.h`, `WHeightMapEdit.h`, `WorldBuilderDoc.h`, `WorldBuilderView.h`
- `GameLogic/LogicRandomValue.h`, `W3DDevice/GameClient/HeightMap.h`, `Common/Debug.h`
- `DrawObject.h`, `GroveOptions.h`, `GameLogic/PolygonTrigger.h`, `MapObjectProps.h`
