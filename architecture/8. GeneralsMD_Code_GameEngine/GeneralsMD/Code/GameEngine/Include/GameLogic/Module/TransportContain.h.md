# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/TransportContain.h

## Purpose
Defines the transport containment module for units that can carry other objects (e.g., vehicles carrying troops).

## Responsibilities
- Manages transport capacity and exit behavior
- Handles rider upgrades and exit timing
- Provides container validation and state tracking
- Implements capture/removal logic for contained objects

## Key Types
- **TransportContainModuleData (Class)**: Configuration data for transport behavior (capacity, exit settings, etc.)
- **InitialPayload (Struct)**: Stores initial cargo (object name and count)
- **TransportContain (Class)**: Core transport containment logic
- **TransportContainMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **TransportContain_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### `isValidContainerFor`
- Purpose: Checks if an object can be contained by this transport
- Calls: Not inferable

### `onCapture`
- Purpose: Handles ejection of riders when transport is captured
- Calls: Not inferable

### `update`
- Purpose: Frame update for transport logic (exit timing, etc.)
- Calls: Not inferable

### `reserveDoorForExit`
- Purpose: Reserves an exit door for a rider leaving the transport
- Calls: Not inferable

## Globals
- None

## Dependencies
- `OpenContain.h` (base class)
- `MultiIniFieldParse`, `INI` (INI parsing)
- `AsciiString`, `Real`, `Bool`, `Int`, `UnsignedInt` (primitives)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`, `MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
