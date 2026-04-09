# Generals/Code/Libraries/Source/WWVegas/WWDownload/Download.cpp

## Purpose
Implements the CDownload class for handling FTP-based file downloads with progress tracking and error handling.

## Responsibilities
- Manages FTP connection, login, and file transfer
- Tracks download progress and predicts remaining time
- Handles resume functionality for interrupted downloads
- Notifies listener interface of status changes and errors

## Key Types
- CDownload (Class): Main download manager
- DOWNLOADSTATUS (Enum): Download state flags (e.g., DOWNLOADSTATUS_GO, DOWNLOADSTATUS_DOWNLOADING)

## Key Functions
### DownloadFile
- Purpose: Initiates a file download with given parameters
- Calls: m_Ftp->DisconnectFromServer(), m_Ftp->FileRecoveryPosition(), Listener->OnQueryResume()

### PumpMessages
- Purpose: Drives the download state machine and handles progress
- Calls: m_Ftp->ConnectToServer(), m_Ftp->LoginToServer(), m_Ftp->FindFile(), m_Ftp->GetNextFileBlock(), Listener->OnStatusUpdate(), Listener->OnProgressUpdate(), Listener->OnError(), Listener->OnEnd()

### Abort
- Purpose: Cancels the current download and resets state
- Calls: m_Ftp->DisconnectFromServer()

## Globals
- None

## Dependencies
- "DownloadDebug.h", "download.h", <mmsystem.h>, <assert.h>, <direct.h>, <stdlib.h>, <stdio.h>, <sys/stat.h>
- FTP-related functions (m_Ftp->*)
- Listener interface callbacks (Listener->*)
