# GeneralsMD/Code/GameEngine/Source/GameNetwork/Transport.cpp - Enhanced Analysis

## Architectural Role
This file implements the low-level network transport layer for the SAGE engine, bridging between the game's higher-level networking logic (e.g., `NetworkInterface`) and the underlying UDP socket operations. It handles packet encryption, queuing, and basic statistics, serving as the foundational transport mechanism for multiplayer functionality.

## Cross-References
### Incoming
- `NetworkInterface.cpp` (likely calls `queueSend`, `doSend`, `doRecv` for message routing)
- `GameLogic` subsystems (uses `getIncomingBytesPerSecond` for network health monitoring)

### Outgoing
- `UDP` class (from `NetworkInterface.h`) for socket operations
- `CRC` class for packet validation
- Winsock2 API for low-level networking

## Design Patterns
- **Resource Pooling**: Uses fixed-size buffers (`m_outBuffer`, `m_inBuffer`) for message queuing, avoiding dynamic allocation during gameplay.
- **Guard Pattern**: `encryptBuf`/`decryptBuf` process data in 4-byte chunks, leaving trailing bytes unencrypted for performance.
- **Rolling Mask**: Encryption uses a rolling XOR mask (`0x0000Fade + 0x00000321`), balancing speed and basic obfuscation.
