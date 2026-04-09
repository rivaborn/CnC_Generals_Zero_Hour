# GeneralsMD/Code/GameEngine/Include/Common/FunctionLexicon.h

## Purpose
Manages collections of function pointers for callback management in the game engine.

## Responsibilities
- Maintains lookup tables for various game window and layout callbacks
- Provides methods to retrieve function pointers by name key
- Validates uniqueness of function entries
- Supports different callback types (system, input, tooltip, draw, layout)

## Key Types
- **FunctionLexicon (Class)**: Main class managing function pointer tables
- **TableEntry (Struct)**: Contains name key, function name, and function pointer
- **TableIndex (Enum)**: Defines indices for different function tables (game window system/input/tooltip/draw, window layout init/update/shutdown)

## Key Functions
### `findFunction`
- Purpose: Finds a function pointer by name key, optionally limited to a specific table
- Calls: `keyToFunc`

### `loadTable`
- Purpose: Loads a lookup table with runtime values
- Calls: None visible

### `validate`
- Purpose: Validates that all entries in the tables are unique
- Calls: None visible

## Globals
- **TheFunctionLexicon (FunctionLexicon*)**: Global instance of the function lexicon

## Dependencies
- `SubsystemInterface.h`
- `NameKeyGenerator.h`
- `GameMemory.h`
- `GameWindow.h`
- `WindowLayout.h`
- Function types: `GameWinSystemFunc`, `GameWinInputFunc`, `GameWinTooltipFunc`, `GameWinDrawFunc`, `WindowLayoutInitFunc`, `WindowLayoutUpdateFunc`, `WindowLayoutShutdownFunc`
