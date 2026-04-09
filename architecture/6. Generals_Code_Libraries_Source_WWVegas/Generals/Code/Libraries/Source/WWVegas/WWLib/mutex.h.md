# Generals/Code/Libraries/Source/WWVegas/WWLib/mutex.h

## Purpose
Provides thread synchronization primitives (mutex and critical section) for multi-threaded access control.

## Responsibilities
- Defines `MutexClass` for inter-process locking
- Defines `CriticalSectionClass` for faster intra-process synchronization
- Implements RAII-style lock guards (`LockClass`) for both primitives
- Enforces scoped locking via private lock/unlock methods

## Key Types
- **MutexClass (Class)**: Inter-process mutex wrapper with timed locking
- **LockClass (Class)**: RAII lock guard for `MutexClass`
- **CriticalSectionClass (Class)**: Faster intra-process critical section
- **LockClass (Class)**: RAII lock guard for `CriticalSectionClass`
- **WAIT_INFINITE (Enum)**: Constant for infinite wait time

## Key Functions
### MutexClass::Lock
- Purpose: Acquires the mutex with optional timeout
- Calls: Not inferable

### MutexClass::Unlock
- Purpose: Releases the mutex
- Calls: Not inferable

### CriticalSectionClass::Lock
- Purpose: Acquires the critical section
- Calls: Not inferable

### CriticalSectionClass::Unlock
- Purpose: Releases the critical section
- Calls: Not inferable

## Globals
None

## Dependencies
- `always.h` (header include)
- Platform-specific synchronization APIs (not defined here)
