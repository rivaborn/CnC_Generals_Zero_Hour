# GeneralsMD/Code/GameEngine/Source/Common/System/Snapshot.cpp

## Purpose
Base class for data structures involved in game saves, loads, and CRC checks.

## Responsibilities
- Defines the Snapshot class interface
- Provides default constructor and destructor
- Manages snapshot lifecycle during game state operations

## Key Types
- Snapshot (Class): base class for serializable game data structures

## Key Functions
### Snapshot::Snapshot()
- Purpose: Default constructor for Snapshot class
- Calls: None

### Snapshot::~Snapshot()
- Purpose: Destructor that handles cleanup during game loading
- Calls: None (commented-out call to TheGameState->notifySnapshotDeleted())

## Globals
- None

## Dependencies
- "PreRTS.h" (include)
- "Common/GameState.h" (include)
- "Common/Snapshot.h" (include)
- TheGameState (external symbol)
