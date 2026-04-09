# Generals/Code/GameEngine/Source/GameNetwork/GameSpy/Thread/PingThread.cpp

## Purpose
Implements a multi-threaded ICMP ping system for network latency measurement in Generals/Zero Hour.

## Responsibilities
- Manages worker threads for concurrent ping operations
- Handles hostname resolution and ICMP echo requests
- Tracks ping results in a thread-safe map
- Provides ping data as a formatted string for GameSpy integration

## Key Types
- **Pinger (Class)**: Main ping manager with request/response queues and thread control
- **PingThreadClass (Class)**: Worker thread that executes actual ping operations
- **RequestQueue (typedef)**: Queue of pending ping requests
- **ResponseQueue (typedef)**: Queue of completed ping responses
- **PingRequest (struct)**: Contains hostname, timeout, and repetition count
- **PingResponse (struct)**: Contains hostname, average ping time, and success count

## Key Functions
### Pinger::addRequest
- Purpose: Adds a new ping request to the queue
- Calls: MutexClass::LockClass

### Pinger::addResponse
- Purpose: Stores completed ping response and updates ping map
- Calls: MutexClass::LockClass

### PingThreadClass::doPing
- Purpose: Executes single ICMP echo request and returns round-trip time
- Calls: LoadLibrary, GetProcAddress, IcmpCreateFile, IcmpSendEcho, IcmpCloseHandle

### Pinger::getPingString
- Purpose: Generates GameSpy-compatible ping string from stored results
- Calls: MutexClass::LockClass

## Globals
- **NumWorkerThreads (const Int)**: Fixed number of worker threads (10)
- **ThePinger (PingerInterface*)**: Global singleton instance of the pinger

## Dependencies
- `mutex.h`, `thread.h` for threading primitives
- `winsock.h` for socket operations
- `ICMP.DLL` functions (dynamically loaded) for ICMP operations
- `Common/StackDump.h` for exception handling
