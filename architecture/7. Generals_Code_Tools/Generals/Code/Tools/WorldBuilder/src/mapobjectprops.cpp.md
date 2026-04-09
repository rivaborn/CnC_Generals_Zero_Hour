# Generals/Code/Tools/WorldBuilder/src/mapobjectprops.cpp

## Purpose
Handles the MapObjectProps dialog in WorldBuilder, allowing users to edit properties of selected map objects.

## Responsibilities
- Manages property editing for map objects (name, health, team, etc.)
- Handles undo/redo operations for property changes
- Updates UI based on selected objects
- Provides sliders for height and angle adjustments

## Key Types
- **MapObjectProps (Class)**: Main dialog class for property editing
- **Dict (Type)**: Dictionary structure for storing object properties
- **ModifyObjectUndoable (Class)**: Undoable action for object modifications

## Key Functions
### getNthKeyStr
- Purpose: Retrieves the key string for a dictionary entry
- Calls: TheNameKeyGenerator->keyToName

### getNthValueStr
- Purpose: Retrieves the formatted value string for a dictionary entry
- Calls: None directly visible

### MapObjectProps::updateTheUI
- Purpose: Updates the UI based on the currently selected map object
- Calls: Various _DictTo* methods

### MapObjectProps::OnEditprop
- Purpose: Handles property editing when user clicks edit button
- Calls: PropEdit dialog, DictItemUndoable creation

### MapObjectProps::getAllSelectedDicts
- Purpose: Collects all dictionaries of currently selected objects
- Calls: MapObject::getFirstMapObject, MapObject::getNext

## Globals
- **NEUTRAL_TEAM_UI_STR (const char*)**: String for neutral team UI display
- **NEUTRAL_TEAM_INTERNAL_STR (const char*)**: Internal string for neutral team
- **TheMapObjectProps (MapObjectProps*)**: Singleton instance of the dialog

## Dependencies
- MFC dialog framework (CDialog, CWnd, etc.)
- WorldBuilder-specific classes (MapObject, CWorldBuilderDoc)
- Common utilities (Dict, AsciiString, UnicodeString)
- Game logic modules (UpgradeModule, GenerateMinefieldBehavior)
