# GeneralsMD/Code/GameEngine/Include/GameClient/LoadScreen.h

## Purpose
Defines the base `LoadScreen` class and its derived classes for handling loading screens in different game contexts (single-player, multiplayer, challenges, etc.).

## Responsibilities
- Provide a base interface for load screens with virtual methods for initialization, updates, and progress handling.
- Manage progress bars, player info, and UI elements specific to each load screen type.
- Handle video playback and audio during loading.
- Support network progress updates for multiplayer scenarios.

## Key Types
- **LoadScreen (Class)**: Base class for all load screens.
- **SinglePlayerLoadScreen (Class)**: Handles single-player mission loading with objectives and unit descriptions.
- **ChallengeLoadScreen (Class)**: Manages challenge mission loading with general bios and portraits.
- **ShellGameLoadScreen (Class)**: Simple load screen for shell game mode.
- **MultiPlayerLoadScreen (Class)**: Displays progress for multiple players in multiplayer games.
- **GameSpyLoadScreen (Class)**: Shows player stats (wins, rank, etc.) during multiplayer loading.
- **MapTransferLoadScreen (Class)**: Manages map transfer progress during multiplayer setup.

## Key Functions
### `update(Int percent)`
- Purpose: Updates the progress bar with a percentage value.
- Calls: Not inferable (implementation in .cpp).

### `processProgress(Int playerId, Int percentage)`
- Purpose: Processes progress updates for a specific player.
- Calls: Not inferable (implementation in .cpp).

### `setProgressRange(Int min, Int max)`
- Purpose: Sets the minimum and maximum values for the progress range.
- Calls: Not inferable (implementation in .cpp).

## Globals
- None

## Dependencies
- `Lib/BaseType.h`, `Common/SubsystemInterface.h`, `GameClient/GameWindow.h`, `GameNetwork/GameInfo.h`, `GameClient/CampaignManager.h`, `GameClient/ChallengeGenerals.h`
- Forward declarations: `VideoBuffer`, `VideoStreamInterface`, `WindowVideoManager`
