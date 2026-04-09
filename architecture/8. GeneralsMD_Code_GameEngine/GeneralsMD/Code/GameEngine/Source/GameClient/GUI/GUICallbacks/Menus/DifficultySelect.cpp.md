# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/DifficultySelect.cpp

## Purpose
Handles the campaign difficulty selection menu UI and logic in Command & Conquer Generals Zero Hour.

## Responsibilities
- Initializes the difficulty selection UI window
- Manages radio button selection for difficulty levels
- Processes user input for difficulty selection
- Saves selected difficulty to preferences
- Triggers game start with selected difficulty

## Key Types
- `GameDifficulty` (Enum): Represents difficulty levels (EASY, NORMAL, HARD)
- `OptionPreferences` (Class): Manages game preferences including difficulty settings

## Key Functions
### `SetDifficultyRadioButton`
- Purpose: Sets the initial radio button selection based on saved preferences
- Calls: `GadgetRadioSetSelection`, `pref.getCampaignDifficulty()`

### `DifficultySelectInit`
- Purpose: Initializes the difficulty selection window and its controls
- Calls: `TheNameKeyGenerator->nameToKey()`, `TheWindowManager->winGetWindowFromId()`, `SetDifficultyRadioButton()`

### `DifficultySelectSystem`
- Purpose: Handles system messages for the difficulty selection window
- Calls: `pref.setCampaignDifficulty()`, `pref.write()`, `layout->destroyWindows()`, `setupGameStart()`, `TheCampaignManager->setCampaign()`, `TheWindowManager->winUnsetModal()`

## Globals
- `s_AIDiff` (GameDifficulty): Stores the currently selected difficulty level
- `buttonOkID`/`buttonOk` (NameKeyType/GameWindow*): References for the OK button
- `buttonCancelID`/`buttonCancel` (NameKeyType/GameWindow*): References for the Cancel button
- `radioButtonEasyAIID`/`radioButtonEasyAI` (NameKeyType/GameWindow*): References for Easy difficulty radio button
- `radioButtonMediumAIID`/`radioButtonMediumAI` (NameKeyType/GameWindow*): References for Medium difficulty radio button
- `radioButtonHardAIID`/`radioButtonHardAI` (NameKeyType/GameWindow*): References for Hard difficulty radio button

## Dependencies
- `PreRTS.h`, `UserPreferences.h`, `WindowLayout.h`, `Gadget.h`, `Shell.h`, `KeyDefs.h`, `GameWindowManager.h`, `GadgetPushButton.h`, `GadgetRadioButton.h`, `CampaignManager.h`, `ScriptEngine.h`
- `TheNameKeyGenerator`, `TheWindowManager`, `TheScriptEngine`, `TheCampaignManager`
