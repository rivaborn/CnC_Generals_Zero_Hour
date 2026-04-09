# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/saveloadstatus.cpp

## Purpose
Manages status text during save/load operations, providing thread-safe access.

## Responsibilities
- Stores and retrieves status text for save/load progress
- Ensures thread-safe access via mutex
- Handles multiple status text slots (up to MAX_STATUS_TEXT_ID)

## Key Types
- None

## Key Functions
### Set_Status_Text
- Purpose: Sets status text for a given ID, clearing secondary text if primary is updated
- Calls: CriticalSectionClass::LockClass, WWASSERT

### Get_Status_Text
- Purpose: Retrieves status text for a given ID
- Calls: CriticalSectionClass::LockClass, WWASSERT

## Globals
- text_mutex (CriticalSectionClass): Mutex for thread-safe access
- status_text (StringClass[MAX_STATUS_TEXT_ID]): Array storing status texts

## Dependencies
- saveloadstatus.h
- mutex.h
- CriticalSectionClass, StringClass, WWASSERT (external)
