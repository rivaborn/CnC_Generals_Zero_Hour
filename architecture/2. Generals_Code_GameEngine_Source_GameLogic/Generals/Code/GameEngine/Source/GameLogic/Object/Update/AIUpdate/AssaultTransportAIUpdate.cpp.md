# Generals/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/AssaultTransportAIUpdate.cpp

## Purpose
This file implements the AI logic for assault transports, managing troop deployment, attack orders, and return to transport.

## Responsibilities
- Manages state transitions for assault transport AI.
- Handles commands to deploy troops, order them to attack, and retrieve them.
- Ensures wounded troops are healed before rejoining combat.
- Updates positions and statuses of transported troops.

## Key Types
- **AssaultTransportAIUpdate (Class)**: Manages the AI logic for assault transports.
- **Coord3D (Struct)**: Represents 3D coordinates.
- **ObjectID (Type)**: Unique identifier for game objects.

## Key Functions
### calcSleepTime
- Purpose: Determines the sleep time for updates.
- Calls: None

### aiDoCommand
- Purpose: Processes AI commands to reset state and handle attack orders.
- Calls: `reset`, `aiAttackMoveToPosition`

### update
- Purpose: Updates the transport's state, manages troop deployment, and handles combat logic.
- Calls: `TheGameLogic->findObjectByID`, `getContain`, `setAllowedToChase`, `aiExit`, `aiEnter`, `aiAttackObject`, `aiAttackMoveToPosition`

## Globals
- None

## Dependencies
- **Common/Player.h**
- **Common/ThingFactory.h**
- **GameClient/Drawable.h**
- **GameLogic/ExperienceTracker.h**
- **GameLogic/Module/BodyModule.h**
- **GameLogic/Module/ContainModule.h**
- **GameLogic/Module/AssaultTransportAIUpdate.h**
- **GameLogic/Module/PhysicsUpdate.h**
- **GameLogic/Object.h**
- **GameLogic/PartitionManager.h**
- **GameLogic/Weapon.h**
