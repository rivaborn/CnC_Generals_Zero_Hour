# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/timer.h

## Purpose
Provides timer utility classes for game timing operations.

## Responsibilities
- Defines three timer classes: BasicTimerClass, TTimerClass, and CDTimerClass
- Implements timer functionality with start/stop/pause capabilities
- Supports countdown timers and regular timers
- Provides conversion operators for seamless integration with integral types

## Key Types
- **BasicTimerClass<T> (Class)**: Basic timer that counts up from a starting value
- **TTimerClass<T> (Class)**: Timer with start/stop functionality
- **CDTimerClass<T> (Class)**: Countdown timer that counts down to zero

## Key Functions
### BasicTimerClass<T>::operator int
- Purpose: Conversion operator to allow timer to function as integral type
- Calls: Timer(), Started

### TTimerClass<T>::Stop
- Purpose: Stops the timer from incrementing
- Calls: BasicTimerClass<T>::Value(), Started

### TTimerClass<T>::Start
- Purpose: Resumes a stopped timer
- Calls: Timer(), Started

### CDTimerClass<T>::Stop
- Purpose: Pauses the countdown timer
- Calls: *this, Started

### CDTimerClass<T>::Start
- Purpose: Resumes a paused countdown timer
- Calls: Timer(), Started

## Globals
- None

## Dependencies
- Key includes: "noinit.h"
- External symbols: NoInitClass (used in constructors)
