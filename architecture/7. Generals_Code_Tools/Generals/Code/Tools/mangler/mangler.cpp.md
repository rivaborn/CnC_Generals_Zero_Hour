# Generals/Code/Tools/mangler/mangler.cpp

## Purpose
This file implements a UDP packet mangler tool for the game, likely used for network debugging or packet modification.

## Responsibilities
- Reads configuration from a file
- Sets up UDP listeners on multiple ports
- Processes incoming packets, validates CRC, and forwards them
- Supports "blitz" mode to forward packets to additional ports
- Logs operations and errors

## Key Types
- `ManglerData` (struct): Not inferable (used in packet handling)
- `ConfigFile` (class): Configuration file reader
- `UDP` (class): UDP socket wrapper
- `Wstring` (class): Wide string utility

## Key Functions
### `DisplayHelp`
- Purpose: Shows usage information and exits
- Calls: `cout`, `exit`

### `main`
- Purpose: Main entry point that sets up logging, Winsock, UDP listeners, and packet processing loop
- Calls: `ConfigFile::readFile`, `MsgManager::setAllStreams`, `WSAStartup`, `UDP::Bind`, `UDP::Wait`, `UDP::Read`, `Passes_CRC_Check`, `Build_Packet_CRC`, `UDP::Write`, `fopen`, `fclose`, `rename`, `inet_addr`, `ntohl`, `ntohs`

## Globals
- `None`

## Dependencies
- `<iostream.h>`, `<signal.h>`, `<process.h>`, `mangler.h`, `crc.h`, `endian.h`, `configfile.h`, `threadfac.h`, `xtime.h`, `<filed.h>`, `<wstring.h>`, `<wdebug.h>`, `<udp.h>`
- `MsgManager`, `FileD`, `WSAStartup`, `WSADATA`, `inet_addr`, `ntohl`, `ntohs`
