# Generals/Code/Tools/mangler/wlib/critsec.cpp

## Purpose
Implements a cross-platform critical section (mutex) wrapper for thread synchronization.

## Responsibilities
- Manages thread-safe locking/unlocking via platform-specific APIs
- Tracks lock ownership and reference counts per thread
- Provides error handling and debugging for mutex operations

## Key Types
- **CritSec (Class)**: Thread synchronization primitive with lock/unlock semantics

## Key Functions
### CritSec::lock(int *refcount)
- Purpose: Acquires the mutex, optionally returning the current reference count
- Calls: `pthread_mutex_trylock`, `pthread_mutex_lock`, `EnterCriticalSection`

### CritSec::unlock(void)
- Purpose: Releases the mutex, decrementing the reference count
- Calls: `pthread_mutex_unlock`, `LeaveCriticalSection`

## Globals
- **None**

## Dependencies
- `<pthread.h>` (Unix)
- `<windows.h>` (Win32)
- `assert.h`
- `wlib/wdebug.h`
