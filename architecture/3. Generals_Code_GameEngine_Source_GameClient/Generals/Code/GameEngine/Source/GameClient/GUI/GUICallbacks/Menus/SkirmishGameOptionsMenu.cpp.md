# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/SkirmishGameOptionsMenu.cpp

## Purpose
Handles the skirmish game options menu UI, including player setup, map selection, and game start logic.

## Responsibilities
- Manages player slot configuration (name, color, faction, team, start position)
- Handles game speed/FPS settings
- Validates CD presence before starting
- Updates UI based on game state
- Saves/loads skirmish preferences

## Key Types
- SkirmishGameInfo (Class): Global game info for skirmish mode
- SkirmishPreferences (Class): Handles INI file storage for skirmish settings
- GREATER_NO_FPS_LIMIT (Enum): Constant for unlimited FPS setting

## Key Functions
### setFPSTextBox
- Purpose: Updates the FPS display text based on slider position
- Calls: GadgetStaticTextSetText

### reallyDoStart
- Purpose: Initiates the actual game start after validation
- Calls: TheGameLogic->clearGameData, TheSkirmishGameInfo->startGame, InitGameLogicRandom

### startPressed
- Purpose: Handles the "Start Game" button press logic
- Calls: CheckForCDAtGameStart, reallyDoStart, cancelStartBecauseOfNoCD

### populateSkirmishBattleHonors
- Purpose: Populates the battle honors display with player achievements
- Calls: GadgetListBoxAddEntryImage, InsertBattleHonor

### SkirmishGameOptionsMenuInit
- Purpose: Initializes the skirmish options menu UI
- Calls: InitSkirmishGameGadgets, skirmishUpdateSlotList

## Globals
- TheSkirmishGameInfo (SkirmishGameInfo*): Global skirmish game state
- parentSkirmishGameOptionsID (NameKeyType): ID for the main menu window
- textEntryPlayerNameID (NameKeyType): ID for player name input field
- comboBoxPlayerID/ColorID/TemplateID/TeamID (NameKeyType[MAX_SLOTS]): IDs for player configuration dropdowns
- sliderGameSpeedID (NameKeyType): ID for game speed slider
- doUpdateSlotList (Bool): Flag to trigger slot list updates

## Dependencies
- Common/BattleHonors.h, SkirmishBattleHonors.h
- GameClient/Gadget*.h (various UI components)
- GameNetwork/GameInfo.h
- GameClient/CDCheck.h (for CD validation)
- WWDownload/Registry.h (for preorder check)
