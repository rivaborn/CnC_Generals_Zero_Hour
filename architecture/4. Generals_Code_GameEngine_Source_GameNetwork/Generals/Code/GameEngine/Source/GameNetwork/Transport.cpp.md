# Generals/Code/GameEngine/Source/GameNetwork/Transport.cpp

## Purpose
Handles low-level network transport for Generals, including packet encryption, UDP socket management, and statistics tracking.

## Responsibilities
- Manages UDP socket initialization and cleanup
- Encrypts/decrypts network packets using XOR and CRC
- Queues and sends/receives network messages
- Tracks network statistics (bytes/packets per second)
- Simulates latency/packet loss in debug builds

## Key Types
- `Transport` (Class): Main network transport class managing UDP communication
- `TransportMessage` (Struct): Header + payload for network packets
- `TransportMessageHeader` (Struct): Contains magic number, CRC, and flags

## Key Functions
### `encryptBuf`
- Purpose: XOR-encrypts a buffer in 4-byte chunks with a rolling mask
- Calls: `htonl`

### `decryptBuf`
- Purpose: Reverses `encryptBuf` by XOR-ing with the same mask sequence
- Calls: `htonl`

### `queueSend`
- Purpose: Prepares a message for sending with encryption and CRC
- Calls: `encryptBuf`, `CRC::computeCRC`

### `isGeneralsPacket`
- Purpose: Validates packet authenticity via magic number and CRC
- Calls: `CRC::computeCRC`

### `doSend` / `doRecv`
- Purpose: Handles actual sending/receiving of queued messages
- Calls: `UDP::Write`, `UDP::Read`, `encryptBuf`, `decryptBuf`

## Globals
- `GENERALS_MAGIC_NUMBER` (const): Packet identification constant
- `MAX_MESSAGE_LEN` (const): Maximum packet size
- `MAX_MESSAGES` (const): Queue size for pending messages

## Dependencies
- `UDP` class (from NetworkInterface.h)
- `CRC` class (from Common/CRC.h)
- Winsock2 API (`WSADATA`, `sockaddr_in`, etc.)
- `TheGlobalData` (for debug latency/packet loss simulation)
