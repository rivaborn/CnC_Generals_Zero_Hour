# GeneralsMD/Code/GameEngine/Include/GameClient/GadgetSlider.h

## Purpose
Header file defining helper functions for slider gadgets in the game UI.

## Responsibilities
- Provides inline functions for slider manipulation (position, images, colors)
- Manages slider thumb properties (images, colors, borders)
- Supports enabled/disabled/hilite states for sliders and thumbs
- Handles min/max value retrieval for sliders

## Key Types
- (anonymous enum): Contains `HORIZONTAL_SLIDER_THUMB_POSITION` constant
- HORIZONTAL_SLIDER_THUMB_POSITION (Enum): Defines thumb position for horizontal sliders

## Key Functions
### GadgetSliderGetMinMax
- Purpose: Retrieves min/max values for a slider
- Calls: Accesses `SliderData` from window user data

### GadgetSliderGetThumb
- Purpose: Returns the thumb child window of a slider
- Calls: `winGetChild()`

### GadgetSliderSetPosition
- Purpose: Sets the slider position
- Calls: `TheWindowManager->winSendSystemMsg()`

### GadgetSliderGetPosition
- Purpose: Gets the current slider position
- Calls: Accesses `SliderData` from window user data

### GadgetSliderSetEnabledImages
- Purpose: Sets enabled state images for slider components
- Calls: `winSetEnabledImage()`

### GadgetSliderSetEnabledThumbImage
- Purpose: Sets enabled state image for slider thumb
- Calls: `GadgetButtonSetEnabledImage()`

### GadgetSliderGetEnabledThumbImage
- Purpose: Gets enabled state image for slider thumb
- Calls: `GadgetButtonGetEnabledImage()`

## Globals
- `HORIZONTAL_SLIDER_THUMB_POSITION` (Int): Predefined thumb position value

## Dependencies
- `GameWindow.h`, `GameWindowManager.h`, `GadgetPushButton.h`, `Gadget.h`, `Image.h`
- `SliderData` struct (forward reference)
- `GadgetButtonSet/Get*` functions
- `TheWindowManager` global instance
