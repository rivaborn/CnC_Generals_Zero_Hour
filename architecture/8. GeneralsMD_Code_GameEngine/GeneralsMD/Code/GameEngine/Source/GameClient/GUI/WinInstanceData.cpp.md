# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/WinInstanceData.cpp

## Purpose
Manages instance data for game window elements, including text, tooltips, and visual states.

## Responsibilities
- Handles allocation and cleanup of display strings for text and tooltips
- Manages visual state data (enabled/disabled/highlighted)
- Provides methods to set text, tooltips, and video buffers
- Initializes default values for window instance properties

## Key Types
- `WinInstanceData` (Class): Container for window element data (text, tooltips, visual states)
- `DrawData` (Struct): Stores image and color data for different states
- `TextData` (Struct): Stores color data for text rendering

## Key Functions
### `WinInstanceData::init`
- Purpose: Resets all instance data to default values
- Calls: `TheDisplayStringManager->freeDisplayString`

### `WinInstanceData::setTooltipText`
- Purpose: Sets the tooltip text for the window element
- Calls: `TheDisplayStringManager->newDisplayString`, `m_tooltip->setText`

### `WinInstanceData::setText`
- Purpose: Sets the display text for the window element
- Calls: `TheDisplayStringManager->newDisplayString`, `m_text->setText`

### `WinInstanceData::setVideoBuffer`
- Purpose: Assigns a video buffer to the window element
- Calls: None

## Globals
- `TheDisplayStringManager` (External): Manages display string allocation/freeing

## Dependencies
- `GameClient/WinInstanceData.h`
- `GameClient/GameWindow.h`
- `GameClient/DisplayStringManager.h`
- `Common/Debug.h`
- `PreRTS.h`
