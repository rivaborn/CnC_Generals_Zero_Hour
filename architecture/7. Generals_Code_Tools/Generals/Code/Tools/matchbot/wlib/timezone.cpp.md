# Generals/Code/Tools/matchbot/wlib/timezone.cpp

## Purpose
Provides timezone information retrieval for the matchbot tool.

## Responsibilities
- Retrieves timezone name and offset
- Handles platform-specific timezone APIs
- Returns timezone string and offset in minutes

## Key Types
None

## Key Functions
### GetTimezoneInfo
- Purpose: Retrieves timezone name and offset via platform-specific APIs
- Calls: `_ftime`, `_daylight`, `_tzname`, `gettimeofday`, `localtime_r`, `tzname`, `daylight`, `altzone`, `timezone`

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
- Windows API: `_ftime`, `_timeb`, `_daylight`, `_tzname`
- POSIX API: `gettimeofday`, `timeval`, `timezone`, `localtime_r`, `tm`, `tzname`, `daylight`, `altzone`
