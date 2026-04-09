# Generals/Code/Tools/WorldBuilder/src/LightOptions.cpp

## Purpose
Handles the UI for editing light properties in WorldBuilder, a level editor tool.

## Responsibilities
- Manages a dialog for light property editing (color, height, radius)
- Updates UI based on selected light object
- Applies changes to the selected light's properties
- Invalidates view to reflect changes

## Key Types
- LightOptions (Class): Dialog for light property editing
- MapObject (External): Represents map objects (lights in this case)
- Dict (External): Property dictionary for MapObject
- RGBColor (External): Color representation
- TheKey_* (External): Well-known property keys

## Key Functions
### LightOptions::getSingleSelectedLight
- Purpose: Finds the single selected light object in the scene.
- Calls: MapObject::getFirstMapObject, MapObject::isSelected, MapObject::isLight

### LightOptions::updateTheUI
- Purpose: Updates the dialog controls with the selected light's properties.
- Calls: getSingleSelectedLight, Dict::getReal, Dict::getInt, RGBColor::setFromInt

### LightOptions::update
- Purpose: Public interface to update the UI when needed.
- Calls: updateTheUI

### LightOptions::OnInitDialog
- Purpose: Initializes the dialog when created.
- Calls: CDialog::OnInitDialog

### LightOptions::OnChangeLightEdit
- Purpose: Handles changes to light property edit fields.
- Calls: getSingleSelectedLight, Dict::getReal, Dict::getInt, Dict::setReal, Dict::setInt, WbView3d::invalObjectInView

## Globals
- m_staticThis (LightOptions*): Static pointer to the dialog instance

## Dependencies
- MFC (CDialog, CWnd, etc.)
- WorldBuilder-specific classes (MapObject, Dict, RGBColor, WbView3d)
- Common/WellKnownKeys.h for property key definitions
