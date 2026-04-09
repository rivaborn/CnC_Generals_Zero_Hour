# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/LoadScreen.cpp

## Purpose
Manages load screen UI for different game modes (single-player, multiplayer, map transfer) in Command & Conquer Generals.

## Responsibilities
- Creates and updates load screen windows for different game types
- Handles player progress bars and status displays
- Manages animations and transitions during loading
- Displays campaign briefings and objectives
- Shows multiplayer player stats (wins/losses, ranks, etc.)

## Key Types
- LoadScreen (Class): Base class for load screen functionality
- SinglePlayerLoadScreen (Class): Handles single-player campaign load screens
- GameSpyLoadScreen (Class): Manages multiplayer load screens with player stats
- MapTransferLoadScreen (Class): Controls map transfer progress screens
- (anonymous enum) (Enum): Frame timing constants for animations

## Key Functions
### positionStartSpots
- Purpose: Positions start spot indicators on the map preview
- Calls: Not inferable

### updateMapStartSpots
- Purpose: Updates start spot positions based on game info
- Calls: Not inferable

### positionAdditionalImages
- Purpose: Positions additional images on the map preview
- Calls: Not inferable

### updateTeletypeText
- Purpose: Updates teletype text animation during loading
- Calls: Not inferable

### GetAdditionalDisconnectsFromUserFile
- Purpose: Retrieves additional disconnect counts from user file
- Calls: Not inferable

## Globals
- TELETYPE_UPDATE_FREQ (Int): Frequency of teletype text updates (2 frames)

## Dependencies
- GameWindowManager, Display, Audio, Network, GameText, WindowLayout
- GameSpy-specific classes (GameSpyGameSlot, PSPlayerStats)
- MapUtil for map previews
- ChallengeGenerals for rank calculations
- Various GUI gadget classes (GadgetProgressBar, GadgetStaticText)
