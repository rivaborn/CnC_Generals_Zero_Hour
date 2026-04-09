# Generals/Code/Tools/WorldBuilder/include/BuildListTool.h

## Purpose
Defines the BuildListTool class, a tool for adding items to a build list in the WorldBuilder editor.

## Responsibilities
- Manages build list tool operations (add, move, rotate).
- Handles mouse input for object manipulation.
- Maintains UI state (cursors, dialogs).
- Tracks tool activation/deactivation.

## Key Types
- **BuildListTool (Class)**: Main tool class for build list operations.
- **BuildListInfo (Class)**: Not inferable (forward-declared).
- **WorldHeightMapEdit (Class)**: Not inferable (forward-declared).

## Key Functions
### BuildListTool::mouseDown
- Purpose: Handles mouse down events for object manipulation.
- Calls: Not inferable (implementation in .cpp).

### BuildListTool::mouseUp
- Purpose: Handles mouse up events for object manipulation.
- Calls: Not inferable.

### BuildListTool::mouseMoved
- Purpose: Handles mouse movement for object dragging/rotating.
- Calls: Not inferable.

### BuildListTool::activate
- Purpose: Activates the tool and sets up UI state.
- Calls: Not inferable.

### BuildListTool::deactivate
- Purpose: Deactivates the tool and cleans up UI state.
- Calls: Not inferable.

## Globals
- **m_static_pickBuildingDlg (PickUnitDialog*)**: Static reference to the building selection dialog.
- **m_isActive (Bool)**: Tracks if the tool is currently active.

## Dependencies
- **Tool.h**: Base class for WorldBuilder tools.
- **Common/AsciiString.h**: String utilities.
- **PickUnitDialog.h**: Dialog for selecting buildings.
- **WbView**, **CWorldBuilderDoc**: WorldBuilder document/view classes.
- **Coord3
