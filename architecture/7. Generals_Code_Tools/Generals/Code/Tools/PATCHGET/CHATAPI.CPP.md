# Generals/Code/Tools/PATCHGET/CHATAPI.CPP

## Purpose
Handles online patch checking and downloading for the game via GameSpy's chat API.

## Responsibilities
- Checks for available game patches
- Downloads patches via FTP
- Manages download progress UI
- Handles patch queueing and installation

## Key Types
- **DownloadManagerMunkee (Class)**: Custom download manager for patch files
- **QueuedDownload (Struct)**: Represents a patch file to download
- **EVENT_TYPES (Enum)**: Download event types (NOUPDATE_EVENT, ABORT_EVENT)

## Key Functions
### DownloadManagerMunkee::OnProgressUpdate
- Purpose: Updates download progress UI
- Calls: DownloadManager::OnProgressUpdate, SendDlgItemMessage, LoadString, sprintf

### patchCheckCallback
- Purpose: Handles GameSpy HTTP patch check response
- Calls: DEBUG_LOG, queuePatch, startOnline

### queuePatch
- Purpose: Parses patch URL and queues download
- Calls: nextToken, DEBUG_LOG

### startOnline
- Purpose: Initiates patch download process
- Calls: MessageBox, DialogBox, TheDownloadManager operations

## Globals
- **g_DownloadWindow (HWND)**: Main download dialog window
- **g_ContactWindow (HWND)**: Contact/connection window
- **g_PrimaryWindow (HWND)**: Primary application window
- **queuedDownloads (std::list)**: List of patches to download
- **checksLeft (int)**: Remaining patch checks

## Dependencies
- GameSpy HTTP library (ghttp.h)
- DownloadManager base class
- Windows API (windows.h)
- Registry and URL builder utilities
- Resource strings (resource.h)
