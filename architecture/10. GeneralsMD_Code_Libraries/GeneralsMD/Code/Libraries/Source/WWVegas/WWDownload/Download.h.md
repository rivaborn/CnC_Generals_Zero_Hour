# GeneralsMD/Code/Libraries/Source/WWVegas/WWDownload/Download.h

## Purpose
Declares interfaces and classes for handling file downloads with progress and status callbacks.

## Responsibilities
- Defines the `IDownload` callback interface for download events.
- Implements the `CDownload` class to manage FTP downloads.
- Tracks download progress, status, and predictions.
- Provides methods to start, abort, and query download state.

## Key Types
- **IDownload (Class)**: Callback interface for download events (error, progress, status).
- **CDownload (Class)**: Manages FTP downloads, progress tracking, and callbacks.

## Key Functions
### CDownload::PumpMessages
- Purpose: Processes download messages and updates state.
- Calls: Not inferable.

### CDownload::Abort
- Purpose: Cancels the ongoing download.
- Calls: Not inferable.

### CDownload::DownloadFile
- Purpose: Initiates a download from an FTP server.
- Calls: Not inferable.

### CDownload::GetLastLocalFile
- Purpose: Retrieves the last downloaded file path.
- Calls: Not inferable.

## Globals
- **None**

## Dependencies
- `WWDownload/ftp.h`
- `WWDownload/downloaddefs.h`
- `Cftp` (external FTP class)
- `DOWNLOADSTATUS_NONE` (enum from downloaddefs.h)
