# Generals/Code/GameEngine/Source/GameNetwork/GameSpy/Thread/GameResultsThread.cpp

## Purpose
Manages a threaded queue system for sending game results to a GameSpy server.

## Responsibilities
- Manages a queue of game result requests and responses
- Handles threading for sending game results asynchronously
- Resolves hostnames to IP addresses for network communication
- Formats game results into HTTP POST requests
- Provides error handling and logging for network operations

## Key Types
- **GameResultsQueue (Class)**: Manages the request/response queues and thread lifecycle.
- **GameResultsThreadClass (Class)**: Worker thread that processes game result requests.
- **RequestQueue (typedef)**: Queue of pending game result requests.
- **ResponseQueue (typedef)**: Queue of completed game result responses.

## Key Functions
### WrapHTTP
- Purpose: Formats game results into an HTTP POST header.
- Calls: None.

### getWSAErrorString
- Purpose: Converts Winsock error codes to human-readable strings.
- Calls: None.

### GameResultsThreadClass::sendGameResults
- Purpose: Sends game results over a TCP socket to a specified IP and port.
- Calls: `socket`, `connect`, `send`, `closesocket`, `WSAGetLastError`, `getWSAErrorString`.

## Globals
- **NumWorkerThreads (const Int)**: Number of worker threads (always 1).
- **TheGameResultsQueue (GameResultsInterface*)**: Global instance of the game results queue.

## Dependencies
- `PreRTS.h`, `winsock.h`, `GameNetwork/GameSpy/GameResultsThread.h`, `mutex.h`, `thread.h`, `Common/StackDump.h`, `Common/SubsystemInterface.h`
- Winsock API (`socket`, `connect`, `send`, `closesocket`, `WSAStartup`, `WSACleanup`, `WSAGetLastError`)
- STL (`std::queue`, `std::string`)
