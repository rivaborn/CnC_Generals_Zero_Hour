# Generals/Code/Tools/matchbot/wlib/threadfac.cpp

## Purpose
Implements cross-platform thread management for the game's toolchain, supporting both function-based and class-based threads.

## Responsibilities
- Manages thread creation and lifecycle
- Provides thread counting and synchronization
- Handles platform-specific thread APIs (Win32/POSIX)
- Supports both standalone functions and class-based runnable objects

## Key Types
- ThreadInformation (struct): Contains thread startup parameters (function/class pointer, data, and destroy flag)
- Runnable (class): Abstract base class for threadable objects with thread counting

## Key Functions
### ThreadFactory::startThread(Runnable &, void *, bit8)
- Purpose: Starts a thread for a Runnable-derived class
- Calls: Runnable::CritSec_.lock/unlock, _beginthreadex/pthread_create, threadClassLauncher

### ThreadFactory::startThread(void (*)(void *), void *)
- Purpose: Starts a thread for a standalone function
- Calls: _beginthreadex/pthread_create, threadFuncLauncher

### threadFuncLauncher(void *)
- Purpose: Platform-independent launcher for function-based threads
- Calls: delete (on ThreadInformation)

### threadClassLauncher(void *)
- Purpose: Platform-independent launcher for class-based threads
- Calls: Runnable::run, delete (on ThreadInformation and optionally the Runnable), Runnable::CritSec_.lock/unlock

## Globals
- Runnable::ThreadCount_ (int): Tracks total active threads
- Runnable::CritSec_ (CritSec): Protects ThreadCount_ access

## Dependencies
- threadfac.h (header)
- Platform-specific APIs: _beginthreadex (Win32), pthread_create (POSIX)
- CritSec (critical section/mutex type)
