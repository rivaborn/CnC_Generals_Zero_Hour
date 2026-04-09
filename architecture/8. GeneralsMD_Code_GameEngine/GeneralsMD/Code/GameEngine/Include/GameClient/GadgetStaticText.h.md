# GeneralsMD/Code/GameEngine/Include/GameClient/GadgetStaticText.h

## Purpose
Header file defining helper functions for managing static text UI elements in the game.

## Responsibilities
- Provides inline functions for setting/getting text, font, and visual states (enabled/disabled/highlighted) of static text gadgets
- Encapsulates GameWindow methods for static text manipulation
- Organizes visual properties (images, colors, borders) for different states

## Key Types
None

## Key Functions
### GadgetStaticTextSetText
- Purpose: Sets the text content of a static text gadget
- Calls: Not inferable

### GadgetStaticTextGetText
- Purpose: Retrieves the text content of a static text gadget
- Calls: Not inferable

### GadgetStaticTextSetFont
- Purpose: Sets the font for a static text gadget
- Calls: Not inferable

### GadgetStaticTextSetEnabledImage/Color/BorderColor
- Purpose: Configures visual appearance when gadget is enabled
- Calls: GameWindow::winSetEnabledImage/Color/BorderColor

### GadgetStaticTextGetEnabledImage/Color/BorderColor
- Purpose: Retrieves visual appearance settings for enabled state
- Calls: GameWindow::winGetEnabledImage/Color/BorderColor

### GadgetStaticTextSetDisabledImage/Color/BorderColor
- Purpose: Configures visual appearance when gadget is disabled
- Calls: GameWindow::winSetDisabledImage/Color/BorderColor

### GadgetStaticTextGetDisabledImage/Color/BorderColor
- Purpose: Retrieves visual appearance settings for disabled state
- Calls: GameWindow::winGetDisabledImage/Color/BorderColor

### GadgetStaticTextSetHiliteImage/Color/BorderColor
- Purpose: Configures visual appearance when gad
