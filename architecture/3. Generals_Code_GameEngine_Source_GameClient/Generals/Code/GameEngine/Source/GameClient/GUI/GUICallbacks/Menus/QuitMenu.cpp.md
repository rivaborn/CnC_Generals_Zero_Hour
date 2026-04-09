# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/QuitMenu.cpp

## Purpose
Handles the quit menu UI and its associated callbacks in the game.

## Responsibilities
- Manages quit menu visibility and transitions
- Handles user actions (quit, restart, save/load, options)
- Cleans up game state on quit/restart
- Shows confirmation dialogs for critical actions
- Disables/enables buttons based on game mode

## Key Types
- **QuitMenuSystem** (Function): Window message handler for quit menu events
- **WindowLayout** (Type): UI layout structure
- **GameWindow** (Type): UI window reference
- **NameKeyType** (Type): UI element identifier

## Key Functions
### `ToggleQuitMenu`
- Purpose: Shows/hides the quit menu and handles related UI state
- Calls: `destroyQuitMenu`, `initGadgetsFullQuit`, `initGadgetsNoSaveQuit`, `TheTransitionHandler->setGroup`

### `restartMissionMenu`
- Purpose: Restarts the current mission after cleanup
- Calls: `TheGameLogic->clearGameData`, `TheMessageStream->appendMessage`

### `QuitMenuSystem`
- Purpose: Processes window messages for quit menu controls
- Calls: `QuitMessageBoxYesNo`, `MessageBoxYesNo`, `ToggleQuitMenu`

### `destroyQuitMenu`
- Purpose: Cleans up quit menu resources
- Calls: `WindowLayout->destroyWindows`, `WindowLayout->deleteInstance`

## Globals
- **quitMenuLayout** (WindowLayout*): Current quit menu layout
- **isVisible** (Bool): Tracks quit menu visibility
- **quitConfirmationWindow** (GameWindow*): Reference to confirmation dialog
- **buttonExit/Restart/Return/Options/SaveLoad** (NameKeyType): UI element identifiers

## Dependencies
- GameEngine.h, GameState.h, MessageStream.h, Player.h
- WindowLayout.h, GameWindowManager.h, Gadget.h
- GameText.h, MessageBox.h, Shell.h, InGameUI.h
- GameLogic.h, VictoryConditions.h, ControlBar.h
- GameWindowTransitions.h, DisconnectMenu.h, ScriptEngine.h
