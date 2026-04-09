# GeneralsMD/Code/GameEngine/Include/GameClient/GadgetComboBox.h

## Purpose
Header file defining helper functions and inline methods for managing ComboBox gadgets in the game UI.

## Responsibilities
- Provides an interface for manipulating ComboBox properties (text, entries, selection, colors, images).
- Encapsulates ComboBox sub-components (dropdown button, list box, edit box).
- Supports font, input validation, and display customization.

## Key Types
- **ComboBoxData (struct)**: Internal data structure for ComboBox (not fully defined here).

## Key Functions
### GadgetComboBoxSetFont
- Purpose: Sets the font for the ComboBox.
- Calls: Not inferable.

### GadgetComboBoxAddEntry
- Purpose: Adds an entry to the ComboBox with specified text and color.
- Calls: Not inferable.

### GadgetComboBoxSetColors
- Purpose: Configures all visual states (enabled/disabled/hilite) for the ComboBox and its sub-components.
- Calls: Not inferable.

### GadgetComboBoxGetDropDownButton / GetListBox / GetEditBox
- Purpose: Retrieves references to ComboBox sub-components.
- Calls: `winGetUserData()` (via `ComboBoxData` access).

## Globals
- None.

## Dependencies
- **Includes**: `GameClient/Gadget.h`, `GameClient/GameWindow.h`
- **Types**: `GameWindow`, `GameFont`, `UnicodeString`, `Color`, `Image`
- **External**: `ComboBoxData` (forward-referenced), `winSetEnabledImage`, `winGetUserData`, etc.
