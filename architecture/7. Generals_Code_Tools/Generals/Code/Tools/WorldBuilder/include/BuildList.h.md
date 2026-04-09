# Generals/Code/Tools/WorldBuilder/include/BuildList.h

## Purpose
Header for the BuildList dialog class used in WorldBuilder for managing building placement and properties.

## Responsibilities
- Manages building list UI for WorldBuilder
- Handles building selection, ordering, and properties
- Provides sliders for height and angle adjustments
- Supports export functionality for building lists

## Key Types
- **BuildList (Class)**: Main dialog class for building list management
- **WorldHeightMapEdit (Class)**: External dependency for terrain editing
- **BuildListInfo (Class)**: External dependency for building list data
- **(anonymous enum)**: Contains NAME_MAX_LEN constant
- **(anonymous enum)**: Contains IDD constant

## Key Functions
### BuildList::OnInitDialog
- Purpose: Initializes the dialog UI
- Calls: loadSides

### BuildList::OnSelchangeSidesCombo
- Purpose: Handles side selection changes
- Calls: updateCurSide

### BuildList::addBuilding
- Purpose: Adds a building to the list
- Calls: None

### BuildList::update
- Purpose: Updates the building list display
- Calls: loadSides

### BuildList::GetPopSliderInfo
- Purpose: Provides slider configuration information
- Calls: None

### BuildList::PopSliderChanged
- Purpose: Handles slider value changes
- Calls: None

### BuildList::PopSliderFinished
- Purpose: Handles slider value finalization
- Calls: None

## Globals
- **m_staticThis (BuildList*)**: Static pointer to the dialog instance
- **m_updating (Bool)**: Flag indicating if updates are in progress

## Dependencies
- "TerrainSwatches.h"
- "OptionsPanel.h"
- "WBPopupSlider.h"
- "Common/AsciiString.h"
- MFC classes (CWnd
