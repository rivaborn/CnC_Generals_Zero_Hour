# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/saveloadstatus.h

## Purpose
Header defining the SaveLoadStatus namespace for managing save/load progress UI text and counters.

## Responsibilities
- Declares functions for setting and retrieving save/load status text
- Provides status counter management (reset, increment, get)
- Defines convenience macros for initializing status text

## Key Types
- None

## Key Functions
### Set_Status_Text
- Purpose: Sets the status text for a given ID (0 or 1).
- Calls: None

### Reset_Status_Count
- Purpose: Resets the save/load status counter to zero.
- Calls: None

### Inc_Status_Count
- Purpose: Increments the save/load status counter.
- Calls: None

### Get_Status_Count
- Purpose: Retrieves the current save/load status counter value.
- Calls: None

### Get_Status_Text
- Purpose: Retrieves the status text for a given ID into a StringClass.
- Calls: None

## Globals
- None

## Dependencies
- "always.h" (for basic includes)
- "wwstring.h" (for StringClass)
- Uses SaveLoadStatus namespace
