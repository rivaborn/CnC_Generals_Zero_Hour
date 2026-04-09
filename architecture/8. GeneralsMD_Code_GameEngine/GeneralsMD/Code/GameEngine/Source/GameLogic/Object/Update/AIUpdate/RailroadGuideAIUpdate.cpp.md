# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/RailroadGuideAIUpdate.cpp

## Purpose
Implements railroad train behavior, including track following, collision handling, and train management.

## Responsibilities
- Manages train movement along predefined tracks
- Handles collisions with other objects
- Controls train physics and sound effects
- Manages train coupling/decoupling
- Implements station stopping and passenger handling

## Key Types
- **RailroadBehaviorModuleData (Class)**: Contains configuration data for railroad behavior
- **RailroadBehavior (Class)**: Main behavior class for railroad objects
- **PullInfo (Struct)**: Stores information about train pulling mechanics
- **PartitionFilterIsValidCarriage (Class)**: Filter for valid carriage objects
- **ConductorState (Enum)**: States for train conductor logic
- **StationTask (Enum)**: Tasks for station handling

## Key Functions
### alignToTerrain
- Purpose: Aligns object to terrain surface
- Calls: Not inferable

### PartitionFilterIsValidCarriage/allow
- Purpose: Determines if an object is a valid carriage
- Calls: Not inferable

## Globals
- **INVALID_PATH (Int)**: Constant for invalid path value

## Dependencies
- Common/Player.h
- Common/ThingFactory.h
- GameLogic/Locomotor.h
- GameLogic/Module/RailroadGuideAIUpdate.h
- GameLogic/Object.h
- GameLogic/PartitionManager.h
- GameClient/Drawable.h
- GameClient/Statistics.h
