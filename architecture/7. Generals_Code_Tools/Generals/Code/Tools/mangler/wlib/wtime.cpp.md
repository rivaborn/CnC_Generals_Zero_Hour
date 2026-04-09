# Generals/Code/Tools/mangler/wlib/wtime.cpp

## Purpose
Provides time and date manipulation utilities for the SAGE engine, including parsing, formatting, and arithmetic operations.

## Responsibilities
- Time/date parsing and formatting (RFC 1123, custom formats)
- Time arithmetic with microsecond precision
- Platform-specific time retrieval (Windows/Unix)
- Thread-safe localtime implementation for Windows

## Key Types
- Wtime (Class): Represents a time value with seconds and microseconds
- None: No other significant types

## Key Functions
### localtime_r
- Purpose: Thread-safe localtime implementation for Windows
- Calls: localtime, memcpy

### Wtime::ParseDate
- Purpose: Parses modified RFC 1123 date strings with optional minute offset
- Calls: strncmp, atoi, atol, mktime

### Wtime::FormatTime
- Purpose: Formats time according to custom format strings (e.g., "mm/dd/yy hh:mm:ss")
- Calls: sprintf, GetMonth, GetMDay, GetYear, GetHour, GetMinute, GetSecond

### Wtime::Update
- Purpose: Updates internal time from system clock
- Calls: _ftime (Windows) or gettimeofday (Unix)

### Wtime::GetSecond/GetMinute/GetHour/etc.
- Purpose: Retrieves time components from internal seconds value
- Calls: localtime_r

### Wtime::Compare
- Purpose: Compares two Wtime objects
- Calls: None

### Wtime::SignedAdd/SignedSubtract
- Purpose: Performs signed time arithmetic
- Calls: operator+, operator-, Compare

## Globals
- DAYS (char*): Short day names array
- FULLDAYS (char*): Full day names array
- MONTHS (char*): Short month names array
- FULLMONTHS (char*): Full month names array
- localtime_critsec (CritSec): Critical section for thread safety (Windows)

## Dependencies
- Key includes: ctype.h, wtime.h, critsec.h (Windows)
- External symbols: localtime, memcpy, _ftime (Windows), gettimeofday (Unix), mktime, sprintf, strncmp, atoi, atol
