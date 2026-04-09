# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/critsection.cpp

## Purpose
Implements a cross-platform critical section (mutex) for thread synchronization.

## Responsibilities
- Manages thread-safe critical sections using platform-specific APIs
- Provides RAII-style locking via `LockClass`
- Handles initialization and cleanup of critical section objects
- Tracks lock state with `inside` flag

## Key Types
- `CriticalSectionClass` (Class): Wrapper for platform-specific critical section
- `LockClass` (Class): RAII-style lock guard for `CriticalSectionClass`

## Key Functions
### `CriticalSectionClass::Enter()`
- Purpose: Acquires the critical section lock
- Calls: `EnterCriticalSection(&Bar)`, sets `inside=true`

### `CriticalSectionClass::Exit()`
- Purpose: Releases the critical section lock
- Calls: Sets `inside=false`, `LeaveCriticalSection(&Bar)`

### `CriticalSectionClass::LockClass::LockClass(CriticalSectionClass &c)`
- Purpose: RAII lock constructor that automatically enters the critical section
- Calls: `crit.Enter()`

### `CriticalSectionClass::LockClass::~LockClass()`
- Purpose: RAII lock destructor that automatically exits the critical section
- Calls: `crit.Exit()`

## Globals
- `inside` (bool): Tracks whether the critical section is currently locked

## Dependencies
- `critsection.h`: Header with class declarations
- `WWASSERT`: Assert macro for debug checks
- Windows API (`InitializeCriticalSection`, `EnterCriticalSection`, `LeaveCriticalSection`, `DeleteCriticalSection`) for non-Unix builds
