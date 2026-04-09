# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/QuitMenu.cpp

## Purpose
Handles the quit menu UI and its associated callbacks in Command & Conquer Generals Zero Hour.

## Responsibilities
- Manages quit menu visibility and transitions
- Handles user actions (quit, restart, save/load, options)
- Controls game state during menu interactions
- Manages confirmation dialogs for critical actions
- Cleans up resources when menu is destroyed

## Key Types
- `WindowLayout` (Class): UI layout container
- `GameWindow` (Class): UI window element
- `NameKeyType` (Type): UI element identifier
- `GameMessage` (Class): Game logic message

## Key Functions
### `initGadgetsFullQuit`
- Purpose: Initializes UI elements for full quit menu
- Calls: `TheNameKeyGenerator->nameToKey`, `TheWindowManager->winGetWindowFromId`

### `destroyQuitMenu`
- Purpose: Cleans up quit menu resources
- Calls: `destroyWindows`, `deleteInstance`

### `exitQuitMenu`
- Purpose: Handles game exit logic
- Calls: `TheMessageStream->appendMessage`, `TheGameLogic->clearGameData`

### `restartMissionMenu`
- Purpose: Restarts current mission
- Calls: `TheRecorder->stopRecording`, `TheGameLogic->clearGameData`, `TheMessageStream->appendMessage`

### `ToggleQuitMenu`
- Purpose: Shows/hides quit menu
- Calls: `TheTransitionHandler->reverse`, `TheGameLogic->setGamePaused`, `TheWindowManager->winDestroy`

### `QuitMenuSystem`
- Purpose: Handles quit menu UI events
- Calls: `QuitMessageBoxYesNo`, `MessageBoxYesNo`, `TheShell->getSaveLoadMenuLayout`

## Globals
- `quitMenuLayout` (WindowLayout*): Current quit menu layout
- `fullQuitMenuLayout` (WindowLayout*): Full quit menu layout
- `noSaveLoadQuitMenuLayout` (WindowLayout*): No save/load quit menu layout
- `isVisible` (Bool): Menu visibility state
- `quitConfirmationWindow` (GameWindow*): Confirmation dialog window
- `saveLoadMenuLayout` (WindowLayout*): Save/load menu layout
- `buttonRestartWin` (GameWindow*): Restart button window
- `buttonSaveLoadWin` (GameWindow*): Save/load button window
- `buttonOptionsWin` (GameWindow*): Options button window
- `buttonExitWin` (GameWindow*): Exit button window
- `buttonExit` (NameKeyType): Exit button ID
- `buttonRestart` (NameKeyType): Restart button ID
- `buttonReturn` (NameKeyType): Return button ID
- `buttonOptions` (NameKeyType): Options button ID
- `buttonSaveLoad` (NameKeyType): Save/load button ID

## Dependencies
- `PreRTS.h`, `GameEngine.h`, `GameState.h`, `MessageStream.h`, `Player.h`, `PlayerList.h`, `RandomValue.h`, `Recorder.h`, `GUICallbacks.h`, `WindowLayout.h`, `GameWindowManager.h`, `Gadget.h`, `GadgetPushButton.h`, `GameText.h`, `MessageBox.h`, `Shell.h`, `InGameUI.h`, `GameLogic.h`, `VictoryConditions.h`, `ControlBar.h`, `GameWindowTransitions.h`, `DisconnectMenu.h`, `ScriptEngine.h`
