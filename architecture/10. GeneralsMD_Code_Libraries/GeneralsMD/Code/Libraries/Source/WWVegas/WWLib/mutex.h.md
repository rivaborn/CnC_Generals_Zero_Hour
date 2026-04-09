# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/mutex.h

## Purpose
Provides thread synchronization primitives: mutexes, critical sections, and fast critical sections.

## Responsibilities
- Defines `MutexClass` for inter-process locking.
- Defines `CriticalSectionClass` for faster intra-process synchronization.
- Defines `FastCriticalSectionClass` for high-performance, single-thread reentrancy.
- Implements RAII-style lock classes (`LockClass`) for each primitive.

## Key Types
- **MutexClass (Class)**: Inter-process mutex with timed locking.
- **CriticalSectionClass (Class)**: Faster intra-process critical section.
- **FastCriticalSectionClass (Class)**: High-speed critical section (non-reentrant).
- **LockClass (Class)**: RAII lock wrapper for each primitive.
- **WAIT_INFINITE (Enum)**: Constant for infinite wait time.

## Key Functions
### MutexClass::Lock
- Purpose: Acquires the mutex with a timeout.
- Calls: Not inferable (implementation in another file).

### CriticalSectionClass::Lock
- Purpose: Acquires the critical section.
- Calls: Not inferable.

### FastCriticalSectionClass::LockClass::LockClass
- Purpose: Acquires the fast critical section using inline assembly.
- Calls: `ThreadClass::Switch_Thread()`.

## Globals
- None.

## Dependencies
- `always.h`, `thread.h`
- `ThreadClass::Switch_Thread()` (external).
