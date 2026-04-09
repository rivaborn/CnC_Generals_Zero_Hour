# Generals/Code/Libraries/Source/WWVegas/WWLib/timer.h

## Purpose
Provides timer utility classes for game timing operations, including basic, pausable, and countdown timers.

## Responsibilities
- Define timer classes (`BasicTimerClass`, `TTimerClass`, `CDTimerClass`)
- Support timer operations (start, stop, value retrieval)
- Enable timer-to-integer conversion for compatibility

## Key Types
- **BasicTimerClass<T> (Class)**: Basic timer that increments at a constant rate.
- **TTimerClass<T> (Class)**: Pausable timer that can be started/stopped.
- **CDTimerClass<T> (Class)**: Countdown timer that decrements toward zero.

## Key Functions
### BasicTimerClass<T>::operator int
- Purpose: Convert timer value to integer.
- Calls: `Timer()`, `Started`

### TTimerClass<T>::Stop
- Purpose: Pause the timer and accumulate elapsed time.
- Calls: `BasicTimerClass<T>::Value()`

### CDTimerClass<T>::Value
- Purpose: Get the remaining countdown time.
- Calls: `BasicTimerClass<T>::Value()`

## Globals
None

## Dependencies
- `noinit.h` (for `NoInitClass`)
- External timer classes (e.g., `FrameTimerClass`, `SystemTimerClass`) used as template parameters.
