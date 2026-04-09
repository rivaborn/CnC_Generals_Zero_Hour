# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DHorizontalSlider.cpp

## Purpose
Implements rendering functions for horizontal slider UI gadgets in the SAGE engine.

## Responsibilities
- Draws colored horizontal sliders using standard graphics
- Renders sliders with user-supplied images
- Handles different visual states (enabled/disabled/highlighted)
- Manages image scaling and positioning for sliders

## Key Types
- None

## Key Functions
### W3DGadgetHorizontalSliderDraw
- Purpose: Draws a colored horizontal slider using standard graphics
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `GadgetSliderGetDisabledBorderColor`, `GadgetSliderGetDisabledColor`, `GadgetSliderGetHiliteBorderColor`, `GadgetSliderGetHiliteColor`, `GadgetSliderGetEnabledBorderColor`, `GadgetSliderGetEnabledColor`, `TheWindowManager->winOpenRect`, `TheWindowManager->winFillRect`

### W3DGadgetHorizontalSliderImageDraw
- Purpose: Draws a horizontal slider with user-supplied images
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `GadgetSliderGetHiliteImageLeft`, `GadgetSliderGetDisabledImageRight`, `GadgetSliderGetDisabledImageLeft`, `window->winGetUserData`, `TheDisplay->getWidth`, `TheWindowManager->winDrawImage`

### W3DGadgetHorizontalSliderImageDrawB
- Purpose: Draws a horizontal slider with user-supplied images (alternative implementation)
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `window->winGetUserData`, `TheDisplay->getWidth`, `TheDisplay->getHeight`, `GadgetSliderGetHiliteImageLeft`, `GadgetSliderGetDisabledImageLeft`, `GadgetSliderGetDisabledImageRight`, `TheWindowManager->winDrawImage`, `instData->setTooltipText`

### W3DGadgetHorizontalSliderImageDrawA
- Purpose: Draws a horizontal slider with user-supplied images (advanced implementation with clipping)
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `window->winGetUserData`, `GadgetSliderGetDisabledImageLeft`, `GadgetSliderGetDisabledImageRight`, `GadgetSliderGetHiliteImageLeft`, `GadgetSliderGetHiliteImageRight`, `GadgetSliderGetHiliteImageCenter`, `GadgetSliderGetHiliteImageSmallCenter`, `GadgetSliderGetEnabledImageLeft`, `GadgetSliderGet
