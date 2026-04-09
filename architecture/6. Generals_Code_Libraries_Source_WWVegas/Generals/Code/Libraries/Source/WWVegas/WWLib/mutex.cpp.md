# Generals/Code/Libraries/Source/WWVegas/WWLib/mutex.cpp

## Purpose
Implements Windows-specific mutex and critical section synchronization primitives for thread safety.

## Responsibilities
- Manages `MutexClass` (named mutex) and `CriticalSectionClass` (spinlock-style)
- Provides RAII-style locking via nested `LockClass` helpers
- Handles Windows HANDLE and CRITICAL_SECTION lifecycle
- Tracks lock state with internal counters

## Key Types
- `MutexClass` (Class): Wrapper for Windows named mutex
- `CriticalSectionClass` (Class): Wrapper for Windows critical section
- `MutexClass::LockClass` (Class): RAII lock guard for mutex
- `CriticalSectionClass::LockClass` (Class): RAII lock guard for critical section

## Key Functions
### `MutexClass::Lock(int time)`
- Purpose: Acquires mutex with optional timeout
- Calls: `WaitForSingleObject`

### `MutexClass::Unlock()`
- Purpose: Releases mutex
- Calls: `ReleaseMutex`

### `CriticalSectionClass::Lock()`
- Purpose: Enters critical section
- Calls: `EnterCriticalSection`

### `CriticalSectionClass::Unlock()`
- Purpose: Leaves critical section
- Calls: `LeaveCriticalSection`

## Globals
None

## Dependencies
- `mutex.h` (header)
- `wwdebug.h` (asserts)
- `<windows.h>` (Win32 API)
- `W3DNEWARRAY` (memory allocator)
