# Generals/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetHorizontalSlider.cpp

## Purpose
Handles input and system messages for a horizontal slider GUI gadget.

## Responsibilities
- Processes mouse and keyboard input for slider interaction
- Manages slider position and value updates
- Handles slider resizing and focus changes
- Communicates slider state to parent window

## Key Types
- `SliderData` (struct): Stores slider position, min/max values, and tick spacing
- `GameWindow` (class): Base window class for GUI elements
- `WinInstanceData` (class): Window instance data container

## Key Functions
### GadgetHorizontalSliderInput
- Purpose: Handles user input for horizontal slider
- Calls: `winGetUserData`, `winGetInstanceData`, `winGetSize`, `winGetChild`, `winGetStyle`, `winGetOwner`, `winSendSystemMsg`, `winSetFocus`, `winGetScreenPosition`, `winSetPosition`, `winNextTab`, `winPrevTab`

### GadgetHorizontalSliderSystem
- Purpose: Handles system messages for horizontal slider
- Calls: `winGetUserData`, `winGetInstanceData`, `winGetSize`, `winGetChild`, `winGetScreenPosition`, `winGetPosition`, `winSetPosition`, `winSendSystemMsg`, `winGetWindowId`

## Globals
- `HORIZONTAL_SLIDER_THUMB_WIDTH` (const): Width of slider thumb
- `HORIZONTAL_SLIDER_THUMB_POSITION` (const): Y position of slider thumb

## Dependencies
- `PreRTS.h`, `Language.h`, `GameWindowManager.h`, `Gadget.h`, `GadgetSlider.h`
- `TheWindowManager` (global instance)
- Various window message constants (GWM_*, GSM_*, GBM_*)
