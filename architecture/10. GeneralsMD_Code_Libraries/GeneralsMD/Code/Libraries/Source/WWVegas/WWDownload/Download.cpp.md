# GeneralsMD/Code/Libraries/Source/WWVegas/WWDownload/Download.cpp

## Purpose
Implements the CDownload class for handling FTP-based file downloads in the game.

## Responsibilities
- Manages FTP connections and file transfers
- Handles download state transitions (connecting, logging in, downloading, etc.)
- Provides progress updates and error reporting via a listener interface
- Supports download resumption and patch file checks

## Key Types
- CDownload (Class): Main download manager class
- DownloadStatus (Enum): Download state flags (DOWNLOADSTATUS_NONE, DOWNLOADSTATUS_GO, etc.)

## Key Functions
### DownloadFile
- Purpose: Initiates a file download with given parameters
- Calls: m_Ftp->DisconnectFromServer(), m_Ftp->FileRecoveryPosition(), Listener->OnQueryResume()

### PumpMessages
- Purpose: Drives the download state machine and handles FTP operations
- Calls: m_Ftp->ConnectToServer(), m_Ftp->LoginToServer(), m_Ftp->FindFile(), m_Ftp->GetNextFileBlock(), Listener->OnStatusUpdate(), Listener->OnError(), Listener->OnProgressUpdate(), Listener->OnEnd()

### Abort
- Purpose: Cancels the current download and resets state
- Calls: m_Ftp->DisconnectFromServer()

## Globals
- None

## Dependencies
- download.h (header)
- DownloadDebug.h (debug macros)
- mmsystem.h (timeGetTime)
- FTP-related functions (m_Ftp->* methods)
- Listener interface (OnStatusUpdate, OnError, etc.)
