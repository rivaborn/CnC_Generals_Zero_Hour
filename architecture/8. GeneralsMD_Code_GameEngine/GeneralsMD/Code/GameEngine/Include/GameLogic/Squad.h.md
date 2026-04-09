# GeneralsMD/Code/GameEngine/Include/GameLogic/Squad.h

## Purpose
Header defining the `Squad` class, which manages groups of game objects (units, buildings) for team or AI group operations.

## Responsibilities
- Maintains collections of `ObjectID` and `Object*` references.
- Provides methods to add/remove objects and query squad membership.
- Supports serialization via `Snapshot` interface.
- Bridges between `Team` and `AIGroup` affiliations.

## Key Types
- **Squad (Class)**: Manages a group of game objects.
- **VecObjectID (typedef)**: Vector of `ObjectID` for tracking squad members.
- **VecObjectPtr (typedef)**: Vector of `Object*` for cached object references.
- **SquadMagicEnum (Enum)**: Not inferable (placeholder for memory pool glue).

## Key Functions
### `addObject(Object *objectToAdd)`
- Purpose: Adds an object to the squad.
- Calls: Not inferable (implementation in .cpp).

### `removeObject(Object *objectToRemove)`
- Purpose: Removes an object from the squad.
- Calls: Not inferable.

### `squadFromTeam(const Team* fromTeam, Bool clearSquadFirst)`
- Purpose: Populates the squad with members of a team.
- Calls: Not inferable.

### `squadFromAIGroup(const AIGroup* fromAIGroup, Bool clearSquadFirst)`
- Purpose: Populates the squad from an AI group.
- Calls: Not inferable.

### `aiGroupFromSquad(AIGroup* aiGroupToFill)`
- Purpose: Creates an AI group from the squadâs members.
- Calls: Not inferable.

## Globals
- **None**

## Dependencies
- `Common/Snapshot.h` (for serialization)
- `Common/GameMemory.h` (for `Memory
