# Generals/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarUnderConstruction.cpp

## Purpose
Handles UI updates for objects under construction in the control bar.

## Responsibilities
- Updates construction progress text display
- Populates the control bar for under-construction objects
- Manages context updates for construction state changes
- Sets up cancel construction button and object portrait
- Handles rally point display for constructible objects

## Key Types
- None

## Key Functions
### updateConstructionTextDisplay
- Purpose: Updates the construction progress text for an object.
- Calls: TheGameText->fetch, GadgetStaticTextSetText

### populateUnderConstruction
- Purpose: Sets up the control bar UI for an object under construction.
- Calls: findCommandButton, TheWindowManager->winGetWindowFromId, setControlCommand, win->winSetStatus, updateConstructionTextDisplay, setPortraitByObject, showRallyPoint

### updateContextUnderConstruction
- Purpose: Updates the control bar context when an object's construction state changes.
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
