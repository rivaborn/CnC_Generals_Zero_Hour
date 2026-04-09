# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DVerticalSlider.cpp

## Purpose
Implements rendering logic for vertical slider gadgets in the game UI.

## Responsibilities
- Draws colored vertical sliders using standard graphics
- Draws vertical sliders with user-supplied images
- Handles different visual states (enabled, disabled, hilited)
- Manages image tiling and positioning for complex slider backgrounds

## Key Types
None

## Key Functions
### W3DGadgetVerticalSliderDraw
- Purpose: Draws a colored vertical slider using standard graphics
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `GadgetSliderGetDisabledBorderColor`, `GadgetSliderGetDisabledColor`, `GadgetSliderGetHiliteBorderColor`, `GadgetSliderGetHiliteColor`, `GadgetSliderGetEnabledBorderColor`, `GadgetSliderGetEnabledColor`, `TheWindowManager->winOpenRect`, `TheWindowManager->winFillRect`

### W3DGadgetVerticalSliderImageDraw
- Purpose: Draws a vertical slider with user-supplied images, handling tiling and positioning
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `GadgetSliderGetDisabledImageTop`, `GadgetSliderGetDisabledImageBottom`, `GadgetSliderGetDisabledImageCenter`, `GadgetSliderGetDisabledImageSmallCenter`, `GadgetSliderGetHiliteImageTop`, `GadgetSliderGetHiliteImageBottom`, `GadgetSliderGetHiliteImageCenter`, `GadgetSliderGetHiliteImageSmallCenter`, `GadgetSliderGetEnabledImageTop`, `GadgetSliderGetEnabledImageBottom`, `GadgetSliderGetEnabledImageCenter`, `GadgetSliderGetEnabledImageSmallCenter`, `TheWindowManager->winDrawImage`

## Globals
None

## Dependencies
- `GameClient/GadgetSlider.h`
- `GameClient/GameWindowGlobal.h`
- `GameClient/GameWindowManager.h`
- `W3DDevice/GameClient/W3DGadget.h`
- `W3DDevice/GameClient/W3DDisplay.h`
- `TheWindowManager` (external symbol)
- `WinInstanceData` (external type)
- `GameWindow` (external type)
- `Color` (external type)
- `ICoord2D` (external type)
- `Image` (external type)
