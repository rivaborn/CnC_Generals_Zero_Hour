# Generals/Code/GameEngine/Source/GameNetwork/DownloadManager.cpp

## Purpose
Manages file downloads via FTP in the game engine, handling queued downloads and network status.

## Responsibilities
- Manages FTP downloads with resume support
- Handles download queue processing
- Provides status/error callbacks
- Initializes Winsock for networking

## Key Types
- **DownloadManager (Class)**: Main download manager singleton
- **QueuedDownload (Struct)**: Holds download parameters (server, credentials, file paths)
- **CDownload (Class)**: Internal download handler (forward-declared)

## Key Functions
### `downloadFile`
- Purpose: Initiates an FTP download
- Calls: `m_download->DownloadFile`

### `queueFileForDownload`
- Purpose: Adds a download to the queue
- Calls: None (modifies `m_queuedDownloads`)

### `downloadNextQueuedFile`
- Purpose: Processes next queued download
- Calls: `downloadFile`

### `OnError`
- Purpose: Handles download errors with localized strings
- Calls: `TheGameText->fetch`

### `OnStatusUpdate`
- Purpose: Updates download status text
- Calls: `TheGameText->fetch`

## Globals
- **TheDownloadManager (DownloadManager*)**: Singleton instance

## Dependencies
- `DownloadManager.h` (header)
- `GameText.h` (for localized strings)
- Winsock API (`WSAStartup`, `WSACleanup`)
- `CDownload` class (internal implementation)
