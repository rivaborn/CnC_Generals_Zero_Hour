# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DTextEntry.cpp

## Purpose
Implements rendering for text entry gadgets in the W3D (Westwood 3D) device layer.

## Responsibilities
- Renders text entry fields with or without images
- Handles IME (Input Method Editor) composition display
- Manages cursor blinking and positioning
- Applies appropriate colors based on widget state (enabled/disabled/hilited)
- Supports both single-line and multi-line text entry

## Key Types
- **EntryData (struct)**: Contains text entry state (text, cursor position, etc.)
- **GameWindow (class)**: Window management structure
- **WinInstanceData (class)**: Window instance data
- **DisplayString (class)**: Text rendering object
- **UnicodeString (class)**: Unicode text string
- **IRegion2D (struct)**: 2D clipping region
- **ICoord2D (struct)**: 2D coordinate pair
- **Color**: Color value type

## Key Functions
### drawTextEntryText
- Purpose: Renders the actual text content of a text entry field
- Calls: `TheIMEManager->isAttachedTo`, `TheIMEManager->isComposing`, `TheIMEManager->getCompositionString`, `TheIMEManager->getCompositionCursorPosition`, `TheWindowManager->winGetScreenPosition`, `TheWindowManager->winGetSize`, `TheWindowManager->winFillRect`, `TheWindowManager->winSetCursorPosition`

### W3DGadgetTextEntryDraw
- Purpose: Draws a text entry field using standard graphics primitives
- Calls: `GadgetTextEntryGetDisabledColor`, `GadgetTextEntryGetDisabledBorderColor`, `GadgetTextEntryGetHiliteColor`, `GadgetTextEntryGetHiliteBorderColor`, `GadgetTextEntryGetEnabledColor`, `GadgetTextEntryGetEnabledBorderColor`, `TheWindowManager->winOpenRect`, `TheWindowManager->winFillRect`, `TheWindowManager->winFontHeight`, `drawTextEntryText`

### W3DGadgetTextEntryImageDraw
- Purpose: Draws a text entry field using tiled images for the background
- Calls: `GadgetTextEntryGetDisabledImageLeft`, `GadgetTextEntryGetDisabledImageRight`, `GadgetTextEntryGetDisabledImageCenter`, `GadgetTextEntryGetDisabledImageSmallCenter`, `GadgetTextEntryGetHiliteImageLeft`, `GadgetTextEntryGetHiliteImageRight`, `GadgetTextEntryGetHiliteImageCenter`, `GadgetTextEntryGetHiliteImageSmallCenter`, `GadgetTextEntryGetEnabledImage
