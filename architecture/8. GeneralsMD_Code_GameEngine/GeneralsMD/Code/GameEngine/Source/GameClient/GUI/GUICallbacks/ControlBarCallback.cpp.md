# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/ControlBarCallback.cpp

## Purpose
Handles input and system callbacks for the in-game control bar and left HUD (radar) in Command & Conquer Generals Zero Hour.

## Responsibilities
- Processes mouse and keyboard input for the control bar and radar
- Manages control bar visibility and animations
- Handles button clicks for build commands, special powers, and UI toggles
- Controls beacon placement and text editing
- Manages context-sensitive UI elements

## Key Types
- `LeftHUDInput` (Function): Handles radar and left HUD input
- `ControlBarInput` (Function): Processes control bar input
- `ControlBarSystem` (Function): System callback for control bar parent window
- `popupCommunicatorLayout` (WindowLayout*): Layout for popup communicator

## Key Functions
### LeftHUDInput
- Purpose: Handles mouse input over the left HUD/radar area
- Calls: `TheRadar->localPixelToRadar`, `TheRadar->radarToWorld`, `TheMessageStream->appendMessage`, `TheInGameUI->getGUICommand`, `TheMouse->setCursor`

### ControlBarSystem
- Purpose: Processes system messages for the control bar parent window
- Calls: `TheControlBar->processContextSensitiveButtonTransition`, `TheControlBar->processContextSensitiveButtonClick`, `TheControlBar->togglePurchaseScience`, `TheControlBar->toggleControlBarStage`, `ToggleQuitMenu`, `TheInGameUI->selectNextIdleWorker`

### ShowControlBar
- Purpose: Forces the control bar to be shown with optional animation
- Calls: `showReplayControls`, `TheControlBar->showSpecialPowerShortcut`, `TheControlBar->switchControlBarStage`, `TheTacticalView->setHeight`, `TheControlBar->m_animateWindowManager->registerGameWindow`

### HideControlBar
- Purpose: Forces the control bar to be hidden with optional animation
- Calls: `hideReplayControls`, `TheControlBar->hideSpecialPowerShortcut`, `TheTacticalView->setHeight`, `TheControlBar->m_animateWindowManager->reverseAnimateWindow`, `TheControlBar->hidePurchaseScience`

### ToggleControlBar
- Purpose: Toggles the control bar visibility
- Calls: `toggleReplayControls`, `TheControlBar->showSpecialPowerShortcut`, `TheTacticalView->setHeight`, `TheControlBar->switchControlBarStage`, `TheControlBar->m_animateWindowManager->registerGameWindow`

## Globals
- `popupCommunicatorLayout` (WindowLayout*): Stores the layout for the popup communicator window

## Dependencies
- Key includes: `PreRTS.h`, `Common/Player.h`, `GameClient/ControlBar.h`, `GameClient/GameWindow.h`, `GameLogic/GameLogic.h`
- External symbols: `ThePlayerList`, `TheRadar`, `TheMouse`, `TheInGameUI`, `TheMessageStream`, `TheControlBar`, `TheTacticalView`, `TheWindowManager`, `TheNameKeyGenerator`, `TheScriptEngine`, `TheGameClient`, `TheDisplay`, `TheLanguageFilter`, `TheGlobalData`
