# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DPushButton.cpp

## Purpose
Implements rendering logic for push button UI elements in the W3D (W3DDevice) subsystem.

## Responsibilities
- Renders push buttons with either solid colors or custom images
- Handles different button states (enabled/disabled, hilited/selected)
- Draws button text with appropriate colors
- Supports overlay images, clocks, and borders
- Manages three-part button images (left/center/right)

## Key Types
- **None** (only functions, no classes/structs/enums defined)

## Key Functions
### `drawButtonText`
- Purpose: Renders button text with proper alignment and color based on state
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `text->setWordWrapCentered`, `text->setWordWrap`, `window->winGetStatus`, `window->winGetDisabledTextColor`, `window->winGetDisabledTextBorderColor`, `window->winGetHiliteTextColor`, `window->winGetHiliteTextBorderColor`, `window->winGetEnabledTextColor`, `window->winGetEnabledTextBorderColor`, `text->getFont`, `window->winGetFont`, `text->getSize`, `text->draw`

### `W3DGadgetPushButtonDraw`
- Purpose: Draws colored push buttons using standard graphics primitives
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `GadgetButtonGetDisabledSelectedColor`, `GadgetButtonGetDisabledSelectedBorderColor`, `GadgetButtonGetDisabledColor`, `GadgetButtonGetDisabledBorderColor`, `GadgetButtonGetHiliteSelectedColor`, `GadgetButtonGetHiliteSelectedBorderColor`, `GadgetButtonGetHiliteColor`, `GadgetButtonGetHiliteBorderColor`, `GadgetButtonGetEnabledSelectedColor`, `GadgetButtonGetEnabledSelectedBorderColor`, `GadgetButtonGetEnabledColor`, `GadgetButtonGetEnabledBorderColor`, `TheWindowManager->winOpenRect`, `TheWindowManager->winFillRect`, `drawButtonText`, `TheDisplay->drawVideoBuffer`, `window->winGetUserData`, `TheDisplay->drawImage`, `TheDisplay->drawRectClock`, `TheDisplay->drawRemainingRectClock`, `window->winSetUserData`, `TheDisplay->drawOpenRect`

### `W3DGadgetPushButtonImageDraw`
- Purpose: Dispatches to either single-image or three-part image drawing based on button configuration
- Calls: `GadgetButtonGetMiddleEnabledImage`, `window->winGetScreenPosition`, `window->winGetSize`, `DEBUG_CRASH`, `W3DGadgetPushButtonImageDrawOne`, `W3DGadgetPushButtonImageDrawThree`

### `W3DGadgetPushButtonImageDrawOne`
- Purpose: Renders buttons using a single image with state-specific overlays
- Calls: `GadgetButtonGetEnabledImage`, `window->winGetStatus`, `GadgetButtonGetDisabledSelectedImage`, `GadgetButtonGetDisabledImage`, `GadgetButtonGetHiliteSelectedImage`, `GadgetButtonGetHiliteImage`, `window->winGetScreenPosition`, `window->winGetSize`, `TheDisplay->drawImage`, `drawButtonText`, `TheDisplay->drawVideoBuffer`, `window->winGetUserData`, `TheDisplay->drawImage`, `TheDisplay->drawRectClock`, `TheDisplay->drawRemainingRectClock`, `window->winSetUserData`,
