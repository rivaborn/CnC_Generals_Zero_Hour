# Generals/Code/Libraries/Source/WWVegas/WWAudio/Utils.h

## Purpose
Provides utility functions and classes for audio system management in the SAGE engine.

## Responsibilities
- Defines safe memory deletion macros.
- Implements a critical section lock class for audio operations.
- Provides a helper function to extract filenames from paths.

## Key Types
- **MMSLockClass (Class)**: RAII wrapper for AIL audio locking/unlocking.

## Key Functions
### Get_Filename_From_Path
- Purpose: Extracts the filename portion from a full path string.
- Calls: `::strrchr`

## Globals
- **MMSLockClass::_MSSLockCriticalSection (CRITICAL_SECTION)**: Static critical section for audio locking.

## Dependencies
- `Mss.H` (AIL audio library)
- Windows API (`CRITICAL_SECTION`, `::AIL_lock`, `::AIL_unlock`)
- C runtime (`::strrchr`)
