# Generals/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetVerticalSlider.cpp

## Purpose
Handles input and system messages for a vertical slider GUI control in the game.

## Responsibilities
- Processes mouse and keyboard input for vertical slider interaction
- Manages slider position and range updates
- Handles slider drag, click, and keyboard navigation
- Sends slider position change notifications to parent window
- Manages slider child (thumb) positioning and sizing

## Key Types
- **SliderData (struct)**: Contains slider position, min/max values, and tick spacing
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
- PreRTS.h, Language.h, GameWindowManager.h, Gadget.h
- TheWindowManager (external)
- GWM_*, GBM_*, GSM_*, GGM_* message constants
- WindowMsgHandledType, GameWindow, SliderData types
