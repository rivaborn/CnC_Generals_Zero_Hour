# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/critsection.h

## Purpose
Provides a thread-synchronization mechanism using Windows critical sections.

## Responsibilities
- Defines `CriticalSectionClass` for mutual exclusion.
- Implements RAII-style locking via `LockClass`.
- Wraps Windows `CRITICAL_SECTION` with C++ semantics.

## Key Types
- **CriticalSectionClass (Class)**: Manages a critical section (mutex).
- **LockClass (Class)**: RAII lock guard for `CriticalSectionClass`.

## Key Functions
### CriticalSectionClass::Enter
- Purpose: Acquires the critical section.
- Calls: Not inferable.

### CriticalSectionClass::Exit
- Purpose: Releases the critical section.
- Calls: Not inferable.

### LockClass::LockClass
- Purpose: Locks the critical section on construction.
- Calls: `CriticalSectionClass::Enter`.

### LockClass::~LockClass
- Purpose: Unlocks the critical section on destruction.
- Calls: `CriticalSectionClass::Exit`.

## Globals
- None

## Dependencies
- `<windows.h>` (for `CRITICAL_SECTION`)
- `"always.h"`, `"wwdebug.h"` (project headers)
