# Generals/Code/GameEngine/Source/GameClient/MessageStream/GUICommandTranslator.cpp

## Purpose
Handles translation of GUI-initiated commands (e.g., weapon firing, guard, rally points) into game messages.

## Responsibilities
- Processes mouse clicks for pending GUI commands
- Validates target objects under cursor
- Constructs and sends game messages for various commands
- Manages command completion status

## Key Types
- **CommandStatus (Enum)**: Command execution state (incomplete/complete)
- **PickAndPlayInfo (Struct)**: Holds weapon/special power context for voice responses

## Key Functions
### `validUnderCursor`
- Purpose: Checks if object under cursor is valid for given command
- Calls: `TheTacticalView->pickDrawable`, `command->isValidObjectTarget`

### `doFireWeaponCommand`
- Purpose: Handles weapon firing commands (at location/object)
- Calls: `TheMessageStream->appendMessage`, `validUnderCursor`, `TheTacticalView->screenToTerrain`

### `doGuardCommand`
- Purpose: Processes guard commands (at object/position)
- Calls: `TheMessageStream->appendMessage`, `validUnderCursor`, `pickAndPlayUnitVoiceResponse`

### `doAttackMoveCommand`
- Purpose: Executes attack-move command
- Calls: `TheMessageStream->appendMessage`, `TheTacticalView->screenToTerrain`, `pickAndPlayUnitVoiceResponse`

### `doSetRallyPointCommand`
- Purpose: Sets rally point for selected structure
- Calls: `TheMessageStream->appendMessage`, `TheTacticalView->screenToTerrain`

### `doPlaceBeacon`
- Purpose: Places beacon at mouse position
- Calls: `TheMessageStream->appendMessage`, `TheTacticalView->screenToTerrain`

### `translateGameMessage`
- Purpose: Main message handler for GUI commands
- Calls: All command functions above, `TheInGameUI->getGUICommand`, `TheInGameUI->setGUICommand`

## Globals
- **TheTacticalView**: Access to view/picking system
- **TheInGameUI**: UI state and selection management
- **TheMessageStream**: Game message system
- **ThePlayerList**: Player data access

## Dependencies
- `GameMessage`, `CommandButton`, `Drawable`, `Object`, `Coord3D`, `ICoord2D`
- `GameAudio.h`, `ActionManager.h`, `Player.h`, `SpecialPower.h`
