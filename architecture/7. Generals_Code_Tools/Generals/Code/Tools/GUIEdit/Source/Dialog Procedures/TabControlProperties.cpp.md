# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/TabControlProperties.cpp

## Purpose
Handles the properties dialog for tab control gadgets in the GUI editor.

## Responsibilities
- Manages tab control property dialog creation and callbacks
- Updates tab pane names based on parent tab control name
- Saves/loads tab control visual states (enabled/disabled/highlighted)
- Configures tab layout (orientation, edges, dimensions)

## Key Types
- **TabControlData (struct)**: Stores tab control configuration (width, height, active tab, etc.)
- **ImageAndColorInfo (struct)**: Holds image/color/border data for tab states
- **GameWindow (class)**: Base window class for UI elements

## Key Functions
### GadgetTabControlUpdatePaneNames
- Purpose: Updates sub-pane names based on parent tab control name
- Calls: `winGetUserData`, `winGetInstanceData`, `updateWindowName`

### tabControlPropertiesCallback
- Purpose: Handles dialog messages for tab control properties
- Calls: `HandleCommonDialogMessages`, `SaveCommonDialogProperties`, `GadgetTabControlSet*`, `GetStateInfo`, `GadgetTabControlComputeTabRegion`, `GadgetTabControlResizeSubPanes`, `GadgetTabControlShowSubPane`, `GadgetTabControlUpdatePaneNames`

### InitTabControlPropertiesDialog
- Purpose: Initializes and displays the tab control properties dialog
- Calls: `CreateDialog`, `CommonDialogInitialize`, `GadgetTabControlGet*`, `StoreImageAndColor`, `SetDlgItemInt`, `CheckDlgButton`

## Globals
- None

## Dependencies
- `GameClient/GadgetTabControl.h` (tab control specific functions)
- `GameClient/Gadget.h` (base gadget class)
- `Properties.h` (common dialog handling)
- `HierarchyView.h` (window hierarchy management)
- `Common/NameKeyGenerator.h` (name generation utilities)
