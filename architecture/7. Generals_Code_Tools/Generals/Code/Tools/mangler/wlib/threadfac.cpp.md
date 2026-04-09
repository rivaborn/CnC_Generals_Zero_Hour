# Generals/Code/Tools/mangler/wlib/threadfac.cpp

## Purpose
Implements cross-platform thread management for the SAGE engine, supporting both function-based and class-based threads.

## Responsibilities
- Manages thread creation and lifecycle
- Provides thread counting and synchronization
- Handles platform-specific thread APIs (Win32/POSIX)
- Supports both standalone functions and class-based runnable objects

## Key Types
- **ThreadInformation (struct)**: Contains thread startup parameters (function/class pointer, data, and destroy flag)
- **Runnable (class)**: Base class for threadable objects with thread counting and synchronization

## Key Functions
### `ThreadFactory::startThread(Runnable &, void *, bit8)`
- Purpose: Starts a thread for a Runnable object
- Calls: `Runnable::CritSec_.lock/unlock`, `_beginthreadex` (Win32), `pthread_create` (UNIX)

### `ThreadFactory::startThread(void (*)(void *), void *)`
- Purpose: Starts a thread for a standalone function
- Calls: `_beginthreadex` (Win32), `pthread_create` (UNIX)

### `threadFuncLauncher(void *)`
- Purpose: Platform-specific launcher for function-based threads
- Calls: `delete` on ThreadInformation, calls the target function

### `threadClassLauncher(void *)`
- Purpose: Platform-specific launcher for class-based threads
- Calls: `delete` on ThreadInformation, `Runnable::run()`, `Runnable::CritSec_.lock/unlock`, `ExitThread` (Win32)

## Globals
- **Runnable::ThreadCount_ (int)**: Tracks active thread count
- **Runnable::CritSec_ (CritSec)**: Protects ThreadCount_ access

## Dependencies
- `threadfac.h` (header)
- Win32 API (`_beginthreadex`, `ExitThread`)
- POSIX threads (`pthread_create`, `pthread_attr_t`)
- `CritSec` synchronization primitive
