# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_Lock.cpp

## Purpose
Implements a debug-only locking mechanism for thread synchronization in the audio subsystem.

## Responsibilities
- Initializes lock objects
- Acquires and releases locks
- Checks lock state
- Validates lock integrity via assertions

## Key Types
- Lock (struct): Thread synchronization primitive with debug tracking

## Key Functions
### LockInit
- Purpose: Initializes a lock object
- Calls: DBG_ASSERT, LOCK_INIT, DBG_SET_TYPE

### LockAcquire
- Purpose: Acquires a lock for exclusive access
- Calls: DBG_ASSERT_TYPE, DBG_ASSERT, LOCK_ACQUIRE

### LockRelease
- Purpose: Releases a previously acquired lock
- Calls: DBG_ASSERT_TYPE, DBG_ASSERT, LOCK_RELEASE

### Locked
- Purpose: Checks if a lock is currently held
- Calls: DBG_ASSERT_TYPE, DBG_ASSERT, LOCKED

## Globals
- None

## Dependencies
- wpaudio/altypes.h
- wpaudio/lock.h
- DBG_DECLARE_TYPE, DBG_ASSERT, DBG_ASSERT_TYPE, DBG_SET_TYPE macros
- LOCK_INIT, LOCK_ACQUIRE, LOCK_RELEASE, LOCKED macros
