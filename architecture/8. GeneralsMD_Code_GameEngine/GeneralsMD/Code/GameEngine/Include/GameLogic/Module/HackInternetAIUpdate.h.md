# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/HackInternetAIUpdate.h

## Purpose
Defines the AI state machine and interface for the "Hack Internet" ability, which generates cash for the player.

## Responsibilities
- Manages state transitions for hacking, packing, and unpacking animations
- Handles cash generation based on unit rank
- Provides interface for querying hacking state
- Configures timing and cash amounts via module data

## Key Types
- **HackInternetStateMachine (Class)**: Base state machine for hacking behavior
- **HackInternetState (Class)**: State for active cash hacking
- **PackingState (Class)**: State for packing up after hacking
- **UnpackingState (Class)**: State for setting up before hacking
- **HackInternetAIUpdateModuleData (Class)**: Configuration data for hacking parameters
- **HackInternetAIInterface (Class)**: Interface for querying hacking status
- **HackInternetAIUpdate (Class)**: Main AI update module implementing hacking logic

## Key Functions
### `aiDoCommand`
- Purpose: Processes AI commands for hacking behavior
- Calls: Not inferable

### `update`
- Purpose: Updates hacking state machine and handles cash generation
- Calls: Not inferable

### `hackInternet`
- Purpose: Initiates the hacking sequence
- Calls: Not inferable

### `makeStateMachine`
- Purpose: Creates the state machine instance
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/StateMachine.h`
- `GameLogic/Module/AIUpdate.h`
- `AIStateMachine`, `State`, `AIUpdateInterface`, `AIUpdateModuleData`, `AICommandParms`, `Xfer`, `MultiIniFieldParse`, `INI`
