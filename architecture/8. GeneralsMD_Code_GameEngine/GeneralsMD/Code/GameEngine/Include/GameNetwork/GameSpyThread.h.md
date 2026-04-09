# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameSpyThread.h

## Purpose
Defines the GameSpyThreadClass for handling GameSpy-related operations in a separate thread.

## Responsibilities
- Manages GameSpy login, stats updates, and locale settings.
- Queues operations for thread-safe execution.
- Provides access to shell screen and locale select state.

## Key Types
- **GameSpyThreadClass (Class)**: Thread class for GameSpy operations.

## Key Functions
### GameSpyThreadClass::queueLogin
- Purpose: Queues a login request with credentials.
- Calls: None.

### GameSpyThreadClass::Thread_Function
- Purpose: Main thread function for processing queued GameSpy operations.
- Calls: Not inferable.

### GameSpyThreadClass::getNextShellScreen
- Purpose: Retrieves the next shell screen to display.
- Calls: None.

### GameSpyThreadClass::showLocaleSelect
- Purpose: Checks if locale selection should be shown.
- Calls: None.

## Globals
- **TheGameSpyThread (GameSpyThreadClass*)**: Global instance of the GameSpy thread.
- **TheGameSpyMutex (MutexClass)**: Mutex for thread synchronization.

## Dependencies
- `mutex.h`, `thread.h`
- `AsciiString`, `Bool`, `ThreadClass`
