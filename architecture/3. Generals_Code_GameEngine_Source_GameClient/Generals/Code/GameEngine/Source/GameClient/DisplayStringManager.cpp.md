# Generals/Code/GameEngine/Source/GameClient/DisplayStringManager.cpp

## Purpose
Manages a linked list of display strings for the game client.

## Responsibilities
- Maintains a master list of display strings
- Provides linking/unlinking functionality for display strings
- Ensures proper cleanup of the string list

## Key Types
- DisplayStringManager (Class): manages display strings
- DisplayString (Class): individual display string (defined elsewhere)

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
- DisplayString class (external)
