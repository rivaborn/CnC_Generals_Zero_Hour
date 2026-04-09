# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/GeneralsExpPoints.cpp

## Purpose
Handles input and system messages for the Generals experience points (exp) screen UI.

## Responsibilities
- Processes mouse and keyboard input for the exp screen
- Manages focus changes and input focus requests
- Handles button click events (e.g., exit button)
- Clears building placement mode when entering the exp screen

## Key Types
None

## Key Functions
### GeneralsExpPointsInput
- Purpose: Handles mouse and keyboard input for the exp screen
- Calls: TheInGameUI->placeBuildAvailable

### GeneralsExpPointsSystem
- Purpose: Processes system messages for the exp screen window
- Calls: TheControlBar->hidePurchaseScience, TheControlBar->processContextSensitiveButtonClick

## Globals
None

## Dependencies
- GameClient/ControlBar.h
- GameClient/GUICallbacks.h
- GameClient/GameWindow.h
- GameClient/Gadget.h
- GameClient/KeyDefs.h
- GameClient/InGameUI.h
