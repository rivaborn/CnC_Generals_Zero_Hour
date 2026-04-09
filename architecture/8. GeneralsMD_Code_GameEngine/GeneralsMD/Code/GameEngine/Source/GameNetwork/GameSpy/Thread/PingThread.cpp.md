# GeneralsMD/Code/GameEngine/Source/GameNetwork/GameSpy/Thread/PingThread.cpp

## Purpose
Manages ICMP ping operations using a thread pool to measure network latency to hosts.

## Responsibilities
- Spawns and manages worker threads for ping requests
- Handles hostname resolution and ICMP echo requests
- Tracks ping results in a map and generates a ping string
- Provides thread-safe request/response queues

## Key Types
- **Pinger (Class)**: Main interface for ping operations and thread management
- **PingThreadClass (Class)**: Worker thread implementing ICMP ping logic
- **RequestQueue (typedef)**: Queue for pending ping requests
- **ResponseQueue (typedef)**: Queue for completed ping responses
- **PingRequest (struct)**: Contains hostname, repetitions, and timeout
- **PingResponse (struct)**: Contains hostname, average ping, and good replies

## Key Functions
### Pinger::addRequest
- Purpose: Adds a ping request to the queue
- Calls: MutexClass::LockClass

### Pinger::addResponse
- Purpose: Adds a completed ping response and updates the ping map
- Calls: MutexClass::LockClass

### PingThreadClass::doPing
- Purpose: Executes a single ICMP ping and returns round-trip time
- Calls: LoadLibrary, GetProcAddress, IcmpCreateFile, IcmpSendEcho, IcmpCloseHandle

### Pinger::getPingString
- Purpose: Generates a string of ping values for all hosts
- Calls: MutexClass::LockClass

## Globals
- **NumWorkerThreads (const Int)**: Number of worker threads (10)
- **ThePinger (PingerInterface*)**: Global pinger instance

## Dependencies
- `winsock.h`, `GameNetwork/GameSpy/PingThread.h`, `mutex.h`, `thread.h`
- ICMP.DLL functions: `IcmpCreateFile`, `IcmpCloseHandle`, `IcmpSendEcho`
- Windows API: `LoadLibrary`, `GetProcAddress`, `FreeLibrary`, `inet_addr`, `gethostbyname`
