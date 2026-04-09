# GeneralsMD/Code/GameEngine/Include/GameClient/DisplayStringManager.h

## Purpose
Manages creation and lifecycle of display strings in the game client.

## Responsibilities
- Factory for creating and freeing display strings
- Maintains a linked list of active display strings
- Provides specialized strings (group numerals, formation letters)
- Handles initialization, reset, and update cycles

## Key Types
- **DisplayStringManager (Class)**: Factory for managing display strings
- **DisplayString (Class)**: Managed string type (defined elsewhere)

## Key Functions
### DisplayStringManager::newDisplayString
- Purpose: Allocate a new display string
- Calls: None (pure virtual)

### DisplayStringManager::freeDisplayString
- Purpose: Free a display string
- Calls: unLink

### DisplayStringManager::link
- Purpose: Add a display string to the manager's list
- Calls: None

### DisplayStringManager::unLink
- Purpose: Remove a display string from the manager's list
- Calls: None

## Globals
- **TheDisplayStringManager (DisplayStringManager*)**: Singleton instance of the manager

## Dependencies
- `SubsystemInterface` (base class)
- `DisplayString` (managed type)
- Common game engine interfaces
