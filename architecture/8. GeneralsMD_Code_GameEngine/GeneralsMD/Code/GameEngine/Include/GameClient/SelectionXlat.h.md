# GeneralsMD/Code/GameEngine/Include/GameClient/SelectionXlat.h

## Purpose
Defines the `SelectionTranslator` class for handling unit selection logic in the game client.

## Responsibilities
- Translates game messages related to unit selection
- Manages drag selection and mouse button states
- Tracks selected units and their counts
- Handles special selection modes (e.g., "Hand of God" in debug builds)

## Key Types
- `ThingTemplate` (Class): Not inferable.
- `SelectCountMap` (Class): Maps `ThingTemplate` to selection count.
- `SelectCountMapIt` (Class): Iterator for `SelectCountMap`.
- `SelectionTranslator` (Class): Handles unit selection translation and logic.

## Key Functions
### `CanSelectDrawable`
- Purpose: Checks if a drawable can be selected.
- Calls: Not inferable.

### `selectFriends`
- Purpose: Selects friendly units.
- Calls: Not inferable.

### `killThemKillThemAll`
- Purpose: Handles "kill all" selection logic.
- Calls: Not inferable.

### `translateGameMessage`
- Purpose: Translates game messages for selection.
- Calls: Not inferable.

### `setDragSelecting`
- Purpose: Toggles drag selection mode.
- Calls: Not inferable.

### `setLeftMouseButton`
- Purpose: Updates left mouse button state.
- Calls: Not inferable.

## Globals
- `TheSelectionTranslator` (SelectionTranslator*): Global instance of the selection translator.

## Dependencies
- `GameClient/InGameUI.h`
- `GameMessageTranslator` (base class)
- `Drawable` (external class)
- `GameMessage` (external class)
- `ThingTemplate` (external class)
