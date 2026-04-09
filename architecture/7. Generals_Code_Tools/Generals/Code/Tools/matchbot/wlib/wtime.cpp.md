# Generals/Code/Tools/matchbot/wlib/wtime.cpp

## Purpose
Provides time and date manipulation utilities for the matchbot tool.

## Responsibilities
- Time/date parsing and formatting
- Cross-platform time handling (Windows/Unix)
- Time arithmetic and comparison
- RFC 1123 date string support

## Key Types
- Wtime (Class): wrapper for time/date with microsecond precision
- localtime_r (Function): thread-safe localtime implementation for Windows

## Key Functions
### localtime_r
- Purpose: Thread-safe localtime implementation for Windows
- Calls: localtime, memcpy

### Wtime::ParseDate
- Purpose: Parses modified RFC 1123 date strings with optional minute offset
- Calls: strncmp, atoi, atol, mktime

### Wtime::FormatTime
- Purpose: Formats time according to Microsoft-style format strings
- Calls: sprintf, GetMonth, GetMDay, GetYear, GetHour, GetMinute, GetSecond

### Wtime::Update
- Purpose: Updates internal time from system clock
- Calls: _ftime (Windows) or gettimeofday (Unix)

### Wtime::GetSecond/GetMinute/GetHour/etc.
- Purpose: Retrieve individual time components
- Calls: localtime_r

## Globals
- DAYS (char*): Short day names array
- FULLDAYS (char*): Full day names array
- MONTHS (char*): Short month names array
- FULLMONTHS (char*): Full month names array

## Dependencies
- ctype.h, wtime.h
- Windows: critsec.h, _ftime
- Unix: gettimeofday
- External: memcpy, sprintf, strncmp, atoi, atol, mktime
