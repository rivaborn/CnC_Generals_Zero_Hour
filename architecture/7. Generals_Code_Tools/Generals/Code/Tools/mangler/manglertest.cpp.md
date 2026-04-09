# Generals/Code/Tools/mangler/manglertest.cpp

## Purpose
Test utility for the Mangler network port mapping system, simulating client-server communication.

## Responsibilities
- Resolves server IP addresses (numeric or hostname).
- Configures and tests UDP socket communication.
- Validates packet CRC and command types.
- Logs debug/info/warning messages to file.
- Handles Winsock initialization (Windows).

## Key Types
- **ManglerData (struct)**: Packet structure for port mapping requests/responses.
- **UDP (class)**: Wrapper for UDP socket operations.
- **ConfigFile (class)**: Handles configuration file parsing.

## Key Functions
### ResolveIP
- Purpose: Convert IP address string to host byte order unsigned long.
- Calls: `inet_addr`, `gethostbyname`, `ntohl`.

### DisplayHelp
- Purpose: Print usage instructions and exit.
- Calls: `cout`, `exit`.

### main
- Purpose: Orchestrate test sequence: config load, Winsock init, UDP bind, packet send/receive, CRC validation.
- Calls: `ConfigFile::readFile`, `UDP::Bind`, `UDP::Write`, `UDP::Wait`, `UDP::Read`, `Build_Packet_CRC`, `Passes_CRC_Check`, `WSAStartup`, `WSACleanup`.

## Globals
- **BigEndian (bool)**: Tracks endianness of the system.

## Dependencies
- `<iostream.h>`, `<signal.h>`, `<process.h>` (Windows), `mangler.h`, `crc.h`, `configfile.h`, `threadfac.h`, `endian.h`, `xtime.h`, `<filed.h>`, `<wstring.h>`, `<wdebug.h>`, `<udp.h>`.
