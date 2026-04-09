# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DPushButton.cpp

## Purpose
Implements rendering logic for push button UI elements in the W3D (Westwood 3D) device layer.

## Responsibilities
- Renders push buttons with either solid colors or custom images
- Handles different button states (enabled/disabled, hilited/selected)
- Draws button text with appropriate colors and positioning
- Supports overlay images, clocks, and borders
- Manages three-part button images (left/center/right)

## Key Types
- `PushButtonData` (struct): Stores button-specific data like overlay images and clock settings
- `DisplayString` (class): Handles text rendering for buttons
- `Image` (class): Represents button images

## Key Functions
### `drawButtonText`
- Purpose: Renders button text with appropriate colors based on state
- Calls: `text->setWordWrapCentered`, `text->setWordWrap`, `text->getSize`, `text->draw`

### `W3DGadgetPushButtonDraw`
- Purpose: Draws colored push buttons using standard graphics
- Calls: `GadgetButtonGetDisabledSelectedColor`, `TheWindowManager->winOpenRect`, `TheWindowManager->winFillRect`, `drawButtonText`, `TheDisplay->drawVideoBuffer`

### `W3DGadgetPushButtonImageDraw`
- Purpose: Draws push buttons with user-supplied images
- Calls: `GadgetButtonGetMiddleEnabledImage`, `W3DGadgetPushButtonImageDrawThree`, `W3DGadgetPushButtonImageDrawOne`

### `W3DGadgetPushButtonImageDrawOne`
- Purpose: Draws buttons using a single image with state overlays
- Calls: `GadgetButtonGetEnabledImage`, `TheDisplay->drawImage`, `drawButtonText`, `TheDisplay->drawRectClock`

### `W3DGadgetPushButtonImageDrawThree`
- Purpose: Draws buttons using three-part images (left/center/right)
- Calls: `GadgetButtonGetLeftDisabledImage`, `TheWindowManager->winDrawImage`, `drawButtonText`, `TheDisplay->setClipRegion`

## Globals
- `TheWindowManager` (GameWindowManager*): Manages window rendering
- `TheDisplay` (Display*): Handles display operations
- `TheMappedImageCollection` (ImageCollection*): Stores button overlay images

## Dependencies
- `GameClient/Gadget.h`
- `GameClient/GadgetPushButton.h`
- `GameClient/Display.h`
- `W3DDevice/GameClient/W3DGameWindow.h`
- `W3DDevice/GameClient/W3DDisplay.h`
- `W3DDevice/GameClient/W3DGadget.h`
