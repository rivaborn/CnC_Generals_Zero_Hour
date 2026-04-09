# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/_timer.cpp

## Purpose
Manages game timing mechanisms, including frame timing and tick counting.

## Responsibilities
- Provides frame timer synchronized between processes
- Maintains global tick count timer
- Uses system timer class as base implementation

## Key Types
None

## Key Functions
None

## Globals
- FrameTimer (CDTimerClass<SystemTimerClass>): Synchronized game frame timer
- TickCount (TTimerClass<SystemTimerClass>): Global tick count timer object

## Dependencies
- `always.h`
- `Timer.h`
- `SystemTimerClass` (external)
- `CDTimerClass` (external)
- `TTimerClass` (external)
