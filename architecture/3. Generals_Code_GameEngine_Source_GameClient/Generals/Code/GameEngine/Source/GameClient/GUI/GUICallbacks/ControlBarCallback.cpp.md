# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/ControlBarCallback.cpp

## Purpose
Handles input and system callbacks for the in-game control bar and left HUD area.

## Responsibilities
- Processes mouse and keyboard input for the control bar and radar
- Manages control bar visibility and animations
- Handles button clicks for build commands, special powers, and UI toggles
- Controls beacon placement and text editing
- Manages replay controls visibility

## Key Types
- None

## Key Functions
### LeftHUDInput
- Purpose: Handles input events for the left HUD (radar area)
- Calls: ThePlayerList->getLocalPlayer(), TheRadar->isRadarForced(), TheRadar->isRadarHidden(), TheInGameUI->getGUICommand(), TheInGameUI->getAllSelectedLocalDrawables(), TheMouse->setCursor(), TheRadar->localPixelToRadar(), TheRadar->radarToWorld(), TheTacticalView->lookAt(), TheMessageStream->appendMessage(), TheGameClient->evaluateContextCommand(), TheInGameUI->clearAttackMoveToMode()

### ControlBarInput
- Purpose: Handles input events for the control bar
- Calls: None

### ControlBarSystem
- Purpose: Handles system messages for the control bar parent window
- Calls: TheNameKeyGenerator->nameToKey(), TheScriptEngine->isGameEnding(), TheControlBar->processContextSensitiveButtonTransition(), TheControlBar->findCommandButton(), TheInGameUI->setGUICommand(), TheMessageStream->appendMessage(), TheWindowManager->winGetWindowFromId(), GadgetTextEntrySetText(), TheControlBar->togglePurchaseScience(), TheControlBar->switchControlBarStage(), TheControlBar->processContextSensitiveButtonClick(), TheInGameUI->selectNextIdleWorker(), ToggleDiplomacy(), HideQuitMenu(), ToggleQuitMenu()

### ShowControlBar
- Purpose: Shows the control bar with optional animation
- Calls: showReplayControls(), TheControlBar->showSpecialPowerShortcut(), TheNameKeyGenerator->nameToKey(), TheWindowManager->winGetWindowFromId(), TheControlBar->switchControlBarStage(), TheTacticalView->setHeight(), TheControlBar->m_animateWindowManager->reset(), TheControlBar->m_animateWindowManager->registerGameWindow(), TheControlBar->animateSpecialPowerShortcut(), TheControlBar->markUIDirty()

### HideControlBar
- Purpose: Hides the control bar with optional animation
- Calls: hideReplayControls(), TheControlBar->hideSpecialPowerShortcut(), TheNameKeyGenerator->nameToKey(), TheWindowManager->winGetWindowFromId(), TheTacticalView->setHeight(), TheControlBar->m_animateWindowManager->reverseAnimateWindow(), TheControlBar->animateSpecialPowerShortcut(), TheControlBar->hidePurchaseScience()

### ToggleControlBar
- Purpose: Toggles the control bar visibility
- Calls: toggleReplayControls(), TheNameKeyGenerator->nameToKey(), TheWindowManager->winGetWindowFromId(), TheControlBar->showSpecialPowerShortcut(), TheTacticalView->setHeight(), TheControlBar->switchControlBarStage(), TheControlBar->m_animateWindowManager->reset(), TheControlBar->m_animateWindowManager->registerGameWindow(), TheControlBar->animateSpecialPowerShortcut(), TheControlBar->hideSpecialPowerShortcut()

## Globals
- popupCommunicatorLayout (WindowLayout*): Stores the layout for the communicator popup

## Dependencies
- PreRTS.h, Common/NameKeyGenerator.h, Common/Player.h, Common/PlayerList.h, Common/Message
