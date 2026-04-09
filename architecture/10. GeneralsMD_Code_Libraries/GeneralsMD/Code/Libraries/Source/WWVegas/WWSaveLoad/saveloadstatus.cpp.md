# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/saveloadstatus.cpp

## Purpose
Manages save/load operation status text and progress counting with thread safety.

## Responsibilities
- Maintains status text for save/load operations
- Tracks progress count for save/load operations
- Provides thread-safe access to status information
- Supports multiple status text slots (up to 2)

## Key Types
- None

## Key Functions
### Set_Status_Text
- Purpose: Sets status text for a given ID with thread safety
- Calls: CriticalSectionClass::LockClass

### Get_Status_Text
- Purpose: Retrieves status text for a given ID with thread safety
- Calls: CriticalSectionClass::LockClass

### Reset_Status_Count
- Purpose: Resets the save/load progress counter to zero
- Calls: None

### Inc_Status_Count
- Purpose: Increments the save/load progress counter
- Calls: None

### Get_Status_Count
- Purpose: Returns the current save/load progress counter value
- Calls: None

## Globals
- text_mutex (CriticalSectionClass): Mutex for thread-safe status text access
- status_text (StringClass[MAX_STATUS_TEXT_ID]): Array storing status text messages
- status_count (int): Counter tracking save/load progress

## Dependencies
- "saveloadstatus.h"
- "mutex.h"
- CriticalSectionClass
- StringClass
- WWASSERT macro
