# Generals/Code/Tools/matchbot/wlib/threadfac.h

## Purpose
Provides platform-independent thread creation utilities for Windows and POSIX systems.

## Responsibilities
- Defines `ThreadFactory` for launching threads from functions or `Runnable` objects
- Provides `Runnable` base class for object-oriented threading
- Manages thread counts and synchronization via critical sections

## Key Types
- `Runnable` (Class): Base class for threadable objects with `run()` method
- `ThreadFactory` (Class): Static factory for creating threads

## Key Functions
### `ThreadFactory::startThread(void (*start_func)(void *), void *data)`
- Purpose: Launches a thread executing a function
- Calls: `threadFuncLauncher`

### `ThreadFactory::startThread(Runnable &runnable, void *data, bit8 destroy)`
- Purpose: Launches a thread executing a `Runnable` object's `run()` method
- Calls: `threadClassLauncher`

### `Runnable::startThread(void *data, bit8 destroy)`
- Purpose: Convenience method to start a thread for this `Runnable`
- Calls: `ThreadFactory::startThread`

### `Runnable::isRunning()`
- Purpose: Checks if any thread is running in this `Runnable` class
- Calls: None

### `Runnable::getThreadCount()`
- Purpose: Returns the count of active threads in this `Runnable` class
- Calls: None

## Globals
- `Runnable::ThreadCount_` (int): Tracks active thread count
- `Runnable::CritSec_` (CritSec): Protects `ThreadCount_` access

## Dependencies
- `wstypes.h`, `critsec.h`
- Platform-specific headers (`wtypes.h` for Windows, `pthread.h` for POSIX)
- `bit8` type from `wst
