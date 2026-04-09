# Generals/Code/Tools/mangler/wlib/timezone.h

## Purpose
Provides convenience functions to retrieve current timezone information, including daylight savings adjustments.

## Responsibilities
- Exposes functions to get timezone description and GMT offset
- Handles daylight savings time logic
- Returns static timezone string and offset values

## Key Types
None

## Key Functions
### GetTimezoneInfo
- Purpose: Fills in timezone description and GMT offset via reference parameters
- Calls: Not inferable

### TimezoneString
- Purpose: Returns the description of the current timezone (including daylight savings)
- Calls: Not inferable

### TimezoneOffset
- Purpose: Returns the GMT offset of the current timezone
- Calls: Not inferable

## Globals
None

## Dependencies
- No includes or external symbols used
