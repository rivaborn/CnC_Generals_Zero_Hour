# Generals/Code/Libraries/Source/WWVegas/WWLib/stimer.h

## Purpose
Defines timer constants and a system timer class for the game engine.

## Responsibilities
- Declares timer-related constants (seconds, minutes, ticks).
- Defines a `SystemTimerClass` for querying system time.
- Provides fade palette timing constants.

## Key Types
- **SystemTimerClass (Class)**: Wrapper for system time retrieval.

## Key Functions
### `SystemTimerClass::operator()`
- Purpose: Returns the current system time as a long integer.
- Calls: Not inferable (implementation in .cpp).

### `SystemTimerClass::operator long`
- Purpose: Conversion operator to long for system time.
- Calls: Not inferable (implementation in .cpp).

## Globals
- **TIMER_SECOND (const)**: 60 ticks per second.
- **TIMER_MINUTE (const)**: 60 * TIMER_SECOND.
- **FADE_PALETTE_FAST (const)**: Fast fade time (TIMER_SECOND/8).
- **FADE_PALETTE_MEDIUM (const)**: Medium fade time (TIMER_SECOND/4).
- **FADE_PALETTE_SLOW (const)**: Slow fade time (TIMER_SECOND/2).
- **TICKS_PER_SECOND (const)**: 15 ticks per second.
- **TICKS_PER_MINUTE (const)**: 15 * 60.
- **TICKS_PER_HOUR (const)**: TICKS_PER_MINUTE * 60.
- **GRAYFADETIME (const)**: 1 second for gray fade.

## Dependencies
- None (header-only, no includes).
