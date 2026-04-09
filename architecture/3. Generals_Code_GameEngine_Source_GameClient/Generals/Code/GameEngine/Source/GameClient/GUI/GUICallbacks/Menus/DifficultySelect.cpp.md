# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/DifficultySelect.cpp

## Purpose
Handles the campaign difficulty selection menu UI and logic in Command & Conquer Generals.

## Responsibilities
- Manages difficulty selection UI elements (radio buttons, OK/Cancel buttons)
- Updates game preferences based on selected difficulty
- Initializes and handles input for the difficulty selection window
- Calls game start function with selected difficulty

## Key Types
- `GameDifficulty` (enum): Represents difficulty levels (EASY, NORMAL, HARD)
- `GameWindow` (class): UI window element
- `WindowLayout` (class): UI layout manager
- `OptionPreferences` (class): Handles game preferences

## Key Functions
### `SetDifficultyRadioButton`
- Purpose: Sets the radio button selection based on current difficulty preference
- Calls: `GadgetRadioSetSelection`, `pref.getCampaignDifficulty()`

### `DifficultySelectInit`
- Purpose: Initializes the difficulty selection window and its controls
- Calls: `TheNameKeyGenerator->nameToKey()`, `TheWindowManager->winGetWindowFromId()`, `SetDifficultyRadioButton()`

### `DifficultySelectInput`
- Purpose: Handles input events for the difficulty selection window
- Calls: None (currently empty implementation)

### `DifficultySelectSystem`
- Purpose: Handles system messages for the difficulty selection window
- Calls: `pref.setCampaignDifficulty()`, `pref.write()`, `layout->destroyWindows()`, `layout->deleteInstance()`, `setupGameStart()`, `TheCampaignManager->setCampaign()`, `TheWindowManager->winUnsetModal()`

## Globals
- `s_AIDiff` (GameDifficulty): Stores currently selected difficulty
- `buttonOkID`/`buttonCancelID` (NameKeyType): IDs for OK/Cancel buttons
- `buttonOk`/`buttonCancel` (GameWindow*): Pointers to OK/Cancel buttons
- `radioButtonEasyAIID`/`radioButtonMediumAIID`/`radioButtonHardAIID` (NameKeyType): IDs for difficulty radio buttons
- `radioButtonEasyAI`/`radioButtonMediumAI`/`radioButtonHardAI` (GameWindow*): Pointers to difficulty radio buttons

## Dependencies
- `PreRTS.h`, `UserPreferences.h`, `WindowLayout.h`, `Gadget.h`, `Shell.h`, `KeyDefs.h`, `GameWindowManager.h`, `GadgetPushButton.h`, `GadgetRadioButton.h`, `CampaignManager.h`, `ScriptEngine.h`
- `TheNameKeyGenerator`, `TheWindowManager`, `TheScriptEngine`, `TheCampaignManager`
