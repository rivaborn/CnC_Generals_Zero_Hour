# Generals/Code/Tools/matchbot/wlib/critsec.h

## Purpose
Provides a cross-platform critical section (mutex) implementation for thread synchronization.

## Responsibilities
- Wraps platform-specific mutex/locking mechanisms (Win32 CRITICAL_SECTION or POSIX pthread_mutex)
- Manages thread ownership and reference counting (POSIX version)
- Exposes lock/unlock operations for thread-safe code sections

## Key Types
- **CritSec (Class)**: Cross-platform critical section wrapper for thread synchronization.

## Key Functions
### CritSec::CritSec
- Purpose: Constructs and initializes the critical section.
- Calls: Platform-specific initialization (InitializeCriticalSection or pthread_mutex_init)

### CritSec::~CritSec
- Purpose: Destroys and cleans up the critical section.
- Calls: Platform-specific cleanup (DeleteCriticalSection or pthread_mutex_destroy)

### CritSec::lock
- Purpose: Acquires the lock, optionally tracking reference count.
- Calls: Platform-specific lock (EnterCriticalSection or pthread_mutex_lock)

### CritSec::unlock
- Purpose: Releases the lock.
- Calls: Platform-specific unlock (LeaveCriticalSection or pthread_mutex_unlock)

## Globals
- None

## Dependencies
- **wstypes.h**: For sint32 type definition
- **Windows.h/winbase.h**: For CRITICAL_SECTION on Win32
- **pthread.h/errno.h**: For pthread_mutex_t on Unix
