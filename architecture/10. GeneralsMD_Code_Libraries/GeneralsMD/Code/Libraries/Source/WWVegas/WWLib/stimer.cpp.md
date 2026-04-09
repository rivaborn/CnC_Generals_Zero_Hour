# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/stimer.cpp

## Purpose
Implements a system timer class for the game engine, providing time measurement functionality.

## Responsibilities
- Converts system time into a game-usable time value.
- Provides operator overloads for time retrieval.
- Interfaces with the Windows time API.

## Key Types
- SystemTimerClass (Class): wraps system time functionality for the game.

## Key Functions
### SystemTimerClass::operator long
- Purpose: Returns the current system time divided by 16.
- Calls: TIMEGETTIME()

### SystemTimerClass::operator ()
- Purpose: Returns the current system time divided by 16.
- Calls: TIMEGETTIME()

## Globals
None

## Dependencies
- "always.h", "stimer.h", "win.h", "systimer.h"
- TIMEGETTIME() (external Windows API function)
