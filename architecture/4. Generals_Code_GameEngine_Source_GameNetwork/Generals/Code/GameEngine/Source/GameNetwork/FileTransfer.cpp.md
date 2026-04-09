# Generals/Code/GameEngine/Source/GameNetwork/FileTransfer.cpp

## Purpose
Handles file transfers between clients in a multiplayer game session, including map files and associated assets.

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

### DoAnyMapTransfers
- Purpose: Orchestrates transfer of all required map files based on a bitmask
- Calls: doFileTransfer, GetPreviewFromMap, GetINIFromMap, GetStrFileFromMap, GetSoloINIFromMap, GetAssetUsageFromMap, GetReadmeFromMap

### GetPreviewFromMap / GetINIFromMap / GetStrFileFromMap / GetSoloINIFromMap / GetAssetUsageFromMap / GetReadmeFromMap
- Purpose: Constructs paths for map-related files from the base map path
- Calls: GetBasePathFromPath, GetBaseFileFromFile, GetFileFromPath

## Globals
- None

## Dependencies
- GameClient/LoadScreen.h (MapTransferLoadScreen)
- GameClient/Shell.h (TheShell)
- GameNetwork/FileTransfer.h
- GameNetwork/NetworkUtil.h (TheNetwork)
- PreRTS.h
