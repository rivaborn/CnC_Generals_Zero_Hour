# GeneralsMD/Code/GameEngine/Include/Common/CustomMatchPreferences.h

## Purpose
Defines the `CustomMatchPreferences` class for saving/loading custom match settings in Generals Zero Hour.

## Responsibilities
- Stores user preferences for custom matches (faction, color, map, etc.)
- Manages ladder server connection details
- Controls UI elements (chat size, game list length)
- Handles restrictions (observers, text, superweapons, factions)
- Tracks stats usage

## Key Types
- **CustomMatchPreferences (Class)**: Base class for custom match preferences, inheriting from `UserPreferences`.

## Key Functions
### `setLastLadder`
- Purpose: Sets the last used ladder server address and port.
- Calls: None.

### `getLastLadderAddr`
- Purpose: Retrieves the last used ladder server address.
- Calls: None.

### `getLastLadderPort`
- Purpose: Retrieves the last used ladder server port.
- Calls: None.

### `setPreferredFaction`
- Purpose: Sets the preferred faction for custom matches.
- Calls: None.

### `getPreferredFaction`
- Purpose: Retrieves the preferred faction.
- Calls: None.

### `setPreferredColor`
- Purpose: Sets the preferred player color.
- Calls: None.

### `getPreferredColor`
- Purpose: Retrieves the preferred player color.
- Calls: None.

### `setChatSizeSlider`
- Purpose: Sets the chat size slider value.
- Calls: None.

### `getChatSizeSlider`
- Purpose: Retrieves the chat size slider value.
- Calls: None.

### `setPreferredMap`
- Purpose: Sets the preferred map for custom matches.
- Calls: None.

### `getPreferredMap`
- Purpose: Retrieves the preferred map.
- Calls: None.

### `setUsesSystemMapDir
