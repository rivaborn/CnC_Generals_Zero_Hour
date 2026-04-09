# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DComboBox.cpp

## Purpose
Implements rendering for W3D combo box UI elements, supporting both colored and image-based drawing modes.

## Responsibilities
- Renders combo box UI elements with appropriate colors based on state (enabled/disabled/highlighted)
- Handles title text rendering for combo boxes
- Supports image-based combo box backgrounds with offset positioning
- Manages visual feedback for user interaction states

## Key Types
- None

## Key Functions
### W3DGadgetComboBoxDraw
- Purpose: Renders a combo box with colored background and border
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `TheWindowManager->winFontHeight`, `GadgetComboBoxGetDisabledColor`, `GadgetComboBoxGetDisabledBorderColor`, `window->winGetDisabledTextColor`, `window->winGetDisabledTextBorderColor`, `GadgetComboBoxGetHiliteColor`, `GadgetComboBoxGetHiliteBorderColor`, `window->winGetHiliteTextColor`, `window->winGetHiliteTextBorderColor`, `GadgetComboBoxGetEnabledColor`, `GadgetComboBoxGetEnabledBorderColor`, `window->winGetEnabledTextColor`, `window->winGetEnabledTextBorderColor`, `title->setFont`, `title->draw`, `TheWindowManager->winOpenRect`, `TheWindowManager->winFillRect`

### W3DGadgetComboBoxImageDraw
- Purpose: Renders a combo box with an image background
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `GadgetComboBoxGetDisabledImage`, `window->winGetDisabledTextColor`, `window->winGetDisabledTextBorderColor`, `GadgetComboBoxGetHiliteImage`, `window->winGetHiliteTextColor`, `window->winGetHiliteTextBorderColor`, `GadgetComboBoxGetEnabledImage`, `window->winGetEnabledTextColor`, `window->winGetEnabledTextBorderColor`, `TheWindowManager->winDrawImage`, `title->setFont`, `title->draw`, `TheWindowManager->winFontHeight`

## Globals
- None

## Dependencies
- `GameClient/GameWindowGlobal.h`
- `GameClient/GameWindowManager.h`
- `GameClient/GadgetComboBox.h`
- `GameClient/GadgetListBox.h`
- `W3DDevice/GameClient/W3DGadget.h`
- `W3DDevice/GameClient/W3DDisplay.h`
- `stdlib.h`
