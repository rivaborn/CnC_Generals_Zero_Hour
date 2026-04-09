# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/systimer.cpp

## Purpose
Manages system timing with millisecond precision for the game engine.

## Responsibilities
- Initializes and cleans up Windows timer resolution
- Provides time measurement utilities
- Tracks timer wrap-around
- Detects timer overflow conditions

## Key Types
- SysTimeClass (Class): System timer wrapper for millisecond-precision timing

## Key Functions
### SysTimeClass::SysTimeClass
- Purpose: Constructor that sets Windows timer resolution to 1ms
- Calls: `timeBeginPeriod(1)`

### SysTimeClass::~SysTimeClass
- Purpose: Destructor that restores default timer resolution
- Calls: `timeEndPeriod(1)`

### SysTimeClass::Reset
- Purpose: Resets the timer to current system time
- Calls: `timeGetTime()`

### SysTimeClass::Is_Getting_Late
- Purpose: Checks if timer is approaching overflow (signed max value)
- Calls: None

## Globals
- SystemTime (SysTimeClass): Global timer instance

## Dependencies
- `systimer.h` (header)
- Windows API: `timeBeginPeriod`, `timeEndPeriod`, `timeGetTime`
