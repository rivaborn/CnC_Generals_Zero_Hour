# GeneralsMD/Code/GameEngine/Include/GameClient/GadgetListBox.h

## Purpose
Header file defining the interface for list box gadgets in the game's UI system.

## Responsibilities
- Declares functions for managing list box contents (entries, selection, data)
- Provides accessors for list box properties (colors, images, visibility)
- Defines helper structs for list box operations
- Exposes scrollbar and button management functions

## Key Types
- **RightClickStruct (struct)**: Stores mouse coordinates and position for right-click handling

## Key Functions
### GadgetListBoxGetEntryBasedOnXY
- Purpose: Determines list box entry at given screen coordinates
- Calls: Not inferable

### GadgetListBoxAddEntryText/Image
- Purpose: Adds text or image entries to the list box
- Calls: Not inferable

### GadgetListBoxSetSelected/GetSelected
- Purpose: Manages selection state of list box entries
- Calls: Not inferable

### GadgetListBoxSetColors
- Purpose: Configures all visual colors for the list box
- Calls: Not inferable

### GadgetListBoxGetSlider/UpButton/DownButton
- Purpose: Retrieves child gadgets (scrollbar and buttons)
- Calls: winGetUserData()

## Globals
- None

## Dependencies
- GameClient/Gadget.h
- GameClient/GameWindow.h
- Uses GameWindow, GameFont, Image, Color, UnicodeString types
