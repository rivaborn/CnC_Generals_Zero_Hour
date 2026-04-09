# GeneralsMD/Code/GameEngine/Source/GameNetwork/FileTransfer.cpp

## Purpose
Handles file transfers between game clients, particularly for map-related files during multiplayer sessions.

## Responsibilities
- Manages file transfer progress and timeouts
- Constructs paths for map-related files (preview, INI, STR, etc.)
- Coordinates transfers via TheNetwork
- Updates load screen UI during transfers

## Key Types
- None

## Key Functions
### doFileTransfer
- Purpose: Initiates and monitors a file transfer between clients
- Calls: TheNetwork->sendFileAnnounce, TheNetwork->sendFile, TheNetwork->getFileTransferProgress, TheNetwork->areAllQueuesEmpty, ls->setCurrentFilename, ls->processTimeout, ls->update, ls->processProgress

### GetBasePathFromPath
- Purpose: Extracts the directory path from a full file path
- Calls: None

### GetFileFromPath
- Purpose: Extracts the filename from a full file path
- Calls: None

### GetExtensionFromFile
- Purpose: Extracts the file extension from a filename
- Calls: None

### GetBaseFileFromFile
- Purpose: Removes the extension from a filename
- Calls: None

### GetPreviewFromMap
- Purpose: Constructs the path for a map's preview image
- Calls: GetBaseFileFromFile, GetBasePathFromPath

### GetINIFromMap
- Purpose: Constructs the path for a map's INI file
- Calls: GetBasePathFromPath

### GetStrFileFromMap
- Purpose: Constructs the path for a map's STR file
- Calls: GetBasePathFromPath

### GetSoloINIFromMap
- Purpose: Constructs the path for a map's solo INI file
- Calls: GetBasePathFromPath

### GetAssetUsageFromMap
- Purpose: Constructs the path for a map's asset usage file
- Calls: GetBasePathFromPath

### GetReadmeFromMap
- Purpose: Constructs the path for a map's readme file
- Calls: GetBasePathFromPath

### DoAnyMapTransfers
- Purpose: Orchestrates the transfer of all required map files to clients that need them
- Calls: doFileTransfer, GetPreviewFromMap, GetINIFromMap, GetStrFileFromMap, GetSoloINIFromMap, GetAssetUsageFromMap, GetReadmeFromMap, TheShell->hideShell, TheShell->showShell

## Globals
- None

## Dependencies
- GameClient/LoadScreen.h
- GameClient/Shell.h
- GameNetwork/FileTransfer.h
- GameNetwork/NetworkUtil.h
- PreRTS.h
- TheNetwork (external
