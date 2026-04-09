# Generals/Code/Tools/mangler/wlib/xtime.cpp

## Purpose
Extended time/date handling library for the SAGE engine, supporting large date ranges and precise time arithmetic.

## Responsibilities
- Date/time arithmetic and normalization
- Conversion between day counts and calendar dates
- Time formatting and parsing
- Platform-specific time retrieval (Windows/Unix)

## Key Types
- `Xtime` (Class): Extended time/date representation with day/msec precision
- `Get_Day` (Function): Converts calendar date to day count since year 0
- `Get_Date_From_Day` (Function): Converts day count to calendar date
- `Max_Day` (Function): Returns max days in a month/year

## Key Functions
### `Xtime::addSeconds`
- Purpose: Adds seconds to the time value
- Calls: `normalize()`

### `Xtime::getTime`
- Purpose: Extracts calendar components (month/day/year/hour/min/sec)
- Calls: `Get_Date_From_Day()`

### `Xtime::setTime`
- Purpose: Sets time from calendar components
- Calls: `Get_Day()`

### `Xtime::compare`
- Purpose: Compares two Xtime values
- Calls: None

## Globals
- `DAYS` (char*): Short day names
- `FULLDAYS` (char*): Full day names
- `MONTHS` (char*): Short month names
- `FULLMONTHS` (char*): Full month names

## Dependencies
- `<time.h>`, `<sys/time.h>` (Unix), `<ctype.h>`
- `xtime.h` (header)
- Platform-specific time functions (`_ftime`, `gettimeofday`)
