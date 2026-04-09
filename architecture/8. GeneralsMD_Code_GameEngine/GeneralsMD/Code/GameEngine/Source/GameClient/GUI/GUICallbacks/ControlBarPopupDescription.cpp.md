# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/ControlBarPopupDescription.cpp

## Purpose
Handles the display and management of control bar popup descriptions/tooltips in the game UI.

## Responsibilities
- Manages tooltip layout creation, population, and display
- Handles animation of tooltip windows
- Updates tooltip content based on game state and selected objects
- Manages tooltip visibility and timing

## Key Types
- **ControlBarPopupDescriptionUpdateFunc (Function)**: Updates tooltip animation state
- **WindowLayout (Type)**: Holds the tooltip window layout
- **GameWindow (Type)**: Represents individual UI windows
- **AnimateWindowManager (Type)**: Manages window animations
- **CommandButton (Type)**: Represents control bar command buttons

## Key Functions
### ControlBarPopupDescriptionUpdateFunc
- Purpose: Updates tooltip animation state and cleans up when animation completes
- Calls: TheScriptEngine->isGameEnding(), TheControlBar->hideBuildTooltipLayout(), TheControlBar->getShowBuildTooltipLayout(), TheControlBar->deleteBuildTooltipLayout(), TheGlobalData->m_animateWindows, theAnimateWindowManager->isReversed(), theAnimateWindowManager->reverseAnimateWindow(), theAnimateWindowManager->update(), theAnimateWindowManager->isFinished()

### ControlBar::showBuildTooltipLayout
- Purpose: Displays tooltip for a given command button with delay and animation
- Calls: TheInGameUI->areTooltipsDisabled(), TheScriptEngine->isGameEnding(), TheControlBar->getShowBuildTooltipLayout(), TheGlobalData->m_animateWindows(), populateBuildTooltipLayout(), TheWindowManager->winCreateLayout(), TheDisconnectMenu->isScreenVisible(), TheGameLogic->isInReplayGame(), TheInGameUI->isQuitMenuVisible()

### ControlBar::populateBuildTooltipLayout
- Purpose: Fills tooltip with content based on command button or window type
- Calls: ThePlayerList->getLocalPlayer(), TheGameText->fetch(), TheInGameUI->getFirstSelectedDrawable(), TheBuildAssistant->canMakeUnit(), TheUpgradeCenter->canAffordUpgrade(), TheScienceStore->getNameAndDescription(), TheScienceStore->getSciencePurchaseCost(), TheWindowManager->winGetWindowFromId(), GadgetStaticTextSetText(), TheDisplayStringManager->newDisplayString(), TheDisplayStringManager->freeDisplayString(), TheControlBar->getBackgroundMarkerPos()

### ControlBar::hideBuildTooltipLayout
- Purpose: Hides the tooltip with optional animation
- Calls: TheControlBar->getShowBuildTooltipLayout(), TheGlobalData->m_animateWindows(), theAnimateWindowManager->isReversed(), theAnimateWindowManager->reverseAnimateWindow(), deleteBuildTooltipLayout()

### ControlBar::deleteBuildTooltipLayout
- Purpose: Cleans up tooltip resources
- Calls: None

## Globals
- **theLayout (WindowLayout*)**: Stores the current tooltip layout
- **theWindow (GameWindow*)**: Stores the current tooltip window
- **theAnimateWindowManager (AnimateWindowManager*)**: Manages tooltip animations
- **prevWindow (GameWindow*)**: Tracks the previously hovered window
- **useAnimation (Bool)**: Flag for enabling animations

## Dependencies
- Common/GlobalData.h, Common/BuildAssistant.h, Common/Player.h, Common/PlayerList.h, Common/ProductionPrerequisite.h, Common/ThingTemplate.h, Common/Upgrade.h
- GameClient/AnimateWindowManager.h, GameClient/DisconnectMenu.h, GameClient/GameWindow.h, GameClient/Gadget.h, GameClient/GadgetTextEntry.h, GameClient/GadgetPushButton.h, GameClient/GadgetStatic
