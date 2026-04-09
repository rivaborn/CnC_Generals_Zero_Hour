# GeneralsMD/Code/GameEngine/Source/GameNetwork/Connection.cpp

## Purpose
Manages network connections, command queuing, and packet transmission for multiplayer gameplay.

## Responsibilities
- Handles sending and retrying network commands
- Manages packetization of commands
- Processes acknowledgments for sent commands
- Tracks connection latency and retry metrics
- Manages connection state (quitting, retry timing)

## Key Types
- MaxQuitFlushTime (Enum): Maximum time (30000ms) to wait for flushing commands before quitting

## Key Functions
### Connection()
- Purpose: Initializes connection state
- Calls: None

### init()
- Purpose: Resets connection to initial state
- Calls: NetCommandList::init(), NetCommandList::reset()

### doSend()
- Purpose: Packetizes and sends queued commands
- Calls: NetPacket::addCommand(), Transport::queueSend(), processAck()

### processAck()
- Purpose: Removes acknowledged commands from queue
- Calls: timeGetTime()

### setQuitting()
- Purpose: Marks connection as quitting and sets quit timer
- Calls: timeGetTime()

## Globals
- MaxQuitFlushTime (Enum): Timeout value for quitting connections

## Dependencies
- Connection.h, NetworkUtil.h, GameLogic.h
- NetCommandMsg, NetPacket, Transport, User classes
- timeGetTime() from Windows API
