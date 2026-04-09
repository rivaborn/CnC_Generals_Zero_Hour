# Generals/Code/Tools/PATCHGET/DownloadManager.h

## Purpose
Manages file downloads from remote servers, including queuing and error handling.

## Responsibilities
- Initiates and manages file downloads via `CDownload`
- Handles download callbacks (progress, errors, completion)
- Queues files for sequential download
- Tracks download state and provides status information

## Key Types
- **QueuedDownload (struct)**: Stores download parameters (server, credentials, file paths, etc.)
- **DownloadManager (class)**: Manages downloads, implements `IDownload` interface
- **CDownload (class)**: External download handler (not defined here)

## Key Functions
### `downloadFile`
- Purpose: Initiates a file download with specified parameters
- Calls: `m_download->downloadFile`

### `queueFileForDownload`
- Purpose: Adds a file to the download queue
- Calls: None (directly modifies `m_queuedDownloads`)

### `downloadNextQueuedFile`
- Purpose: Processes the next file in the queue
- Calls: `downloadFile`

### `update`
- Purpose: Updates the download state
- Calls: `m_download->update`

## Globals
- **TheDownloadManager (DownloadManager*)**: Singleton instance for global access

## Dependencies
- `WWDownload/downloadDefs.h`, `WWDownload/download.h` (external download API)
- `<string>`, `<list>` (STL containers)
- `IDownload` interface (inherited)
