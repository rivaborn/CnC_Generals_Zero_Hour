# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/ListboxProperties.cpp

## Purpose
Handles the listbox properties dialog in the GUI editor tool, allowing users to modify listbox appearance and behavior.

## Responsibilities
- Manages scrollbar creation/removal for listboxes
- Handles dialog callbacks for listbox property modifications
- Initializes the listbox properties dialog with current values
- Updates listbox visual states (enabled/disabled/highlighted)
- Configures multi-select, word-wrap, and column settings

## Key Types
- `ListboxData` (struct): Stores listbox configuration (scrollbar, multi-select, etc.)
- `ImageAndColorInfo` (struct): Holds image and color data for UI elements
- `GameWindow` (class): Base window class for UI elements

## Key Functions
### `addScrollbar`
- Purpose: Adds scrollbar components to a listbox
- Calls: `GadgetListboxCreateScrollbar`, `GadgetListBoxGet*`, `GadgetButtonSet*`, `GadgetSliderSet*`, `TheDefaultScheme->getImageAndColor`

### `removeScrollbar`
- Purpose: Removes scrollbar components from a listbox
- Calls: `TheWindowManager->winDestroy`

### `listboxPropertiesCallback`
- Purpose: Handles dialog messages for listbox property modifications
- Calls: `HandleCommonDialogMessages`, `GetStateInfo`, `StoreColor`, `GadgetListBoxSet*`, `GadgetListBoxGet*`, `GadgetListBoxAddMultiSelect`, `GadgetListBoxRemoveMultiSelect`

### `InitListboxPropertiesDialog`
- Purpose: Initializes and displays the listbox properties dialog
- Calls: `CreateDialog`, `CommonDialogInitialize`, `StoreImageAndColor`, `GadgetListBoxGet*`, `GadgetButtonGet*`, `GadgetSliderGet*`, `SwitchToState`

## Globals
- `TheEditor` (Editor): Access to editor instance
- `TheWindowManager` (WindowManager): Window management interface
- `TheDefaultScheme` (LayoutScheme): Default UI layout scheme

## Dependencies
- `GUIEdit.h`, `Properties.h`, `LayoutScheme.h`, `Resource.h`
- `GameClient/GadgetListBox.h`, `GameClient/GadgetPushButton.h`, `Gameclient/GadgetSlider.h`, `GameClient/GameWindowManager.h`
- Windows API (HWND, WM_COMMAND, etc.)
- SAGE engine UI classes (GameWindow, ImageAndColorInfo)
