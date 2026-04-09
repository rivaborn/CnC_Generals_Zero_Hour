# Generals/Code/Tools/WorldBuilder/include/GroveTool.h

## Purpose
Defines the `GroveTool` class for placing groves of trees in the WorldBuilder editor.

## Responsibilities
- Manages tree/shrub placement via mouse interactions
- Handles grove generation with recursive placement logic
- Tracks drag state and object placement
- Integrates with WorldBuilder's tool system

## Key Types
- **GroveTool (Class)**: Main tool class for grove placement
- **WorldHeightMapEdit (Class)**: External heightmap editor (forward declared)
- **(anonymous enum) (Enum)**: Defines hysteresis threshold (3)
- **HYSTERESIS (Enum)**: Constant for drag hysteresis

## Key Functions
### `plantTree`
- Purpose: Places a single tree at the given position
- Calls: `addObj`

### `plantShrub`
- Purpose: Places a single shrub at the given position
- Calls: `addObj`

### `plantGrove`
- Purpose: Recursively generates a grove of trees/shrubs
- Calls: `plantTree`, `plantShrub`, `_plantGroveInBox`

### `_plantGroveInBox`
- Purpose: Places grove within a defined bounding box
- Calls: Not inferable

### `addObj`
- Purpose: Adds a map object at the specified position
- Calls: Not inferable

### `mouseDown`
- Purpose: Handles mouse press to start grove placement
- Calls: `activate`, `_plantGroveInBox`

### `mouseUp`
- Purpose: Handles mouse release to finalize placement
- Calls: Not inferable

### `mouseMoved`
- Purpose: Handles mouse movement during drag
- Calls: `_plantGroveInBox`

## Globals
- **m_downPt (CPoint)**: Stores initial
