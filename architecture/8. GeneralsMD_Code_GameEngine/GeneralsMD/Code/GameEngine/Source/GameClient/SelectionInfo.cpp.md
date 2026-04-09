# GeneralsMD/Code/GameEngine/Source/GameClient/SelectionInfo.cpp

## Purpose
Handles selection logic and context-sensitive commands for game objects.

## Responsibilities
- Determines context commands for new selections
- Manages pick types for selection based on game state
- Filters drawables for selection based on visibility and relationships
- Tracks counts of selected objects by relationship (friendly/enemy/civilian)

## Key Types
- **SelectionInfo (Class)**: Tracks counts of selected objects by type/relationship
- **PickDrawableStruct (Class)**: Helper struct for drawable filtering during selection
- **KindOfMaskType (Type)**: Bitmask for object type filtering

## Key Functions
### contextCommandForNewSelection
- Purpose: Evaluates if a context command should be executed for a new selection
- Calls: TheGameClient->evaluateContextCommand, TheInGameUI->isInForceAttackMode, TheInGameUI->isInPreferSelectionMode

### getPickTypesForContext
- Purpose: Determines which object types can be picked based on current game state
- Calls: getPickTypesForCurrentSelection, TheInGameUI->getGUICommand

### getPickTypesForCurrentSelection
- Purpose: Gets pick types based on currently selected objects' capabilities
- Calls: TheInGameUI->areSelectedObjectsControllable, TheInGameUI->getAllSelectedDrawables

### translatePickTypesToKindof
- Purpose: Converts pick type flags to KindOf bitmask
- Calls: None

### addDrawableToList
- Purpose: Filters and adds drawables to selection list based on visibility and relationships
- Calls: draw->getTemplate()->isAnyKindOf, draw->isSelectable, obj->getContainedBy()->getContain

## Globals
- None

## Dependencies
- GameLogic/Damage.h, GameLogic/Module/ContainModule.h
- Common/ActionManager.h, Common/ThingTemplate.h, Common/PlayerList.h, Common/Player.h
- GameClient/SelectionInfo.h, GameClient/CommandXlat.h, GameClient/ControlBar.h, GameClient/GameClient.h, GameClient/Drawable.h, GameClient/KeyDefs.h
