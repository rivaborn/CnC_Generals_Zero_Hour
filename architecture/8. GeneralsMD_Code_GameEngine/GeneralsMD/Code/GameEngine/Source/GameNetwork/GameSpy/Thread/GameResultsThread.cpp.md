# GeneralsMD/Code/GameEngine/Source/GameNetwork/GameSpy/Thread/GameResultsThread.cpp

## Purpose
Manages a thread-based system for sending game results to a GameSpy server.

## Responsibilities
- Manages a queue of game results requests and responses
- Spawns and controls worker threads for sending results
- Handles network communication for result submission
- Provides synchronization for thread-safe operations

## Key Types
- **GameResultsQueue (Class)**: Manages request/response queues and thread lifecycle
- **GameResultsThreadClass (Class)**: Worker thread that processes result submissions
- **RequestQueue (typedef)**: Queue for outgoing game result requests
- **ResponseQueue (typedef)**: Queue for incoming responses

## Key Functions
### GameResultsQueue::addRequest
- Purpose: Adds a game result request to the queue
- Calls: MutexClass::LockClass

### GameResultsQueue::getRequest
- Purpose: Retrieves a request from the queue
- Calls: MutexClass::LockClass

### GameResultsThreadClass::Thread_Function
- Purpose: Main thread loop for processing requests
- Calls: TheGameResultsQueue->getRequest, sendGameResults, Switch_Thread

### GameResultsThreadClass::sendGameResults
- Purpose: Sends game results over network to GameSpy server
- Calls: socket, connect, send, closesocket

## Globals
- **NumWorkerThreads (const Int)**: Number of worker threads (always 1)
- **TheGameResultsQueue (GameResultsInterface**)**: Global instance of the queue manager

## Dependencies
- `GameNetwork/GameSpy/GameResultsThread.h`
- `mutex.h`, `thread.h`
- Winsock API (`winsock.h`)
- `Common/StackDump.h`
