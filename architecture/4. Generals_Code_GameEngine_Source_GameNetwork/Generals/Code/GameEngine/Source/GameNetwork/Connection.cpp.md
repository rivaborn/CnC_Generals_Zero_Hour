# Generals/Code/GameEngine/Source/GameNetwork/Connection.cpp

## Purpose
Manages network connections, packetization, and retry logic for sending network commands in the game.

## Responsibilities
- Handles sending and retrying network commands
- Manages packetization of commands into transport packets
- Processes acknowledgments for sent commands
- Tracks connection latency and retry metrics
- Supports graceful disconnection

## Key Types
- MaxQuitFlushTime (Enum): Maximum time (30000ms) to wait for flushing before quitting

## Key Functions
### Connection()
- Purpose: Initializes connection state
- Calls: None

### init()
- Purpose: Resets connection to initial state
- Calls: newInstance(NetCommandList), NetCommandList::init()

### doSend()
- Purpose: Packetizes and sends queued network commands
- Calls: newInstance(NetPacket), NetPacket::init(), Transport::queueSend(), NetPacket::deleteInstance()

### processAck()
- Purpose: Removes acknowledged commands from send queue
- Calls: timeGetTime()

### setQuitting()
- Purpose: Marks connection as quitting and sets quit timer
- Calls: timeGetTime()

## Globals
- MaxQuitFlushTime (Enum): Timeout value for quitting connections

## Dependencies
- PreRTS.h, Connection.h, NetworkUtil.h, GameLogic.h
- NetPacket, NetCommandList, Transport, User classes
- timeGetTime() from Windows API
