# GeneralsMD/Code/Libraries/Source/profile/internal_cmd.h

## Purpose
Defines the `ProfileCmdInterface` class for handling profile-related debug commands in the SAGE engine.

## Responsibilities
- Manages registration and execution of profile result functions
- Provides command execution interface for debug commands
- Handles command argument parsing and result processing

## Key Types
- **ProfileCmdInterface (Class)**: Interface for profile command execution and result handling
- **Factory (Struct)**: Holds function pointer, name, and argument for result function registration
- **Debug (Class)**: Base debug interface (external)

## Key Functions
### `AddResultFunction`
- Purpose: Registers a profile result function with the interface
- Calls: None (static method)

### `RunResultFunctions`
- Purpose: Executes all registered result functions
- Calls: None

### `Execute`
- Purpose: Processes debug commands and routes them to appropriate handlers
- Calls: `RunResultFunctions`

## Globals
- **numResIf (unsigned)**: Tracks number of registered result interfaces
- **resIf (Factory*)**: Array of registered result function factories
- **numResFunc (unsigned)**: Count of active result functions (volatile due to optimizer bug)

## Dependencies
- `DebugCmdInterface` (base class)
- `ProfileResultInterface` (external)
- `Debug` (external debug interface)
