# Generals/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetTabControl.cpp

## Purpose
Implements a tab control GUI gadget for the game, handling input, layout, and sub-pane management.

## Responsibilities
- Processes user input for tab switching
- Manages tab layout and sub-pane visibility
- Handles system messages (creation, destruction, resizing)
- Creates and resizes sub-panes dynamically
- Maintains tab control state and child window relationships

## Key Types
- **TabControlData (struct)**: Stores tab control configuration (tab positions, active tab, sub-pane references)
- **None**: No classes defined in this file

## Key Functions
### GadgetTabControlInput
- Purpose: Handles mouse input for tab switching
- Calls: GadgetTabControlShowSubPane

### GadgetTabControlSystem
- Purpose: Processes system messages for the tab control
- Calls: GadgetTabControlResizeSubPanes, GadgetTabControlComputeTabRegion, TheWindowManager->winSendSystemMsg

### GadgetTabControlComputeTabRegion
- Purpose: Calculates tab positions based on control dimensions and configuration
- Calls: None

### GadgetTabControlComputeSubPaneSize
- Purpose: Determines sub-pane dimensions and position
- Calls: None

### GadgetTabControlShowSubPane
- Purpose: Shows the selected sub-pane and hides others
- Calls: None

### GadgetTabControlCreateSubPanes
- Purpose: Creates or updates sub-panes for the tab control
- Calls: GadgetTabControlComputeSubPaneSize, GadgetTabControlShowSubPane, TheWindowManager->winCreate

### GadgetTabControlResizeSubPanes
- Purpose: Resizes existing sub-panes when control is resized
- Calls: GadgetTabControlComputeSubPaneSize

### GadgetTabControlFixupSubPaneList
- Purpose: Maps child windows to sub-pane array during initialization
- Calls: None

## Globals
- **None**: No global/static variables defined

## Dependencies
- **Includes**: PreRTS.h, Language.h, GameWindowManager.h, Gadget.h, GadgetTabControl.h
- **External Symbols**: TheWindowManager, WIN_STATUS_NONE, WIN_STATUS_ENABLED, GWS_TAB_PANE, PassSelectedButtonsToParentSystem, GWM_LEFT_DOWN, GWM_CREATE, GWM_DESTROY, GGM_RESIZED, GBM_SELECTED, MSG_HANDLED, MSG_IGNORED, NUM_TAB_PANES
