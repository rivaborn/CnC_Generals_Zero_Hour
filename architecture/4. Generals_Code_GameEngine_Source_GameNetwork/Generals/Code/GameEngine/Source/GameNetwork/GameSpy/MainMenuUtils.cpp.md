# Generals/Code/GameEngine/Source/GameNetwork/GameSpy/MainMenuUtils.cpp

## Purpose
Handles GameSpy integration for online functionality, including patch checks, downloads, and connection management.

## Responsibilities
- Manages patch checks and downloads before online play
- Handles GameSpy login flow and configuration
- Provides async DNS resolution and HTTP request management
- Tracks online statistics and player counts

## Key Types
- (anonymous enum): DNS lookup states (LOOKUP_INPROGRESS/FAILED/SUCCEEDED)
- QueuedDownload: Represents a file to be downloaded (server, user, password, file paths)

## Key Functions
### StartDownloadingPatches
- Purpose: Initiates queued patch downloads
- Calls: TheDownloadManager->queueFileForDownload, downloadNextQueuedFile

### startOnline
- Purpose: Begins GameSpy login process after checks
- Calls: SetUpGameSpy, TheShell->push

### queuePatch
- Purpose: Adds a patch to the download queue
- Calls: None directly (parses URL)

### HTTPThinkWrapper
- Purpose: Manages HTTP and DNS operations with error handling
- Calls: ghttpThink, asyncGethostbyname

### StartPatchCheck
- Purpose: Initiates patch checking before online play
- Calls: MessageBoxCancel, asyncGethostbyname

## Globals
- checkingForPatchBeforeGameSpy (Bool): Tracks if patch check is in progress
- queuedDownloads (list<QueuedDownload>): Stores pending patch downloads
- onlineCancelWindow (GameWindow*): Reference to cancel dialog
- s_asyncDNSThreadHandle (HANDLE): Handle for DNS lookup thread

## Dependencies
- GameSpy HTTP SDK (ghttp.h)
- DownloadManager for patch downloads
- WindowManager for UI elements
- Registry access for configuration
- ScriptEngine for UI events
