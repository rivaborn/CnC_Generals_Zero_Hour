# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/mutex.cpp

## Purpose
Implements platform-specific mutex and critical section synchronization primitives for Windows.

## Responsibilities
- Wraps Windows `CreateMutex`, `WaitForSingleObject`, and `ReleaseMutex` for cross-platform compatibility.
- Manages critical sections via `InitializeCriticalSection`/`DeleteCriticalSection`.
- Provides RAII-style locking via nested `LockClass` helpers.
- Includes debug assertions for locked-state validation.

## Key Types
- **MutexClass (class)**: Wrapper for Windows mutex objects.
- **CriticalSectionClass (class)**: Wrapper for Windows critical sections.
- **LockClass (nested class)**: RAII lock guard for both mutex and critical section.

## Key Functions
### `MutexClass::Lock(int time)`
- Purpose: Acquires the mutex with optional timeout.
- Calls: `WaitForSingleObject`, `WWASSERT`.

### `MutexClass::Unlock()`
- Purpose: Releases the mutex.
- Calls: `ReleaseMutex`, `WWASSERT`.

### `CriticalSectionClass::Lock()`
- Purpose: Enters the critical section.
- Calls: `EnterCriticalSection`.

### `CriticalSectionClass::Unlock()`
- Purpose: Leaves the critical section.
- Calls: `LeaveCriticalSection`, `WWASSERT`.

## Globals
None.

## Dependencies
- `mutex.h` (header)
- `wwdebug.h` (for `WWASSERT`)
- `<windows.h>` (Win32 API)
- `W3DNEWARRAY` (memory allocation)
