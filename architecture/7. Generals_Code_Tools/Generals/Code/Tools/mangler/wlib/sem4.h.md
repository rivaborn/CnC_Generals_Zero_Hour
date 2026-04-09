# Generals/Code/Tools/mangler/wlib/sem4.h

## Purpose
Defines a cross-platform semaphore wrapper class for thread synchronization.

## Responsibilities
- Provides semaphore operations (wait, try-wait, post, get value, destroy)
- Supports both Windows and POSIX semaphores via conditional compilation
- Manages semaphore lifecycle (construction/destruction)
- Handles reentrant thread-safe operations

## Key Types
- Sem4 (Class): Cross-platform semaphore wrapper for thread synchronization.

## Key Functions
### Sem4()
- Purpose: Default constructor initializes semaphore with value 0.
- Calls: Not inferable (platform-specific semaphore init).

### Sem4(uint32 value)
- Purpose: Constructor initializes semaphore with specified value.
- Calls: Not inferable (platform-specific semaphore init).

### ~Sem4()
- Purpose: Destructor cleans up semaphore resources.
- Calls: Not inferable (platform-specific semaphore cleanup).

### Wait()
- Purpose: Blocks until semaphore can be acquired.
- Calls: Not inferable (platform-specific semaphore wait).

### TryWait()
- Purpose: Attempts to acquire semaphore without blocking.
- Calls: Not inferable (platform-specific semaphore try-wait).

### Post()
- Purpose: Releases semaphore, allowing another thread to proceed.
- Calls: Not inferable (platform-specific semaphore post).

### GetValue(int *sval)
- Purpose: Retrieves current semaphore value.
- Calls: Not inferable (platform-specific semaphore value query).

### Destroy()
- Purpose: Explicitly destroys semaphore resources.
- Calls: Not inferable (platform-specific semaphore destroy).

## Globals
None

## Dependencies
- `<limits.h>`: For integer limits
- `<unistd.h>`: POSIX API (non-Windows)
-
