# GeneralsMD/Code/GameEngine/Source/GameNetwork/DownloadManager.cpp

## Purpose
Manages file downloads from FTP servers, including queuing, progress tracking, and error handling.

## Responsibilities
- Handles FTP downloads via CDownload
- Manages download queue
- Tracks download status and errors
- Initializes Winsock for networking

## Key Types
- DownloadManager (Class): Main download manager
- QueuedDownload (Struct): Represents a queued download
- CDownload (Class): Internal download handler (not shown)

## Key Functions
### DownloadManager::downloadFile
- Purpose: Initiates a file download from FTP server
- Calls: m_download->DownloadFile

### DownloadManager::queueFileForDownload
- Purpose: Adds a file to the download queue
- Calls: m_queuedDownloads.push_back

### DownloadManager::downloadNextQueuedFile
- Purpose: Processes the next queued download
- Calls: downloadFile, m_queuedDownloads.pop_front

### DownloadManager::OnError
- Purpose: Handles download errors and sets error strings
- Calls: TheGameText->fetch

### DownloadManager::OnStatusUpdate
- Purpose: Updates download status strings
- Calls: TheGameText->fetch

## Globals
- TheDownloadManager (DownloadManager*): Singleton instance

## Dependencies
- CDownload (external class)
- TheGameText (external singleton)
- Winsock API (WSAStartup/WSACleanup)
- GameText.h, DownloadManager.h
