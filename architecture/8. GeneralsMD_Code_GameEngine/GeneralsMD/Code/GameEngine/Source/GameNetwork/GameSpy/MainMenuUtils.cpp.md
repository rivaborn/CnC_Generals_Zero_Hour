# GeneralsMD/Code/GameEngine/Source/GameNetwork/GameSpy/MainMenuUtils.cpp

## Purpose
Handles GameSpy online functionality, including patch checks, downloads, and connection setup.

## Responsibilities
- Manages patch checks and downloads before online play
- Handles GameSpy login flow and configuration
- Manages DNS lookups and HTTP requests asynchronously
- Provides callbacks for various online operations

## Key Types
- (anonymous enum): DNS lookup states (LOOKUP_INPROGRESS, LOOKUP_FAILED, LOOKUP_SUCCEEDED)
- QueuedDownload (struct): Represents a file to be downloaded

## Key Functions
### StartDownloadingPatches
- Purpose: Initiates the download of queued patches
- Calls: TheDownloadManager->queueFileForDownload, TheDownloadManager->downloadNextQueuedFile

### startOnline
- Purpose: Starts the online process after patch checks
- Calls: SetUpGameSpy, TheShell->push

### queuePatch
- Purpose: Queues a patch for download
- Calls: None

### motdCallback
- Purpose: Handles MOTD (Message of the Day) download completion
- Calls: startOnline

### configCallback
- Purpose: Handles configuration file download completion
- Calls: startOnline

### gamePatchCheckCallback
- Purpose: Processes patch check results
- Calls: queuePatch, startOnline

### asyncGethostbyname
- Purpose: Performs asynchronous DNS lookup
- Calls: CreateThread

### HTTPThinkWrapper
- Purpose: Processes HTTP requests and DNS lookups
- Calls: ghttpThink, reallyStartPatchCheck

### StartPatchCheck
- Purpose: Initiates patch checks before online play
- Calls: asyncGethostbyname, reallyStartPatchCheck

### reallyStartPatchCheck
- Purpose: Starts all patch and configuration checks
- Calls: ghttpGet, ghttpHead, CheckOverallStats, CheckNumPlayersOnline

## Globals
- checkingForPatchBeforeGameSpy (Bool): Tracks if patch checks are in progress
- checksLeftBeforeOnline (Int): Counts remaining checks
- timeThroughOnline (Int): Tracks current online session
- mustDownloadPatch (Bool): Indicates if a mandatory patch is needed
- cantConnectBeforeOnline (Bool): Tracks connection failures
- queuedDownloads (list<QueuedDownload>): Stores patches to download
- MOTDBuffer (char*): Stores MOTD content
- configBuffer (char*): Stores configuration content
- onlineCancelWindow (GameWindow*): Reference to cancel dialog
- s_asyncDNSThreadDone (Bool): Tracks DNS lookup completion
- s_asyncDNSThreadSucceeded (Bool): Tracks DNS lookup success
- s_asyncDNSLookupInProgress (Bool): Tracks DNS lookup state
- s_asyncDNSThreadHandle (HANDLE): Handle to DNS lookup thread
- isHttpOk (Bool): Tracks HTTP request success

## Dependencies
- PreRTS.h, Common headers, GameClient headers, GameLogic headers
- GameSpy headers (ghttp.h, BuddyThread.h, PeerThread.h)
- GameNetwork headers (DownloadManager.h, PeerDefs.h)
- WWDownload headers (Registry.h, URLBuilder.h)
