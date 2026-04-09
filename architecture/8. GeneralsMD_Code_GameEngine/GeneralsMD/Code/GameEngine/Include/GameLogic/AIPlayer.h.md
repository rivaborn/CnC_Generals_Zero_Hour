# GeneralsMD/Code/GameEngine/Include/GameLogic/AIPlayer.h

## Purpose
Header defining the AIPlayer class and related structures for computer-controlled opponent behavior in Generals Zero Hour.

## Responsibilities
- Manages AI player logic including base building, team training, and resource management
- Handles production queues, team reinforcement, and structure repair
- Implements difficulty-based decision making
- Tracks AI state and coordinates with game objects

## Key Types
- **WorkOrder (Class)**: Represents a unit production task in the build queue
- **TeamInQueue (Class)**: Tracks teams being built or waiting to deploy
- **AIPlayer (Class)**: Main AI controller managing all automated player behavior
- **BuildListInfo (Class)**: External reference for build planning (forward declared)
- **INVALID_SKILLSET_SELECTION (Enum)**: Constant for invalid skillset selection

## Key Functions
### `update()`
- Purpose: Main simulation loop for AI behavior
- Calls: `doBaseBuilding`, `checkReadyTeams`, `checkQueuedTeams`, `doTeamBuilding`, `doUpgradesAndSkills`

### `buildSpecificAITeam()`
- Purpose: Immediately builds a specified team prototype
- Calls: `startTraining`, `isAGoodIdeaToBuildTeam`

### `repairStructure()`
- Purpose: Initiates repair of a damaged structure
- Calls: `findDozer`, queue management functions

### `selectTeamToBuild()`
- Purpose: Determines next team to build based on game state
- Calls: `isPossibleToBuildTeam`, `isAGoodIdeaToBuildTeam`

## Globals
- **MAX_STRUCTURES_TO_REPAIR (Enum)**: Constant for max repair queue size

## Dependencies
- `Common/GameMemory.h`, `Common/Snapshot.h`
- `Player`, `Object`, `Team`, `TeamPrototype`, `ThingTemplate` classes
- `AsciiString`, `Coord3D`, `ObjectID`, `Region2D` types
- Memory pool and snapshot system infrastructure
