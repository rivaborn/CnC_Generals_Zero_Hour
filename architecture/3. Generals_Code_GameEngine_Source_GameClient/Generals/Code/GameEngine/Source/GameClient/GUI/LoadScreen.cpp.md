# Generals/Code/GameEngine/Source/GameClient/GUI/LoadScreen.cpp

## Purpose
Manages load screen UI for different game modes (single-player, multiplayer, map transfer) in Command & Conquer Generals.

## Responsibilities
- Creates and updates load screen windows for different game types
- Handles player progress bars and statistics display
- Manages map previews and start positions
- Processes network load progress updates
- Controls animations and transitions during loading

## Key Types
- LoadScreen (Class): Base class for load screen functionality
- SinglePlayerLoadScreen (Class): Handles single-player mission loading UI
- GameSpyLoadScreen (Class): Manages multiplayer load screen with player stats
- MapTransferLoadScreen (Class): Controls map transfer progress UI
- (anonymous enum) (Enum): Contains frame timing constants for animations

## Key Functions
### positionStartSpots
- Purpose: Positions start spot indicators on the map preview
- Calls: Not inferable

### updateMapStartSpots
- Purpose: Updates the visibility of start spot indicators
- Calls: Not inferable

### positionAdditionalImages
- Purpose: Positions additional map images
- Calls: Not inferable

### GetAdditionalDisconnectsFromUserFile
- Purpose: Retrieves additional disconnect counts from user file
- Calls: Not inferable

## Globals
- FRAME_FUDGE_ADD (Int): Frame timing adjustment constant

## Dependencies
- GameClient headers (WindowManager, Display, GameText)
- Common game headers (GameEngine, GameState)
- Network headers (NetworkInterface, GameSpy)
- Audio headers (GameAudio)
- UI component headers (GadgetProgressBar, GadgetStaticText)
