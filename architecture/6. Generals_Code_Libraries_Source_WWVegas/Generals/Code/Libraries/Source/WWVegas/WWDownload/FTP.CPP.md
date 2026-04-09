# Generals/Code/Libraries/Source/WWVegas/WWDownload/FTP.CPP

## Purpose
Implements FTP client functionality for file downloads in the game.

## Responsibilities
- Manages FTP connections and file transfers
- Handles non-blocking socket operations for firewall compatibility
- Implements file recovery and partial download support
- Manages directory creation for downloaded files

## Key Types
- Cftp (Class): Main FTP client class handling connections and transfers
- sockaddr_in (Struct): Socket address structure for network operations

## Key Functions
### Cftp::ConnectToServer
- Purpose: Establishes and manages FTP server connection
- Calls: AsyncGetHostByName, RecvReply, SendCommand, OpenDataConnection

### Cftp::FileRecoveryPosition
- Purpose: Checks for partial downloads and returns file position
- Calls: fopen, fseek, ftell

### Prepare_Directories
- Purpose: Creates necessary directory structure for file downloads
- Calls: CreateDirectory

## Globals
- gThreadAddress (sockaddr_in): Stores thread address for async hostname resolution
- gThreadFlag (int): Flag for thread completion status

## Dependencies
- winsock.h: Windows socket API
- ftp.h: FTP protocol definitions
- DownloadDebug.h: Debug logging utilities
- Registry functions: For firewall compatibility settings
