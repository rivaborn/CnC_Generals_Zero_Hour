# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/stimer.h

## Purpose
Defines timer constants and a system timer class for the game engine.

## Responsibilities
- Declares timer-related constants (e.g., TIMER_SECOND, TICKS_PER_SECOND).
- Provides a `SystemTimerClass` for system timing operations.
- Defines fade palette timing constants.

## Key Types
- **SystemTimerClass (Class)**: Wrapper for system timing operations.

## Key Functions
### SystemTimerClass::operator()
- Purpose: Allows the timer to be used in expressions returning a long.
- Calls: None visible.

### SystemTimerClass::operator long()
- Purpose: Conversion operator to long for the timer value.
- Calls: None visible.

## Globals
- **TIMER_SECOND (const)**: 60 ticks per second.
- **TIMER_MINUTE (const)**: 60 seconds in minutes.
- **FADE_PALETTE_FAST/MEDIUM/SLOW (const)**: Fade timing constants.
- **TICKS_PER_SECOND/MINUTE/HOUR (const)**: Game tick rate constants.
- **GRAYFADETIME (const)**: Gray fade duration.

## Dependencies
- None (header-only, no includes).
