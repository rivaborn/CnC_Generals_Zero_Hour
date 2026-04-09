# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/ControlBarPopupDescription.cpp

## Purpose
Manages the display and behavior of control bar popup descriptions/tooltips in the game UI.

## Responsibilities
- Handles showing/hiding build tooltips for control bar buttons
- Populates tooltip content based on command buttons or generic windows
- Manages tooltip animations and layout updates
- Processes prerequisite requirements and cost information for tooltips

## Key Types
- `ControlBarPopupDescriptionUpdateFunc` (Function): Updates tooltip layout and animations
- `WindowLayout` (Type): Represents the tooltip layout window
- `GameWindow` (Type): Represents individual windows in the UI
- `AnimateWindowManager` (Type): Manages window animations
- `CommandButton` (Type): Represents control bar command buttons

## Key Functions
### `ControlBarPopupDescriptionUpdateFunc`
- Purpose: Updates tooltip layout and handles animation state
- Calls: `TheScriptEngine->isGameEnding()`, `TheControlBar->hideBuildTooltipLayout()`, `TheControlBar->getShowBuildTooltipLayout()`, `theAnimateWindowManager->reverseAnimateWindow()`, `TheControlBar->deleteBuildTooltipLayout()`, `theAnimateWindowManager->update()`, `theAnimateWindowManager->isFinished()`, `theAnimateWindowManager->isReversed()`

### `ControlBar::showBuildTooltipLayout`
- Purpose: Displays the build tooltip for a given command button
- Calls: `TheInGameUI->areTooltipsDisabled()`, `TheScriptEngine->isGameEnding()`, `GadgetButtonGetData()`, `TheGameLogic->isInReplayGame()`, `TheInGameUI->isQuitMenuVisible()`, `TheDisconnectMenu->isScreenVisible()`, `populateBuildTooltipLayout()`, `TheWindowManager->winCreateLayout()`, `NEW AnimateWindowManager()`, `theAnimateWindowManager->reset()`, `theAnimateWindowManager->registerGameWindow()`

### `ControlBar::populateBuildTooltipLayout`
- Purpose: Fills tooltip content based on command button or window type
- Calls: `ThePlayerList->getLocalPlayer()`, `TheGameText->fetch()`, `commandButton->getThingTemplate()`, `commandButton->getUpgradeTemplate()`, `TheScienceStore->getNameAndDescription()`, `TheBuildAssistant->canMakeUnit()`, `TheUpgradeCenter->canAffordUpgrade()`, `TheInGameUI->getFirstSelectedDrawable()`, `TheWindowManager->winGetWindowFromId()`, `GadgetStaticTextSetText()`, `TheDisplayStringManager->newDisplayString()`, `TheDisplayStringManager->freeDisplayString()`, `TheControlBar->getBackgroundMarkerPos()`

### `ControlBar::hideBuildTooltipLayout`
- Purpose: Hides the build tooltip layout
- Calls: `theAnimateWindowManager->isReversed()`, `theAnimateWindowManager->reverseAnimateWindow()`, `deleteBuildTooltipLayout()`

### `ControlBar::deleteBuildTooltipLayout`
- Purpose: Cleans up and deletes the tooltip layout
- Calls: None

## Globals
- `theLayout` (WindowLayout*): Stores the current tooltip layout
- `theWindow` (GameWindow*): Stores the current tooltip window
- `theAnimateWindowManager` (AnimateWindowManager*): Manages tooltip animations
- `prevWindow` (GameWindow*): Tracks the previous window that triggered a tooltip
- `useAnimation` (Bool): Flag indicating whether to use animations

## Dependencies
- Key includes: `PreRTS.h`, `Common/GlobalData.h`, `Common/BuildAssistant.h`, `GameClient/AnimateWindowManager.h`, `GameClient/Controlbar.h`, `GameLogic/GameLogic.h`
