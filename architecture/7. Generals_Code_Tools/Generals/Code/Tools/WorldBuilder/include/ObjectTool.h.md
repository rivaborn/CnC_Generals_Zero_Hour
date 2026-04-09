# Generals/Code/Tools/WorldBuilder/include/ObjectTool.h

## Purpose
Defines the `ObjectTool` class, a tool for blending edges in the WorldBuilder editor.

## Responsibilities
- Implements mouse interaction for edge blending
- Calculates angles between 3D points
- Manages tool activation/deactivation
- Handles mouse events (down, up, moved)

## Key Types
- **ObjectTool (Class)**: Edge blending tool for WorldBuilder.
- **WorldHeightMapEdit (Class)**: Forward declaration (external dependency).

## Key Functions
### `calcAngle`
- Purpose: Calculate angle between two 3D points in a view.
- Calls: None (static utility).

### `mouseDown`
- Purpose: Handle mouse down event for edge blending.
- Calls: Not inferable.

### `mouseUp`
- Purpose: Handle mouse up event for edge blending.
- Calls: Not inferable.

### `mouseMoved`
- Purpose: Handle mouse movement during edge blending.
- Calls: Not inferable.

### `activate`
- Purpose: Activate the tool.
- Calls: Not inferable.

### `deactivate`
- Purpose: Deactivate the tool.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- `Tool.h` (base class)
- `WbView` (external)
- `CWorldBuilderDoc` (external)
- `Coord3D` (external)
- `CPoint` (external)
- `Real` (external)
