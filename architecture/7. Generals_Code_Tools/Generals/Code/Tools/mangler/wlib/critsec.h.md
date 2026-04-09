# Generals/Code/Tools/mangler/wlib/critsec.h

## Purpose
Provides a cross-platform critical section (mutex) wrapper for thread synchronization.

## Responsibilities
- Encapsulates platform-specific mutex/locking mechanisms
- Supports reference counting for POSIX implementation
- Provides lock/unlock operations
- Maintains thread ownership for POSIX version

## Key Types
- CritSec (Class): Cross-platform critical section wrapper

## Key Functions
### CritSec::CritSec
- Purpose: Constructor initializes the critical section
- Calls: Platform-specific initialization (CRITICAL_SECTION or pthread_mutex_t)

### CritSec::~CritSec
- Purpose: Destructor cleans up the critical section
- Calls: Platform-specific cleanup

### CritSec::lock
- Purpose: Acquires the lock, optionally tracking reference count
- Calls: Platform-specific lock acquisition

### CritSec::unlock
- Purpose: Releases the lock
- Calls: Platform-specific unlock operation

## Globals
None

## Dependencies
- wstypes.h (for sint32)
- Platform-specific headers (windows.h/winbase.h for Win32, pthread.h/errno.h for UNIX)
- Uses CRITICAL_SECTION (Win32) or pthread_mutex_t (POSIX)
