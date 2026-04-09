# Generals/Code/Libraries/Source/WWVegas/WWLib/stimer.cpp

## Purpose
Implements a system timer class for high-resolution timing using Windows multimedia timer functions.

## Responsibilities
- Provides timer functionality via `SystemTimerClass`
- Converts system time to a scaled value (divided by 16)
- Exposes timer value through operator overloading

## Key Types
- `SystemTimerClass` (Class): Wrapper for Windows multimedia timer functionality

## Key Functions
### `SystemTimerClass::operator ()`
- Purpose: Returns current timer value scaled by 1/16
- Calls: `timeGetTime()`

### `SystemTimerClass::operator long`
- Purpose: Conversion operator returning scaled timer value
- Calls: `timeGetTime()`

## Globals
- None

## Dependencies
- `always.h`, `stimer.h`, `win.h`
- Windows multimedia timer API (`timeGetTime()` from `<mmsystem.h>`)
