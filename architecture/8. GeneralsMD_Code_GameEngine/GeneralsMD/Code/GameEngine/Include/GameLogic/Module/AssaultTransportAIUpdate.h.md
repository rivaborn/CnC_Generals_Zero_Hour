# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/AssaultTransportAIUpdate.h

## Purpose
Defines the AI logic for assault transport units (troop crawlers) to deploy troops, manage assaults, and handle troop healing/retrieval.

## Responsibilities
- Manages assault transport state machine (IDLE/ASSAULTING)
- Handles troop deployment, healing, and retrieval
- Controls assault execution and final orders
- Provides interface for beginning assaults

## Key Types
- **AssaultStateTypes (Enum)**: Defines transport states (IDLE, ASSAULTING)
- **AssaultTransportAIUpdateModuleData (Class)**: Module configuration data
- **AssaultTransportAIInterface (Class)**: Interface for assault initiation
- **AssaultTransportAIUpdate (Class)**: Main AI update module for assault transports

## Key Functions
### AssaultTransportAIUpdate::aiDoCommand
- Purpose: Handles AI commands for the transport
- Calls: Not inferable

### AssaultTransportAIUpdate::update
- Purpose: Updates transport AI state
- Calls: Not inferable

### AssaultTransportAIUpdate::beginAssault
- Purpose: Initiates an assault sequence
- Calls: Not inferable

### AssaultTransportAIUpdate::retrieveMembers
- Purpose: Retrieves troops back to transport
- Calls: Not inferable

### AssaultTransportAIUpdate::giveFinalOrders
- Purpose: Issues final orders to troops
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/StateMachine.h`
- `GameLogic/Module/AIUpdate.h`
- `MultiIniFieldParse`, `INI` (for configuration parsing)
