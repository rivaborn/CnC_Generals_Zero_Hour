# Generals/Code/Tools/WorldBuilder/include/PointerTool.h

## Purpose
Defines the `PointerTool` class for object selection, movement, and rotation in WorldBuilder.

## Responsibilities
- Handles object selection, movement, and rotation via mouse input.
- Manages undo operations for object modifications.
- Controls cursor behavior during tool operations.
- Integrates with polygon tool functionality for polygon triggers.

## Key Types
- **PointerTool (Class)**: Main tool class for object manipulation.
- **ModifyObjectUndoable (Class)**: Undoable operation for object modifications.
- **WorldHeightMapEdit (Class)**: External class for heightmap editing.
- **HYSTERESIS (Enum)**: Defines hysteresis threshold for mouse movement.

## Key Functions
### PointerTool::checkForPropertiesPanel
- Purpose: Checks for properties panel (implementation not shown).
- Calls: Not inferable.

### PointerTool::activate
- Purpose: Activates the tool and clears selection.
- Calls: `clearSelection`.

### PointerTool::deactivate
- Purpose: Deactivates the tool.
- Calls: Not inferable.

### PointerTool::setCursor
- Purpose: Sets cursor based on tool state.
- Calls: Not inferable.

### PointerTool::mouseDown
- Purpose: Handles mouse down event for selection/movement.
- Calls: Not inferable.

### PointerTool::mouseMoved
- Purpose: Handles mouse movement for dragging/rotating.
- Calls: Not inferable.

### PointerTool::mouseUp
- Purpose: Handles mouse up event to finalize operations.
- Calls: Not inferable.

### PointerTool::clearSelection
- Purpose: Clears selected object flags.
- Calls: Not inferable.

### PointerTool::allowPick
- Purpose: Determines if an object can be picked.
- Calls: Not inferable.

## Globals
-
