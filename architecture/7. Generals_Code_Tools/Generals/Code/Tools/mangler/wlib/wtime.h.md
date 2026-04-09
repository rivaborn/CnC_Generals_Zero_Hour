# Generals/Code/Tools/mangler/wlib/wtime.h

## Purpose
Header file defining the `Wtime` class for time manipulation and formatting.

## Responsibilities
- Encapsulate time values (seconds and microseconds since epoch)
- Provide time formatting and parsing utilities
- Support time arithmetic and comparisons
- Handle platform-specific time APIs

## Key Types
- **Wtime (Class)**: Wrapper for time values with arithmetic and formatting
- **(anonymous enum)**: Sign indicators (POSITIVE/NEGATIVE)
- **POSITIVE (Enum)**: Positive time indicator
- **NEGATIVE (Enum)**: Negative time indicator

## Key Functions
### Wtime::Update
- Purpose: Synchronize internal time with system time
- Calls: Platform-specific time APIs

### Wtime::PrintTime
- Purpose: Format time into human-readable string
- Calls: None

### Wtime::ParseDate
- Purpose: Parse date string into time structure
- Calls: None

### Wtime::Compare
- Purpose: Compare two time values
- Calls: None

### Wtime::operator==
- Purpose: Equality comparison for Wtime objects
- Calls: Compare

## Globals
- None

## Dependencies
- `<stdio.h>`, `<stdlib.h>`, `<assert.h>`, `<sys/types.h>`
- Platform-specific headers (`<unistd.h>`, `<sys/time.h>` or `<sys/timeb.h>`, `<winsock.h>`)
- `<time.h>`, `<string.h>`
- `wstypes.h` (for `bit8`, `uint32` types)
