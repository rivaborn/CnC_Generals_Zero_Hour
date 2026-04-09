# Generals/Code/Tools/WorldBuilder/src/GroveOptions.cpp

## Purpose
Handles UI and configuration for tree/grove placement options in the WorldBuilder tool.

## Responsibilities
- Manages tree type selection and distribution ratios
- Handles placement restrictions (water/cliff)
- Persists settings via Windows registry
- Populates UI controls with available tree types
- Validates and updates configuration values

## Key Types
- GroveOptions (Class): Main dialog class for grove configuration
- PairNameDisplayName (Struct): Pairs tree name with display name
- VecPairNameDisplayNameIt (Iterator): Iterates over tree name pairs

## Key Functions
### GetDisplayNameFromPair
- Purpose: Retrieves display name from a name pair, falling back to ASCII if Unicode is empty
- Calls: None

### GroveOptions::OnInitDialog
- Purpose: Initializes dialog controls with default values
- Calls: _buildTreeList, _setTreesToLists, _setDefaultRatios, _updateTreeWeights, _setDefaultNumTrees, _setDefaultPlacementAllowed

### GroveOptions::_updateTreeWeights
- Purpose: Updates tree distribution ratios and calculates total
- Calls: AfxGetApp()->WriteProfileInt

### GroveOptions::_updateGroveMakeup
- Purpose: Saves selected tree types to registry
- Calls: AfxGetApp()->WriteProfileInt

## Globals
- TheGroveOptions (GroveOptions*): Singleton instance pointer

## Dependencies
- MFC (CWnd, CDialog, CComboBox, CButton)
- Common/STLTypedefs.h, GroveOptions.h, ThingFactory.h, ThingSort.h, ThingTemplate.h
- Windows registry via AfxGetApp()
- UnicodeString class for string handling
