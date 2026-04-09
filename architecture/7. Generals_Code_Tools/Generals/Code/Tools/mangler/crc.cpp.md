# Generals/Code/Tools/mangler/crc.cpp

## Purpose
Implements CRC (Cyclic Redundancy Check) computation and validation for network packets.

## Responsibilities
- Computes CRC for packet data
- Validates packet integrity via CRC
- Handles endianness conversion for cross-platform compatibility

## Key Types
- None

## Key Functions
### Add_CRC
- Purpose: Updates CRC value with a byte
- Calls: None

### Build_Packet_CRC
- Purpose: Computes and stores CRC in packet buffer
- Calls: Add_CRC, DBGMSG, htonl

### Passes_CRC_Check
- Purpose: Validates packet CRC against stored value
- Calls: Add_CRC, DBGMSG, htonl

## Globals
- None

## Dependencies
- `<iostream>`, `<signal.h>`, `<process.h>`, `crc.h`, `configfile.h`, `threadfac.h`, `endian.h`, `xtime.h`, `<filed.h>`, `<wstring.h>`, `<wdebug.h>`, `<udp.h>`
- DBGMSG, htonl
