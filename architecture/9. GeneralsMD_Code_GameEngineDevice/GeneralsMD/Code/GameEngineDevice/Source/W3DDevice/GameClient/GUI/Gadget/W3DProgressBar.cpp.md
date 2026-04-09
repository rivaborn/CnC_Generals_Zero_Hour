# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DProgressBar.cpp

## Purpose
Implements rendering for progress bar GUI controls in the W3D (W3D) device layer.

## Responsibilities
- Renders colored progress bars using standard graphics primitives
- Renders progress bars with user-supplied images
- Handles different visual states (enabled, disabled, hilited)
- Manages progress bar drawing with borders, backgrounds, and progress fills

## Key Types
- None

## Key Functions
### W3DGadgetProgressBarDraw
- Purpose: Draws a colored progress bar using standard graphics primitives
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `GadgetProgressBarGetDisabledColor`, `GadgetProgressBarGetDisabledBorderColor`, `GadgetProgressBarGetDisabledBarColor`, `GadgetProgressBarGetDisabledBarBorderColor`, `GadgetProgressBarGetHiliteColor`, `GadgetProgressBarGetHiliteBorderColor`, `GadgetProgressBarGetHiliteBarColor`, `GadgetProgressBarGetHiliteBarBorderColor`, `GadgetProgressBarGetEnabledColor`, `GadgetProgressBarGetEnabledBorderColor`, `GadgetProgressBarGetEnabledBarColor`, `GadgetProgressBarGetEnabledBarBorderColor`, `TheWindowManager->winOpenRect`, `TheWindowManager->winFillRect`, `TheWindowManager->winDrawLine`

### W3DGadgetProgressBarImageDrawA
- Purpose: Draws a progress bar with user-supplied images (simplified version)
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `GadgetProgressBarGetEnabledBarImageCenter`, `GadgetProgressBarGetEnabledBarImageRight`, `GadgetProgressBarGetEnabledImageLeft`, `GadgetProgressBarGetEnabledImageRight`, `GadgetProgressBarGetEnabledImageCenter`, `TheWindowManager->winDrawImage`

### W3DGadgetProgressBarImageDraw
- Purpose: Draws a progress bar with user-supplied images (full version with left/right/center pieces)
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `GadgetProgressBarGetDisabledImageLeft`, `GadgetProgressBarGetDisabledImageRight`, `GadgetProgressBarGetDisabledImageCenter`, `GadgetProgressBarGetDisabledBarImageRight`, `GadgetProgressBarGetDisabledBarImageCenter`, `GadgetProgressBarGetHiliteImageLeft`, `GadgetProgressBarGetHiliteImageRight`, `GadgetProgressBarGetHiliteImageCenter`, `Gadget
