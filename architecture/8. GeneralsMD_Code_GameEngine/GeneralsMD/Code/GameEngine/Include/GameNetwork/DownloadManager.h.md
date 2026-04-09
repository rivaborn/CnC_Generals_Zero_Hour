# GeneralsMD/Code/GameEngine/Include/GameNetwork/DownloadManager.h

## Purpose
Manages file downloads from remote servers, including queuing and error handling.

## Responsibilities
- Initiates and manages file downloads
- Handles download callbacks (progress, errors, completion)
- Queues files for sequential download
- Tracks download status and errors

## Key Types
- **QueuedDownload (struct)**: Stores download parameters (server, credentials, file paths, etc.)
- **DownloadManager (class)**: Main download manager implementing IDownload interface
- **CDownload (class)**: External download handler (forward declared)

## Key Functions
### `downloadFile`
- Purpose: Initiates a file download with specified parameters
- Calls: Not inferable

### `queueFileForDownload`
- Purpose: Adds a file to the download queue
- Calls: Not inferable

### `downloadNextQueuedFile`
- Purpose: Processes the next file in the download queue
- Calls: Not inferable

### `update`
- Purpose: Updates the download state
- Calls: Not inferable

## Globals
- **TheDownloadManager (DownloadManager*)**: Singleton instance of the download manager

## Dependencies
- `WWDownload/downloadDefs.h`, `WWDownload/download.h`
- `IDownload` interface
- `AsciiString`, `UnicodeString`, `std::list`
