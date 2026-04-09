# GeneralsMD/Code/GameEngine/Include/GameLogic/AI.h

## Purpose
Header file defining core AI systems, including groups, commands, and pathfinding for Command & Conquer Generals.

## Responsibilities
- Declares AI subsystem classes and enums
- Defines command types and parameters
- Provides interfaces for group management and pathfinding
- Contains data structures for AI configuration and side-specific behavior

## Key Types
- **AI (Class)**: Main AI subsystem interface
- **AIGroup (Class)**: Collection of AI-controlled objects
- **AICommandParms (Class)**: Parameters for AI commands
- **TAiData (Class)**: AI configuration data
- **AISideInfo (Class)**: Faction-specific AI settings
- **AICommandType (Enum)**: All possible AI command types
- **AttitudeType (Enum)**: AI behavior modifiers (sleep, passive, normal, etc.)

## Key Functions
### `findClosestEnemy`
- Purpose: Locate nearest enemy object matching criteria
- Calls: Not visible in header

### `createGroup`
- Purpose: Instantiate a new AI group
- Calls: Not visible in header

### `aiDoCommand`
- Purpose: Execute an AI command with given parameters
- Calls: Not visible in header

## Globals
- **TheAI (AI*)**: Singleton AI subsystem instance

## Dependencies
- Common/Snapshot.h, Common/SubsystemInterface.h
- GameLogic/Damage.h, Common/STLTypedefs.h
- Forward declarations for Object, Pathfinder, Player classes
