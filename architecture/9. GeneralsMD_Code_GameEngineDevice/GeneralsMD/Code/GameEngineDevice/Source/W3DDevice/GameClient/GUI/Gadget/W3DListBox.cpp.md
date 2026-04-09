# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DListBox.cpp

## Purpose
Implements the W3D (Westwood 3D) rendering for list box GUI controls in the game engine.

## Responsibilities
- Renders list box backgrounds and selection highlights
- Handles text and image drawing within list box items
- Manages clipping regions for proper display within bounds
- Supports both colored and image-based list box styles
- Draws scroll bars and handles multi-column layouts

## Key Types
- `ListboxData` (Struct): Stores list box state including items, selections, and display parameters
- `ListEntryCell` (Struct): Represents individual cells within list box items (text or images)
- `Image` (Class): Used for drawing image-based list box backgrounds and selection highlights

## Key Functions
### `drawHiliteBar`
- Purpose: Draws the selection highlight bar using left/right/center/smallCenter images
- Calls: `TheWindowManager->winDrawImage`, `TheDisplay->setClipRegion`, `TheDisplay->enableClipping`

### `drawListBoxText`
- Purpose: Renders all text and images within the list box items, handling selection highlights and clipping
- Calls: `TheWindowManager->winDrawImage`, `TheWindowManager->winOpenRect`, `TheWindowManager->winFillRect`, `TheDisplay->setClipRegion`, `TheDisplay->enableClipping`, `DisplayString::draw`

### `W3DGadgetListBoxDraw`
- Purpose: Main entry point for drawing colored list boxes with standard graphics
- Calls: `drawListBoxText`, `GadgetListBoxGetDisabledColor`, `GadgetListBoxGetHiliteColor`, `GadgetListBoxGetEnabledColor`, etc.

### `W3DGadgetListBoxImageDraw`
- Purpose: Main entry point for drawing list boxes with user-supplied background images
- Calls: `drawListBoxText`, `GadgetListBoxGetDisabledImage`, `GadgetListBoxGetHiliteImage`, `GadgetListBoxGetEnabledImage`

## Globals
- `TheWindowManager` (GameWindowManager*): Global window manager instance
- `TheDisplay` (W3DDisplay*): Global display device instance

## Dependencies
- `GameClient/GameWindowGlobal.h`
- `GameClient/GameWindowManager.h`
- `GameClient/GadgetListBox.h`
- `W3DDevice/GameClient/W3DGadget.h`
- `W3DDevice/GameClient/W3DDisplay.h`
- Uses `DisplayString`, `Image`, `GameWindow`, `WinInstanceData` classes from other modules
