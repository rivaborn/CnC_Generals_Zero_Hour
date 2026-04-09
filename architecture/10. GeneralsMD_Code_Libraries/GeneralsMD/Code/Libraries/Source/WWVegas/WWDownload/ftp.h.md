# GeneralsMD/Code/Libraries/Source/WWVegas/WWDownload/ftp.h

## Purpose
Declares the `Cftp` class for FTP client functionality, handling file downloads, server connections, and data transfers.

## Responsibilities
- Manages FTP command and data socket connections
- Handles file transfer operations (downloads, restarts, recovery)
- Processes FTP server replies and commands
- Maintains state for active file transfers

## Key Types
- **Cftp (Class)**: FTP client implementation for file downloads

## Key Functions
### Cftp::SendData
- Purpose: Sends data over the command socket
- Calls: Not inferable

### Cftp::RecvData
- Purpose: Receives data over the command socket
- Calls: Not inferable

### Cftp::SendNewPort
- Purpose: Negotiates a new data port with the server
- Calls: Not inferable

### Cftp::OpenDataConnection
- Purpose: Establishes a data connection for file transfers
- Calls: Not inferable

### Cftp::CloseDataConnection
- Purpose: Closes the active data connection
- Calls: Not inferable

### Cftp::AsyncGetHostByName
- Purpose: Resolves a hostname asynchronously
- Calls: Not inferable

### Cftp::GetDownloadFilename
- Purpose: Generates a temporary filename for downloads
- Calls: Not inferable

### Cftp::CloseSockets
- Purpose: Closes all active sockets
- Calls: Not inferable

### Cftp::ZeroStuff
- Purpose: Resets internal state variables
- Calls: Not inferable

### Cftp::ConnectToServer
- Purpose: Connects to an FTP server
- Calls: Not inferable

### Cftp::DisconnectFromServer
- Purpose: Disconnects
