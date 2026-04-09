# Generals/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetListBox.cpp

## Purpose
Implements the list box GUI control for the game, handling display, selection, and input for lists of items.

## Responsibilities
- Manages list box rendering and scrolling
- Handles single/multi selection modes
- Processes user input (mouse/keyboard)
- Maintains list item data and layout

## Key Types
- `AddMessageStruct` (struct): Holds parameters for adding list entries
- `TextAndColor` (struct): Stores text and its color
- `ListboxData` (struct): Main list box data structure (defined elsewhere)
- `ListEntryRow` (struct): Represents a row in the list (defined elsewhere)
- `ListEntryCell` (struct): Represents a cell in a row (defined elsewhere)

## Key Functions
### `doAudioFeedback`
- Purpose: Plays audio feedback when list box is interacted with
- Calls: `TheAudio->addAudioEvent`

### `getListboxEntryBasedOnCoord`
- Purpose: Determines which list entry is at given screen coordinates
- Calls: `window->winGetScreenPosition`, `TheWindowManager->winFontHeight`

### `adjustDisplay`
- Purpose: Updates display position and scrollbar when list changes
- Calls: `getListboxTopEntry`, `TheWindowManager->winSendSystemMsg`

### `computeTotalHeight`
- Purpose: Calculates total height of all list entries
- Calls: `TheWindowManager->winFontHeight`, `TheDisplayStringManager->freeDisplayString`

### `addImageEntry`
- Purpose: Adds an image entry to the list at specified position
- Calls: `computeTotalHeight`

### `GadgetListBoxInput`
- Purpose: Handles single-selection list box input
- Calls: `doAudioFeedback`, `getListboxEntryBasedOnCoord`, `adjustDisplay`

### `GadgetListBoxMultiInput`
- Purpose: Handles multi-selection list box input
- Calls: `doAudioFeedback`, `getListboxEntryBasedOnCoord`, `adjustDisplay`

### `GadgetListBoxSetListLength`
- Purpose: Resizes the list box to accommodate new length
- Calls: `TheDisplayStringManager->freeDisplayString`, `computeTotalHeight`

## Globals
- `doubleClickTime` (UnsignedInt): Stores system double-click time setting

## Dependencies
- `PreRTS.h`, `Common/AudioEventRTS.h`, `Common/Language.h`, `Common/Debug.h`, `Common/GameAudio.h`
- `GameClient/DisplayStringManager.h`, `GameClient/GameWindow.h`, `GameClient/Gadget.h`
- `GameClient/GameWindowManager.h`, `GameClient/GadgetListBox.h`, `GameClient/GadgetPushButton.h`
- `GameClient/GadgetSlider.h`, `GameClient/GameWindowGlobal.h`, `GameClient/Keyboard.h`
- Uses `TheWindowManager`, `TheDisplayStringManager`, `TheAudio` global instances
