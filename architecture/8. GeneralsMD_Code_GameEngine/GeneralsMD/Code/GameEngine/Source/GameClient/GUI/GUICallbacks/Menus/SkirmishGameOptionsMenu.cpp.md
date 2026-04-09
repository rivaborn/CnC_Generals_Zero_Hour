# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/SkirmishGameOptionsMenu.cpp

## Purpose
Handles the skirmish game options menu UI, including player setup, map selection, and game parameters.

## Responsibilities
- Manages player slots, colors, factions, and teams
- Handles map selection and start position configuration
- Controls game speed, superweapons, and starting cash settings
- Displays battle honors and player statistics
- Validates CD presence before starting the game

## Key Types
- SkirmishGameInfo (Class): Global game state for skirmish mode
- SkirmishPreferences (Class): Handles skirmish preferences and settings persistence
- GREATER_NO_FPS_LIMIT (Enum): Constant for FPS limit value

## Key Functions
### SkirmishGameOptionsMenuInit
- Purpose: Initializes the skirmish game options menu UI
- Calls: InitSkirmishGameGadgets, populateSkirmishBattleHonors

### startPressed
- Purpose: Handles the start game button press event
- Calls: CheckForCDAtGameStart, reallyDoStart, cancelStartBecauseOfNoCD

### populateSkirmishBattleHonors
- Purpose: Populates the battle honors display with player achievements
- Calls: BattleHonorTooltip, GadgetListBoxReset, InsertBattleHonor

### updateSkirmishGameOptions
- Purpose: Updates game options based on UI changes
- Calls: GadgetComboBoxGetSelected, GadgetSliderGetPosition

## Globals
- TheSkirmishGameInfo (SkirmishGameInfo*): Global skirmish game state
- parentSkirmishGameOptionsID (NameKeyType): ID for the parent window
- textEntryPlayerNameID (NameKeyType): ID for player name input
- comboBoxPlayerID (NameKeyType[MAX_SLOTS]): IDs for player selection comboboxes
- skirmishMapSelectLayout (WindowLayout*): Layout for map selection UI

## Dependencies
- Common/BattleHonors.h, Common/GameEngine.h, Common/PlayerTemplate.h
- GameClient/AnimateWindowManager.h, GameClient/WindowLayout.h
- GameClient/Gadget.h, GameClient/Shell.h, GameClient/ShellHooks.h
- GameNetwork/GameInfo.h, GameNetwork/GUIUtil.h
- GameClient/CDCheck.h, GameClient/ExtendedMessageBox.h
