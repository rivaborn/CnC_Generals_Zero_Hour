# GeneralsMD/Code/GameEngine/Include/Common/ScopedMutex.h

## Purpose
RAII wrapper for Windows mutex handles, ensuring automatic lock/unlock within a scope.

## Responsibilities
- Locks a mutex on construction
- Unlocks the mutex on destruction
- Logs timeout errors during locking

## Key Types
- ScopedMutex (Class): RAII mutex locker

## Key Functions
### ScopedMutex::ScopedMutex
- Purpose: Locks the provided mutex handle
- Calls: `WaitForSingleObject`, `DEBUG_LOG`

### ScopedMutex::~ScopedMutex
- Purpose: Releases the mutex lock
- Calls: `ReleaseMutex`

## Globals
- None

## Dependencies
- Windows API: `HANDLE`, `WaitForSingleObject`, `ReleaseMutex`
- Debug logging: `DEBUG_LOG`
