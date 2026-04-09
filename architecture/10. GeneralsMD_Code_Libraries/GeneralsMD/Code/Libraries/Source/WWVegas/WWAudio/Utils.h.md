# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/Utils.h

## Purpose
Provides utility functions and classes for audio system management in the SAGE engine.

## Responsibilities
- Defines safe memory deletion macros (SAFE_DELETE, SAFE_DELETE_ARRAY, SAFE_FREE)
- Implements MMSLockClass for thread-safe audio operations
- Provides path string manipulation (Get_Filename_From_Path)

## Key Types
- MMSLockClass (Class): RAII wrapper for AIL audio locking/unlocking

## Key Functions
### Get_Filename_From_Path
- Purpose: Extracts filename from a full path string
- Calls: ::strrchr

### MMSLockClass::MMSLockClass
- Purpose: Locks audio system on construction
- Calls: ::AIL_lock

### MMSLockClass::~MMSLockClass
- Purpose: Unlocks audio system on destruction
- Calls: ::AIL_unlock

## Globals
- MMSLockClass::_MSSLockCriticalSection (CRITICAL_SECTION): Static critical section for audio locking

## Dependencies
- Mss.H (AIL audio library)
- Uses ::AIL_lock/::AIL_unlock (AIL functions)
- Uses ::strrchr (C runtime)
- Uses CRITICAL_SECTION (Windows API)
