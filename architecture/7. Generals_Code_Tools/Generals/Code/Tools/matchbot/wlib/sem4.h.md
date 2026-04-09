# Generals/Code/Tools/matchbot/wlib/sem4.h

## Purpose
Provides a cross-platform semaphore wrapper for thread synchronization.

## Responsibilities
- Encapsulates platform-specific semaphore operations
- Supports creation, waiting, posting, and destruction of semaphores
- Handles Windows and POSIX semaphore APIs via preprocessor directives

## Key Types
- Sem4 (Class): cross-platform semaphore wrapper

## Key Functions
### Sem4()
- Purpose: Default constructor (creates semaphore with initial value 0)
- Calls: Not inferable

### Sem4(uint32 value)
- Purpose: Constructor that initializes semaphore with specified value
- Calls: Not inferable

### ~Sem4()
- Purpose: Destructor (cleans up semaphore resources)
- Calls: Not inferable

### Wait()
- Purpose: Blocks until semaphore can be acquired
- Calls: Not inferable

### TryWait()
- Purpose: Attempts to acquire semaphore without blocking
- Calls: Not inferable

### Post()
- Purpose: Releases the semaphore
- Calls: Not inferable

### GetValue(int *sval)
- Purpose: Retrieves current semaphore value
- Calls: Not inferable

### Destroy()
- Purpose: Explicitly destroys the semaphore
- Calls: Not inferable

## Globals
None

## Dependencies
- `<limits.h>` (C standard library)
- `<unistd.h>` (POSIX API)
- `<semaphore.h>` (POSIX semaphores)
- `<windows.h>` (Windows API)
- `wstypes.h` (custom types like uint32, sint32)
