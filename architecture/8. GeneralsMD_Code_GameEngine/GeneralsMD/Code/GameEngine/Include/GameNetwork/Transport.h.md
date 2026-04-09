# GeneralsMD/Code/GameEngine/Include/GameNetwork/Transport.h

## Purpose
Defines the Transport class, a thin layer around a UDP socket for packet handling in the game's networking layer.

## Responsibilities
- Manages UDP socket communication
- Handles packet queuing and transmission
- Tracks bandwidth metrics (bytes/packets per second)
- Supports latency/packet loss simulation for debugging
- Filters Generals-specific packets

## Key Types
- **Transport (Class)**: UDP transport layer for game networking
- **TransportMessage (Struct)**: Not defined here, but used for packet buffers
- **DelayedTransportMessage (Struct)**: Used in debug builds for latency simulation

## Key Functions
### Transport::queueSend
- Purpose: Queues a packet for sending to a specified address/port
- Calls: None visible in header

### Transport::update
- Purpose: Updates the transport layer once per game tick
- Calls: None visible in header

### Transport::doRecv/doSend
- Purpose: Services receive/transmit queues
- Calls: None visible in header

### Transport::isGeneralsPacket
- Purpose: Checks if a packet is a Generals-specific packet
- Calls: None visible in header

## Globals
- **m_outBuffer/m_inBuffer (TransportMessage[])**: Buffers for outgoing/incoming packets
- **m_delayedInBuffer (DelayedTransportMessage[])**: Debug-only buffer for latency simulation
- **m_incomingBytes/m_outgoingBytes (UnsignedInt[])**: Bandwidth tracking arrays

## Dependencies
- **udp.h**: UDP socket implementation
- **NetworkDefs.h**: Network-related constants and types
- **AsciiString/UnsignedShort/Bool/Real**: Basic types from game engine
