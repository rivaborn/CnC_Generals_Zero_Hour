# Generals/Code/Tools/WorldBuilder/include/mapobjectprops.h

## Purpose
Header for the MapObjectProps dialog class used in WorldBuilder to edit properties of selected map objects.

## Responsibilities
- Manages UI for editing map object properties (position, health, team, etc.)
- Handles undo/redo for property changes
- Provides sliders for height and angle adjustments
- Synchronizes UI with underlying Dict objects

## Key Types
- **MapObjectProps (Class)**: Dialog for editing map object properties.
- **MapObject (Class)**: Reference to the selected map object (external).
- **ModifyObjectUndoable (Class)**: Undoable action for object modifications (external).
- **Dict (Class)**: Property dictionary for map objects (external).
- **WBPopupSliderButton (Class)**: Slider control for height/angle (external).
- **(anonymous enum)**: Dialog resource ID.
- **IDD (Enum)**: Dialog resource ID.

## Key Functions
### MapObjectProps()
- Purpose: Constructor for the MapObjectProps dialog.
- Calls: None visible.

### updateTheUI()
- Purpose: Updates the UI to reflect current object properties.
- Calls: `_DictToTeam`, `_DictToName`, etc.

### PopSliderChanged()
- Purpose: Handles slider value changes (height/angle).
- Calls: None visible.

### PopSliderFinished()
- Purpose: Applies final slider values to the object.
- Calls: None visible.

### getSingleSelectedMapObject()
- Purpose: Retrieves the currently selected map object.
- Calls: None visible.

## Globals
- **NEUTRAL_TEAM_UI_STR (const char*)**: String for neutral team UI display.
- **NEUTRAL_TEAM_INTERNAL_STR (const char*)**: String for neutral team internal representation.

## Dependencies
- `OptionsPanel.h`, `Dict.h`, `WBPopupSlider.h`
- `
