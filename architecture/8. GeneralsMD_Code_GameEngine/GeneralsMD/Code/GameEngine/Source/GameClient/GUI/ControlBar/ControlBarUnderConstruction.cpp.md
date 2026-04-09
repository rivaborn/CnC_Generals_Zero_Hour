# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarUnderConstruction.cpp

## Purpose
Handles UI updates for objects under construction in the control bar.

## Responsibilities
- Updates construction progress text display
- Populates the under-construction UI context
- Manages context updates for objects under construction

## Key Types
- None

## Key Functions
### updateConstructionTextDisplay
- Purpose: Updates the construction progress text for an object.
- Calls: TheGameText->fetch, GadgetStaticTextSetText

### populateUnderConstruction
- Purpose: Sets up the UI for an under-construction object.
- Calls: findCommandButton, TheWindowManager->winGetWindowFromId, setControlCommand, win->winSetStatus, updateConstructionTextDisplay, setPortraitByObject, showRallyPoint

### updateContextUnderConstruction
- Purpose: Updates the under-construction UI context if needed.
- Calls: evaluateContextUI, updateConstructionTextDisplay

## Globals
- None

## Dependencies
- PreRTS.h
- Common/NameKeyGenerator.h
- Common/ThingTemplate.h
- GameLogic/Object.h
- GameLogic/Module/UpdateModule.h
- GameClient/Drawable.h
- GameClient/GameText.h
- GameClient/ControlBar.h
- GameClient/GameWindow.h
- GameClient/GameWindowManager.h
- GameClient/GadgetStaticText.h
