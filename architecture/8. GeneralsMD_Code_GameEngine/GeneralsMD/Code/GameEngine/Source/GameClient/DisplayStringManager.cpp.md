# GeneralsMD/Code/GameEngine/Source/GameClient/DisplayStringManager.cpp

## Purpose
Manages a linked list of game display strings, providing linking/unlinking functionality.

## Responsibilities
- Maintains a master list of display strings
- Provides methods to link/unlink strings
- Ensures proper list integrity via assertions

## Key Types
- DisplayStringManager (Class): manages display string list
- DisplayString (Class): individual display string node (defined elsewhere)

## Key Functions
### DisplayStringManager::link
- Purpose: Adds a display string to the master list
- Calls: None

### DisplayStringManager::unLink
- Purpose: Removes a display string from the master list
- Calls: None

## Globals
- TheDisplayStringManager (DisplayStringManager*): singleton instance

## Dependencies
- "GameClient/DisplayStringManager.h"
- "PreRTS.h"
- assert() for debugging checks
