# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/AssaultTransportAIUpdate.cpp

## Purpose
Manages AI behavior for assault transport vehicles (troop crawlers) to deploy troops, order attacks, and handle healing/retrieval.

## Responsibilities
- Tracks transport occupants and their status (wounded/healthy/new)
- Deploys troops when in attack range
- Orders wounded troops to return for healing
- Handles attack-move and attack-object commands
- Manages transport positioning relative to combat

## Key Types
- **AssaultTransportAIUpdate (Class)**: Main AI update class for assault transports
- **AssaultStateTypes (Enum)**: State machine states (IDLE, etc.)
- **AssaultTransportAIUpdateModuleData (Struct)**: Configuration data for the module

## Key Functions
### `aiDoCommand`
- Purpose: Handles player/AI commands for the transport
- Calls: `reset()`, `AIUpdateInterface::aiDoCommand()`

### `update`
- Purpose: Main update loop for transport AI logic
- Calls: `TheGameLogic->findObjectByID()`, `aiExit()`, `aiEnter()`, `aiAttackObject()`, `AIUpdateInterface::update()`

### `isMemberWounded`
- Purpose: Checks if a member needs healing
- Calls: `getBodyModule()`, `getHealth()`, `getMaxHealth()`

### `giveFinalOrders`
- Purpose: Transfers attack orders to troops when transport dies
- Calls: `TheGameLogic->findObjectByID()`, `aiAttackObject()`, `aiAttackMoveToPosition()`

## Globals
- **MAX_TRANSPORT_SLOTS (const int)**: Maximum number of transportable units

## Dependencies
- `AIUpdateInterface`, `ContainModuleInterface`, `BodyModuleInterface`
- `TheGameLogic`, `ThePartitionManager`
- Game command constants (AICMD_*)
