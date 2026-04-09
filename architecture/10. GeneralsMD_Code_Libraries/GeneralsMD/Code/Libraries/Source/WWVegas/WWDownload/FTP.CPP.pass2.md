# GeneralsMD/Code/Libraries/Source/WWVegas/WWDownload/FTP.CPP - Enhanced Analysis

## Architectural Role
This file implements the FTP client subsystem for the game's download infrastructure, handling file transfers from remote servers. It integrates with the game's registry system for download state persistence and uses Windows sockets for network operations.

## Cross-References
### Incoming
- Likely called by download managers or content update systems (not shown in file)
- Registry access suggests integration with game settings/configuration

### Outgoing
- Uses Windows API (`RegOpenKeyEx`, `CreateThread`)
- Depends on Winsock (`socket`, `connect`, `recv`, `send`)
- Calls file I/O functions (`fopen`, `fseek`, `ftell`)

## Design Patterns
- **State Machine**: Uses `FTPSTAT` enum to track connection/transfer states
- **Threading**: Separate thread for async host resolution (`AsyncGetHostByName`)
- **Registry Persistence**: Stores download state in Windows registry for recovery

*Not inferable*: No clear use of other patterns like Singleton or Observer.
