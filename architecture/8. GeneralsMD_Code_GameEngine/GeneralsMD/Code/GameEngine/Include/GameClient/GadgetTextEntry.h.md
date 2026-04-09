# GeneralsMD/Code/GameEngine/Include/GameClient/GadgetTextEntry.h

## Purpose
Provides helper functions for manipulating text entry UI elements in the game.

## Responsibilities
- Wraps GameWindow methods for text entry gadgets
- Manages text, font, colors, and images for enabled/disabled/highlighted states
- Simplifies UI state modifications

## Key Types
- GameWindow (Class): Base UI window class

## Key Functions
### GadgetTextEntrySetText
- Purpose: Sets the text content of a text entry gadget
- Calls: TheWindowManager->winSendSystemMsg

### GadgetTextEntryGetText
- Purpose: Retrieves the text content from a text entry gadget
- Calls: Not inferable

### GadgetTextEntrySetFont
- Purpose: Sets the font for a text entry gadget
- Calls: Not inferable

### GadgetTextEntrySetTextColor
- Purpose: Sets text and border colors for enabled/disabled states
- Calls: g->winGetEnabledTextBorderColor, g->winSetEnabledTextColors, g->winSetDisabledTextColors, GameDarkenColor

### GadgetTextEntrySetEnabledImageLeft/Right/Center/SmallCenter
- Purpose: Sets enabled state images for different positions
- Calls: g->winSetEnabledImage

### GadgetTextEntrySetEnabledColor/BorderColor
- Purpose: Sets enabled state colors
- Calls: g->winSetEnabledColor, g->winSetEnabledBorderColor

### GadgetTextEntryGetEnabledImageLeft/Right/Center/SmallCenter
- Purpose: Retrieves enabled state images
- Calls: g->winGetEnabledImage

### GadgetTextEntryGetEnabledColor/BorderColor
- Purpose: Retrieves enabled state colors
- Calls: g->winGetEnabled
