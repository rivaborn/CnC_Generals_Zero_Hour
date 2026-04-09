# Generals/Code/Tools/mangler/wlib/sem4.cpp

## Purpose
Implements a cross-platform semaphore wrapper for thread synchronization.

## Responsibilities
- Provides POSIX and Windows semaphore implementations
- Handles semaphore initialization, waiting, posting, and cleanup
- Offers non-threaded stubs when `_REENTRANT` is not defined

## Key Types
- `Sem4` (Class): Cross-platform semaphore wrapper

## Key Functions
### `Sem4::Sem4()`
- Purpose: Default constructor initializing semaphore to value 1
- Calls: `sem_init` (POSIX) or `CreateSemaphore` (Windows)

### `Sem4::Sem4(uint32 value)`
- Purpose: Constructor initializing semaphore to specified value
- Calls: `sem_init` (POSIX) or `CreateSemaphore` (Windows)

### `Sem4::Wait()`
- Purpose: Blocks until semaphore can be acquired
- Calls: `sem_wait` (POSIX) or `WaitForSingleObject` (Windows)

### `Sem4::Post()`
- Purpose: Releases semaphore
- Calls: `sem_post` (POSIX) or `ReleaseSemaphore` (Windows)

### `Sem4::TryWait()`
- Purpose: Non-blocking attempt to acquire semaphore
- Calls: `sem_trywait` (POSIX) or `WaitForSingleObject` (Windows)

### `Sem4::GetValue(int *sval)`
- Purpose: Retrieves current semaphore value
- Calls: `sem_getvalue` (POSIX) or `ReleaseSemaphore` (Windows)

### `Sem4::Destroy()`
- Purpose: Destroys semaphore
- Calls: `sem_destroy` (POSIX) or `CloseHandle` (Windows)

## Globals
None

## Dependencies
