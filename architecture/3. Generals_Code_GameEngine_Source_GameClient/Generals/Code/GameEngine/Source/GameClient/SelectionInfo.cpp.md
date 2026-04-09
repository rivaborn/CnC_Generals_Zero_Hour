# Generals/Code/GameEngine/Source/GameClient/SelectionInfo.cpp

## Purpose
Handles selection logic and context-sensitive commands for game objects.

## Responsibilities
- Determines context commands for new selections
- Manages pick types for selection based on game state
- Translates pick types to object kinds
- Filters drawables for selection

## Key Types
- **SelectionInfo (Class)**: Tracks counts of selected objects by relationship (enemies, friends, civilians, etc.)
- **PickDrawableStruct (Struct)**: Holds selection criteria and target list
- **None**: No other key types

## Key Functions
### contextCommandForNewSelection
- Purpose: Evaluates if a context command should be executed for a new selection.
- Calls: TheGameClient->evaluateContextCommand, TheActionManager->canPlayerGarrison

### getPickTypesForContext
- Purpose: Determines which object types can be picked based on current game state.
- Calls: TheInGameUI->getGUICommand, getPickTypesForCurrentSelection

### getPickTypesForCurrentSelection
- Purpose: Gets pick types for currently selected objects.
- Calls: TheInGameUI->areSelectedObjectsControllable, TheInGameUI->getAllSelectedDrawables

### translatePickTypesToKindof
- Purpose: Converts pick types to a mask of object kinds.
- Calls: None

### addDrawableToList
- Purpose: Filters and adds drawables to a list based on selection criteria.
- Calls: None

## Globals
- **None**: No global/static variables

## Dependencies
- Key includes: PreRTS.h, SelectionInfo.h, ActionManager.h, Damage.h, Player.h, PlayerList.h, ThingTemplate.h, CommandXlat.h, ControlBar.h, Drawable.h, GameClient.h, KeyDefs.h
- External symbols: TheInGameUI, ThePlayerList, TheActionManager, TheGlobalData, TheGameClient, CommandTranslator
