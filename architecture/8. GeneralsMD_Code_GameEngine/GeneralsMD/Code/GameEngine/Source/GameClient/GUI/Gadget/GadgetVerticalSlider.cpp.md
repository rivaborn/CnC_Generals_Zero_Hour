# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetVerticalSlider.cpp

## Purpose
Handles input and system messages for a vertical slider GUI control in the game.

## Responsibilities
- Processes mouse and keyboard input for vertical slider interaction
- Manages slider position and range updates
- Handles slider drag, click, and keyboard navigation
- Sends slider position change notifications to parent window
- Manages slider thumb (child window) positioning

## Key Types
- **SliderData (struct)**: Contains slider state (position, min/max values, tick size)
- **GameWindow (class)**: Base window class for GUI elements
- **WinInstanceData (class)**: Window instance data container

## Key Functions
### GadgetVerticalSliderInput
- Purpose: Handles user input for vertical slider
- Calls: TheWindowManager->winSendSystemMsg, window->winGetChild, window->winSetPosition, window->winNextTab, window->winPrevTab

### GadgetVerticalSliderSystem
- Purpose: Handles system messages for vertical slider
- Calls: TheWindowManager->winSendSystemMsg, window->winGetChild, window->winSetPosition, window->winGetSize, window->winGetScreenPosition

## Globals
- None

## Dependencies
- PreRTS.h (must be first include)
- Common/Language.h
- Gameclient/GameWindowManager.h
- GameClient/Gadget.h
- Uses TheWindowManager global instance
- Uses various window message constants (GWM_*, GSM_*, GBM_*)
