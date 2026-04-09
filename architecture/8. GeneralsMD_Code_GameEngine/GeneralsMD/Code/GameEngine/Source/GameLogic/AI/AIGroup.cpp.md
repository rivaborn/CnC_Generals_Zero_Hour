# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/AIGroup.cpp

## Purpose
Manages groups of AI-controlled objects in the game, handling their collective behavior, movement, and commands.

## Responsibilities
- Maintains a list of group members and their properties
- Coordinates group actions (movement, attacks, commands)
- Computes group statistics (speed, center position)
- Handles group-level commands and special abilities

## Key Types
- AIGroup (Class): Manages a group of AI-controlled objects
- AIUpdateInterface (Interface): Provides AI-related functionality for objects
- CommandButton (Class): Represents a command that can be issued to the group

## Key Functions
### clampToMap
- Purpose: Adjusts a position to ensure it lies within the map boundaries
- Calls: Not inferable

### clampWaypointPosition
- Purpose: Adjusts a waypoint position to ensure it's valid for pathfinding
- Calls: Not inferable

### getHelicopterOffset
- Purpose: Calculates an offset for helicopter positioning
- Calls: Not inferable

### makeMemberStop
- Purpose: Makes a group member stop its current action
- Calls: Not inferable

## Globals
- PATH_DIAMETER_IN_CELLS (Int): Defines the diameter of a path in cells
- STD_WAYPOINT_CLAMP_MARGIN (Int): Standard margin for waypoint clamping
- STD_AIRCRAFT_EXTRA_MARGIN (Int): Extra margin for aircraft waypoints
- CIRCLE (Coord3D): Predefined circle coordinates

## Dependencies
- Common/ActionManager.h
- Common/Player.h
- GameLogic/AI.h
- GameLogic/AIPathfind.h
- GameLogic/Module/AIUpdate.h
- GameClient/ControlBar.h
- GameClient/Drawable.h
