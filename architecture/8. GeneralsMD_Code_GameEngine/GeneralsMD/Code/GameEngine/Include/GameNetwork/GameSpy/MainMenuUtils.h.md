# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameSpy/MainMenuUtils.h

## Purpose
Header file declaring utility functions for GameSpy-related operations in the main menu, including patch checks and online player stats.

## Responsibilities
- Declares functions for HTTP-based GameSpy interactions
- Manages patch download and version checks
- Handles online player statistics retrieval
- Provides DNS check control

## Key Types
None

## Key Functions
### HTTPThinkWrapper
- Purpose: Wrapper for HTTP-related think logic.
- Calls: Not inferable

### StopAsyncDNSCheck
- Purpose: Stops asynchronous DNS checks.
- Calls: Not inferable

### StartPatchCheck
- Purpose: Initiates a patch version check.
- Calls: Not inferable

### CancelPatchCheckCallback
- Purpose: Cancels an ongoing patch check callback.
- Calls: Not inferable

### StartDownloadingPatches
- Purpose: Begins downloading available patches.
- Calls: Not inferable

### HandleCanceledDownload
- Purpose: Handles a canceled download, with optional dropdown reset.
- Calls: Not inferable

### CheckOverallStats
- Purpose: Requests overall game statistics from GameSpy.
- Calls: Not inferable

### HandleOverallStats
- Purpose: Processes received overall statistics data.
- Calls: Not inferable

### CheckNumPlayersOnline
- Purpose: Queries the number of
