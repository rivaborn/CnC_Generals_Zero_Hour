# GeneralsMD/Code/GameEngine/Include/GameClient/CommandXlat.h

## Purpose
Defines command translation and filtering systems for the game client, including GUI command handling and screen filters.

## Responsibilities
- Translates GUI commands into game messages
- Manages screen filters (black & white, motion blur, crossfade)
- Handles unit voice responses for pick-and-play actions
- Tracks mouse drag state for command evaluation

## Key Types
- **GUICommandType (Enum)**: Not inferable.
- **CommandTranslator (Class)**: Translates GUI commands to game messages.
- **CommandEvaluateType (Enum)**: Command evaluation modes (execute, hint, or evaluate only).
- **FilterTypes (Enum)**: Types of screen filters (BW, motion blur, crossfade).
- **FilterModes (Enum)**: Modes for each filter type.
- **PickAndPlayInfo (Class)**: Stores info for pick-and-play unit voice responses.

## Key Functions
### `evaluateForceAttack`
- Purpose: Evaluates force attack command.
- Calls: Not inferable.

### `evaluateContextCommand`
- Purpose: Evaluates context-sensitive commands.
- Calls: Not inferable.

### `translateGameMessage`
- Purpose: Translates game messages (virtual method).
- Calls: Not inferable.

### `pickAndPlayUnitVoiceResponse`
- Purpose: Handles voice responses for pick-and-play actions.
- Calls: Not inferable.

## Globals
- **None**

## Dependencies
- `GameClient/InGameUI.h`
- `GameMessageTranslator` (base class)
- `GameMessage::Type`
- `Drawable`, `Coord3D`, `CommandButton`, `Object` (external types)
