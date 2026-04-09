# Generals/Code/Libraries/Source/WWVegas/WWDownload/ftp.h

## Purpose
Declares the Cftp class for FTP client functionality in the game.

## Responsibilities
- Manages FTP connections and file transfers
- Handles command and data socket operations
- Implements file download with recovery support
- Processes FTP server replies and commands

## Key Types
- Cftp (Class): FTP client implementation

## Key Functions
### Cftp::SendData
- Purpose: Sends data over the command socket
- Calls: Not inferable

### Cftp::RecvData
- Purpose: Receives data over the command socket
- Calls: Not inferable

### Cftp::SendNewPort
- Purpose: Sends a new port command to the server
- Calls: Not inferable

### Cftp::OpenDataConnection
- Purpose: Opens a data connection for file transfer
- Calls: Not inferable

### Cftp::CloseDataConnection
- Purpose: Closes the data connection
- Calls: Not inferable

### Cftp::AsyncGetHostByName
- Purpose: Resolves hostname asynchronously
- Calls: Not inferable

### Cftp::GetDownloadFilename
- Purpose: Generates a temporary filename for downloads
- Calls: Not inferable

### Cftp::CloseSockets
- Purpose: Closes all FTP sockets
- Calls: Not inferable

### Cftp::ZeroStuff
- Purpose: Initializes member variables to zero
- Calls: Not inferable

### Cftp::ConnectToServer
- Purpose: Establishes connection to FTP server
- Calls: Not inferable

### Cftp::DisconnectFromServer
- Purpose: Closes connection to FTP server
- Calls: Not inferable

### Cftp::LoginToServer
- Purpose: Authentic
