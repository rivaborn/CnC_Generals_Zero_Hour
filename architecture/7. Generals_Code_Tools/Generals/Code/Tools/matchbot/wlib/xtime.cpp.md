# Generals/Code/Tools/matchbot/wlib/xtime.cpp

## Purpose
Provides an extended time/date library (Xtime) for handling dates far beyond the 2038 limit of standard time_t.

## Responsibilities
- Manages time/date calculations with millisecond precision
- Supports date arithmetic and comparisons
- Converts between internal representation and standard formats
- Handles leap years and month boundaries

## Key Types
- Xtime (Class): extended time/date representation with millisecond precision
- None: other types are standard C/C++ (time_t, struct timeval)

## Key Functions
### Get_Day
- Purpose: Calculate day count since year 0 for a given date
- Calls: None

### Get_Date_From_Day
- Purpose: Convert day count since year 0 back to year and day-of-year
- Calls: None

### Max_Day
- Purpose: Get maximum day for a given month/year (handles leap years)
- Calls: None

### Xtime::addSeconds
- Purpose: Add seconds to the time (handles overflow to days)
- Calls: normalize()

### Xtime::getTime
- Purpose: Extract date/time components (month, day, year, etc.)
- Calls: Get_Date_From_Day()

### Xtime::setTime
- Purpose: Set time from date/time components
- Calls: Get_Day()

## Globals
- DAYS (char*): 3-letter day abbreviations
- FULLDAYS (char*): full day names
- MONTHS (char*): 3-letter month abbreviations
- FULLMONTHS (char*): full month names

## Dependencies
- <time.h>, <sys/time.h> (platform-specific)
- xtime.h (header)
- ctime functions (gmtime, ctime, asctime)
- Platform-specific time functions (_ftime on Windows, gettimeofday on Unix)
