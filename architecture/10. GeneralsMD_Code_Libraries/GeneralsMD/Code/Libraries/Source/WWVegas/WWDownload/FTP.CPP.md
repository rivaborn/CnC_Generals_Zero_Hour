# GeneralsMD/Code/Libraries/Source/WWVegas/WWDownload/FTP.CPP

## Purpose
Implements FTP client functionality for downloading files in the game.

## Responsibilities
- Manages FTP connections and file transfers
- Handles non-blocking socket operations for async host resolution
- Implements file recovery and partial download continuation
- Manages directory creation for downloaded files

## Key Types
- `Cftp` (Class): Main FTP client class handling connections and transfers
- `FTPSTAT` (Enum): Status flags for FTP state machine (e.g., `FTPSTAT_CONNECTING`, `FTPSTAT_LOGGEDIN`)
- `sockaddr_in` (Struct): Used for socket address configuration

## Key Functions
### `Cftp::ConnectToServer`
- Purpose: Establishes connection to FTP server and handles file transfer
- Calls: `AsyncGetHostByName`, `SendCommand`, `RecvReply`, `OpenDataConnection`, `RecvData`

### `Cftp::AsyncGetHostByName`
- Purpose: Asynchronously resolves hostname to IP address using a separate thread
- Calls: `gethostbyname`, `CreateThread`

### `Cftp::FileRecoveryPosition`
- Purpose: Checks for partial downloads and returns file position for resuming
- Calls: `fopen`, `fseek`, `ftell`

### `Prepare_Directories`
- Purpose: Creates necessary directory structure for a given file path
- Calls: `CreateDirectory`

## Globals
- `gThreadAddress` (sockaddr_in): Stores resolved host address for async resolution
- `gThreadFlag` (int): Flag indicating async host resolution completion
- `m_iStatus` (int): Current FTP state in the Cftp class

## Dependencies
- Key includes: `winsock.h`, `stdio.h`, `sys/stat.h`, `io.h`, `time.h`, `direct.h`
- External symbols: `gethostbyname`, `CreateThread`, `socket`, `connect`, `recv`, `send`, `closesocket`, `RegOpenKeyEx`, `RegQueryValueEx`
