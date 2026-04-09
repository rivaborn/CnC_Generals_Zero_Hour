# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetTabControl.cpp

## Purpose
Implements the tab control GUI gadget, handling input, layout, and sub-pane management.

## Responsibilities
- Processes user input for tab selection
- Manages tab layout and sub-pane visibility
- Handles system messages (creation, destruction, resizing)
- Creates and resizes sub-panes dynamically
- Maintains tab control state and orientation

## Key Types
- `TabControlData` (struct): Stores tab control configuration and state
- `GadgetTabControlInput`: Handles user input for tab switching
- `GadgetTabControlSystem`: Processes system messages for the tab control

## Key Functions
### GadgetTabControlInput
- Purpose: Handles mouse input for tab selection
- Calls: `GadgetTabControlShowSubPane`, `tabControl->winGetScreenPosition`

### GadgetTabControlSystem
- Purpose: Processes system messages (create, destroy, resize)
- Calls: `GadgetTabControlResizeSubPanes`, `GadgetTabControlComputeTabRegion`, `TheWindowManager->winSendSystemMsg`

### GadgetTabControlComputeTabRegion
- Purpose: Calculates tab positions based on control dimensions
- Calls: `tabControl->winGetSize`

### GadgetTabControlComputeSubPaneSize
- Purpose: Computes sub-pane dimensions and position
- Calls: `tabControl->winGetSize`

### GadgetTabControlShowSubPane
- Purpose: Shows the selected sub-pane and hides others
- Calls: `tabData->subPanes[paneIndex]->winHide`

### GadgetTabControlCreateSubPanes
- Purpose: Creates or updates sub-panes for the tab control
- Calls: `GadgetTabControlComputeSubPaneSize`, `GadgetTabControlShowSubPane`, `TheWindowManager->winCreate`

### GadgetTabControlResizeSubPanes
- Purpose: Resizes sub-panes when the control is resized
- Calls: `GadgetTabControlComputeSubPaneSize`

### GadgetTabControlFixupSubPaneList
- Purpose: Links child windows to the sub-pane array
- Calls: `tabControl->winGetChild`

## Globals
- `TheWindowManager` (GameWindowManager*): Used to create windows and send messages

## Dependencies
- `GameWindow`, `TabControlData` from `GadgetTabControl.h`
- `GameWindowManager` from `GameWindowManager.h`
- `Gadget.h` for base gadget functionality
- `Language.h` for localization support
