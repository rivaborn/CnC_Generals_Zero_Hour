# Generals/Code/Tools/matchbot/wlib/xtime.h

## Purpose
Defines the `Xtime` class for handling time and date operations with extended range support.

## Responsibilities
- Time and date manipulation (get/set components)
- Time comparisons and arithmetic
- Conversion between time representations
- System time updates (with 2038 limitation)

## Key Types
- **Xtime (Class)**: Wrapper for time/date with extended range (year 0 to ~5M).

## Key Functions
### Xtime()
- Purpose: Default constructor initializing to system time.
- Calls: Not inferable.

### update()
- Purpose: Updates internal time to current system time.
- Calls: Not inferable.

### getTime()
- Purpose: Retrieves time components (month, day, year, hour, minute, second).
- Calls: Not inferable.

### setTime()
- Purpose: Sets time components (month, day, year, hour, minute, second).
- Calls: Not inferable.

### addSeconds()
- Purpose: Adds seconds to the current time.
- Calls: Not inferable.

### compare()
- Purpose: Compares two `Xtime` objects.
- Calls: Not inferable.

### normalize()
- Purpose: Adjusts milliseconds overflow into days.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `<stdio.h>`, `<stdlib.h>`, `<assert.h>`, `<sys/types.h>`
- Platform-specific headers (`unistd.h`, `netinet/in.h`, `sys/time.h` for Unix; `sys/timeb.h`, `winsock.h` for Windows)
- `<time.h>`, `<string.h>`
- `wstypes.h` (for `bit8`, `sint32` types)
