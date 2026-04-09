# GeneralsMD/Code/GameEngine/Include/GameClient/DrawGroupInfo.h

## Purpose
Defines the `DrawGroupInfo` structure for configuring text rendering properties in the game.

## Responsibilities
- Stores font properties (name, size, bold)
- Manages text color and drop shadow settings
- Handles pixel/percentage-based text positioning
- Provides INI parsing support via `FieldParse` table

## Key Types
- **DrawGroupInfo (Class)**: Container for text rendering configuration.
- **anonymous union (Class)**: Allows switching between pixel/percentage X offset.
- **anonymous union (Class)**: Allows switching between pixel/percentage Y offset.

## Key Functions
### `DrawGroupInfo()`
- Purpose: Constructor for `DrawGroupInfo`.
- Calls: Not inferable.

### `getFieldParse()`
- Purpose: Returns the INI parsing table for `DrawGroupInfo`.
- Calls: Not inferable.

## Globals
- **TheDrawGroupInfo (DrawGroupInfo*)**: Global instance of `DrawGroupInfo`.

## Dependencies
- `AsciiString`, `Int`, `Bool`, `Color`, `Real` (types)
- `FieldParse` (external parsing structure)
- Likely depends on INI parsing infrastructure for `s_fieldParseTable`.
