# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBar.cpp

## Purpose
Manages the in-game control bar UI, including command buttons, special powers, and science purchases.

## Responsibilities
- Handles command button tooltips and availability
- Manages special power shortcuts and their animations
- Populates and updates science purchase UI elements
- Tracks UI state and marks it as dirty when needed

## Key Types
- `(anonymous enum)` (Enum): Not inferable.
- `RADAR_ATTACK_GLOW_FRAMES` (Enum): Not inferable.
- `RADAR_ATTACK_GLOW_NUM_TIMES` (Enum): Not inferable.

## Key Functions
### `commandButtonTooltip`
- Purpose: Shows build tooltip layout for command buttons.
- Calls: `TheControlBar->showBuildTooltipLayout`

### `ControlBarPopupDescriptionUpdateFunc`
- Purpose: Not inferable.
- Calls: Not inferable.

## Globals
- `TheControlBar` (ControlBar*): Global instance of the control bar.

## Dependencies
- Key includes: `ControlBar.h`, `GameLogic.h`, `Player.h`, `WindowManager.h`
- External symbols: `TheGameLogic`, `TheScriptEngine`, `ThePlayerList`, `TheScienceStore`, `TheWindowManager`, `TheFontLibrary`, `TheDisplayStringManager`
