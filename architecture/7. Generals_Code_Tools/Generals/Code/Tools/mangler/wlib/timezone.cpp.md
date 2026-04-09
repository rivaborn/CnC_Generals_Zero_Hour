# Generals/Code/Tools/mangler/wlib/timezone.cpp

## Purpose
Provides platform-specific timezone information retrieval for the build tools.

## Responsibilities
- Detects current timezone and daylight savings status
- Returns timezone name as a string
- Returns timezone offset in minutes
- Handles Windows and Unix-like platforms differently

## Key Types
None

## Key Functions
### GetTimezoneInfo
- Purpose: Retrieves timezone name and offset, accounting for DST
- Calls: `_ftime`, `_daylight`, `gettimeofday`, `localtime_r`

### TimezoneString
- Purpose: Returns the current timezone name as a string
- Calls: `GetTimezoneInfo`

### TimezoneOffset
- Purpose: Returns the current timezone offset in minutes
- Calls: `GetTimezoneInfo`

## Globals
None

## Dependencies
- `wlib/xtime.h`
- `timezone.h`
- Windows-specific: `_ftime`, `_timeb`, `_tzname`, `_daylight`
- Unix-specific: `gettimeofday`, `timeval`, `timezone`, `localtime_r`, `tm`, `tzname`, `daylight`, `altzone`
