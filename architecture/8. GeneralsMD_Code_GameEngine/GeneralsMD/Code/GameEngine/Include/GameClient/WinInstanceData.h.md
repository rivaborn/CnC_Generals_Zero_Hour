# GeneralsMD/Code/GameEngine/Include/GameClient/WinInstanceData.h

## Purpose
Defines data structures and class for managing game window instances, including text, images, and state.

## Responsibilities
- Stores window instance data (text, images, state, fonts)
- Manages tooltip and display text
- Provides accessors for window properties
- Handles video buffer assignment for window content

## Key Types
- **WinDrawData (struct)**: Stores image and color data for window states
- **TextDrawData (struct)**: Stores text color and border color data
- **WinInstanceData (class)**: Main class managing window instance data
- **GameWindow (class)**: Forward reference to window owner
- **VideoBuffer (class)**: Forward reference to video buffer

## Key Functions
### WinInstanceData::setTooltipText
- Purpose: Sets the tooltip text for the window
- Calls: None

### WinInstanceData::setText
- Purpose: Sets the display text for the window
- Calls: None

### WinInstanceData::setVideoBuffer
- Purpose: Assigns a video buffer to the window for video playback
- Calls: None

## Globals
- **MAX_WINDOW_NAME_LEN (enum)**: Maximum length for window name (64)
- **MAX_DRAW_DATA (enum)**: Maximum draw data elements (9)
- **MAX_TEXT_LABEL (enum)**: Maximum text label length (128)
- **WIN_STATE_HILITED (macro)**: Window state flag for mouse hover/focus
- **WIN_STATE_SELECTED (macro)**: Window state flag for selection

## Dependencies
- **GameClient/DisplayString.h**: For text display handling
- **GameClient/GameFont.h**: For font management
- **GameClient/Image.h**: For image handling
- **UnicodeString**: Used for text storage
- **AsciiString**: Used for string storage
- **Color**: Used for color data
- **ICoord2D**: Used for image offset
