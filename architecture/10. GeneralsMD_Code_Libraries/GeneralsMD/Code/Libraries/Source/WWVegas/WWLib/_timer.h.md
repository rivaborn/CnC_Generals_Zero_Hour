# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/_timer.h

## Purpose
Header file declaring global timer objects for frame timing and tick counting in the SAGE engine.

## Responsibilities
- Declares global timer instances for frame timing and tick counting
- Provides access to timing utilities for game loop and AI systems
- Serves as an interface for timer-related functionality

## Key Types
None

## Key Functions
None

## Globals
- FrameTimer (CDTimerClass<SystemTimerClass>): Tracks frame timing for the game loop
- TickCount (TTimerClass<SystemTimerClass>): Counts game ticks for timing and synchronization

## Dependencies
- `stimer.h`: For CDTimerClass template
- `timer.h`: For TTimerClass template and SystemTimerClass
- External timer class implementations (not defined here)
