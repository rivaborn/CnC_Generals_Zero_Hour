# GeneralsMD/Code/GameEngine/Include/GameClient/CDCheck.h

## Purpose
Header file for CD presence checking functionality at game start.

## Responsibilities
- Declares CD presence check functions
- Defines callback type for game start
- Provides interface for CD verification

## Key Types
- gameStartCallback (typedef): Function pointer type for game start callbacks

## Key Functions
### IsFirstCDPresent
- Purpose: Checks if the first CD is present in the drive
- Calls: Not inferable

### CheckForCDAtGameStart
- Purpose: Initiates CD check at game start with a callback
- Calls: Not inferable

## Globals
- None

## Dependencies
- Uses `Bool` type (likely from game engine)
- Uses `void` callback pattern
- No external symbols defined here
