# GeneralsMD/Code/GameEngine/Include/GameNetwork/FileTransfer.h

## Purpose
Header for file transfer functionality in the game network layer, providing utilities for path manipulation and map file transfers.

## Responsibilities
- Define path manipulation helper functions
- Declare map file transfer interface
- Provide string utilities for file operations

## Key Types
- GameInfo (Class): Not inferable.

## Key Functions
### GetBasePathFromPath
- Purpose: Extract base path from a full path string.
- Calls: None.

### GetFileFromPath
- Purpose: Extract filename from a full path string.
- Calls: None.

### GetExtensionFromFile
- Purpose: Extract file extension from a filename.
- Calls: None.

### GetBaseFileFromFile
- Purpose: Extract base filename without extension.
- Calls: None.

### GetPreviewFromMap
- Purpose: Generate preview file path from map path.
- Calls: None.

### GetINIFromMap
- Purpose: Generate INI file path from map path.
- Calls: None.

### GetStrFileFromMap
- Purpose: Generate string table file path from map path.
- Calls: None.

### GetSoloINIFromMap
- Purpose: Generate solo INI file path from map path.
- Calls: None.

### GetAssetUsageFromMap
- Purpose: Generate asset usage file path from map path.
- Calls: None.

### GetReadmeFromMap
- Purpose: Generate readme file path from map path.
- Calls: None.

### DoAnyMapTransfers
- Purpose: Perform map file transfers between clients.
- Calls: None.

## Globals
- None.

## Dependencies
- AsciiString (external type)
- Bool (external type)
- GameInfo (forward declaration)
