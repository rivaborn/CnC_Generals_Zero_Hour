# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DListBox.cpp

## Purpose
Implements the rendering logic for W3D list box UI gadgets in the game engine.

## Responsibilities
- Renders list box backgrounds and selection highlights
- Handles text and image drawing within list box items
- Manages clipping regions for proper UI rendering
- Supports both colored and image-based list box styles
- Draws scroll bars and title text for list boxes

## Key Types
- `ListboxData` (Struct): Stores list box configuration and item data
- `ListEntryCell` (Struct): Represents individual cells within list box items
- `Image` (Class): Used for image-based list box rendering

## Key Functions
### `drawHiliteBar`
- Purpose: Renders the selection highlight bar using left/right/center/smallCenter images
- Calls: `TheWindowManager->winDrawImage`, `TheDisplay->setClipRegion`, `TheDisplay->enableClipping`

### `drawListBoxText`
- Purpose: Draws all text and images for list box items, handling selection states and clipping
- Calls: `TheWindowManager->winDrawImage`, `TheWindowManager->winOpenRect`, `TheWindowManager->winFillRect`, `TheDisplay->setClipRegion`, `TheDisplay->enableClipping`

### `W3DGadgetListBoxDraw`
- Purpose: Main rendering function for colored list boxes
- Calls: `drawListBoxText`, `GadgetListBoxGetDisabledColor`, `GadgetListBoxGetHiliteColor`, etc.

### `W3DGadgetListBoxImageDraw`
- Purpose: Main rendering function for image-based list boxes
- Calls: `drawListBoxText`, `GadgetListBoxGetDisabledImage`, `GadgetListBoxGetHiliteImage`, etc.

## Globals
- `TheWindowManager` (GameWindowManager*): Global window manager instance
- `TheDisplay` (W3DDisplay*): Global display device instance

## Dependencies
- `GameClient/GameWindowGlobal.h`
- `GameClient/GameWindowManager.h`
- `GameClient/GadgetListBox.h`
- `W3DDevice/GameClient/W3DGadget.h`
- `W3DDevice/GameClient/W3DDisplay.h`
