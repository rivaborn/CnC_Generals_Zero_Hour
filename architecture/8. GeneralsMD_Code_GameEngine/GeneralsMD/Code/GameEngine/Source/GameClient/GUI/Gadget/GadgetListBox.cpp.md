# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetListBox.cpp

## Purpose
Implements the list box GUI control for the game, handling display, selection, and input for lists of items.

## Responsibilities
- Manage list box entries (text and images)
- Handle user input (selection, scrolling)
- Maintain scrollbar synchronization
- Support single and multi-selection modes
- Provide API for external manipulation

## Key Types
- `AddMessageStruct` (struct): Holds parameters for adding entries to the list
- `TextAndColor` (struct): Stores text and its color
- `ListboxData` (struct): Internal list box state (not shown in symbols)
- `ListEntryRow` (struct): Represents a row in the list (not shown in symbols)
- `ListEntryCell` (struct): Represents a cell in a row (not shown in symbols)

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
- Purpose: Calculates total height of all entries and individual row heights
- Calls: `TheWindowManager->winFontHeight`, `TheDisplayStringManager->freeDisplayString`

### `GadgetListBoxInput`
- Purpose: Handles single-selection input events
- Calls: `doAudioFeedback`, `getListboxEntryBasedOnCoord`, `adjustDisplay`

### `GadgetListBoxMultiInput`
- Purpose: Handles multi-selection input events
- Calls: `doAudioFeedback`, `getListboxEntryBasedOnCoord`, `adjustDisplay`

### `GadgetListBoxAddEntryText`
- Purpose: Adds a text entry to the list box
- Calls: `TheDisplayStringManager->createDisplayString`

### `GadgetListBoxAddEntryImage`
- Purpose: Adds an image entry to the list box
- Calls: `addImageEntry`

## Globals
- `doubleClickTime` (UnsignedInt): Stores system double-click time setting

## Dependencies
- `PreRTS.h`, `Common/AudioEventRTS.h`, `Common/Language.h`, `Common/Debug.h`, `Common/GameAudio.h`
- `GameClient/DisplayStringManager.h`, `GameClient/GameWindow.h`, `GameClient/Gadget.h`
- `GameClient/GameWindowManager.h`, `GameClient/GadgetListBox.h`, `GameClient/GadgetPushButton.h`
- `GameClient/GadgetSlider.h`, `GameClient/GameWindowGlobal.h`, `GameClient/Keyboard.h`
- External symbols: `TheAudio`, `TheWindowManager`, `TheDisplayStringManager`
