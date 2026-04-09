# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/RailroadGuideAIUpdate.h

## Purpose
Defines the RailroadBehavior class and related structures for train AI in the game.

## Responsibilities
- Manages train movement along tracks
- Handles train physics and collisions
- Controls train station behavior and passenger disembarking
- Manages train carriage hitching and detachment
- Handles audio events for train sounds

## Key Types
- **RailroadBehaviorModuleData (Class)**: Contains configuration data for train behavior
- **TrackPoint (Struct)**: Represents a point on the train track with position and flags
- **TrainTrack (Struct)**: Manages a list of track points and reference counting
- **RailroadBehavior (Class)**: Main AI behavior class for trains
- **ConductorState (Enum)**: States for train movement control (braking, waiting, accelerating, coasting)
- **StationTask (Enum)**: Tasks to perform at stations (do nothing, disembark)

## Key Functions
### RailroadBehaviorModuleData::buildFieldParse
- Purpose: Registers INI field parsers for train configuration data
- Calls: PhysicsBehaviorModuleData::buildFieldParse

### RailroadBehavior::update
- Purpose: Main update function for train AI logic
- Calls: Not inferable from header

### RailroadBehavior::onCollide
- Purpose: Handles collision events for trains
- Calls: Not inferable from header

### RailroadBehavior::getPulled
- Purpose: Provides information about how this train car is being pulled
- Calls: Not inferable from header

## Globals
- None

## Dependencies
- "GameLogic/Module/AIUpdate.h"
- "GameLogic/Module/PhysicsUpdate.h"
- Waypoint class (forward reference)
- std::vector, std::list
- INI parsing utilities
- AudioEventRTS class
- Coord3D class
- ObjectID, WaypointID types
