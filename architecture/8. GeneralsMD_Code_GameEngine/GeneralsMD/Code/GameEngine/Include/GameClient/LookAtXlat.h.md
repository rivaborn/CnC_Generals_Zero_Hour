# GeneralsMD/Code/GameEngine/Include/GameClient/LookAtXlat.h

## Purpose
Defines the `LookAtTranslator` class, which handles camera movement and scrolling in the game.

## Responsibilities
- Translates game messages into camera actions (scrolling, rotating, zooming).
- Manages scroll states (RMB, key, screen-edge).
- Tracks mouse movement and timestamps for input handling.
- Provides access to scroll anchors and view locations.

## Key Types
- **LookAtTranslator (Class)**: Manages camera translation and scrolling logic.
- **(anonymous enum)**: Defines `MAX_VIEW_LOCS` (8).
- **(anonymous enum)**: Defines scroll types (`SCROLL_NONE`, `SCROLL_RMB`, `SCROLL_KEY`, `SCROLL_SCREENEDGE`).

## Key Functions
### `translateGameMessage`
- Purpose: Translates game messages into camera actions.
- Calls: Not inferable (virtual function).

### `getRMBScrollAnchor`
- Purpose: Returns the scroll anchor position for right-mouse-button scrolling.
- Calls: None.

### `hasMouseMovedRecently`
- Purpose: Checks if the mouse has moved recently.
- Calls: None.

### `setCurrentPos`
- Purpose: Updates the current camera position.
- Calls: None.

### `resetModes`
- Purpose: Resets scrolling/rotation modes when input is disabled.
- Calls: None.

### `setScrolling`
- Purpose: Sets the scrolling state.
- Calls: None.

### `stopScrolling`
- Purpose: Stops the current scrolling action.
- Calls: None.

## Globals
- **TheLookAtTranslator (LookAtTranslator*)**: Global instance of the translator.

## Dependencies
- `GameClient/InGameUI.h` (for `GameMessageTranslator` and related types).
- `ICoord2D`, `Bool`,
