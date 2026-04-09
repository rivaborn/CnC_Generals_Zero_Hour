# Generals/Code/Tools/mangler/mangler.h

## Purpose
Defines data structures and types for network mangling operations in the game's networking layer.

## Responsibilities
- Defines packet structure for network mangling requests/responses
- Specifies port forwarding and address mangling data format
- Provides type definitions for network command types
- Includes platform-specific packing directives for binary compatibility

## Key Types
- **ForwardMaskType (typedef unsigned char)**: Bitmask for port forwarding
- **NetCommandType (enum)**: Network command types (request/response)
- **ManglerData (struct PACK)**: Packet structure for mangling data (CRC, ports, addresses, command type)

## Key Functions
### None
- No functions defined in this header file

## Globals
### None
- No global variables defined

## Dependencies
- Uses platform-specific packing pragmas (`#pragma pack`)
- Relies on `GlobalHeaderType` and `GlobalPacketType` (referenced but not defined here)
- Assumes existence of `GPCommand` constant for packet field access
