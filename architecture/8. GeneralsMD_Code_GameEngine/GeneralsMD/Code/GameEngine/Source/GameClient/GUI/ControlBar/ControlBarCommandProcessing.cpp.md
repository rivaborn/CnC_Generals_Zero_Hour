# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarCommandProcessing.cpp

## Purpose
Handles UI command processing for the control bar in Command & Conquer Generals Zero Hour.

## Responsibilities
- Processes button click messages from the UI
- Validates command preconditions (e.g., money, queue space)
- Dispatches game messages for selected commands
- Manages multi-select and context-sensitive UI states

## Key Types
- **SelectObjectsInfo (struct)**: Holds template and message for object selection

## Key Functions
### `selectObjectOfType`
- Purpose: Selects objects matching a template and adds them to a group
- Calls: `obj->getTemplate()`, `soInfo->msg->appendObjectIDArgument()`, `TheInGameUI->selectDrawable()`

### `ControlBar::processCommandTransitionUI`
- Purpose: Handles button transition messages
- Calls: `switchToContext()`

### `ControlBar::processCommandUI`
- Purpose: Processes button click commands (e.g., build, upgrade, special powers)
- Calls: `TheMessageStream->appendMessage()`, `TheInGameUI->placeBuildAvailable()`, `TheEva->setShouldPlay()`, etc.

## Globals
- None

## Dependencies
- Common: `BuildAssistant`, `Money`, `Player`, `PlayerList`, `Science`, `SpecialPower`, `ThingTemplate`, `Upgrade`, `PlayerTemplate`
- GameClient: `CommandXlat`, `ControlBar`, `Drawable`, `Eva`, `GameClient`, `GadgetPushButton`, `GameWindow`, `GameWindowManager`, `InGameUI`, `AnimateWindowManager`
- GameLogic: `GameLogic`, `Object`, `Module/ProductionUpdate`
