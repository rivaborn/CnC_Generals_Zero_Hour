# Generals/Code/Tools/matchbot/wlib/wtime.h

## Purpose
Header file defining the `Wtime` class for time manipulation and formatting.

## Responsibilities
- Encapsulate time values (seconds/microseconds since epoch)
- Provide time formatting and parsing
- Support time comparisons and arithmetic
- Handle platform-specific time APIs

## Key Types
- **Wtime (Class)**: Time value wrapper with epoch-based storage
- **(anonymous enum)**: Sign flags (POSITIVE/NEGATIVE)
- **POSITIVE (Enum)**: Positive time flag
- **NEGATIVE (Enum)**: Negative time flag

## Key Functions
### Wtime::Update
- Purpose: Synchronize internal time with system time
- Calls: Platform-specific time APIs

### Wtime::PrintTime
- Purpose: Format time as HH:MM:SS string
- Calls: None

### Wtime::Compare
- Purpose: Compare two Wtime instances
- Calls: None

### Wtime::operator==
- Purpose: Equality comparison
- Calls: Compare

### Wtime::SignedAdd/SignedSubtract
- Purpose: Signed time arithmetic
- Calls: None

## Globals
- None

## Dependencies
- `<stdio.h>`, `<stdlib.h>`, `<time.h>`, `<string.h>`
- `<sys/time.h>` (Unix) or `<sys/timeb.h>`/`<winsock.h>` (Windows)
- `wstypes.h` for `bit8`/`uint32` types
