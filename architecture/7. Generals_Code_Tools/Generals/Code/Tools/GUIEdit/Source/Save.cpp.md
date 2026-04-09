# Generals/Code/Tools/GUIEdit/Source/Save.cpp

## Purpose
Handles saving window layout data to files for the GUI editor tool.

## Responsibilities
- Serializes GameWindow objects and their properties to text files
- Validates window names for length and uniqueness
- Manages file I/O operations for layout files
- Handles special cases for different gadget types (sliders, listboxes, etc.)

## Key Types
- `GameWindow` (Class): Represents a UI window/gadget in the editor
- `WinInstanceData` (Struct): Contains instance-specific data for windows
- `GameWindowEditData` (Struct): Holds editor-specific window data
- `EntryData`/`TabControlData` (Structs): Gadget-specific data containers

## Key Functions
### `saveWindow`
- Purpose: Recursively saves a window and all its children to file
- Calls: `saveType`, `savePosition`, `saveName`, `saveStatus`, `saveStyle`, `saveCallbacks`, `saveFont`, `saveHeaderTemplate`, `saveTooltipText`, `saveTooltipDelay`, `saveText`, `saveTextColor`, `saveDrawData`, `saveGadgetData`

### `saveGadgetData`
- Purpose: Dispatches saving of gadget-specific data based on window style
- Calls: `saveListboxData`, `saveComboBoxData`, `saveRadioButtonData`, `saveSliderData`, `saveStaticTextData`, `saveTextEntryData`, `saveTabControlData`

### `validateNames`
- Purpose: Checks window names for validity (length and uniqueness)
- Calls: `TheEditor->isNameDuplicate`

### `writeLayoutBlock`
- Purpose: Writes layout initialization callbacks to file
- Calls: `TheEditor->getLayoutInit`, `TheEditor->getLayoutUpdate`, `TheEditor->getLayoutShutdown`

## Globals
- `buffer` (char[2048]): Temporary buffer for file output
- `offendingNames` (char[65536]): Stores invalid window names for error reporting

## Dependencies
- `GUIEdit.h`, `Common/Debug.h`, `Common/NameKeyGenerator.h`, `Common/FunctionLexicon.h`
- `GameClient/Display.h`, `GameClient/GameWindow.h`, `GameClient/GameWindowManager.h`
- `GameClient/GadgetRadioButton.h`
- Uses `fprintf`, `fopen`, `fclose` from stdio.h
