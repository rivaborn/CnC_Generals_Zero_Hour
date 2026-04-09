# Generals/Code/Tools/PATCHGET/DownloadManager.cpp

## Purpose
Manages FTP-based file downloads for the game, handling queuing, progress, and error states.

## Responsibilities
- Initializes and manages Winsock for network operations
- Queues and executes file downloads via FTP
- Handles download events (progress, errors, completion)
- Maintains download state and status strings

## Key Types
- DownloadManager (Class): Main download manager singleton
- QueuedDownload (Struct): Holds download parameters (server, credentials, file paths)
- CDownload (Class): Internal download handler (forward-declared)

## Key Functions
### DownloadManager::downloadFile
- Purpose: Initiates an FTP download with given credentials and paths
- Calls: m_download->DownloadFile

### DownloadManager::queueFileForDownload
- Purpose: Adds a download to the queue for later execution
- Calls: None (modifies m_queuedDownloads list)

### DownloadManager::OnError
- Purpose: Handles download errors and sets error strings
- Calls: Fetch_String

### DownloadManager::OnProgressUpdate
- Purpose: Processes download progress updates
- Calls: None

### DownloadManager::OnStatusUpdate
- Purpose: Updates status strings based on download state
- Calls: Fetch_String

## Globals
- TheDownloadManager (DownloadManager*): Singleton instance of the download manager

## Dependencies
- debug.h, chatapi.h, DownloadManager.h, resource.h
- Winsock2.h (via WSAStartup/WSACleanup)
- std::string, std::list
- CDownload class (external)
