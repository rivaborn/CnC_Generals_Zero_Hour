# Generals/Code/Tools/matchbot/wlib/critsec.cpp

## Purpose
Implements a cross-platform critical section (mutex) wrapper for thread synchronization.

## Responsibilities
- Manages mutex initialization/destruction for Unix (pthreads) and Windows (CRITICAL_SECTION)
- Provides lock/unlock operations with reference counting
- Handles recursive locking by the same thread
- Reports errors via debug messages

## Key Types
- **CritSec (Class)**: Thread synchronization primitive supporting recursive locks

## Key Functions
### CritSec::lock(int *refcount)
- Purpose: Acquires the mutex, supporting recursive locks by the same thread
- Calls: `pthread_mutex_trylock`, `pthread_mutex_lock`, `pthread_self`, `ERRMSG`

### CritSec::unlock(void)
- Purpose: Releases the mutex, decrementing the reference count
- Calls: `pthread_mutex_unlock`, `pthread_self`, `WRNMSG`, `ERRMSG`

## Globals
- **None**

## Dependencies
- `<pthread.h>` (Unix)
- `<windows.h>` (Windows)
- `assert.h`
- `wlib/wdebug.h` (for `ERRMSG`, `WRNMSG`)
- External symbols: `pthread_mutex_t`, `CRITICAL_SECTION`, `pthread_t`, `errno`
