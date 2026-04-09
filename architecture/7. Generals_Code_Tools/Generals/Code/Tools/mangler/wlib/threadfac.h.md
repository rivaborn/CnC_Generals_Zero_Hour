# Generals/Code/Tools/mangler/wlib/threadfac.h

## Purpose
Provides platform-independent thread creation abstractions for Win32 and POSIX systems.

## Responsibilities
- Defines `ThreadFactory` for launching threads from functions or `Runnable` objects
- Provides `Runnable` base class for object-oriented threading
- Manages thread lifecycle and counting
- Handles platform-specific thread launchers

## Key Types
- `Runnable` (Class): Base class for threadable objects with `run()` method
- `ThreadFactory` (Class): Static factory for creating threads

## Key Functions
### `ThreadFactory::startThread(void (*start_func)(void *), void *data)`
- Purpose: Launches a thread from a function pointer
- Calls: Platform-specific thread launchers

### `ThreadFactory::startThread(Runnable &runnable, void *data, bit8 destroy)`
- Purpose: Launches a thread from a `Runnable` object
- Calls: Platform-specific thread launchers

### `Runnable::run(void *data)`
- Purpose: Pure virtual method defining thread entry point
- Calls: None (must be implemented by derived classes)

### `Runnable::startThread(void *data, bit8 destroy)`
- Purpose: Convenience method to start thread via `ThreadFactory`
- Calls: `ThreadFactory::startThread`

### `Runnable::isRunning()`
- Purpose: Checks if any thread is running in this class
- Calls: None

### `Runnable::getThreadCount()`
- Purpose: Returns count of active threads in this class
- Calls: None

## Globals
- `Runnable::ThreadCount_` (int): Tracks active thread count
- `Runnable::CritSec_` (CritSec): Protects `ThreadCount_` access

## Dependencies
- `wstypes.h`, `critsec.h`
