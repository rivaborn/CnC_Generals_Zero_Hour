# Generals/Code/Libraries/Source/WWVegas/WWAudio/Utils.cpp

## Purpose
This file defines the `MMSLockClass` critical section for thread synchronization in the WWAudio library.

## Responsibilities
- Declares and initializes a global critical section for thread-safe audio operations.
- Provides a base for mutex-like functionality in audio utilities.

## Key Types
- `MMSLockClass` (Class): Manages a critical section for thread synchronization.

## Key Functions
### None
- No functions defined in this file.

## Globals
- `_MSSLockCriticalSection` (CRITICAL_SECTION): Global critical section used for thread synchronization in audio operations.

## Dependencies
- `Utils.H`: Header file for `MMSLockClass`.
- `CRITICAL_SECTION`: Windows API structure for synchronization.
