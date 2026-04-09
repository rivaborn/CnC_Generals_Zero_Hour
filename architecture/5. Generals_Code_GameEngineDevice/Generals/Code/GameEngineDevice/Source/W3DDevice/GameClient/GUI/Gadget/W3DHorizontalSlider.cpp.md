# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DHorizontalSlider.cpp

## Purpose
Implements rendering functions for horizontal slider UI gadgets in the SAGE engine.

## Responsibilities
- Draws colored horizontal sliders using standard graphics
- Renders sliders with user-supplied images
- Handles different visual states (enabled/disabled/highlighted)
- Manages image scaling and positioning for sliders
- Implements three different drawing modes (A, B, and image-based)

## Key Types
- **SliderData (struct)**: Contains slider state (min/max values, position, ticks)
- **ICoord2D (struct)**: 2D coordinate/position data
- **IRegion2D (struct)**: 2D clipping region data

## Key Functions
### W3DGadgetHorizontalSliderDraw
- Purpose: Draws a colored horizontal slider using standard graphics
- Calls: `winGetScreenPosition`, `winGetSize`, `GadgetSliderGetDisabledBorderColor`, `GadgetSliderGetDisabledColor`, `GadgetSliderGetHiliteBorderColor`, `GadgetSliderGetHiliteColor`, `GadgetSliderGetEnabledBorderColor`, `GadgetSliderGetEnabledColor`, `winOpenRect`, `winFillRect`

### W3DGadgetHorizontalSliderImageDraw
- Purpose: Draws a horizontal slider using user-supplied images
- Calls: `winGetScreenPosition`, `winGetSize`, `GadgetSliderGetHiliteImageLeft`, `GadgetSliderGetDisabledImageRight`, `GadgetSliderGetDisabledImageLeft`, `winDrawImage`

### W3DGadgetHorizontalSliderImageDrawB
- Purpose: Alternative image-based slider rendering with debug tooltips
- Calls: `winGetScreenPosition`, `winGetSize`, `GadgetSliderGetHiliteImageLeft`, `GadgetSliderGetDisabledImageLeft`, `GadgetSliderGetDisabledImageRight`, `winDrawImage`, `setTooltipText`

### W3DGadgetHorizontalSliderImageDrawA
- Purpose: Advanced image-based slider rendering with clipping regions
- Calls: `winGetScreenPosition`, `winGetSize`, `GadgetSliderGetDisabledImageLeft`, `GadgetSliderGetDisabledImageRight`, `GadgetSliderGetHiliteImageLeft`, `GadgetSliderGetHiliteImageRight`, `GadgetSliderGetEnabledImageLeft`, `GadgetSliderGetEnabledImageRight`, `winDrawImage`, `setClipRegion`, `enableClipping`

## Globals
- **TheWindowManager (GameWindowManager)**: Manages window/display operations
- **TheDisplay (W3DDisplay)**: Handles
