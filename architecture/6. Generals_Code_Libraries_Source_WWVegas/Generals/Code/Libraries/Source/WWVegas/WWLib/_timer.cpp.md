# Generals/Code/Libraries/Source/WWVegas/WWLib/_timer.cpp

## Purpose
Manages game timing and tick counting using timer classes.

## Responsibilities
- Declares and initializes global frame timer
- Declares and initializes global tick counter
- Provides timing infrastructure for game loop synchronization

## Key Types
None

## Key Functions
None

## Globals
- FrameTimer (CDTimerClass<SystemTimerClass>): Synchronized game frame timer
- TickCount (TTimerClass<SystemTimerClass>): Global tick counter initialized to 0

## Dependencies
- "always.h"
- "timer.h" (inferred from class usage)
- SystemTimerClass (external timer implementation)
- CDTimerClass (template timer class)
- TTimerClass (template timer class)
