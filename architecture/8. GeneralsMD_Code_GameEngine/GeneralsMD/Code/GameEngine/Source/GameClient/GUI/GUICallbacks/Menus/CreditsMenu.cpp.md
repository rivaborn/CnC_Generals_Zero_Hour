# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/CreditsMenu.cpp

## Purpose
Handles the credits screen menu initialization, updates, input, and shutdown in the game.

## Responsibilities
- Initialize and display the credits screen
- Handle user input (e.g., ESC key to exit)
- Manage credits playback and completion
- Control audio events for the credits sequence
- Clean up resources when exiting the credits menu

## Key Types
- **None**

## Key Functions
### CreditsMenuInit
- Purpose: Initializes the credits menu, loads credits, and sets up audio.
- Calls: `TheShell->showShellMap`, `delete`, `new`, `TheCredits->load`, `TheCredits->init`, `TheWindowManager->winGetWindowFromId`, `layout->hide`, `TheWindowManager->winSetFocus`, `TheAudio->removeAudioEvent`, `TheAudio->addAudioEvent`

### CreditsMenuShutdown
- Purpose: Cleans up the credits menu and restores the game state.
- Calls: `TheCredits->reset`, `delete`, `TheShell->showShellMap`, `layout->hide`, `TheShell->shutdownComplete`, `TheAudio->removeAudioEvent`

### CreditsMenuUpdate
- Purpose: Updates the credits screen and checks for completion.
- Calls: `TheWindowManager->winSetFocus`, `TheCredits->update`, `TheCredits->isFinished`, `TheShell->pop`

### CreditsMenuInput
- Purpose: Handles keyboard input for the credits menu.
- Calls: `TheShell->pop`

### CreditsMenuSystem
- Purpose: Handles system messages for the credits menu window.
- Calls: None

## Globals
- **parentMainMenuID (NameKeyType)**: Stores the ID of the parent credits window.
- **parentMainMenu (GameWindow*)**: Pointer to the parent credits window.

## Dependencies
- Key includes: `PreRTS.h`, `Common/GameAudio.h`, `Common/AudioEventRTS.h`, `Common/AudioHandleSpecialValues.h`, `GameClient/Credits.h`, `GameClient/WindowLayout.h`, `GameClient/Gadget.h`, `GameClient/Shell.h`, `GameClient/KeyDefs.h`, `GameClient/GameWindowManager.h`
- External symbols: `TheShell`, `TheCredits`, `TheNameKeyGenerator`, `TheWindowManager`, `TheAudio`
