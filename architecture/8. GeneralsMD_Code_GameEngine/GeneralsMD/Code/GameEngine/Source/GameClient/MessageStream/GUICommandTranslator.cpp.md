# GeneralsMD/Code/GameEngine/Source/GameClient/MessageStream/GUICommandTranslator.cpp

## Purpose
Handles translation of GUI-initiated game commands (e.g., weapon firing, guard, rally points) into game messages.

## Responsibilities
- Processes mouse clicks for pending GUI commands
- Validates target objects/positions under cursor
- Constructs and sends game messages for various commands
- Manages command completion status

## Key Types
- **CommandStatus (Enum)**: Command execution state (incomplete/complete)
- **PickAndPlayInfo (Struct)**: Holds weapon/special power command data

## Key Functions
### `validUnderCursor`
- Purpose: Checks if object under cursor is valid for given command
- Calls: `TheTacticalView->pickDrawable`, `command->isValidObjectTarget`

### `doFireWeaponCommand`
- Purpose: Handles weapon firing commands (at location/object)
- Calls: `TheMessageStream->appendMessage`, `validUnderCursor`

### `doGuardCommand`
- Purpose: Processes guard commands (at object/position)
- Calls: `TheMessageStream->appendMessage`, `validUnderCursor`

### `doAttackMoveCommand`
- Purpose: Executes attack-move command
- Calls: `TheTacticalView->screenToTerrain`, `TheMessageStream->appendMessage`

### `doSetRallyPointCommand`
- Purpose: Sets rally point for selected structure
- Calls: `TheTacticalView->screenToTerrain`, `TheMessageStream->appendMessage`

### `doPlaceBeacon`
- Purpose: Places beacon at mouse position
- Calls: `TheTacticalView->screenToTerrain`, `TheMessageStream->appendMessage`

### `translateGameMessage`
- Purpose: Main message handler for GUI commands
- Calls: All command functions above, `TheInGameUI->setGUICommand`

## Globals
- **TheTacticalView (TacticalView)**: View for world-to-screen conversion
- **TheInGameUI (InGameUI)**: UI state and selection management
- **TheMessageStream (MessageStream)**: Game message system
- **ThePlayerList (PlayerList)**: Player management

## Dependencies
- `GameMessage`, `CommandButton`, `Object`, `Drawable`, `Coord3D`
- `GameAudio`, `Geometry`, `SpecialPower` systems
- `ActionManager`, `NameKeyGenerator` utilities
