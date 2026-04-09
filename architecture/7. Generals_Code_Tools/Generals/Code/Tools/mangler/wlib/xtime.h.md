# Generals/Code/Tools/mangler/wlib/xtime.h

## Purpose
Defines the `Xtime` class for handling time and date operations with extended range support.

## Responsibilities
- Provides time manipulation (addition, subtraction, normalization)
- Supports date parsing and formatting
- Implements time comparisons and arithmetic
- Handles milliseconds and days since year 0
- Compatibility with `time_t` and `struct timeval`

## Key Types
- **Xtime (Class)**: Extended time handling with day/msec storage and wide date range.

## Key Functions
### Xtime::update
- Purpose: Updates internal time to current system time.
- Calls: Platform-specific time functions (e.g., `time()`, `ftime()`).

### Xtime::getTime
- Purpose: Retrieves date/time components (month, day, year, hour, minute, second).
- Calls: None (uses internal state).

### Xtime::setTime
- Purpose: Sets date/time components.
- Calls: `normalize()` to validate and adjust time.

### Xtime::compare
- Purpose: Compares two `Xtime` instances.
- Calls: None (uses internal `day_` and `msec_`).

### Xtime::normalize
- Purpose: Adjusts overflowed milliseconds into days.
- Calls: None (internal arithmetic).

## Globals
- None

## Dependencies
- `<time.h>`, `<sys/time.h>` (Unix) / `<sys/timeb.h>` (Windows)
- `wstypes.h` (for `sint32`, `bit8`)
- Platform-specific time APIs (`time()`, `ftime()`, `gettimeofday()`)
