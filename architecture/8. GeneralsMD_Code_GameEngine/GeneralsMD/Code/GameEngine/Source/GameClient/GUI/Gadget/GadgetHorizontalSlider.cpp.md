# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetHorizontalSlider.cpp

## Purpose
Implements input and system message handling for a horizontal slider GUI gadget.

## Responsibilities
- Handles mouse and keyboard input for slider interaction
- Manages slider position and value calculations
- Processes system messages for slider state changes
- Updates slider thumb position visually
- Communicates slider changes to parent window

## Key Types
- **SliderData (struct)**: Stores slider state (position, min/max values, ticks)
- **GadgetHorizontalSliderInput (function)**: Input message handler
- **GadgetHorizontalSliderSystem (function)**: System message handler

## Key Functions
### GadgetHorizontalSliderInput
- Purpose: Handles user input (mouse/keyboard) for horizontal slider
- Calls: `winGetUserData`, `winGetInstanceData`, `winGetSize`, `winGetOwner`, `winSendSystemMsg`, `winGetChild`, `winGetStyle`, `winGetInstanceData`, `winGetPosition`, `winSetPosition`, `winNextTab`, `winPrevTab`

### GadgetHorizontalSliderSystem
- Purpose: Processes system messages for horizontal slider behavior
- Calls: `winGetUserData`, `winGetInstanceData`, `winGetSize`, `winGetChild`, `winGetScreenPosition`, `winGetPosition`, `winSetPosition`, `winSendSystemMsg`, `winGetWindowId`

## Globals
- **HORIZONTAL_SLIDER_THUMB_POSITION (const)**: Y-position for slider thumb
- **HORIZONTAL_SLIDER_THUMB_WIDTH (const)**: Width of slider thumb

## Dependencies
- `PreRTS.h`, `Language.h`, `GameWindowManager.h`, `Gadget.h`, `GadgetSlider.h`
- `GameWindow`, `WinInstanceData`, `ICoord2D` types
- `TheWindowManager` global instance
- Message constants: `GWM_MOUSE_ENTERING`, `GWM_MOUSE_LEAVING`, `GWM_LEFT_DRAG`, `GWM_LEFT_DOWN`, `GWM_LEFT_UP`, `GWM_CHAR`, `GWM_CREATE`, `GWM_DESTROY`, `GWM_INPUT_FOCUS`, `GGM_LEFT_DRAG`, `GSM_SET_SLIDER`, `GSM_SET_MIN_MAX`, `GGM_RESIZED`, `GSM_SLIDER_TRACK`, `GGM_FOCUS_CHANGE`, `GGM_MOUSE_ENTERING`, `GGM_MOUSE_LEAVING`, `GBM_MOUSE_ENTERING`, `GBM_MOUSE_LEAVING`
- Key constants: `KEY_RIGHT`, `KEY_LEFT`, `KEY_DOWN`, `KEY_TAB`, `KEY_UP
