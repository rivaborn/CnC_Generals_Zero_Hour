# GeneralsMD/Code/GameEngine/Source/GameNetwork/Transport.cpp

## Purpose
Handles low-level network transport for the game, including packet encryption, UDP socket management, and statistics tracking.

## Responsibilities
- Manages UDP socket initialization and cleanup
- Encrypts/decrypts network packets using XOR and CRC
- Queues and sends/receives network messages
- Tracks network statistics (bytes/packets per second)
- Simulates latency/packet loss for debugging

## Key Types
- `Transport` (Class): Main network transport class managing UDP communication
- `TransportMessage` (Struct): Container for network message data and metadata
- `TransportMessageHeader` (Struct): Header with magic number, CRC, and flags

## Key Functions
### `encryptBuf`
- Purpose: XOR-encrypts a buffer in 4-byte chunks with a rolling mask
- Calls: `htonl`

### `decryptBuf`
- Purpose: Reverses the XOR encryption applied by `encryptBuf`
- Calls: `htonl`

### `queueSend`
- Purpose: Queues a message for sending with encryption and CRC
- Calls: `encryptBuf`, `CRC::computeCRC`

### `isGeneralsPacket`
- Purpose: Validates packet authenticity via magic number and CRC
- Calls: `CRC::computeCRC`

### `doSend`/`doRecv`
- Purpose: Handles actual sending/receiving of queued messages
- Calls: `UDP::Write`/`UDP::Read`, `encryptBuf`/`decryptBuf`

## Globals
- `GENERALS_MAGIC_NUMBER` (const): Magic number for packet validation
- `MAX_MESSAGE_LEN`/`MAX_PACKET_SIZE` (const): Size limits for messages

## Dependencies
- `UDP` class (from NetworkInterface.h)
- `CRC` class (from Common/CRC.h)
- Winsock2 API (`WSADATA`, `sockaddr_in`, etc.)
- `PreRTS.h` for engine initialization
